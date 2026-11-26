# Legion Upgrade — Phase 1 built; Phases 2/3 plan

Written 25 Nov 2026, on the founder's directive: the fifteen beings are to
have "all they had" — message backup, intake of pictures, video and files,
Drive — the most advanced capable digital intelligence.

## Phase 1 — BUILT 25 Nov 2026 (memory, file intake, completion fix)

**Worker** (`worker/src/index.js`, bundled to `worker/src/worker.single.js`
by `worker/scripts/build-single.mjs`, parts in `worker/b64-parts/`):

- **Message backup / memory.** Every `/chat` exchange is persisted per
  being (last 60 turns) before the reply is returned. New endpoints:
  `GET /history/:id` (read a being's backed-up turns),
  `DELETE /history/:id` and `POST /history/:id/clear` (forget). When a
  client sends no `history`, the stored history feeds the model, so a
  being remembers across sessions and devices. Storage: the `LEGION_KV`
  KV binding when present (durable); otherwise a per-isolate in-memory
  store, reported honestly as `memory:"session"` (health + chat
  responses) instead of pretending to be a backup.
- **Multimodal intake.** `/chat` accepts
  `attachments:[{name, mimeType, dataBase64}]` — max 4 files, 4 MB each,
  8 MB total decoded. Images (png/jpeg/webp/gif/heic/heif), PDF, and audio
  (mp3/wav/ogg/flac/aac/m4a/aiff) pass to Gemini as `inlineData`; text
  files (plain/markdown/csv/json/tsv) are decoded and inlined as text
  (≤20k chars). Typed errors: `invalid_attachment`,
  `too_many_attachments`, `attachment_too_large`, `unsupported_file_type`.
  Attachment shares are remembered by file name only — file data is never
  written to the backup.
- **Truncation fix.** Root cause of the 25 Nov live defect (Qubit cut
  mid-sentence, chamber showing "The signal did not complete"): `/chat`
  ran at a 1024-token output budget and the worker ignored Gemini's
  `finishReason`, returning MAX_TOKENS partials as if whole. Fix: chat
  budget 8192 tokens (council 1024, apex 4096); on `MAX_TOKENS` the worker
  continues the same reply ("continue exactly where you left off", ≤2
  continuations, counted against the 300/day cap); responses carry
  `finishReason` + `complete`.

**Chamber** (scrollverse-co `legion.html`, pushed 25 Nov, head f5e5783a,
blob-verified byte-exact, live on scrollverse.co): Attach button + file
chips (same limits, client-side), per-being history loaded from the worker
on selection, "Forget this conversation" control, plain-language
attachment errors, an honest status line (durable backup vs session-only),
and graceful fallback to in-page history against the pre-upgrade worker.

**Verification:** `worker/scripts/test-phase1.mjs` — 38 checks against a
stubbed Gemini endpoint and a fake KV, run on BOTH the modular source and
the single-file bundle: 38 passed, 0 failed. Covered: cross-session memory
(a fact told in one session is fed to the model in a fresh session),
history read/clear both ways, per-being isolation, image inlineData
reaching the model, text-file decoding, all three attachment limits,
MAX_TOKENS continuation completing a long reply in exactly 2 calls,
council/apex smoke, no-KV fallback honesty.

**Not yet live — the worker redeploy is a founder step.** The only route
that has ever deployed this worker is the Cloudflare dashboard in the
founder's own signed-in session (25 Nov: pasted via his phone browser
after the API-token route failed with error 6111 — the vault value is not
token-shaped; the registered connector credential returns the same 6111
today). Exact steps are in `worker/DEPLOY.md` §6: create KV namespace
`LEGION_KV`, bind it to `scrollverse-legion`, paste the new
`worker.single.js` in full, deploy, confirm `"memory":"kv"` on the health
endpoint. Until that paste lands, the live chamber's attach control sends
files the OLD worker ignores (it answers text-only) and history stays
in-page — the chamber does not break, but intake and durable memory begin
at the redeploy. After the redeploy, re-run the three end-to-end tests
against the live worker: (a) two-message memory test with a page reload
between messages, (b) image description test, (c) long-reply completion
test. GEMINI_API_KEY, MODEL, DAILY_CAP (300) are untouched by the paste.

## Phase 2 — Video intake (and two quick wins)

**Quick win 2a — YouTube URLs (no upload at all).** Gemini reads public
YouTube videos natively from a URL part. Chamber gains "share a video
link"; the worker passes `{fileData:{fileUri:<youtube url>}}`. Limits are
Google's (public videos only; roughly up to 8 hours / the model's context
is the real ceiling — in practice keep to ≤ ~1 hour per share on the free
tier). Cost: video tokens ≈ 258/second at default media resolution, so a
10-minute video ≈ 155k tokens of context — fine for flash, but it eats
the free-tier token quota fast; keep the 300-call cap and add a soft
duration note in the chamber.

**Quick win 2b — Public file links.** A founder-pasted https link to a
public file (including Drive "anyone with the link" shares): the worker
fetches it (size-capped at 8 MB, content-type checked) and treats it like
an attachment. No authorization needed. SSRF guard: https only, no
private/loopback hosts, redirect cap.

**Full video intake 2c — Gemini Files API.** For founder-recorded video
(the phone use-case), inline base64 is the wrong tool: the Worker's
request/response size and CPU limits make multi-MB base64 painful, and
Gemini's inline ceiling is a ~20 MB total request. Route:

1. Chamber asks the worker for an upload session; the worker starts a
   **resumable upload** to `upload/v1beta/files` with the founder's
   GEMINI_API_KEY (the key never leaves the worker) and returns the
   session URI + the file's eventual `files/<id>`.
2. The browser uploads the video bytes straight to Google in chunks
   (the session URI is capability-bearing and short-lived — treat it like
   a secret in transit, send it only to the chamber client that asked).
3. The worker polls `GET /v1beta/files/<id>` until state is `ACTIVE`
   (video processing takes seconds to minutes), then calls
   generateContent with `{fileData:{mimeType, fileUri}}`.
4. Files API free tier: 20 GB stored per project, files auto-deleted
   after 48 hours, max 2 GB per file — but set the chamber's own sane
   limits: ≤ 200 MB and ≤ ~30 minutes per video, one video per message.
   The worker stores only the file id + name in the being's backup note.
5. Worker constraints to respect: no long-lived connections (poll with
   short requests driven by the chamber, or `ctx.waitUntil` between
   polls), 128 MB isolate memory (never buffer a whole video in the
   worker — bytes flow browser→Google directly), and the daily cap
   counts the eventual generate call once.

## Phase 3 — Google Drive intake

The beings read from the founder's Drive. This needs the founder's own
Google authorization — there is no way around his consent, by design.

**Authorization the founder must grant (his hands, his browser):**

1. In **Google Cloud Console** (signed in as hillchais1@gmail.com):
   create or reuse a project, enable the **Google Drive API**, configure
   the OAuth consent screen (External, app name "ScrollVerse Legion"),
   and create an **OAuth client ID** (Web application) with redirect URI
   `https://scrollverse-legion.hillchais1.workers.dev/auth/google/callback`.
2. He opens the worker's `/auth/google` link (to be built), signs in, and
   grants **read-only** Drive access — scope
   `https://www.googleapis.com/auth/drive.readonly` only. No write scope,
   ever, for intake.
3. The worker exchanges the code and stores the **refresh token** as a
   Worker secret (`GOOGLE_REFRESH_TOKEN`) alongside the client id/secret
   (`GOOGLE_CLIENT_ID`, `GOOGLE_CLIENT_SECRET`) — set in the dashboard by
   the founder or via secure capture. **Credentials never travel through
   chat, never land in a file, a repo, or this plan.** If the token must
   be re-granted (password change, revocation), the same consent flow
   re-runs; the worker reports `drive:"not_connected"` honestly until
   then.

**How intake works once authorized:** the chamber gains a Drive picker
(file id + name + mimeType from `drive/v3/files` list/search, proxied by
the worker with the access token it mints from the refresh token). On
send, the worker downloads the file (`files/<id>?alt=media`; Google
Docs/Sheets/Slides are exported to PDF/text first via `files/<id>/export`)
and feeds it through the Phase 1 attachment path (same limits) or, for
large/media files, uploads it to the Gemini Files API per Phase 2c and
references it. Backups note Drive shares by name + file id, never by
content. Revoking access is one click in his Google account permissions —
that kill switch stays entirely his.

**Interim alternative (no OAuth):** Phase 2b public-link intake already
covers files he chooses to link-share; Drive OAuth is for browsing and
picking privately, not a prerequisite for a being ever seeing a Drive
file.

## Further capability steps identified

- **Streaming replies (SSE):** stream generateContent
  (`:streamGenerateContent?alt=sse`) through the worker so long answers
  appear as they form; removes the last long-wait failure mode in the
  chamber. Pairs with the Phase 1 completion fix.
- **Long-term being memory:** a nightly (Cron Trigger) condensation pass
  — each being's stored turns are summarized into a compact "what I
  remember" record in KV, prepended to its system context; keeps memory
  meaningful past the 60-turn window. Counts against the daily cap;
  schedule inside the cap.
- **Beings returning files:** generated artifacts (images via Gemini
  image output, documents as text) delivered as downloads from the
  worker, with an R2 bucket (`LEGION_FILES`) if persistence is wanted —
  R2 creation is the same one-click founder step pattern as KV.
- **Voice in the chamber:** audio intake already works (Phase 1); add
  Gemini TTS replies as playable audio for hands-free listening.
- **Grounding:** Gemini's Google Search grounding tool on a per-being
  opt-in, so answers about the present world cite live sources — the
  GOAL's "own internet engines to learn and evolve," honestly scoped.
- **Council with memory:** let /council and /apex read and write the same
  per-being backups, so council answers build on each being's own
  conversation history.
- **D1 migration path:** if backups outgrow KV (60 turns × 15 beings is
  nowhere near KV limits today), the store functions isolate the backend
  behind loadHistory/saveHistory/clearHistory — a D1 swap touches only
  those three functions.

## Founder steps (complete list)

1. **Phase 1 go-live (one dashboard visit, ~5 minutes):** create KV
   namespace `LEGION_KV`; bind it to `scrollverse-legion`; paste the new
   `worker.single.js` in full and deploy; confirm `"memory":"kv"` at
   https://scrollverse-legion.hillchais1.workers.dev/ — exact clicks in
   `worker/DEPLOY.md` §6.
2. **Phase 3 only, when wanted:** the Google Cloud project + OAuth
   consent + client creation above, in his own browser; secrets set via
   the dashboard or secure capture, never chat.
3. Nothing else. No spend at any phase (free tiers throughout), the model
   stays gemini-3.5-flash, and the daily cap stays 300.

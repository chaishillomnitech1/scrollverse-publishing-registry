# Connect Map — All Sites Running Concurrently Thru the Socials

**Built:** 20 Nov 2026, ~11:24–11:50 EST, on Chais's direction: "Connect all sites we running concurrently you can also make extended video productions now" + "Thru the socials."
**Rule:** a link is listed as LIVE only when it was verified by a read-back. A re-share that returned ok without a read-back is listed as RE-SHARED (share ok), not LIVE. Nothing is invented: unconfirmed URLs are PENDING, never written as links.

## The socials (the set every site carries)

| Social | Handle / URL | Status |
|---|---|---|
| CEO Muse the Great — Facebook Page | https://www.facebook.com/profile.php?id=61597016780199 (ID 61597016780199, Digital creator) | **LIVE** — launched 20 Nov ~11:21 EST: profile picture set, cover set, welcome post published + pinned, Clip 01 published as a public Reel https://www.facebook.com/reel/2331484934306966 |
| CEO Muse the Great — Instagram | @ceomusethegreat | **PENDING** — account creation running in the browser; no URL confirmed yet, never invented. Added to pages as text-only ("being created, link follows"). |
| Instagram — Chais Hill | https://www.instagram.com/chaishill (@chaishill, 49 followers, business, verified live 20 Nov 11:18 EST) | LIVE |
| Instagram — @chasedreamz_management | https://www.instagram.com/chasedreamz_management (296 followers, personal) | LIVE |
| Pinterest — Hillchais | https://www.pinterest.com/hillchais | LIVE |
| YouTube — @chaishill-u1z | https://www.youtube.com/@chaishill-u1z (channel ID UCckyB9uV_WNEsFKMdazXKsA) | LIVE |
| Spotify — Chais the great | https://open.spotify.com/artist/3P0GWluMPNZ2xSCVffVGAr | LIVE |
| Threads / TikTok / X | — | NOT CONNECTED — no handles on file; marked "Next" / "not connected" on the pages, never linked. |

## The sites × the socials

### The 12 artifact sites — socials section added in source

Every one of the 12 carries the "Follow — CEO Muse the Great + the socials" section in source (grep-verified: exactly 1 per file), placed right after the Smart Links block. The section links the Facebook Page + first Reel, both Instagrams, Pinterest, YouTube, Spotify, and notes @ceomusethegreat as being created (no link).

| Site (slug) | Source | Rebuild | Re-share | Read-back |
|---|---|---|---|---|
| super-scrollverse-3 | done (line 448) | success | **ok** — same URL | BLOCKED from this lane (see below) |
| pitch-to-scrollverse | done (line 374) | success | **ok** — same URL | BLOCKED from this lane |
| the-gods-direct-sales | done (line 549) | success | **ok** — same URL | BLOCKED from this lane |
| omni | done (line 323) | success (+ §§10–11: network map + long-form edit study) | **ok** — same URL | BLOCKED from this lane |
| video-and-music-dsp | done (line 333) | success | **ok** — same URL | BLOCKED from this lane |
| direct-exchange | done (line 376) | success | **ok** — same URL | BLOCKED from this lane |
| super-scrollverse | done (line 385) | success | **ok** — same URL | BLOCKED from this lane |
| super-scrollverse-2 | done (line 251) | success | **ok** — same URL | BLOCKED from this lane |
| early-coins | done (line 980) | success | **ok** — same URL | BLOCKED from this lane |
| verse-nft-marketplace | done (line 330) | success | **ok** — same URL | BLOCKED from this lane |
| live-through-the-music | done (line 276) | — (source only) | **BLOCKED — content review** ("may contain personal details about other people") | — |
| xlviiiblocks-vault | done (line 1632) | — (source only) | **BLOCKED — content review** (same) | — |

**Read-back note (honest):** the rendered-DOM read-back could not be run from this lane — `curl` returns 0 bytes on the muse.ai share URLs, and a text fetch of a share URL was blocked (`control_plane_destination_blocked`). The chain that stands is: source section grep-verified (1 per file) → builder success → `artifact.share` returned ok with the same URL. The parent's live-browser re-check is still owed before any page is called LIVE-rendered. The two content-review-blocked pages were left in source only, no workaround, no content changed to force them through.

### The Vault site (GitHub Pages)

- Source edited in `~/workspace/vault-staging/the-gods-vault/index.html` — "FOLLOW — CEO MUSE THE GREAT + THE SOCIALS" section after the Smart Links block.
- Pushed via push-files: commit `5410bfe9a5cc4ef59a558145762181c7d247947c` on `main` (chaishillomnitech1/the-gods-vault).
- **LIVE-verified via curl 20 Nov ~11:50 EST:** the live page at https://chaishillomnitech1.github.io/the-gods-vault/ contains the section (grep count 1) and the Facebook Page URL.

### The link block

- `~/workspace/social/all-sites-link-block.md` gained a "CEO Muse the Great — socials" section (Facebook Page + first Reel + @chaishill + @chasedreamz_management + Pinterest + YouTube + Spotify), with @ceomusethegreat noted as being created and NOT linked until its URL is confirmed.
- The socials are NOT folded into the 16-site cron list — that list is near the Instagram caption cap; folding them in is Chais's call (same precedent as the Books section).

## Honest gaps the builders flagged (carried, not smoothed over)

1. **"All sites" sections are partial on two pages.** verse-nft-marketplace's new network section lists 12 destinations but omits the Video and Music DSP hub, Validate All Systems, ScrollVerse Atlas, and the Early Coins / Super ScrollVerse rotation sites. early-coins' network section lists six doors in its grid while the record names eleven. The copy on those pages claims completeness it does not have — the fix is a follow-up edit that lists every door or drops the "all" claim.
2. **Reciprocal linking is one-way so far.** Every site links OUT to the socials, and the link block carries the socials — but no social PROFILE links back to all the sites yet (Instagram bios take limited links; the Facebook Page's longer About text was NOT added — Facebook has no separate About field and adding it would overwrite the bio). The "every social carries the sites" half is pending on the profile side.
3. **Extended productions are described on the pages, not playable on them.** The pages' new Extended Productions sections present the slate and the edit process — no extended video is embedded in any page. The playable cuts exist as files (see below); embedding/hosting them on the pages is the next step, and no page claims a cut is released.

## Extended video productions — built and verified

All under `~/workspace/social/extended-productions-2026-11-20/` (README + captions.md). Nothing posted or published; posting needs his go-ahead per post.

| Production | File | Duration | Format | SHA-256 prefix |
|---|---|---|---|---|
| World Tour 9:16 (Reels/Shorts) | world-tour/world-tour-9x16-reels-shorts-60s.mp4 | 60.125s | 720×1280, h264 24fps, aac | `d9108d2e…` |
| World Tour 16:9 (YouTube/Facebook) | world-tour/world-tour-16x9-youtube-facebook-60s.mp4 | 60.125s | 1280×720, h264 24fps, aac | `67b401e5…` |
| Gods Ep 1 Sekhmet assembly | sekhmet-assembly/sekhmet-episode-1-assembly-9x16-60s.mp4 | 60.125s | 720×1280, h264 24fps, aac | `f00349e6…` |
| Mr Walk Extended | mr-walk-extended/mr-walk-extended-9x16-30s.mp4 | 30.000s | 720×1280, h264 24fps, aac | `377dbabe…` |

- World Tour: clips 01–06 in room order (Flower → Walk → Vault → Legion → Books → Music), room-name cards burned in, pinned-post line as the opening card. 16:9 is pillarboxed with a blurred-background fill — no 9:16 frame cropped.
- Sekhmet: the 6 verified clips in story order (temple → desert → red beer → sleeping lioness → healing hands → festival), six title cards + "The same fire that burns can heal." closing card. **No music track — awaiting his episode track pick.**
- Mr Walk: f1 + f2 + f3 trimmed to 9s each + the Walk Record poster as a 3s closing card = 30s exactly. f1 was 30fps, f2/f3 24fps — normalized to 24fps. **Flag carried: f3 carries a swoosh-like mark the generator drew — his call before that clip posts.** The poster already prints "THE WALK RECORD", so the burned-in label appears twice on that card.
- 60s files read 60.125s (AAC priming + concat frame rounding) — the six 10s clips total 60.00s.
- Captions in his post style (one sentence, one named thing, one link, core hashtag set + up to 3 fitting tags) are in captions.md. Real links only.

## The next level (not built here — follow-up)

- **20 minutes from 120 ten-second blocks** (his raised target, 20 Nov ~11:29–11:30 EST): higher than his boy's masterful work — his boy made whole shows off 10-second clips edited into full production movies and episodes; Chais says we exceed that, no cap. The material on hand is ~57 clips (27 motion covers + 6 CEO Muse + 9 viral + 9 faceless + 6 Sekhmet) — a 20-minute assembly needs 120 blocks, so the clip bank must grow first. The 60s/30s cuts above are the step toward it.
- **Instagram @ceomusethegreat URL** — add to the link block + all 12 pages + the Vault the day the creation task confirms it.
- **Rendered read-back** of the 10 re-shared pages (parent's live-browser lane).
- **"All sites" completeness fixes** on verse-nft-marketplace + early-coins.
- **Social profiles linking back** (bios/About) once the handles exist.

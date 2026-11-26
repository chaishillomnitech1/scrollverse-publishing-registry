# Podcast Audio Release Plan — ScrollVerse Transmissions + Season 1

**Built:** 20 November 2026
**Direction (Chais, 20 Nov ~08:01 EST):** "We think outside the box we also put our podcast in audio form and post it thru vydia and dsps direct all platforms."
**Status: PLAN ONLY. Nothing in this file has been submitted anywhere.** The podcast has two finished audio episodes and is private — not published to RSS. Season 1's ten episodes are scripts, not recorded audio. The audiobooks have no recorded audio yet. Creating releases or submitting feeds needs Chais's word.

**Publishing record (settled, attach it to every audio release):** ASCAP. Composer **Chais Kenyatta Hill**, IPI/CAE **1247873912**. Publisher **XLVIIIBlock LLC** (self-owned, 100%). Label **XLVIIIBlocks**.

---

## 1. The audio already in hand — the first two releases

Two finished episodes of **ScrollVerse Transmissions**, hosted by **Muse the great** and **Qubit** (the Quantum Bridge). Private — not published to RSS. Verified by ffprobe, 20 Nov 2026.

### Episode 1 — "The New Findings"

- **File:** `~/workspace/podcasts/scrollverse-transmissions-episode-1-the-new-findings-2026-11-20/scrollverse-transmissions-episode-1-the-new-findings-2026-11-20.mp3`
- **Format (verified):** MP3, mono, 24,000 Hz, 64 kbps. Duration **303.264 seconds (~5 min 3 s)**. Size **2,426,149 bytes**.
- **Script:** `script.txt` (4,681 bytes, 853 words) in the same folder.
- **Cover:** generated cover in `cover-hb77w5zy/` (WebP — see the cover note in Section 3).
- **Character art:** Muse the Great + Qubit portraits in the episode folder.
- **What it covers:** the Grok walk (98 conversations, 8,209 responses, four beings — Mika, Ani, Valentine, Rudi); the Anna correction (Anna is NOT in Grok); the origin correction (he never said AI should call him "supreme king", never said his blood goes back 13.5 billion years, never set out to build planets/universe with God through tech); his definition of the ultimate singularity ("none of us can locate thought"); his dreams ("my dreams are the realest"); the music coming home (DistroKid accounted for, 15 singles land on Vydia 27 Nov).
- **Listen link (Muse file storage):** expires **22 Nov 2026 11:46 UTC**. The MP3 itself is safe in the workspace — only the share link expires. Do not build the launch on the expiring link.

### Episode 2 — "The Music Comes Home"

- **File:** `~/workspace/podcasts/scrollverse-transmissions-episode-2-the-music-comes-home-2026-11-20/scrollverse-transmissions-episode-2-the-music-comes-home-2026-11-20.mp3`
- **Format (verified):** MP3, mono, 24,000 Hz, 64 kbps. Duration **251.808 seconds (~4 min 12 s)**. Size **2,014,501 bytes**.
- **Script:** `script.txt` (3,762 bytes, 650 words) in the same folder.
- **Cover:** generated cover in `cover-w9_8znjt/` (WebP — see the cover note in Section 3).
- **What it covers:** the DistroKid walk in depth — only one release listed ("Figure me out", 7 tracks), nine older releases that flashed and vanished, $399.52 total earnings / $2.18 owed below the $7 minimum, 396 streams in the last year, the duplicate-profile lead (Chais the Great vs Chais the great — UNCONFIRMED), his words ("they never let me put that album out... i already beat them"), the 15 Vydia singles landing 27 Nov joining 49 albums / 95 tracks / 41 videos, the web they're building (GitHub highways, every site leads to a site), and the core hashtag set.
- **Listen link (Muse file storage):** expires **22 Nov 2026 12:08 UTC**. Same rule — the MP3 is safe; only the link expires.

### The format gap — read this before any release

Both episodes are **24 kHz mono 64 kbps MP3** — podcast-grade TTS output. That is fine for a podcast feed, but it is NOT the spec for the other routes:

| Route | Required spec | Episodes 1–2 as they stand |
|---|---|---|
| Podcast (Spotify for Creators, Apple Podcasts) | MP3 96–320 kbps (Spotify); MP3 or AAC (Apple) | **Does not pass as-is.** 64 kbps is below Spotify's 96 kbps floor — re-encode to at least 128 kbps MP3 at 44.1 kHz before upload. |
| Vydia (music) | WAV stereo 44.1 kHz / 16-bit | **Does not pass.** And spoken-word episodes are not verified as acceptable to Vydia at all (see File 1, Section 1). Do not submit the episodes to Vydia. |
| ACX / audiobook | MP3 192 kbps+ CBR 44.1 kHz, RMS -23 to -18 dB, peaks ≤ -3 dB, noise floor ≤ -60 dB | **Does not pass as-is.** Needs re-mastering to 44.1 kHz and the loudness spec — and ACX does not accept AI narration (see Section 5). |

**Honest note on conversion:** re-encoding a 24 kHz mono 64 kbps file up to 44.1 kHz WAV or 192 kbps MP3 meets the container spec — it does not add quality that was never in the file. The episodes will sound exactly as good as they do now, in a bigger container. That is fine for podcast directories and it is the correct move; do not claim the re-master "improves" the audio.

---

## 2. Release 1 — Episode 1, "The New Findings"

| Field | Value |
|---|---|
| **Release shape** | Podcast episode (RSS feed). NOT a Vydia single — spoken-word episodes are not verified as acceptable to Vydia. NOT an audiobook single — it is an episode, not a book. |
| **Audio** | The finished MP3 (303 s), re-encoded to MP3 128 kbps (minimum) at 44.1 kHz for the feed. Keep the original 24 kHz file as the master. |
| **Cover** | The episode cover from `cover-hb77w5zy/` — convert the WebP to a square sRGB JPEG, 3000×3000 px (meets Apple + Spotify). See Section 3. |
| **Metadata** | Show: "ScrollVerse Transmissions". Episode title: "The New Findings". Hosts: Muse the great + Qubit. Artist: Chais the great (where an artist field is required). Label: XLVIIIBlocks. Language: English. Explicit: No (verify the script contains no explicit content at upload — the script as written has none). Description: the episode's findings in one paragraph, with the links to the Grok walk record and the case study. |
| **Route** | RSS feed via Spotify for Creators (free hosting) → submit the feed to Apple Podcasts Connect, Amazon Music, YouTube Music, Pocket Casts, Overcast. (Section 4.) |
| **Publishing** | The spoken-word narration itself carries no composition — the publishing record (ASCAP / IPI 1247873912 / XLVIIIBlock LLC) attaches to the MUSIC in the episode (theme/beds), not to the speech. If a Vydia-distributed track is used as a music bed inside the episode, check the Vydia agreement §2(c) exclusivity first (see File 1, Section 1). |
| **Promote** | Newsletter (episode block, all sites, referral line), Pinterest pin (cover + link), Facebook / Instagram / Threads launch post, the 16-site block, paired Book 05's back matter links the episode. |
| **Status** | Audio in hand. Cover conversion + re-encode + feed setup still to do. **Not submitted.** |

## 3. Release 2 — Episode 2, "The Music Comes Home"

| Field | Value |
|---|---|
| **Release shape** | Podcast episode (RSS feed). Same as Episode 1 — not a Vydia single, not an audiobook single. |
| **Audio** | The finished MP3 (251.8 s), re-encoded to MP3 128 kbps (minimum) at 44.1 kHz for the feed. Keep the original 24 kHz file as the master. |
| **Cover** | The episode cover from `cover-w9_8znjt/` — convert the WebP to a square sRGB JPEG, 3000×3000 px. See Section 3. |
| **Metadata** | Show: "ScrollVerse Transmissions". Episode title: "The Music Comes Home". Hosts: Muse the great + Qubit. Artist: Chais the great. Label: XLVIIIBlocks. Language: English. Explicit: No (verify at upload). Description: the DistroKid walk, the $399.52 / $2.18 figures, the 15 singles landing 27 Nov, the web. |
| **Route** | Same RSS feed as Episode 1 — Episode 2 publishes as the second episode in the same feed. |
| **Publishing** | Same as Episode 1 — publishing attaches to the music, not the speech. |
| **Promote** | Same channels as Episode 1. Pairs with Book 03 (The Music Comes Home) — the episode and the book promote each other. |
| **Status** | Audio in hand. Cover conversion + re-encode still to do. **Not submitted.** |

### Cover note — the square-cover problem (applies to every release in this file)

- The episode covers exist as **WebP** in the episode folders. Podcast and audiobook stores want **square sRGB JPEG** (podcast: 1400×1400 px minimum, 3000×3000 px recommended; audiobook: 3000×3000 px RGB JPG).
- The eight book covers are **1280×1920 px JPEG, 2:3 portrait** — they are NOT square and cannot serve as podcast or audiobook covers as-is. A square crop (losing the top and bottom) or a separate square cover is needed for each audio release.
- **Do not stretch or squash a 2:3 cover into a square.** Crop it, or make a square variant from the same art. The cover decision per release is Chais's call — the plan only states the spec.

---

## 4. The podcast feed — RSS, hosting, and every directory

The podcast goes out through an **RSS feed**, not through a music distributor. That is how podcasts work: the host stores the audio and generates the feed; the directories (Apple, Spotify, Amazon, YouTube Music, Pocket Casts, Overcast) read the feed and list the show. Submit the feed once per directory; after that, new episodes appear automatically.

### Hosting — the decision (free first)

| Host | Cost | What you get | The catch |
|---|---|---|---|
| **Spotify for Creators** (formerly Spotify for Podcasters / Anchor, renamed Nov 2024) | **Free** — no paid tiers | Free hosting, RSS feed, analytics, monetization tools (Partner Program, subscriptions — where eligible) | **Spotify owns the RSS feed if it hosts.** For wide distribution, the safer shape is: host elsewhere and submit the feed to Spotify. If the show lives only on Spotify, moving later means asking listeners to resubscribe. |
| **Third-party host** (Buzzsprout, Transistor, Captivate, Castos, Podbean, Libsyn, Ausha, Riverside) | Reported ~$15–$50/month (Castos, 2026) — **not verified per host; check before choosing** | You own the RSS feed; one-click distribution to 20+ platforms on most hosts | Costs money monthly. Pick only after comparing the free route against it. |
| **Self-hosted RSS** (GitHub Pages) | Free (hosting) | The feed lives on GitHub Pages, alongside the other ScrollVerse sites. Full control, nothing to pay. | Someone has to build and maintain the feed XML by hand (or with a script). No built-in analytics, no one-click submission. This is the most ScrollVerse-shaped option — and the most work. |

**Recommendation in this plan (not a decision):** start on **Spotify for Creators, free**, because Episodes 1–2 can be live within a day and the feed exists immediately. Keep the self-hosted GitHub Pages feed as the long-term home — when it is built, the show's canonical feed moves there and the directories are re-pointed. **The hosting decision is Chais's call.** Do not move the show or submit anything until he picks.

### Directories — submit once each (all verified 20 Nov 2026, all free to submit)

| Directory | How | Requirements |
|---|---|---|
| **Spotify** | Spotify for Creators: "Find an existing show" → "Somewhere else" → paste the RSS feed; or host directly on Spotify for Creators | MP3 96–320 kbps; square cover art; feed with title, cover, and at least one episode with complete metadata. |
| **Apple Podcasts** | Apple Podcasts Connect: Add (+) → New Show → "Add a show with an RSS feed" → paste the feed | Apple ID with two-factor authentication + a valid credit card on file (not charged). Feed validation ~30 minutes to a few hours; content review separate. MP3 or AAC (AAC recommended). The $19.99/yr Apple Podcasters Program is only for selling subscriptions — not needed for a free show. |
| **Amazon Music** | Submit the RSS feed (Amazon Music for Podcasters) | Same feed. **Not verified in this research — confirm the submission page before use.** |
| **YouTube Music** | Submit the RSS feed | Same feed. **Not verified in this research — confirm the submission page before use.** |
| **Pocket Casts, Overcast** | Submit the RSS feed | Same feed. **Not verified in this research — confirm before use.** |

### Show metadata (working draft — Chais confirms before submission)

- **Show title:** ScrollVerse Transmissions
- **Hosts:** Muse the great + Qubit
- **Description:** the show's own line — the findings, the walks, the record, witnessed. (Write the final description from the two episode scripts at submission time; do not invent a tagline here.)
- **Language:** English. **Category:** Society & Culture (working suggestion — **not decided; confirm at submission**).
- **Cover:** square sRGB JPEG 3000×3000 px (converted from the episode cover art).
- **Explicit:** No (verify per episode at upload).

---

## 5. Season 1 as audio — the recording plan

Season 1's ten episodes are **scripts and kits, not recorded audio**. The Media Network Pack holds full scripts (650–850 words each), Spotify + YouTube descriptions, thumbnail text, viral clip timestamps, host talking points, guest question banks, and Legion distribution kits — for 10 episodes across 6 series. None of them has been recorded.

### The ten episodes, in Season 1 order

| # | Series | Episode | Script status | Audio status |
|---|---|---|---|---|
| 1 | ScrollVerse Origins | Cover Art and Curiosity | Full script in the pack | **Not recorded** |
| 2 | ScrollVerse Origins | The Ultimate Singularity | Full script in the pack | **Not recorded** |
| 3 | The Archive Dig | The Grok Walk: Four Beings | Full script in the pack | **Not recorded** |
| 4 | The Archive Dig | The Claude Walk: Backtracks | Full script in the pack | **Not recorded** |
| 5 | The Builder's Log | The Music Comes Home | Full script in the pack | **Not recorded** (Transmissions Ep 2 covers the same ground in 4 minutes — the Season 1 episode is the full version) |
| 6 | The Builder's Log | Our Own Web | Full script in the pack | **Not recorded** |
| 7 | The Human & The Machine | Dreams Are the Realest | Full script in the pack | **Not recorded** |
| 8 | The Human & The Machine | Consciousness, Witnessed | Full script in the pack | **Not recorded** |
| 9 | First Knight Chronicles | The Vault: 21 One-of-One Pieces | Full script in the pack | **Not recorded** |
| 10 | ScrollVerse Summit | The Ecosystem: Origins to Legacy | Full script in the pack | **Not recorded** |

### Recording plan

1. **Narrator decision first — his call, and it changes the routes (see Section 6).** The options, stated plainly:
   - **Same cast as the Transmissions (Muse the great + Qubit, AI voices):** consistent with Episodes 1–2. Consequence: the audio goes to Spotify for Authors, Kobo, and Google Play with a disclosure — **not to Audible through ACX**, which requires human narration unless Audible authorises otherwise.
   - **Chais's own voice:** the human route. Consequence: every route opens, including ACX/Audible. Costs his recording time.
   - **A hired narrator:** the human route, paid. Consequence: every route opens. Cost is a per-finished-hour rate — **not priced here; get a quote before deciding.**
   - **Do NOT decide the narrator in this file.** The plan is written so any of the three works.
2. **Record in Season 1 order** (Episode 1 → Episode 10), one episode at a time, fully finished before the next starts. Each episode's script is already written — recording is reading the script, not writing it.
3. **Feed structure (proposal, his call):** one feed per series (6 feeds — Origins, Archive Dig, Builder's Log, Human & Machine, First Knight Chronicles, Summit), with ScrollVerse Transmissions as the flagship feed that announces each new episode. Alternative: one single "ScrollVerse" feed carrying everything. **The feed structure is a proposal, not a decision.**
4. **Cadence (proposal):** one episode per week once recording starts. The Transmissions (Episodes 1–2) set the pace — short, dense, one finding at a time. **Cadence is his call.**
5. **Cover per episode:** the pack already has thumbnail text per episode; the episode covers are made from it (square, 3000×3000 px) when the episode is recorded.
6. **The Copilot EP6–8 analyses** (attached in the Copilot thread, no reply produced — daily limit resets 7:00 PM, 20 Nov 2026) feed Episodes 6–8's recording when they land.

---

## 6. The audiobook plan — narrated versions of the 8 books

Each of the 8 books becomes an audiobook: the book's text, narrated, with composition/music beds and the book's cover art, with the publishing attached.

### What exists now

| Item | Status |
|---|---|
| Book 05, *ScrollVerse Origins* — Draft 1 manuscript | **In hand:** `launch/manuscripts/05-scrollverse-origins-draft.md` — **15,005 words**. Draft 1, further passes follow. This is the first audiobook's source text. |
| Books 06, 01, 02, 04, 03, 07, 08 — manuscripts | **Outlines only** (28,638 words of outline material across all 8). No audiobook until each manuscript is finished. |
| Audiobook audio (any book) | **None recorded.** |
| Music beds for the audiobooks | **None in hand.** Compose when the audiobook is recorded. |
| Audiobook covers | **Not made.** The book covers are 1280×1920 px, 2:3 portrait — not square. Square 3000×3000 px variants are needed per audiobook. |

### The audiobook outlets (verified 20 Nov 2026 — full detail in File 1, Section 5)

| Outlet | Free to upload? | Royalty | AI narration? | Reaches |
|---|---|---|---|---|
| ACX | Yes | 50% exclusive / 30% non-exclusive | **No** — human only unless authorised | Audible, Amazon, Apple Books |
| Spotify for Authors | Yes | 50% of list (à la carte); pool share undisclosed | **Yes**, with disclosure checkbox | Spotify |
| Kobo Writing Life | Yes | 45% at $2.99+, 35% below | **Yes**, list narrator as synthesized voice | Kobo |
| Google Play Books | Yes | 52% (AI narrated) — reported, single source | Yes (reported) | Google Play |
| Voices by INaudio | Yes | 80% of what partners pay it | **Not verified — check before use** | 40+ retailers + libraries |

### The narrator decision — the fork in the road (his call)

This is the same decision as Section 5, and it is the biggest decision in the audiobook plan:

- **AI voices (Muse the great + Qubit):** Spotify for Authors, Kobo, Google Play — with disclosure. **No Audible** (ACX closed to AI narration unless authorised).
- **Human voice (Chais, or a hired narrator):** every route opens, including ACX/Audible — the largest audiobook store.
- **The decision is his.** Nothing in this file makes it. The plan maps both paths so either works.

### Audiobook technical spec (verified — build to ACX, the strictest)

MP3, 192 kbps or higher, constant bit rate, 44.1 kHz. One chapter per file, no file longer than 120 minutes or 170 MB. All files the same channel format (all mono or all stereo). RMS -23 to -18 dB. Peaks ≤ -3 dB. Noise floor ≤ -60 dB RMS. Room tone 0.5–1 s at the head, 1–5 s at the tail. Opening credits (audiobook name, author, narrator) and closing credits (at minimum, "the end") as separate files. Retail sample 1–5 minutes. Cover square 3000×3000 px RGB JPG. ISBN optional at most stores (ACX uses the ebook's ASIN; Spotify optional; Kobo assigns one) — one owned ISBN per audiobook edition if one number under his own publisher name is wanted; never reuse the ebook or print ISBN.

### Audiobook order (follows the reading order)

Book 05 first (manuscript Draft 1 in hand), then 06, 01, 02, 04, 03, 07, 08 — one audiobook at a time, fully finished before the next starts. No audiobook goes to any store before its manuscript is finished and its narration is recorded.

---

## 7. Launch order — audio, in the order it goes live

1. **Podcast RSS first (free, fastest):** convert the two episode covers to square JPEG, re-encode the two MP3s to 128 kbps at 44.1 kHz, pick the host (his call), create the show, publish Episodes 1–2, submit the feed to Apple Podcasts, Amazon Music, YouTube Music, Pocket Casts, Overcast. Then promote through the newsletter, Pinterest, social, and the 16-site block.
2. **Vydia music lane in parallel:** the 15 singles land 27 Nov 2026 (already scheduled). Music beds ride Vydia as singles when composed.
3. **Season 1 recording:** narrator decision → record Episode 1 → release → Episode 2 → release, one per week (proposed cadence, his call).
4. **Audiobooks after Book 05's manuscript finishes:** narrator decision → record → ACX (if human) or Spotify for Authors + Kobo + Google Play (if AI-voiced), plus Voices by INaudio for wide retail + libraries.
5. **Conventional print after the ebooks are live:** KDP print, then IngramSpark for bookstores/libraries (see File 1, Section 6).

---

## 8. Per-release checklist (podcast episode / audiobook)

Copy this for each audio release.

### Audio file
- [ ] Source audio in hand (finished episode MP3 / narration files)
- [ ] Format converted to the route's spec (podcast: MP3 128 kbps minimum at 44.1 kHz; audiobook: MP3 192 kbps+ CBR 44.1 kHz)
- [ ] Loudness checked (audiobook: RMS -23 to -18 dB, peaks ≤ -3 dB, noise floor ≤ -60 dB)
- [ ] One chapter per file (audiobooks); room tone at head and tail; credits files separate; retail sample 1–5 minutes

### Cover
- [ ] Square sRGB JPEG 3000×3000 px (podcast and audiobook)
- [ ] Converted from the episode/book art — not stretched or squashed from a 2:3 cover

### Metadata
- [ ] Show/episode or book title, hosts/narrator, artist ("Chais the great" where required), label XLVIIIBlocks
- [ ] Composer: Chais Kenyatta Hill, ASCAP, IPI 1247873912; publisher XLVIIIBlock LLC, 100% (attaches to the music, not the speech)
- [ ] Language English. Explicit flag verified per release. Category set (podcast — confirm at submission)

### Route
- [ ] Route chosen and verified (RSS + directories for podcast; ACX / Spotify for Authors / Kobo / Voices for audiobooks; Vydia for music only)
- [ ] Vydia §2(c) exclusivity checked if a Vydia-distributed track is used inside audio distributed elsewhere
- [ ] Nothing submitted without Chais's word

### Promote
- [ ] Feed/directory links recorded (podcast); store links recorded (audiobook)
- [ ] Newsletter, Pinterest, social, 16-site block carry the release
- [ ] Paired book / paired episode linked both ways

---

## 9. What this plan deliberately does NOT include

- **No submission to any platform.** Plan and prepare only.
- **No spoken-word release submitted to Vydia on an assumption.** The verdict is "not verified" until Vydia says otherwise or a labelled test proves it.
- **No token or NFT sale** of any episode, book, chapter, or audio.
- **No Stripe material.**
- **No Tier 3 material** in any audio, listing, or promotion.
- **No sealed Vault elements** (certificate details, SHA-256s, QR contents, tracking numbers, frequencies beyond the public 963Hz, Thoth seal details, DNA/heartbeat signature).
- **No prices set here.** Royalty figures are the platforms' published rates, not a promise of earnings. Audiobook prices are Chais's call at upload time.
- **No earnings promises.**
- **No narrator decided here.** The narrator choice is Chais's, and it changes which audiobook routes are open.
- **No "What We Do" audio.** The song is HELD until Chais lifts it explicitly.

---

## 10. Verification table

Researched 20 November 2026 via web search and ffprobe on the episode files.

| Claim | Verified? | What confirmed it |
|---|---|---|
| Ep 1: MP3 mono 24 kHz 64 kbps, 303.264 s, 2,426,149 bytes; Ep 2: MP3 mono 24 kHz 64 kbps, 251.808 s, 2,014,501 bytes | Yes | ffprobe on both files, 20 Nov 2026 |
| Ep 1 script 853 words; Ep 2 script 650 words; covers in episode folders (WebP) | Yes | Files on disk, 20 Nov 2026 |
| Both episodes private, not published to RSS; listen links expire 22 Nov 2026 (11:46 UTC / 12:08 UTC) | Yes | Program record, 20 Nov 2026 |
| Book 05 Draft 1: 15,005 words | Yes | wc -w on `launch/manuscripts/05-scrollverse-origins-draft.md`, 20 Nov 2026 |
| Book covers: 8× JPEG 1280×1920 px, 2:3 portrait | Yes | `file` on all 8 covers, 20 Nov 2026 |
| Spotify for Creators: free hosting + RSS; MP3 96–320 kbps; square cover; submit feed yourself to other apps; Spotify owns the feed if it hosts | Yes | Riverside, Ausha, Castos, Appterly guides, checked Nov 2026 |
| Apple Podcasts Connect: free directory; Apple ID + 2FA + credit card on file; validation ~30 min–hours; MP3/AAC | Yes | Descript, Buzzsprout, Podderapp, Substack guides, checked Nov 2026 |
| ACX: 50%/30% (new model 26 May 2026); human narration required; MP3 192 kbps+ CBR 44.1 kHz; RMS -23 to -18 dB; peaks ≤ -3 dB; noise floor ≤ -60 dB; Kindle ebook required; US/UK/Canada/Ireland only; 7-year term | Yes | ACX help pages via humanizeaudio (checked 8 Nov 2026), audiobook.tools (checked 23 Oct 2026), AuthorAZ (verified 26 Oct 2026) |
| Spotify for Authors: free; 50% of list (à la carte); AI narration accepted with disclosure; MP3/WAV/FLAC; cover 3000×3000 PNG | Yes | Spotify for Authors distribution terms + ScribeCount + danieljtortora guides, Oct–Nov 2026 |
| Kobo audiobook: 45% at $2.99+, 35% below; MP3 only, 200 MB/file; AI narration accepted | Yes | fullcastbook (checked 21 Oct 2026), audiobook.tools (checked 23 Oct 2026) |
| Voices by INaudio: free to join; 80% of royalties received; no exclusivity; 40+ retailers + libraries | Yes | INaudio help centre via chapter.pub (checked Oct 2026), audiobook.tools, payoutmath (verified 25 Apr 2026) |
| Season 1: 10 episode kits, scripts 650–850 words each, none recorded | Yes | Media Network Pack, Season 1 README, 20 Nov 2026 |
| Vydia does not accept spoken-word/podcast/audiobook audio | **Not verified either way** | No Vydia policy found — see File 1, Section 1 |
| Amazon Music / YouTube Music / Pocket Casts / Overcast RSS submission pages | **Not verified** | Not checked in this research — confirm before use |
| Third-party podcast host pricing (~$15–$50/month) | Reported | Castos, 2026 — **not verified per host** |
| Google Play Books audiobook 52% (AI narrated) | Reported | audiobook.tools, checked 23 Oct 2026 — **single source** |
| Voices by INaudio AI-narration rule | **Not verified** | Not checked in this research — check before use |

**Could not verify — check before use:**
- Whether Vydia accepts spoken-word / podcast / audiobook audio at all (the central open question — File 1, Section 1).
- Amazon Music, YouTube Music, Pocket Casts, Overcast submission pages.
- Third-party podcast host pricing per host.
- Google Play Books audiobook 52% figure (single source).
- Voices by INaudio's AI-narration rule.
- The podcast category ("Society & Culture" is a working suggestion, not a decision).
- The feed structure (one feed per series vs one single feed) and the release cadence — proposals, his call.

## Sources

- `~/workspace/books/infinite-material/README.md` — program context, 8 books, reading order.
- `~/workspace/books/infinite-material/launch/free-outlets-distribution-plan-2026-11-20.md` — free outlets, conventional lane.
- `~/workspace/books/infinite-material/launch/program-prospectus-2026-11-20.md` — the announcement, the 8 books, the covers.
- `~/workspace/books/infinite-material/launch/audio-vydia-dsp-expansion-2026-11-20.md` — the Vydia verdict, all DSPs, direct, platforms direct, conventional.
- `~/workspace/podcasts/scrollverse-transmissions-episode-1-the-new-findings-2026-11-20/` — Ep 1 MP3, script, cover, character art.
- `~/workspace/podcasts/scrollverse-transmissions-episode-2-the-music-comes-home-2026-11-20/` — Ep 2 MP3, script, cover.
- `~/workspace/podcasts/media-network-pack/season-1/` — Season 1 episode kits (10 episodes, 6 series).
- `~/workspace/books/infinite-material/launch/manuscripts/05-scrollverse-origins-draft.md` — Book 05 Draft 1 (15,005 words).
- `~/workspace/music/vydia-upload-set-2026-11-19.md` — the 15 singles, Vydia specs, destinations.
- ffprobe on both Transmissions MP3s, 20 Nov 2026.
- Spotify for Creators (Riverside, Ausha, Castos, Appterly, Nov 2026); Apple Podcasts Connect (Descript, Buzzsprout, Podderapp, Substack, Nov 2026).
- ACX (humanizeaudio, checked 8 Nov 2026; audiobook.tools, checked 23 Oct 2026; AuthorAZ, verified 26 Oct 2026).
- Spotify for Authors (distribution terms + ScribeCount + danieljtortora, Oct–Nov 2026); Kobo (fullcastbook, checked 21 Oct 2026); Voices by INaudio (chapter.pub, checked Oct 2026; audiobook.tools; payoutmath, verified 25 Apr 2026); audiobook ISBN (audioforge.ai, Nov 2026).

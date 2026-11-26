# Storybook Score Treatment — standing spec for all nine flagship books

**Original directive (founder, 25 Nov 2026, his words):** "We can even attach my music as score but not over powering the narrator."
**Pilot landed:** *The Architecture of Eternity* — `flagship/architecture-of-eternity/narration-score-pilot.mp3`, SHA-256 `55e5a7f6b81ca5bc10ed2b0f42565fa3c57028b8a9f2e979ad8bcd3511aeb250`, full mix record in that book's `illustrations-record.md` ("Narration + score pilot" section). The pilot's bed-and-ducking mix stands as **v1**.

**SUPERSEDING DIRECTIVE — the founder's mix law (25 Nov 2026, ~16:16 EST, his words):** *"Let's not put the music until the talking stops so it don't clash and we can have multiple digital intelligence discuss together in many ways but we play the music at the end so all had it's place."* **No music under speech, anywhere.** The music plays only where no one is talking: the theme, full and present, at the beginning before the first word, and the theme again at the end after the last word. This law supersedes the pilot's bed/ducking treatment everywhere in this spec (see §6, where the old numbers are kept, marked superseded, for the record).
**Theme pick (founder, 25 Nov 2026): "Faces"** — his signature song is THE theme, first struck for *The Architecture of Eternity* (`narration-score-theme-cut.mp3`, the standing version; full record in that book's `illustrations-record.md`, "Theme cut" section).

---

## 1. The rule

Every flagship storybook gets a narrated reading of its full text, **clean — no music beneath any word** — framed by **the founder's own music as the theme**: full and present before the first word, and full again after the last word, so the voices and the music each have their place and never clash. A brief musical breath may sit inside a natural silence at a page transition **only where it genuinely fits** (measured per book; in the Eternity stem every pause runs 0.60–0.72 s and none fit, so none were placed). The clean narration stem is the permanent asset of every book; the theme is a frame that can be swapped without ever touching the voice.

## 2. His music only — source discipline

- All music used — bookend themes and any transition breaths — comes **only from the founder's own catalog and masters** held locally. He owns 100% of his catalog; no third-party tracks, no stock music, no streaming downloads.
- **Instrumentals first.** A bed must not carry a lead vocal — a second voice under the narrator breaks the rule no matter how low it sits. Documented instrumentals and the beats held in his masters are the source pool.
- **Excluded, always:** the 146 Nero Knight beat previews in `~/workspace/gmail-cleanup/backup-music-2026-11-17/` — those are another producer's previews sent to him, not his catalog. Also excluded: TTS/narration audio, podcast episodes, and any file whose provenance is unclear (e.g. unattributed "score" clips from studio sessions).
- **Vocal masters are not beds** unless the founder names a specific song for a specific book. If he ever wants a named song's music under a book, the file needed is that song's **instrumental/beat version** from his masters or Drive — vocal masters will not be substituted silently.
- Every bed is fingerprinted (SHA-256) in the book's record before mixing, from its canonical local source.

## 3. Local score pool (verified on disk, 25 Nov 2026)

From 645 audio files workspace-wide, the usable pool of his music is:

- **His documented solo instrumental:** `drilltypebeat` (untitled, title TBD by the founder) — `~/workspace/music-masters/phone/drilltypebeat.mp3`, 291.9 s, SHA-256 `d502a2f1…` — catalogued as "Chais The Great — INSTRUMENTAL" in `all-songs-master-inventory-2026-11-19.md`. **Used in the pilot.**
- **His beats library** (`~/workspace/music-masters/drive-new/beats/`, 22 files): All Me, Already, BankRoll 180, California, Divinity, DoveLove 80, Feel It In The Air (178 bpm), ForeverYoung 143, GLASS, GhostHalo 92, Legend, Major, Nevermind, Penance, ShotGunner 140, Solitude, Sunset, Visiting, Windy, Written In The Stars (Yung Nab, 144 bpm — the beat under his own "What We Do"), broke guitar, + `penny beat` (browser downloads copy).
- **The VICTORY bed precedent:** `~/workspace/video-catalogue/feature-program-2026-11-21/feature-01-restoration-film/score-bed.m4a` (24:55, built from his VICTORY for his own film program, already level-set ≈10 dB under master level) — proof the house has done this treatment before; usable for an anthemic book after a vocal-content check.
- **His song masters** (41 phone masters in `~/workspace/user/files/` + the full archive under `~/workspace/music-masters/` — drive, drive-new, gmail-mtm, phone, vydia-wav, unreleased): the catalog itself; vocal, so reference/context only under §2 unless he names one.

## 4. Per-book music selection — the theme is the founder's pick

Under the mix law, each book's music is its **theme** — a signature song the founder picks from his catalog (Faces for Eternity, picked 25 Nov 2026) — heard at the open and the close, never under the reading. The mood-matched candidates below remain useful as the founder's picking list and as the only permitted source of *transition breaths* (a breath, where a silence genuinely fits, comes from the book's instrumental pool, never from a vocal master). The founder's ear and word confirm each book's theme before its cut is final.

| Book | Mood | Theme / breath candidate(s) | Status |
|---|---|---|---|
| The Architecture of Eternity | Cosmic, sovereign, golden | **Theme: "Faces" (founder's pick)** — phone master, SHA-256 `906b4231…`; v1 pilot bed was `drilltypebeat` | **Theme cut landed — standing version** |
| The Fluidity of Existence | Flowing, philosophical, deep | Solitude · GhostHalo 92 · Divinity | Candidate — his ear |
| The Echo Stream | Reflective, echoing, spacious | GhostHalo 92 · Solitude | Candidate — his ear |
| Elara and the Shimmering Seed | Wonder, young, luminous | DoveLove 80 · ForeverYoung 143 | Candidate — his ear |
| The Paths of Elara | Journey, gentle adventure | Sunset · ForeverYoung 143 | Candidate — his ear |
| The Little Cloud Who Stayed | Softest, tender, children's | DoveLove 80 · broke guitar | Candidate — his ear |
| Akito's Grand Adventure | Bright, anime adventure energy | Windy · Sunset | Candidate — his ear |
| Karate Scotty and the Lumina's Light | Playful action, light | Major · ShotGunner 140 (low in the mix) | Candidate — his ear |
| The ScrollVerse Unfurled | Anthemic, founding, epic | VICTORY bed (score-bed.m4a precedent) · Written In The Stars | Candidate — his ear + vocal check on the bed |

## 5. Narration standard

- House TTS, **one narrator voice per book** (pilot voice: Helio, the house default), same voice across a book's whole reading.
- Text is the book's recovered text **verbatim**: spoken title block (title, subtitle if any, author line), then the pages in order. Mechanical "Page N" labels are not spoken; page turns are carried by a natural pause.
- The voice stem is loudness-normalized **before** any assembly (pilot: −17 LUFS target; measured −18.28 LUFS integrated, true peak −1.83 dB) and **preserved in the book's flagship folder as `narration-voice-stem.mp3`, fingerprinted in the book's record** — it is the book's permanent audio asset. Themes are assembled around it; the stem itself is never re-rendered or re-processed to change a theme.

## 6. Mix standard — the mix law (standing, 25 Nov 2026)

- **No music under speech. Zero.** The narration stem enters the assembly untouched and alone; no bed, no ducking, no exceptions — for narrators and for intelligences in discussion alike, the talking is never scored.
- **Theme bookends:** a full-presence excerpt of the book's theme (20–40 s; Eternity: 32 s) opens the piece before the first word — let the song establish itself, choosing its strongest passage (Eternity/Faces: the build through the full-power entrance, master 0:12–0:44). After the last word, the theme returns and closes the piece in full presence with a clean ending (Eternity: the master's own outro and natural fade, 31.6 s). Short clean silences separate theme from voice (≈1 s each side) so the two never touch.
- **Transition breaths (optional, measured):** only inside a natural silence at a page transition, only where the pause genuinely fits a breath that fades fully in and out without touching speech on either side. Measure the stem's pauses first; if none fit, place none and record that decision (Eternity: thirteen pauses, all 0.60–0.72 s — none placed).
- **Staging:** theme excerpts carry **one shared gain per master** (the master's internal balance stays honest), staged hot — full presence, a few dB above the voice's integrated level (Eternity: excerpts −4.0 dB → open ≈ −14.0 LUFS against the voice's −18.28 LUFS). The voice is never gained to meet the music.
- **Final pass:** one **constant gain** across the assembled program to −16 LUFS integrated, true peak ≤ −1.5 dB (Eternity: −0.82 dB → measured −16.26 LUFS / TP −2.95 dB). **No limiter, no compressor, no loudnorm dynamics in the delivered chain** — the Eternity build proved by null test that a safety limiter was not transparent on the voice; it was pulled and the cut rebuilt gain-only. If the constant gain cannot satisfy both targets, trim to the peak target and let the integrated level sit where it lands.
- **Delivery:** MP3 192 kbps, 48 kHz, stereo (voice centered); filename `narration-score-theme-cut.mp3` in the book's flagship folder during the transition (the pilot keeps its `-pilot` name as v1).
- **Verification before delivery (all four, measured, recorded):** (1) master null test — the narration window of the assembled master minus the clean stem reads digital silence (−91.0 dB at Eternity); (2) delivered-file null test — the same window minus the stem through the same gain reads codec floor only (−49.9 dB mean / −30.7 dB max at Eternity); (3) the silences between theme and voice measure pure silence; (4) theme windows at both ends measure full presence. SHA-256 of the cut, the theme master, and the stem all entered in the book's record.

### Superseded — the v1 pilot treatment (kept for the record)

The numbers below governed the Eternity pilot mix only and are **superseded by the founder's mix-law directive of 25 Nov 2026 (~16:16 EST)**; they are not the standing treatment for any book:

- Static bed level −20 dB under the narration mean (band −22 to −18 dB); pilot gain −28.4 dB → bed mean −38.6 dB.
- Sidechain ducking keyed by the narration (6:1, threshold 0.02, attack 40 ms, release 350 ms), bed breathing in the pauses.
- Bed fades 3 s in / 6 s out across a ~3 s music tail; final loudness pass −16 LUFS / TP −1.5 dB.

## 7. How it attaches to each presentation

Each book's presentation artifact gains a **"Listen"** element by edit, on the strength of the founder's word already given for this treatment:

- The theme cut sits at the book's presentation beside its motion cover — the cover in motion as the visual anchor, the reading as the audio layer (a native audio player on the page; the file itself stays in the book's flagship folder as the fingerprinted master).
- The certificate panel gains one line: the theme credit — the theme song's name/source and its fingerprint, with the mix-law line: *his music as the theme at the beginning and the end; no music under the narration, so all had its place.*
- Nothing about sharing changes: artifacts stay unshared until the founder's explicit word, per standing rule. The scored reading inherits the book's own status (HELD / presented), and the hidden-keys layer is untouched — the audio carries the story's words only, no key, no value.

## 8. Gaps and honest limits

- Locally, exactly **one** of his tracks is documented as a solo instrumental (`drilltypebeat`); the rest of the pool is his beats library. If the founder wants a specific **song's** instrumental as a bed, that song's instrumental file has to come from his masters/Drive — it is not in the local pool today.
- Candidate pairings in §4 are mood matches by title and character, not yet by his ear; each becomes final only when he confirms it (or names another).
- The VICTORY `score-bed.m4a` needs a vocal-content check before any use under narration — its title tag is the vocal master, and a bed with his sung/rapped voice under the narrator would break §2 even at pilot levels.

---

**Amendment — final tightening (25 Nov 2026, founder's words): "But while talking music only beginning then end."** The transition-breath allowance is removed: music appears ONLY at the very beginning (theme, before the first word) and at the very end (theme, after the last word) — nowhere else, not even in silences between pages. The body of every book is voice alone, start to finish. Themes are assigned per book from the founder's pool (Moment · Listen · Paradise AC · Promise Land · What's It Gonna Take · Faces as the signature for The ScrollVerse Unfurled). This supersedes the bed, blended, ducked, spurts, and breath treatments above wherever they conflict.

---

## THE COMPLETION LAW — EVERY STORYBOOK HAS AUDIO NARRATION (founder, 25 Nov 2026)
*His words: "make sure the story books every one has audio narration."*
Every storybook in the census — all 1,193 titles — gets its audio narration. A book is NOT complete without its voice: text, illustrations, motion, **narration**, video, presentation, registration — the narration is a required layer, never optional. The flagship nine carry theirs (mix law: theme at the beginning and the end only, voice alone between; clean stems preserved). The Thursday perpetual build carries the law book by book in census order — recover, illustrate, move, **narrate**, assemble, present, register — until the whole census speaks. No book is ever presented as finished with its narration missing; a book mid-pipeline is reported as exactly that.

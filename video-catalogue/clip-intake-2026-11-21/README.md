# Clip Intake — README

This folder is the intake desk for Chais Hill's film clips. He sends clips in bulk; this is where they get catalogued and turned into new work.

## Files

- `catalog.md` — the master catalog. One row per clip: stable ID, file, batch, duration, dimensions/orientation, content description, suggested placement. Also the placement lanes.
- `first-creation-plan.md` — the first new creation built from the intake clips ("LEY LINE WALKER — The Map Remembers"). Plan only until Chais approves generation.
- Future creation plans go here as `creation-plan-NN-<slug>.md`.

## Clip IDs

Stable IDs, assigned in arrival order — cite these in plans, never the hash filenames:
- `BIKE-01` — the dirt-bike video (Vineland Marketplace).
- `B1-01`–`B1-99` — Batch 1 (10 clips, 21 Nov ~15:22 EST).
- `B2-01`–`B2-99` — Batch 2 (9 clips, 21 Nov ~15:27 EST).
- `B3-01`–`B3-99` — Batch 3, Chronovisor (10 clips, 21 Nov ~15:35 EST).
- `B4-01`–`B4-99` — Batch 4 (10 clips, 21 Nov ~15:39 EST).
- `B5-01`–`B5-99` — Batch 5 (10 clips, 21 Nov ~15:42 EST).
- Next batch: `B6-01`…, and so on.

## Adding a new batch

1. **List the files** under `~/workspace/user/media_library/video/<hash>/<hash>.mp4` and note the batch number + arrival time.
2. **ffprobe each clip** (duration, dimensions):
   ```bash
   cd ~/workspace/user/media_library/video
   for f in <batch files>; do printf '%s | ' "$f"; ffprobe -v error -show_entries stream=width,height -show_entries format=duration,size -of csv=p=0 "$f" | tr '\n' ' '; echo; done
   ```
3. **Extract mid-frames** and build a contact sheet (one frame per clip, normalized to 320×320 padded, tiled 5 across):
   ```bash
   mkdir -p /tmp/intakeN
   # per clip: mid=$(duration/2); ffmpeg -ss $mid -i "$f" -frames:v 1 -vf "scale=320:320:force_original_aspect_ratio=decrease,pad=320:320:(ow-iw)/2:(oh-ih)/2" /tmp/intakeN/fNN.jpg
   # then hstack rows of 5 + vstack into a sheet, and read the sheet image
   ```
4. **Describe each clip** from its mid-frame (and, for long clips like B1-07, check 2–3 frames across the duration). One sentence of content + one suggested placement.
5. **Append rows** to `catalog.md` with the next batch IDs, and update the totals at the top. Update the placement lanes if a new lane appears (as "Ley Line Walker" did in Batch 2).
6. **Do not move, copy, or rename the source files** — the catalog describes them where they live in the media library.

## Rules that never change

- **Plan only until approved:** new generations, spends, and publishes need Chais's go-ahead. The intake itself (cataloguing, frames, plans) is covered by his standing mandate.
- **Contest separation:** the Higgsfield Talent Contest entry (Black Atlantic City) is built from Higgsfield generations/edits only. Intake clips enter that film only via a Qualifying Higgsfield Edit, on his go-ahead — never as-is.
- **Likeness:** clips showing a real person or a real place (e.g. BIKE-01, Vineland Marketplace) never go into the contest entry or any fictional-only register.
- **No spend without go-ahead.** Kling Bonus credits expire 22 Dec 2026; Higgsfield sits at 6 credits; Flow is 50 free credits/day.

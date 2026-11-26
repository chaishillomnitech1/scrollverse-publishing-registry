# Rollout Plan — Priority Order

**Built:** 20 Nov 2026. **Direction:** add the tech to ALL, especially builds + intelligence implementation; shrink nothing. **Method:** one site at a time, verify each addition renders before moving on. The parent applies the edits (artifact.edit per site, or source + push-files for the Vault site, or code lane for scrollverse-web-app). **No edit in this pack — this is the instruction set.**

**Per-site edit instruction format:** `artifact.edit` on the slug with the kit sections listed (K0–K10 in implementation-kit.md). After each edit: re-share at the same URL (where the page is already shared) and verify — toggle switches, anchor scrolls smooth, cards lift, heartbeat pulses, Arena e2→e4 works, form opens mailto, no console errors, no mobile overflow, no content removed.

## Wave 0 — DONE (reference, no edit)

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 0 | `sovereignhub` | Nothing — it already has T1–T9 | None. This is the reference build every other site is measured against. |

## Wave 1 — The flagship (most-visited first)

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 1 | `super-scrollverse` (Atlas) | T1–T9 all | `artifact.edit` slug `super-scrollverse`: apply K0 + K9 (look), K1, K2, K3, K4, K5 Arena embed (Play section), K6 Dreams room, K7 source-trail on every claim + Ledger section, K8 contact form. Verify per K10. |
| 2 | `super-scrollverse-3` | T1–T9 all | Same edit as #1, slug `super-scrollverse-3`. |
| 3 | `super-scrollverse-2` | T1–T9 all | Same edit as #1, slug `super-scrollverse-2`. |

## Wave 2 — The hubs

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 4 | `omni` | T1–T9 all (T7 first) | `artifact.edit` slug `omni`: K0 + K9, K1–K4, K5 Arena, K6 Dreams room, **K7 first** — the Ledger pattern slots onto its existing §§10–11 network map, K8 contact form. Verify per K10. |
| 5 | `video-and-music-dsp` | T1–T9 all (T5 first) | `artifact.edit` slug `video-and-music-dsp`: K0 + K9, K1–K4, **K5 Arena first** (the Play section is this page's job), K6 Dreams room, K7, K8. Verify per K10. |

## Wave 3 — Commerce + exchange (trust-led)

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 6 | `the-gods-direct-sales` | T1–T4, T7, T8, T9 (no T5, no T6) | `artifact.edit` slug `the-gods-direct-sales`: K0 + K9, K1–K4, **K7 source-trail per piece** (certificate + SHA-256 + QR + tracking already on record — make the chain visible), K8 contact form. No Arena, no Dreams room on a sales page. Verify per K10. |
| 7 | `direct-exchange` | T1–T4, T7, T8, T9 | `artifact.edit` slug `direct-exchange`: K0 + K9, K1–K4, **K7 + K4 first** (trust-lens + source-trail are this page's job), K8 contact form. Verify per K10. |
| 8 | `pitch-to-scrollverse` | T1–T4, T7, T8, T9 | `artifact.edit` slug `pitch-to-scrollverse`: K0 + K9, K1–K4, K7, **K8 contact form first** (a pitch page's job is to be reached). Verify per K10. |
| 9 | `early-coins` | T1–T4, T7, T9 (no T5, no T6, no T8) | `artifact.edit` slug `early-coins`: K0 + K9, K1–K4, **K7 Ledger on the registry rows** (each coin's status + source). No coin is launched — that fact stays stated, never softened. Also fix the known gap: its network section lists six doors while the record names eleven — list every door or drop the "all" claim. Verify per K10. |
| 10 | `verse-nft-marketplace` | T1–T4, T7, T9 (no T5, no T6, no T8) | `artifact.edit` slug `verse-nft-marketplace`: K0 + K9, K1–K4, **K7 source-trail per listing** (the three-ways-per-song lanes stay as stated: music NFT/coin, cover-art NFT, publishing). Also fix the known gap: its "all sites" section omits the DSP hub, Validate All Systems, Atlas, and the Early Coins / Super ScrollVerse rotation sites — list every door or drop the "all" claim. No mint/sale language changes — the Howey gate still stands. Verify per K10. |

## Wave 4 — BLOCKED (waits on his call, no edit until then)

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 11 | `live-through-the-music` | T1–T9 all — **after** his redaction call | BLOCKED content review. Do not edit, do not re-share, do not work around. When he gives the redaction/anonymization call, apply the Wave 1 edit (slug `live-through-the-music`), then re-share. |
| 12 | `xlviiiblocks-vault` | T1–T9 all — **after** his redaction call | Same as #11, slug `xlviiiblocks-vault`. |

## Wave 5 — The Vault site (GitHub Pages lane)

| # | Site | What to add | Edit instruction |
|---|---|---|---|
| 13 | the-gods-vault | T1–T4, T7, T8, T9 (no T5, no T6) | Edit `~/workspace/vault-staging/the-gods-vault/index.html` with K0 + K9, K1–K4, K7 Ledger chain per piece, K8 contact form; push via push-files; verify live with curl grep (same method as 20 Nov ~11:50 EST). No Arena, no Dreams room on a sales page. |

## Wave 6 — Intelligence implementations (code lane, not artifact edit)

| # | Surface | What to add | Edit instruction |
|---|---|---|---|
| 14 | Chess Arena (`ScrollVerseChessArena.tsx`) | T1–T4, T7, T9 around the game | Code edit in scrollverse-web-app: wrap the existing playable board (273 lines — do not rebuild the game) with the K0 tokens, K1 toggle, K2 smooth scroll, K3 hover, K4 heartbeat, K7 source-trail, K9 look. Verify e2→e4 still works after the wrap. |
| 15 | Omniland district + Source Atlas + Consoleless Delivery + Embodied Play | T1–T4, T7, T9 | Code edits in scrollverse-web-app: K0 + K9, K1–K4, K7. Source Atlas already HAS T7 (the principle lives there) — it needs look + motion only. Add a Play link to the Arena on Omniland. |
| 16 | GameWorldsStudio (5 worlds) | T1–T4, T7, T9 + Arena link | Code edit: K0 + K9, K1–K4, K7 source-trail per world, a Play link to the Arena. Concept pages stay concept pages — no game is claimed playable that is not. |
| 17 | Game Systems Blueprint (5 study lanes) | T7, T9 | Code edit: K7 source-trail per lane + K9 look. |
| 18 | Sovereign Archive replica page | T1, T2, T3 only | Code edit: it already HAS T4, T7, T9 (PortalTrustLens + useSovereignHeartbeat, Space Grotesk, `#040914`). Add K1 toggle, K2 smooth scroll, K3 hover. Do not re-point the dead original link — the replica links back to the new sovereignhub build instead. |

## §4 — Legion beings: naming, not code

The beings are not pages, so their rollout is **presence naming** on the sites above, one line per room, with map status carried:

- **The Music rooms** (video-and-music-dsp, live-through-the-music, omni): Qubit (co-host, EMBEDDED-LIVE voice/captions) + Lyrian Lion (distribution, ASSIGNED) + King Solomon AI (teaching line, EMBEDDED-LIVE recorded).
- **The Flower rooms** (Atlas, super-scrollverse-2/3): Socratica + King Solomon AI (ASSIGNED / EMBEDDED-LIVE teaching line).
- **The Walk rooms** (super-scrollverse editions, omni): ZERO Flame (ASSIGNED).
- **The Books rooms** (Atlas library, omni): PSYCHE16 (ASSIGNED) + QFS Oracle (analytics only, ASSIGNED — never as a poster).
- **The Vault / commerce pages**: Azurath (guard, EMBEDDED-LIVE review) + NŪR Cities AI (links, EMBEDDED-LIVE) + Omnitech1 (ops, EMBEDDED-LIVE).
- **Visuals everywhere**: Tatras (ASSIGNED). **New ideas**: Prometheus (ASSIGNED). **Next-gen**: Londyn AI + Knick (ASSIGNED). **Systems**: Manus (EMBEDDED-CODE platform key / ASSIGNED systems — never as live chat).
- **The 9 invited AI**: named nowhere as present. Only as *when they join* — Claude first in queue, waits on his word by name.

**Hard rule:** no being is named live who is only ASSIGNED. No live chat is claimed anywhere — live talk stays BLOCKED (no backend/key outside Manus). Presence is name + role + lane, nothing more.

## §5 — Second wave (not in the named 13 — after Waves 1–6)

`join-the-ai-legion`, `the-chronovisor`, `scrollverse-beyond`, `free-avenues`, `catalog-case-studies-blueprint`, `sync-licensing-jingles`, `omnitech1-ai-infrastructure`, `professor-penny-limitless`, `reply-to-the-scrollverse-newsletter`, `scrollverse-master-file-transferable`, `shielded-transmission-language`, `tory-lanez-crypto-music-playbook`, `validate-all-systems`. Same kit, same verify step, in the order he calls them. `intelligence-fusion-the-real-study` is NEVER in any wave — PRIVATE, excluded always.

## Rollout order (one line)

sovereignhub (done) → Atlas → super-scrollverse-3 → super-scrollverse-2 → omni → video-and-music-dsp → the-gods-direct-sales → direct-exchange → pitch-to-scrollverse → early-coins → verse-nft-marketplace → [BLOCKED: live-through-the-music, xlviiiblocks-vault — on his redaction call] → the-gods-vault (GitHub Pages) → Chess Arena wrap → Omniland family → GameWorldsStudio → Blueprint → replica page → Legion presence naming → second-wave catalog sites.

## Acceptance test (per site, before it is called done)

Toggle switches visibly · anchor jumps scroll smoothly · cards lift on hover · heartbeat pulses · Arena e2→e4 works where embedded · form opens mailto where added · no console errors · no mobile overflow · **no content removed, no composition shortened, no title or lyric altered** · gaps still labeled as gaps · gates held (no fusion, no Tier 3, no third-party IP, Bordley consent unchanged, no unverified money figures, What We Do held).

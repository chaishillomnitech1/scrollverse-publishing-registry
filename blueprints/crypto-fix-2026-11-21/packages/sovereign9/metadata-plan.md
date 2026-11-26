# Sovereign 9 — Per-Token Metadata Plan

**One metadata JSON per player. Verified CIDs only. No invented art.**

## CID verification (21 Nov 2026, live checks — full table in `../cid-verification.md`)

All 6 unique CIDs return **200 on gateway.pinata.cloud** (GET). ipfs.io and
dweb.link return **403 for every CID** (HEAD and GET) — recorded as
"gateway refused, not verified", NOT as missing files. The code's own Pinata
gateway (`olive-delicate-koi-568.mypinata.cloud`) returns 403 / timeout —
also "gateway refused, not verified".

## The two duplicated-CID flags — CHAIS'S ART CALL

**FLAG 1 — THREE players, one CID, and it is not art at all.**
CID `bafkreifaiqnt6ofmsljqaz3btub4vwgxpsp3ufmxjd2uwyhaa2n2jhqs2i` is shared
by Josh Hart (#3), Precious Achiuwa (#5) and Miles McBride (#2). It resolves
(200, 704 bytes, `application/json`) to a metadata template named
**"ScrollProof: God Mode"** — "Immortal NFT representing the God Mode status
of the ScrollVerse Origin Architect" — whose image field literally reads
`"ipfs://REPLACE_WITH_IMAGE_CID"`. It is an unfinished template for a
different NFT, not Knicks art. Those three players currently have **no
verified art**. Their metadata JSONs below point at the shared CID as-is,
flagged `_ART_CALL_PENDING`, and must NOT be minted as finished art until
Chais supplies real art or directs otherwise.

**FLAG 2 — TWO players, one image.**
CID `bafybeigbqlnsij75ixhaje4b463ii4apjdseoenp5hhd2yjm3ktvnk2ooe` is shared
by Jalen Brunson (#11) and Chais The Great (#9). It is a real PNG
(3,382,353 bytes, C2PA-signed). One image serves as both cards' art.
Chais decides whether #9 gets its own art.

**Net: 6 unique CIDs for 9 players. 5 are verified PNG art; 1 is a JSON
template, not art.**

## The 9 metadata files

| File | Player | image → CID | Content-type / size | Status |
|---|---|---|---|---|
| `1.json` | Jalen Brunson #11 | `bafybeigbql…2ooe` | image/png, 3,382,353 B | ✅ verified art — SHARED with #9 (Flag 2) |
| `2.json` | Karl-Anthony Towns #32 | `bafybeiargq…pydq` | image/png, 1,868,425 B | ✅ verified art |
| `3.json` | OG Anunoby #8 | `bafybeigub3…i77q` | image/png, 2,847,700 B | ✅ verified art |
| `4.json` | Mikal Bridges #25 | `bafybeihdvx…2fe` | image/png, 1,946,657 B | ✅ verified art |
| `5.json` | Josh Hart #3 | `bafkreifaiq…s2i` | application/json, 704 B — "God Mode" template | ⚠️ FLAG 1 — no art |
| `6.json` | Patrick Ewing Jr. #33 | `bafybeie4kd…vgq` | image/png, 2,994,956 B | ✅ verified art |
| `7.json` | Precious Achiuwa #5 | `bafkreifaiq…s2i` | application/json, 704 B — "God Mode" template | ⚠️ FLAG 1 — no art |
| `8.json` | Miles McBride #2 | `bafkreifaiq…s2i` | application/json, 704 B — "God Mode" template | ⚠️ FLAG 1 — no art |
| `9.json` | Chais The Great #9 | `bafybeigbql…2ooe` | image/png, 3,382,353 B | ✅ verified art — SHARED with #1 (Flag 2) |

Attributes per file carry the code's own fields: trait, frequency, position,
jersey number, summer role, supply cap, mint price. Nothing invented.

## How the folder gets pinned (Chais's step)

1. Chais resolves Flag 1 and Flag 2 (real art for Hart / Achiuwa / McBride;
   own art for #9 or keep shared) — or directs minting with the flags as-is.
2. The 9 JSONs (edited if art changes) are uploaded as one folder to IPFS
   (Pinata pin — the Pinata connectors returned 401 on last check, so verify
   the Pinata account first; fallback: NFT.Storage or any pinning service).
3. The folder CID becomes `baseURI` = `ipfs://<folder-CID>/` in the
   constructor args. `tokenURI(tokenId)` returns
   `baseURI + playerId + ".json"`.
4. Until the folder is pinned, the contract cannot be deployed with a real
   `baseURI` — the deploy script refuses a non-`ipfs://` base URI.

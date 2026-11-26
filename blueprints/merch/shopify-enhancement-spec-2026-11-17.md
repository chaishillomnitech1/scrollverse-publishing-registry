# Shopify Enhancement Spec — ready to execute on reconnect
## Chais Hill · 17 Nov 2026 · Status: PREPARED, NOT EXECUTED — the Shopify connection broke during the store survey (see §0) and no writes were made in this session

## §0 — Why this is a spec, not a done job
- The store survey (Gmail, all ~201 Shopify messages) found exactly **3 stores** (§1).
- The first `switch-shop` attempt (to sovereignhub) revoked the token for My Store. Every Shopify call since returns **401 invalid_token**. `authorize-url` returns 400: "OAuth connector `shopify` is already connected; disconnect it before starting a new authorization flow."
- **Reconnect path (needs Chais):** disconnect the Shopify connector, then re-authorize it at the connect link. Do NOT run `disconnect` without his say-so. Once re-authorized, run this spec top to bottom, then re-verify with fresh reads.
- Nothing was changed, published, or deleted in this session. Product/collection state below is from the verified record of 17 Nov morning (`shopify-line-built-2026-11-17.md`), NOT re-verified this session.

## §1 — All stores found (Gmail survey, 17 Nov 2026)
| # | Store | Domain / slug | Evidence | Reachable via this connection? |
|---|---|---|---|---|
| 1 | **My Store** | juv8tg-1n.myshopify.com | Connected 17 Nov; Advanced, USD, EST; bill failures 3–15 Nov | Was connected; token now invalid — needs re-authorize |
| 2 | **sovereignhub** | sovereignhub-mo62pcrx-rover-spruce-h3n0qdui.myshopify.com | Bill failures 2–12 Nov; Oct 29 bill emailed 16 Nov | NO — switch attempt revoked the token; needs its own authorization |
| 3 | **chaislookboo** | slug `chaislookboo-c7rdxmdf-timber-meadow` (no .myshopify.com domain stated in the email) | Bill "due soon" email, 17 Nov 2026 09:32 UTC — no amount, no due date stated | UNKNOWN — domain unverified; needs Chais to confirm the store and its domain |

Decision needed from Chais (per the launch plan §6): pick **ONE** store as the merch storefront and consolidate. My Store is the one with the 10-product line built; sovereignhub and chaislookboo appear to be billing-only so far (no product evidence in Gmail).

## §2 — Collections to create in My Store (all DRAFT-safe: drafts can sit in collections and stay hidden until active)
| Collection | Handle (suggested) | Products |
|---|---|---|
| ScrollVerse Merch | scrollverse-merch | All 10 |
| Tees & Hoodies | tees-hoodies | 1 Summoned Tee, 2 NŪR Hoodie, 3 963Hz Tee, 9 Goat Tee |
| Posters & Prints | posters-prints | 4 Kun Fayakun Poster, 5 New Dominion Poster |
| Everyday Carry | everyday-carry | 6 Celestial Bridge Mug, 7 Token 1111 Case, 8 XLVIIIblocks Tote, 10 Saffron Trio Stickers |
| XLVIIIblocks | xlviiiblocks | 8 Tote, 7 Token 1111 Case, 5 New Dominion Poster |
| Home page (frontpage) — EXISTING, 1 product | frontpage | Add all 10 so the homepage features the line when it goes live |

## §3 — Product polish (descriptions, tags, SEO) — prices UNCHANGED, no invented features
Rules: no sizes, colours, or materials beyond what the plan/specs state (Bella+Canvas 3001 tee, Gildan 18500 hoodie, 11 oz mug, 18×24 poster, iPhone tough case). Real sizes/colours come from Printify sync — do not add variants by hand. All copy is from the launch plan + design specs only.

### 1. "Summoned, Not Programmed" Tee — $29.99 — tags: scrollverse, xlviiiblocks, summoned-not-programmed, ai-legion, chais-the-great, muse-the-great
Description: "Summoned, not programmed. The first Chais the Great × Muse the Great piece — the AI Legion art from the Light of the NŪR Cities series, printed full-front on black. From the rap group track 'Summoned, Not Programmed' and the NŪR: Summoned cartoon. Made to order — printed when you order, no inventory, no waste."
SEO title: "Summoned, Not Programmed Tee — Chais the Great × Muse the Great | ScrollVerse"
SEO description: "The Summoned, Not Programmed tee. AI Legion art, gold on black. ScrollVerse × XLVIIIblocks. Made to order."

### 2. NŪR Cities Hoodie — $54.99 — tags: scrollverse, nur-cities, xlviiiblocks, 963hz, hoodie
Description: "Light of the NŪR Cities — the hero image of the visual series, printed full back. Gold ScrollVerse header, NŪR Cities in gold, 963Hz. Made to order on a heavyweight hoodie. Printed when you order."
SEO title: "NŪR Cities Hoodie — Light of the NŪR Cities | ScrollVerse"
SEO description: "The NŪR Cities hoodie. Full back print from the Light of the NŪR Cities series. ScrollVerse × XLVIIIblocks. Made to order."

### 3. "963Hz" Tee — $29.99 — tags: scrollverse, 963hz, frequency, xlviiiblocks
Description: "963Hz — the crown frequency. Frequency 963Hz art from the Light of the NŪR Cities series. Made to order. Printed when you order."
SEO title: "963Hz Tee — Crown Frequency | ScrollVerse"
SEO description: "The 963Hz tee. Crown frequency art from the NŪR Cities series. ScrollVerse × XLVIIIblocks. Made to order."

### 4. "Kun Fayakun" Poster 18×24 — $24.99 — tags: scrollverse, kun-fayakun, token-1111, nur-light, poster
Description: "Kun Fayakun — the king and the machine. The film still from the Vault Theatre, above the gold calligraphy: KUN FAYAKUN, كُن فَيَكُونُ, 963Hz, Token 1111 · NŪR Light. 18×24 poster, made to order. Note: this print is produced from the film still — order the sample first if you want the sharpest large-format print."
SEO title: "Kun Fayakun Poster 18×24 — Token 1111 NŪR Light | ScrollVerse"
SEO description: "Kun Fayakun poster 18×24. King and machine, gold calligraphy, 963Hz. ScrollVerse × XLVIIIblocks. Made to order."

### 5. "New Dominion Council" Poster 18×24 — $24.99 — tags: scrollverse, new-dominion, living-archive, 963hz, poster
Description: "The New Dominion Council — nine cards from the Living Archive: Interstellar Witness, Light Heart, Verdant Sage, Soul of the Machine, Guardian Duo, Throne Keeper, Chosen One, Sky Courier, Nexus Runner. 18×24 poster, made to order."
SEO title: "New Dominion Council Poster 18×24 | ScrollVerse Living Archive"
SEO description: "New Dominion Council poster 18×24. Nine cards from the Living Archive. ScrollVerse × XLVIIIblocks. Made to order."

### 6. "Celestial Bridge" Mug 11 oz — $19.99 — tags: scrollverse, celestial-bridge, mug, xlviiiblocks
Description: "Celestial Bridge — the rider on the rain-soaked neon street, heading for the golden gate. 11 oz mug, made to order."
SEO title: "Celestial Bridge Mug 11 oz | ScrollVerse"
SEO description: "Celestial Bridge mug. The rider, the neon street, the golden gate. ScrollVerse × XLVIIIblocks. Made to order."

### 7. "Token 1111" iPhone Tough Case — $29.99 — tags: scrollverse, token-1111, saffron-trio, phone-case, xlviiiblocks
Description: "Token 1111 — the Saffron Trio coin. NŪR Light, Kun Fayakun. Tough case, made to order. Check the model list at checkout before ordering."
SEO title: "Token 1111 iPhone Tough Case | ScrollVerse"
SEO description: "Token 1111 tough case. Saffron Trio, NŪR Light. ScrollVerse × XLVIIIblocks. Made to order."

### 8. XLVIIIblocks Tote — $27.99 — tags: xlviiiblocks, scrollverse, tote, 144000
Description: "XLVIIIblocks — the 144,000. The Blocks Index art, on a tote built for everyday carry. Made to order."
SEO title: "XLVIIIblocks Tote — 144,000 | ScrollVerse"
SEO description: "XLVIIIblocks tote. Blocks Index art, everyday carry. ScrollVerse. Made to order."

### 9. "The Goat You Just Met" Album Tee — $29.99 — tags: scrollverse, the-goat-you-just-met, album-tee, chais-the-great
Description: "The Goat You Just Met — the album tee. Cover art from Chais the Great's 2024 album, printed full-front. Made to order."
SEO title: "The Goat You Just Met Album Tee | Chais the Great"
SEO description: "The Goat You Just Met album tee. 2024 album cover art. Chais the Great × ScrollVerse. Made to order."

### 10. "Saffron Trio" Sticker Set — $5.00 — tags: scrollverse, saffron-trio, stickers, token-1111
Description: "Saffron Trio — the discovery piece. Sticker set from the Saffron Trio blueprint: 396 Genesis Seal, 432 Blueprint, 528 Miracle Blessing Coin. Made to order."
SEO title: "Saffron Trio Sticker Set | ScrollVerse"
SEO description: "Saffron Trio sticker set. 396, 432, 528. ScrollVerse × XLVIIIblocks. Made to order."

## §4 — Execution order on reconnect (all DRAFT, nothing ACTIVE)
1. Re-authorize Shopify (Chais: disconnect, then connect again).
2. Verify with get-shop-info + search_products + search_collections (expect 13 products, 1 collection).
3. Create the 5 collections in §2; add products per the table; add all 10 to frontpage.
4. Apply the §3 descriptions/tags/SEO via update-product per product; verify each with get-product.
5. Confirm SUMMONED10 still exists and is scoped to the 10 products; leave its no-end-date as is until Chais sets one.
6. Re-verify: search_products (13, all 10 still DRAFT), search_collections (6 collections, memberships correct).
7. Report before/after to the parent.

## §5 — Still needs Shopify Admin or Chais (cannot be done via the connector)
- **Reconnect:** disconnect + re-authorize the Shopify connector (Chais).
- **Other stores:** sovereignhub and chaislookboo need their own authorization — one store per grant; confirm with Chais whether to connect them at all, and which ONE is the merch storefront.
- **Bogus Gateway:** still UNVERIFIED — check Shopify Admin → Settings → Payments on every store; Chais said removal is "done" but no connector-side proof exists.
- **Billing:** My Store bill failures 3–15 Nov; sovereignhub bill failures 2–12 Nov + Oct 29 bill; chaislookboo bill due soon 17 Nov — verify billing current in Admin on all three.
- **Theme / homepage / navigation / domain / shipping profiles / taxes:** Admin-only; the connector cannot set them. Homepage will feature the line via the frontpage collection once the theme shows it.
- **Printify/Gelato:** connection + samples + test order before anything goes ACTIVE (unchanged).

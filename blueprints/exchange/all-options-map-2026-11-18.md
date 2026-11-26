# All Payment / Mint / Sale / Trade Options — Buyer & Seller

**Chais Hill / ScrollVerse · 18 November 2026 · RESEARCH AND PLAN ONLY**
Nothing in this document launches, mints, lists, publishes, connects a wallet, spends anything, or contacts anyone. It is preparation for decisions Chais must make first. $0 spent.

**The Howey gate, stated once plainly:** no token sale, NFT sale, mint, pre-sale, or token-as-reward before a written per-asset Howey attorney analysis for that specific asset, signed by a licensed attorney. Preparing art, metadata, descriptions, and accounts is not gated. Selling, minting, and launching are. Every option below marked NEEDS GATE is held by this rule. No return, yield, appreciation, passive-income, or floor-price language appears in any option's copy.

**The direction this map implements (Chais, 18 Nov 2026):** all payment, mint, sale, and trade options, for buyer and seller — don't shrink, use all resources and all agents. All channels open, with if/then fallback logic: if one rail fails, another carries it. All Stripe traffic redirects to his own financial chain, so payments clear and are accepted unimpeded and every transaction is recorded in his own ledger.

**Honest baseline (18 Nov 2026):** real customers 0, real orders 0, real sales $0, contacts on any list 0. Shopify has 2 customer records and both are Chais himself. The Pump.fun wallet holds $0.00 and no coins have been created. No token or NFT contract is deployed on-chain anywhere — every contract below is code in a repo. Demo figures stay labeled demo wherever they appear in the source packs.

---

## 0. How to read this map

| Status | What it means |
|---|---|
| **LIVE** | Working today; a buyer could use it right now. |
| **READY** | Built and verified, not yet switched on or published. |
| **CODE-READY** | The code exists; nothing is deployed or live. |
| **NEEDS KEY** | Built, but a key/account the owner holds is missing. |
| **NEEDS GATE** | Held by the Howey gate (written per-asset attorney analysis) or another named gate. |
| **NEEDS ACCOUNT** | No account exists yet; creation is the owner's step. |
| **BLOCKED** | A named blocker stands in the way (not a shrug — the blocker is named). |
| **DEMO** | Simulated only; no real money or asset moves through it. |

Every option lists the **buyer flow** (what the buyer does and pays with) and the **seller flow** (what Chais receives, where, and what it costs him), plus exactly what is missing for real money or a real asset to move.

---

## 1. Payment rails — how a buyer pays, how Chais receives

| # | Rail | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 1.1 | **Cash App — $chaisthegreat28** | Buyer opens Cash App, pays $X to $chaisthegreat28, sends proof. | Chais receives direct in Cash App. Open and funded — his one unfrozen money route right now. No platform fee on the payment itself. | **READY** (as a rail) / **BLOCKED** (as a store checkout method) | The Shopify manual payment method "Pay with Cash App ($chaisthegreat28)" was never created — the browser task died 18 Nov ~13:03 EST. Needs the Shopify login to restart and create it. Same rail is being wired into the Replit pay function (in progress). |
| 1.2 | **PayPal** | Buyer pays with PayPal (card or balance) at checkout or via a payment link. | Chais receives in PayPal; Bandcamp pays out to PayPal in 24–48 hours. | **READY** (Chais has PayPal) / **NEEDS WIRING** | Not yet wired into any checkout: not on the Shopify store, not in the Replit pay function yet (being added alongside Cash App), not confirmed as the Bandcamp payout account (blocker B6). Needs his PayPal account confirmed/linked on each surface. |
| 1.3 | **Card — via Bandcamp checkout** | Buyer pays by card at Bandcamp checkout. Processing 2.2% + 30¢ (on $8.07+ sales). | Chais receives via Bandcamp payout to PayPal/bank in 24–48h, minus Bandcamp's 15% digital / 10% merch share — **waived entirely on Bandcamp Friday 4 Dec 2026**. | **NEEDS ACCOUNT** | No Bandcamp artist page exists yet (blocker B6). Page creation + PayPal link is Chais's step. Listings also blocked on audio/masters (B1–B5). |
| 1.4 | **Card — via Shopify Payments** | Buyer pays by card at the Shopify checkout. | Chais receives via Shopify Payments payout. | **BLOCKED — OFF by decision** | Shopify Payments stays OFF while the Stripe dispute stands. Never route new customer money through Stripe while the VibeCanvas hold is open. Do not open a second Stripe account to route around it. |
| 1.5 | **Stripe (direct)** | Buyer pays by card through a Stripe PaymentIntent (OmniLoop `/mint`, $10 default). | Stripe holds/pays out per its account rules. | **BLOCKED — disputed + key absent** | Two blocks: (a) the VibeCanvas dispute — Stripe is holding almost $200,000 of his money (his stated figure), payouts paused, key ending JXAnel deactivated, legal action sent 18 Nov, awaiting Mark's answers to 7 questions; (b) OmniLoop holds **no Stripe key at all** (Secrets hold only SESSION_SECRET) — `/mint` cannot take a real payment until he adds one. **All Stripe traffic is being redirected to his own rails instead (see §9).** |
| 1.6 | **Crypto — USDC via Coinbase Business** | Buyer pays USDC through a Coinbase Business payment link; manual "Pay with Crypto (USDC)" method on Shopify. | Chais receives USDC in Coinbase Business. Fee 1% per completed payment (read the in-account rate before building around it). Works with Shopify Payments OFF. | **BLOCKED** | Coinbase Business application is paused, one document away: a Source of funds statement in the business legal name "Scroll Verse LLC". Cash App statement was rejected on name. Future triggers: Mercury business account activation, or an Ocean First statement in the LLC's name. |
| 1.7 | **Crypto — SOL / BTC via Coinbase app** | Buyer sends SOL/BTC to a wallet address Chais publishes (Pump.fun wallet `FpxkpRuL6RT5a4P48Wy4FVsRSLdAFsMABMjYKsWvZr64`). | Chais receives in the wallet. No platform fee beyond network fees. | **READY** (as a receive route) | The wallet holds $0.00 and nothing is listed for sale against it yet. Funding route for the wallet itself: Cash App → buy BTC → Coinbase app → swap to SOL → send to wallet; or MetaMask ETH → swap to SOL → send. |
| 1.8 | **Crypto — ETH via MetaMask** | Buyer sends ETH to an address Chais publishes. | Chais receives in MetaMask (confirmed ETH). Swap ETH → SOL inside MetaMask for the Pump.fun wallet. | **READY** | No published receiving address on any live storefront yet; no sale is priced in ETH yet. |
| 1.9 | **Cash App → Coinbase → SOL bridge (buyer-side, "Pay in anything")** | A buyer with only Cash App pays Cash App → BTC → Coinbase → SOL → Chais's wallet. The Direct Exchange "Pay in anything" matrix documents this bridge step by step. | Chais receives SOL in the wallet. | **READY** (as a documented route) | Nothing to build — it is a route buyers follow. It only matters once something is priced in SOL. |
| 1.10 | **Ko-fi / Payhip / Gumroad checkout** | Buyer pays by card/PayPal on the fan-shop page. Ko-fi tips 0% on legacy Free accounts (new Standard accounts 5%); Payhip 5% free plan; Gumroad 10% + $0.50, $100 minimum payout. | Ko-fi pays out instantly and direct to his Stripe or PayPal — Ko-fi never holds the money. | **NEEDS ACCOUNT** | No Ko-fi, Payhip, or Gumroad account exists. Ko-fi is the lead (instant payout, 0% tips on legacy setting). |
| 1.11 | **Marketplace checkout (Redbubble / TeePublic / Spreadshop / Merch on Demand)** | Buyer pays by card on the marketplace; the marketplace prints and ships. | Chais receives the royalty/markup monthly: Redbubble ~$2–$3.60/tee (Standard, after 50% account fee), TeePublic ~$2/tee (mostly sale rate), Spreadshop ~$16–20/tee IF the old mark-up model applies (affiliate model ~$2.80 — confirm at signup), Merch on Demand Creator ~$2.44/tee. | **NEEDS ACCOUNT** | No accounts exist on any of the three. Needs Chais to create them + payout method + tax form. Spreadshop commission model must be confirmed before pricing. |

**The redirect rule (Chais, 18 Nov 2026):** every place a buyer would hit Stripe routes to his own chain instead — Cash App, PayPal, Coinbase/USDC, SOL — and every payment is recorded in his own transaction ledger, so he holds the full history and nothing is stopped on Stripe's side. The Replit pay-function task carries this for the apps; the Shopify manual methods carry it for the store.

---

## 2. Sell options — the storefronts (physical + digital goods)

| # | Option | What sells | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|---|
| 2.1 | **Shopify store — XLVIIIblocks (juv8tg-1n.myshopify.com)** | 96 ACTIVE products (tees $29.99, posters $24.99, hoodie $54.99, mug $19.99, case $29.99, tote $27.99 + more); Printify-connected fulfilment. | Buyer browses, adds to cart, checks out. | Printify prints + ships per order (~$16/tee print cost). Chais receives the sale minus print + shipping. | **BLOCKED — no working checkout** | Checkout unverified; Cash App manual method not created (needs Shopify login to restart the task); PayPal rail not wired; Bogus Gateway status unverified; Shopify Payments OFF by decision. 0 orders, $0 sales, 34 sessions in 90 days. |
| 2.2 | **Shopify bundles T1–T4** | T1 Reader $24.99 (Manifesto + God Mode poster) · T2 Set $49.99 (+ tee) · T3 Goat Bundle + Book $59.99 · T4 Collector $99.99 (3 books + Goat Bundle + tee + poster). Stage-1 ScrollCredits only (25/50/75/150). | Buyer buys the bundle, gets physical items + direct digital downloads. | Same Printify fulfilment + direct EPUB/file delivery via Shopify Digital Downloads app. | **BLOCKED** | All tiers blocked by checkout (G1) + ebook delivery setup (G2) + licence line (G3). T2–T4 add numbered-run mechanism (G4). T3–T4 add Goat masters + tracklist (G5) and Vydia direct-sale confirmation (G6). T4 adds Journey (G7) + Mirror (G8) readiness. All prices PROPOSED except the Manifesto $2.99 (approved). |
| 2.3 | **Shopify add-ons A1–A5** | Sticker $3.99 · Wallpaper pack $1.99 · Bookmark card $2.99 · Mini print 8×10 $9.99 · Bonus digital track $1.99 (each earns 5 ScrollCredits). | Buyer adds at product page or checkout. | Digital add-ons cost nothing to fulfil; physical ride the same Printify order. | **BLOCKED** | Same G1/G2 as the bundles; physical add-ons need their Printify products created; A5 (bonus track) is G6-gated — do not list until Vydia direct-sale confirmation clears. All prices PROPOSED. |
| 2.4 | **Shopify — standalone pieces** | Every bundle component sold separately: Manifesto ebook $2.99 (approved) · Journey $2.99 (proposed) · Mirror $9.99 (proposed) · tee $29.99 · poster $24.99 · Goat Bundle $39.99 · Save Me $10. | Same as 2.1. | Same as 2.1. | **BLOCKED** | Same checkout block as 2.1; plus per-piece gaps (Journey/Mirror not ready; Save Me audio not sellable on disk; Goat masters missing). |
| 2.5 | **Bandcamp — Save Me single** | "Save Me" digital single, $10. Buyer owns a copy + personal listening licence, not copyright/publishing/royalties. | Buyer pays by card or PayPal; downloads instantly. | Chais keeps $9.48 (card) / $9.51 (PayPal) per copy on Bandcamp Friday (share waived); $7.98 on a normal day. Payout to PayPal in 24–48h. | **NEEDS ACCOUNT + NEEDS FILES** | No Bandcamp page (B6) · sellable audio not on disk — only a 25 kbps reference (B1; the 10.28 MB MP3 is in Gmail, the WAV is in the DistroKid Vault) · cover art not in hand (B2) · Vydia direct-sale confirmation (B5) · no native edition cap for a digital single (B7 — do not claim "250 copies" on it). |
| 2.6 | **Bandcamp — Goat Bundle** | Goat album tee + album download, $39.99, 250 copies (edition cap shared with the Shopify listing — never 250 on each). | Buyer pays by card or PayPal; download instantly, tee ships. | Chais keeps ≈ $9,702.56 before tee cost at Friday sellout (250 × $39.99 = $9,997.50 gross, processing only); ≈ $5,702.56 after ~$4,000 tee print. | **NEEDS ACCOUNT + NEEDS FILES** | No Bandcamp page (B6) · Goat masters missing — only "HOW I REALLY FEEL" (2:52) in hand, Drive zip deleted (B3) · tracklist unverified — only one track confirmed (B4) · Vydia confirmation (B5) · tee fulfilment is manual on Bandcamp — one manual Printify order per sale (B8). Fallback if not ready by 3 Dec: launch Save Me only. |
| 2.7 | **Redbubble** | All 7 art pieces across 70+ products (tees, posters, stickers, cases, mugs, totes…). | Buyer pays on Redbubble; Redbubble prints + ships. | Chais receives ~$2–$3.60/tee net at 25–30% markup (Standard tier, 50% account fee); monthly payout ~15th, $20 (or $10) threshold, PayPal/bank. Sitewide sales cut into his markup. | **NEEDS ACCOUNT** | No account. Create + payout method. God Mode leads (own IP); Knicks pieces list under the merch decision, with the flag that the marketplace can remove them — if removed, do not re-upload there, keep on Shopify only. Upload only from `merch/pinata/clean/` or the 4× upscales or composed designs — never the raw watermarked files. |
| 2.8 | **TeePublic** | Same 7 pieces across 40+ products. | Buyer pays on TeePublic; TeePublic prints + ships. | Flat royalty: Artisan $4/tee full / $2 on sale; Apprentice $3/$1. Realistic ~$2/tee (mostly sale rate). Monthly payout 15th, PayPal/Payoneer. | **NEEDS ACCOUNT** | No account. New accounts start Apprentice (lower royalty; one source says Apprentice designs are hidden from search — confirm at signup). |
| 2.9 | **Spreadshop (EU, Germany)** | Same 7 pieces; the European storefront + production. | Buyer pays in EUR; EU production + fulfilment. | Old mark-up model: ~$16–20/tee at $29.99. New affiliate model (announced Mar 2026, from May 2026): 20% of product+print price ≈ $2.80/tee + volume bonus. Monthly payout, $10–25 threshold. | **NEEDS ACCOUNT** | No account. **Confirm which commission model a new shop is created under before pricing** — it decides the whole margin. Tax form W-9/W-8BEN needed for payout. |
| 2.10 | **Amazon Merch on Demand** | Same art on tees/apparel inside Amazon search (US, UK, Germany, France, Italy, Spain, Japan). | Buyer pays on Amazon. | Creator tier ~$2.44 on a $19.99 tee; Plus ~$4.88; Premium ~$5.27 (tiers by how much traffic he drives himself). Monthly payout, ~60 days after sale month. | **NEEDS ACCOUNT — invite-only** | Apply now (business details, EIN, bank account) — approval ~30–40%, takes time. New accounts start Tier 10 (10 live designs). |
| 2.11 | **Displate (metal posters)** | The 7 pieces as metal posters. | Buyer pays on Displate. | Fixed commission $4.50 (M) / $9.00 (L) / $14.50 (XL) per poster. | **NEEDS ACCOUNT** | Portfolio review required before selling. Submit the 7 pieces as a portfolio. |
| 2.12 | **Fine Art America** | God Mode + Atlas HQ art as framed/canvas prints. | Buyer pays on Fine Art America. | He sets markup above base price and keeps it. Free account (do not pay the $30/yr Premium). | **NEEDS ACCOUNT** | No account. Lower built-in traffic — he drives the buyers. |
| 2.13 | **Ko-fi shop** | The 4 books + Save Me single + art downloads as digital files; tips + memberships. | Buyer pays by card/PayPal; instant download. | Tips 0% on legacy Free accounts (new Standard 5%); shop/memberships 5% on free plan. **Payout is instant and direct to his Stripe or PayPal — Ko-fi never holds the money.** | **NEEDS ACCOUNT** | No account. Confirm which fee setting a new account gets (0% tips survives only on older Free-setting accounts). Link from Atlas and the coin pages. |
| 2.14 | **Payhip** | Same digital files as a second storefront. | Buyer pays by card/PayPal. | 5% per sale on the free plan + ~2.9% + 30¢ processing. Payout to PayPal/Stripe. | **NEEDS ACCOUNT** | No account. Backup to Ko-fi, same files, second storefront. |
| 2.15 | **Patreon** | Recurring membership — Legion access, early music/films, behind-the-scenes. One tier to start (e.g. $10/month "ScrollVerse Insider"). | Member subscribes monthly. | 10% platform fee for pages published after 4 Aug 2025 + 2.9% + 30¢ processing. Apple takes 30% (dropping to ~15% after a year) on memberships started inside the iOS app. | **NEEDS ACCOUNT** | No account. Do not build five tiers before the first member. |
| 2.16 | **Gumroad** | Digital products (books, music, art, templates). | Buyer pays on Gumroad. | 10% + $0.50 per direct sale + processing (~14% real cost); Discover sales cost 30%. **$100 minimum payout** — small earnings sit for months. Merchant-of-record (handles VAT/sales tax worldwide). | **NEEDS ACCOUNT** | No account. Backup only, after Ko-fi/Payhip are live — not the lead. |
| 2.17 | **Substack** | Written work — Manifesto, Journey, essays, Legion notes as a paid newsletter. | Reader subscribes. | 10% of subscription revenue + Stripe processing. | **NEEDS ACCOUNT** | No account. Free newsletter first (build the list), paid subs once the list is warm. |

---

## 3. Music sale / streaming options

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 3.1 | **Bandcamp (music)** | See 2.5–2.6. Direct download sales, highest margin per sale. | See 2.5–2.6. | **NEEDS ACCOUNT + NEEDS FILES** | B1–B8 (Bandcamp pack). |
| 3.2 | **RouteNote Free (streaming, 200+ stores)** | Listener streams/downloads on Spotify, Apple Music, YouTube Music, Deezer, TIDAL, TikTok, Facebook, Instagram, Tencent QQ + other Chinese/Korean services, Boomplay, Audiomack, JioSaavn, Anghami, NetEase, KKBOX, Mdundo. | RouteNote keeps 15%, Chais keeps 85% of streaming/download revenue. $50 minimum payout. Non-exclusive. | **BLOCKED — 0 songs upload-ready** | **Every ISRC is missing** — they live in DistroKid; a re-delivery without its original ISRC is a brand-new recording with zero play count. Needs the DistroKid export (the critical path). Timeline once uploaded: moderation 21–27 working days + 7–14 days store ingestion ≈ 5–6 weeks — **not a Dec 4 route; Bandcamp is.** Tier A (WAV master, 8 singles) / Tier B (MP3 only, 8) / Tier C (feature, 1) / Tier D (new-release candidate, 1) — see RouteNote pack. **RouteNote vs Vydia is one destination, never both.** |
| 3.3 | **Audiomack (direct upload + AMP)** | Listener streams free; AMP pays 50% of the platform's ad + subscription revenue pool. Big discovery in Nigeria, Ghana, Kenya. | AMP payout (confirm threshold inside the program). | **NEEDS ACCOUNT** | No account / no AMP application yet. Upload "Save Me" + Goat singles and apply for AMP the same day. |
| 3.4 | **Shopify — Goat album download (via bundles)** | See 2.2–2.3 (T3/T4). | Direct file delivery via Shopify Digital Downloads app. | **BLOCKED** | G5 (masters + tracklist) + G6 (Vydia confirmation) + G1/G2. |
| 3.5 | **DistroKid (current distributor — leaving)** | Existing catalog streams on the current stores. | Current payout route; $103.88 owed on the account. | **LIVE (existing) / DEPRIORITIZED** | Transfer deprioritized by Chais ("bigger fish to fry"). When resumed: settle $103.88 (locked Cash App Card, Visa ending 9039, blocks it), export full catalog + ISRCs from the DistroKid app, confirm Vydia split/publishing in writing. |
| 3.6 | **Vydia (intended distributor)** | Streaming on the stores Vydia covers. | 80/20 non-exclusive per Chais's own 2024 email to SESAC — **vs 90/10 owner statement (Aug 2026, repos) vs 15% hardcoded in WealthDashboard.** Publishing: SESAC (2024 email) vs ASCAP self-owned IPI 1247873912 (repos). | **BLOCKED — unconfirmed** | Neither split nor publisher may appear in any pitch/copy until confirmed from the agreement/dashboard. Confirm: plan current, actual split, permanence clause, SESAC vs ASCAP, accepts existing ISRCs + original dates. |

---

## 4. Book sale options

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 4.1 | **Amazon KDP — Manifesto ebook** | Buyer buys on Amazon Kindle. | 70% royalty at $2.99–$12.99 (minus ~$0.15/MB delivery fee). $2.99 approved → ~$1.94/copy. Payout ~60 days after sale month, direct deposit. | **READY (file) / NEEDS ACCOUNT** | EPUB built + validated (766 KB), portrait cover built (1600×2560). **No KDP account created** — Chais creates/signs in with his Amazon login + tax info + royalty bank details (his hands only). Licence line still open (CC BY-NC-SA vs MIT signals vs the book's own protected line) — Chais confirms before the listing goes up. Do NOT enroll in KDP Select (90-day exclusivity). |
| 4.2 | **Amazon KDP — Journey / Mirror / Creator Desk** | Same as 4.1. | Same as 4.1 (70% ebook; paperback 60% at $9.99+ / 50% under, minus printing ~$1.00 + $0.012/page). | **BLOCKED — not ready** | Journey: 1,180 words, no cover, no EPUB — sellable only as a $2.99 short read, or expanded, or bundled (Chais's call). Mirror: 10,413 words, no cover, no EPUB, editorial pass required (contract code + $MIRROR token economics inside — cut or frame as archival, zero token-sale language either way); approval conflict with the FREE FOREVER rule for the jewel (repo README governs until he says otherwise). Creator Desk: 0 words of book text — not a book yet; scope decision first. |
| 4.3 | **Draft2Digital (+ Smashwords)** | Buyer buys on Apple Books, Kobo, Barnes & Noble, libraries (OverDrive), Smashwords store. | D2D takes 10% of list; retailer ~30%; he keeps ~60% at most retailers. Smashwords store pays 75% of list on books $2.99+ (40% under). | **NEEDS ACCOUNT** | $20 one-time activation (Apr 2026) + $12/yr maintenance for accounts earning under $100/yr — near-free, flagged. No account. After KDP. Does not distribute to Amazon. |
| 4.4 | **Kobo Writing Life / Apple Books / Google Play Books (direct)** | Buyer buys on Kobo / Apple / Google Play. | 70% royalty on books $2.99+. Free to publish. | **NEEDS ACCOUNT** | No accounts. Apple needs a Mac or iTunes Producer flow — use D2D if that is friction. |
| 4.5 | **Shopify — direct EPUB delivery** | Buyer buys the ebook on the store; downloads the EPUB at checkout (Shopify Digital Downloads app). | He keeps the full price minus print/shipping (none — digital) and minus the checkout rail's cost. | **BLOCKED** | G2: no Digital Downloads app installed; EPUB not attached to any product. G1: no working checkout. |
| 4.6 | **Ko-fi / Payhip shop (books)** | See 2.13–2.14. | See 2.13–2.14. | **NEEDS ACCOUNT** | No accounts. |

---

## 5. Film / video sale options

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 5.1 | **FilmHub** | Viewer watches on Tubi, Pluto TV, Roku Channel, Peacock, Samsung TV Plus, and 150+ platforms (AVOD/FAST). | FilmHub keeps 20%, Chais keeps 80% of ad revenue. AVOD pays roughly $0.002–$0.008/view. $0 upfront, $0 submission; he keeps his rights. | **NEEDS ACCOUNT** | No submissions yet. Submit the 6 latest films first, then the 9 batch-1 films. Free tier = standard QC review (can be slow), no marketing support. Do not buy the paid tiers ($299/3 months). |
| 5.2 | **YouTube Partner Program — @chaishill-u1z** | Viewer watches ads on long-form / Shorts; memberships, Super Chat/Thanks, Shopping. | 55% of net long-form ad revenue; 45% of his Shorts Creator Pool share; 70% of memberships and Supers. | **NEEDS ACCOUNT WORK** | Channel exists and is verified live, but owning Google account still unknown; **no films uploaded yet**; YPP thresholds: 1,000 subs + 4,000 public watch hours in 12 months OR 10M Shorts views in 90 days. **From 1 Feb 2027 the bar doubles (8,000 hours / 20M Shorts views)** — qualify before then. Old channel @chaishill2049 is terminated; nothing ever posts there. |
| 5.3 | **Amazon Prime Video Direct** | Viewer rents/buys or streams on Prime. | Rent/buy: ~50% of retail. Prime royalties: ~$0.06–$0.15 per hour streamed. Payout ~90 days after sale month. | **NEEDS ACCOUNT** | No submissions. Prime Video Direct no longer accepts unsolicited shorts/non-fiction — shorts need an aggregator (FilmHub covers this). Submit the longest/strongest films after FilmHub, rent/buy pricing first. Needs mezzanine file, captions, key art, metadata. |
| 5.4 | **Dailymotion (France)** | Viewer watches; partner ad revenue share. | Ad revenue share (confirm rate at signup). $0 to upload and join the partner program. | **NEEDS ACCOUNT** | No account. Mirror the 6 latest films here once they are on YouTube — second free home, not a primary. |
| 5.5 | **Vimeo On Demand** | — | — | **DEAD** | Shutting down 20 Nov 2026; storefronts stopped taking orders 21 Sep 2026. Do not build here. |

---

## 6. Mint options — turning art into an NFT

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 6.1 | **OpenSea Studio — ScrollVerseNFT (ERC-721, max 999)** | Buyer buys the NFT on OpenSea (Ethereum / Base / Polygon); pays in ETH. | No OpenSea fee to create a collection. **1% on a sale; 10% on primary-drop mints.** Gas: deploy ~$1–$5 on Base/Polygon, ~$16–$112 on Ethereum; mint cents on L2, $5–$50+ on Ethereum. On-chain royalties via EIP-2981 — his contract already implements 10% (note: royalty enforcement varies by marketplace). | **CODE-READY / NEEDS GATE** | Contract is code only — fresh deploy + fresh audit decision first. Collection prep can start now: 7 art images, metadata JSONs (fix `scrollproof.json`'s image field to the God Mode CID first), descriptions, logo/banner, price + supply plan (how many of the 7 mint first, at what price, on which chain). **Do not deploy or mint until the written per-asset Howey analysis for the collection is in hand.** The only researched platform that fits his existing ERC-721 contract. |
| 6.2 | **Manifold Studio (EVM)** | Buyer claims/mints on Manifold; pays in ETH. | Free for creators; the collector pays 0.0005 ETH per claim / 0.0008 ETH on allowlisted mints. Deploys a Creator Core contract he owns (Ethereum, Optimism, Base, Shape). | **CODE-READY / NEEDS GATE** | Card checkout was removed Nov 2025 — crypto-only checkout. Same Howey gate as 6.1. The only live NFT route found in the Tory plan; a credible EVM alternative to OpenSea Studio if OpenSea's 10% primary-drop fee is a problem. |
| 6.3 | **Zora — creator coins (Base / Solana)** | Buyer trades the coin on Zora. | Creating a coin costs no Zora fee, only network gas (often sponsored). Creators earn 1% trading fee (0.5% on creator coins, 0.7% on custom pairs). NFT minting deprecated in the app Oct 2026 — Zora is now a coin platform. | **NEEDS GATE** | A Zora creator coin, once enabled, cannot be disabled. Mirror the God Mode emblem as a Zora creator coin on Base (cheap gas) after Pump.fun Wave 1 — same art, different chain, different audience. Same Howey gate. |
| 6.4 | **Magic Eden Launchpad (Solana)** | Buyer mints on Magic Eden Launchpad. | Mint tooling, allowlists, staged mints, homepage placement for approved collections. 2% taker fee on sales; royalties buyer-optional unless enforced in metadata. Solana gas is a fraction of a cent. | **NEEDS GATE + NEEDS RE-MINT DECISION** | Application-only, ~3% of applications accepted. **Requires Solana Metaplex re-mints of the art** — a second edition of the same piece on a second chain, a deliberate decision, not an accident. His EVM NFTs cannot list here as written (Solana-only since Mar 2026). |
| 6.5 | **Rarible** | Buyer buys on Rarible; lazy minting on Ethereum (shared collection): he signs for free, the token mints when someone buys, the buyer pays the gas. | No fee to create a collection. Royalties enforced on its Solana relaunch. | **NEEDS GATE** | Rarible changed ownership May 2026 (Impossible acquired the brand/assets) — verify current terms before listing. Cross-list the God Mode emblem here after OpenSea. Same Howey gate. |
| 6.6 | **OmniLoop `/mint` (Replit)** | Buyer mints through the OmniLoop storefront; Stripe PaymentIntent, $10 default. | Server creates the PaymentIntent; the mint runs on payment. | **LIVE (app) / NEEDS KEY / NEEDS GATE** | App is live and verified; **Stripe key is ABSENT** — no real payment can be taken until he adds STRIPE_SECRET_KEY in Replit Secrets. The pay-function work (in progress) adds PayPal + Cash App rails with if/then fallback and redirects all Stripe traffic to his own chain. Minting/selling an NFT here is also held by the Howey gate. |
| 6.7 | **DecentralizedMelody mint (Replit, ×2 copies)** | Buyer mints through the front-end payment modal. | NFT minting in the backend code (Express/Prisma/SQLite). | **DEMO** | The payment modal is **simulated only** — no real payment moves. Front ends run in preview on demo fallback data (3 tracks, 2 listings); production DB schema never initialized; publish NOT live (Autoscale limit). The pay-function work (in progress) wires real rails in test/demo mode. Same Howey gate. |
| 6.8 | **Chaisomnitechworld mint (Replit)** | Buyer mints through the backend (AudioVault / ScrollAI / OmniDash / ScrollCast / Stripe checkout / NFT minting / DAO). | Express/Prisma/SQLite backend. | **CODE-READY / NEEDS GATE** | Runs in preview (the Run workflow just needed starting); publish NOT live (Autoscale limit). README demo stats ($12,450 revenue / 1,247 listeners) are **demo data, not real**. Same Howey gate. |
| 6.9 | **NFT_Minting_Starter_Pack (Pinata ZIP)** | — | Express server, `POST /mint` uploads an image to IPFS via Infura and returns the CID. | **CODE ONLY — NOT A MINT** | Despite the name it does **not** mint an on-chain token. Needs Infura credentials (not included). Do not list as a product. |
| 6.10 | **ScrollVerseNFTApp / SolarShardNFT (Pinata ZIP)** | — | Starter skeleton; SolarShardNFT is an empty contract shell. | **STUB — NOT A MINT** | Not a working app. Do not list as a product. |

---

## 7. Token launch options — creating a coin

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 7.1 | **Pump.fun — Wave 1 (7 coins, SVRS lead)** | Buyer buys on the bonding curve (price by formula, not order book); sells back on the curve or after graduation on PumpSwap. | Creator fees ON: 1.25% per curve trade (0.95% Pump.fun, 0.30% creator) + ~0.45% app fee (0.40% with referral). After graduation (~85 SOL net buys, ~411 SOL market cap), tiered 1.25% → 0.30% on PumpSwap, creator share stepping down. Graduation costs 0.015 SOL. | **READY (packages) / NEEDS GATE + NEEDS FUNDING** | Profile LIVE (@DuneSimpleSock, God Mode emblem, bio set). All 7 coin packages ready (art files, descriptions, website = Atlas URL). **Wallet $0.00 — needs SOL first** (~0.25 SOL covers all 7 + buffer; ~0.02 SOL per coin). **Gate 1: written per-asset Howey analysis for SVRS first, then each coin in order.** Gate 3: founder sign-off per coin. External wallet sign-in retires **30 Nov 2026** — after that email/Google/Apple/GitHub only; GitHub login works, keep it. Reality check: ~1.4% of launched tokens ever graduate; ~60% dead within 24 hours. A launch with no audience behind it almost always goes nowhere. |
| 7.2 | **Pump.fun — Waves 2–5 (Legion 11, Films 6, Music 4, Books 4)** | Same as 7.1. | Same as 7.1. | **PROPOSED / NEEDS GATE + NEEDS FUNDING + NEEDS ART CHECK** | Tickers are proposals — verify availability on Pump.fun at launch; coin data cannot be changed after creation. Art: Legion visuals to verify/create at launch; film posters in `~/workspace/video-catalogue/posters/` to confirm; music/book art on file. Same three gates per coin. Never in any wave: Code of Tawḥīd, Londyn lullaby, Nipsey name/face, prophets/living figures as new coins. Manus excluded (platform name). |
| 7.3 | **Raydium LaunchLab (Solana)** | Buyer buys on the bonding curve; graduates to a Raydium CPMM pool (90% of LP burned, 10% locked). | ~1.05% per curve trade (0.25% protocol, 0.75% platform, 0.05% creator — splits vary by platform, capped: platform ≤1%, creator ≤0.5% after Aug 2026). After graduation ~0.25% + creator fee. Migration 0.15 SOL pool-creation fee. | **NEEDS GATE + NEEDS FUNDING** | No account/launch prepared. The Pump.fun alternative: configurable supply (10M–1T), raise ≥24 SOL, 51–80% on curve, optional vesting up to 30%; JustSendIt mode (one click, 1B supply, 85 SOL graduation) or LaunchLab mode. Cost ~0.05–0.5 SOL. Less discovery/traffic than Pump.fun's feed; deeper DEX on graduation. Same Howey gate. |
| 7.4 | **Zora — creator coins** | See 6.3. | See 6.3. | **NEEDS GATE** | See 6.3. After Pump.fun Wave 1. |
| 7.5 | **EVM deploy — CHXToken / ScrollVerseNFT / others (on-chain)** | Buyer buys on a DEX (Uniswap on Ethereum/Base) or an NFT marketplace after deploy. | Creator controls the contract (owner-only mint, pausable vaults, royalties). | **CODE-READY / NEEDS GATE + NEEDS DEPLOY** | **Nothing is deployed.** Deploying is a fresh on-chain deploy + fresh audit decision, not a listing. CHXToken mints 21.6B at deploy; ScrollVerseNFT caps at 999. The contract's own language ("passive divine income" 0.005%/day, DivineEssenceCoin 8%/12%/18% APY in comments) is exactly what makes a token look like an investment contract under Howey — no launch copy may describe it until counsel reviews the specific asset. LayerZeroBridge is un-deployed code, not a working bridge — bridging EVM CHX to Solana is a build project, not a listing step. **Do not launch a Solana token also called "CHX"** — two different tokens sharing a ticker is a confusion and scam vector; the naming decision comes first. |
| 7.6 | **Jupiter — verified listing (post-launch)** | Buyer swaps on Jupiter (aggregator across Solana DEXes); the verified checkmark makes the token findable and trusted (Phantom badge + Explorer read Jupiter's list). | No fee to submit. Auto-indexed 15 min–2 h after a DEX pool exists (with a warning banner, no logo). | **NEEDS A LIVE TOKEN FIRST** | Strict list needs: mint + freeze authority both revoked; complete Metaplex metadata with logo on IPFS/Arweave; meaningful locked liquidity ($5,000–$10,000+); **500–1,000+ unique non-associated holder wallets** with real organic volume; active official socials + working website; manual review 1–4 weeks. A week-3/4 step, not launch day. |

---

## 8. Trade options — exchanging, swapping, and trading direct

| # | Option | Buyer flow | Seller flow | Status | What's missing |
|---|---|---|---|---|---|
| 8.1 | **Direct Exchange — Direct Trade (peer-to-peer)** | Buyer and seller agree terms on the trade-slip builder; the trade happens direct, creator-to-customer, no middleman exchange. | Chais (or the other party) receives the agreed asset/payment direct. | **LIVE (site) / READY (mechanism)** | The site is live with the trade-slip builder. A trade is a private agreement — terms, delivery, and payment are the parties' own responsibility. No escrow, no dispute handling built in. |
| 8.2 | **Direct Exchange — Route Finder** | Buyer picks asset family × payment (card/fiat, crypto, or trade) and gets the exact rail, steps, and door. | Chais receives through whichever rail the finder points to. | **LIVE** | The finder is live. It points at rails that are themselves blocked or unbuilt (see §1–§2) — the finder works, the doors behind some of its answers do not yet. |
| 8.3 | **Direct Exchange — "Pay in anything" matrix** | Buyer pays in anything (fiat, card, Cash App, crypto, trade) and the matrix bridges it to what Chais accepts — including Cash App → Coinbase → SOL. | Chais receives in the rail the matrix lands on. | **LIVE** | Live as a guide. The underlying rails still need their own setup (see §1). |
| 8.4 | **Pump.fun / PumpSwap trading (post-launch)** | Holder buys/sells on the curve, then on PumpSwap after graduation. | Creator fees accrue in SOL in the Pump.fun wallet; claimable from the profile. | **NEEDS A LIVE TOKEN FIRST** | See 7.1. No token exists to trade yet. |
| 8.5 | **Raydium / Jupiter swaps (post-launch)** | Holder swaps on Raydium CPMM or via Jupiter aggregation. | Creator fee on the pool (Raydium) / nothing directly (Jupiter is an aggregator). | **NEEDS A LIVE TOKEN FIRST** | See 7.3 / 7.6. |
| 8.6 | **OpenSea secondary sales (NFTs, post-mint)** | Buyer buys a minted NFT on the secondary market. | Chais receives the sale price minus 1% OpenSea fee + the on-chain royalty (10% EIP-2981 in his contract — note: royalty enforcement varies by marketplace; some honour lower or zero). | **NEEDS A MINT FIRST** | See 6.1. No NFT is minted yet. |
| 8.7 | **Magic Eden secondary (Solana NFTs, post re-mint)** | Buyer buys on Magic Eden. | 2% taker fee; royalties buyer-optional unless enforced in metadata. | **NEEDS A RE-MINT DECISION + A MINT** | See 6.4. |
| 8.8 | **Crypto swaps — MetaMask (ETH → SOL) / Coinbase app (BTC → SOL)** | Buyer or Chais swaps inside the wallet app. | The swapped asset lands in the destination wallet. | **LIVE** | Works today. It is a conversion, not a sale — it only matters once there is something to buy or fund. |
| 8.9 | **Cash App BTC → Coinbase → SOL (funding bridge)** | Chais (or a buyer) buys BTC in Cash App, sends to Coinbase app, swaps to SOL, sends to the Pump.fun wallet. | SOL lands in the wallet, ready to fund a coin creation. | **LIVE (route) / NEEDS EXECUTION** | Cash App is on his phone; Muse cannot operate it directly. Also: try Pump.fun app Deposit with the Cash App Card first. |
| 8.10 | **Direct trade of physical goods (merch for merch / merch for services)** | Two parties agree a swap on the Direct Exchange trade slip. | Each side receives the other's item/service direct. | **LIVE (site)** | Same as 8.1 — no escrow, terms are the parties' own. |

---

## 9. The if/then fallback chain — all channels open, nothing single-point

The rule (Chais, 18 Nov 2026): every channel open; if one rail fails, another carries it. The chain below is the order the system falls back through. No step in it depends on Stripe.

| Step | If… | Then… |
|---|---|---|
| 1 | Buyer pays by card | **Bandcamp checkout** (music/merch) or **Ko-fi/Payhip checkout** (digital) — card works, Stripe is not in the path. |
| 2 | Card checkout is unavailable (no Bandcamp page yet, no Ko-fi yet) | **Cash App** — buyer pays $chaisthegreat28 direct; order marked paid manually. |
| 3 | Buyer has no Cash App | **PayPal** — payment link or PayPal checkout; Chais receives in PayPal. |
| 4 | Buyer pays in crypto | **Coinbase Business USDC link** (when the application completes) or **direct SOL/BTC/ETH to a published wallet address**. |
| 5 | Buyer has only Cash App and wants crypto | **Cash App → BTC → Coinbase → SOL** bridge (Direct Exchange matrix documents it). |
| 6 | Buyer wants to trade, not buy | **Direct Trade** on Direct Exchange — trade-slip builder, peer-to-peer, no middleman. |
| 7 | Buyer wants a token | **Pump.fun** (after Gates 1–3 clear per coin) or **Zora** (after Gate 1) — creator-fee coins, never a Stripe step. |
| 8 | Buyer wants an NFT | **OpenSea / Manifold** (after Gate 1 + deploy) — EVM, crypto checkout. |
| 9 | Any single rail is down, held, or deactivated | **The next rail in this chain carries it.** The ledger records the payment whichever rail it lands on. |
| 10 | A payment lands on any rail | **It is recorded in his own transaction ledger** (the Replit pay-function ledger for the apps; the Shopify order record + ScrollCredits ledger for the store) — the history is his, not a platform's. |

**What the fallback chain does NOT do:** it never routes a buyer to Stripe while the dispute stands; it never opens a second Stripe account; it never promises a token, NFT, or return as part of a purchase; it never sells a free-only item (Code of Tawḥīd, Londyn lullaby) or a screenshot-only work.

---

## 10. What's missing, in order — the critical path to real money

| # | Missing piece | Unblocks | Owner |
|---|---|---|---|
| M1 | **A working checkout on Shopify** — Cash App manual method + verify, then PayPal as second rail. | The store (2.1), bundles (2.2), add-ons (2.3), standalone pieces (2.4), and the CRM home (Move 1). The single gate for every store sale. | Chais — Shopify login to restart the browser task. |
| M2 | **Bandcamp artist page + PayPal payout account** (B6). | Save Me (2.5) + Goat Bundle (2.6) sales; the Dec 4 Friday window. | Chais — create the free page, link PayPal. |
| M3 | **Save Me sellable audio + cover** (B1/B2) and **Goat masters + tracklist** (B3/B4). | Both Bandcamp listings; T3/T4 bundles. | Chais — DistroKid Vault pull (masters + tracklist) and Gmail MP3 download (Save Me); cover from Facebook or supplied file. |
| M4 | **Vydia direct-sale confirmation in writing** (B5/G6). | Any direct sale of a Vydia-distributed song — Save Me, Goat album download, bonus track A5. | Chais — read the signed agreement or ask Vydia support: non-exclusive? direct sales allowed? master download available? |
| M5 | **DistroKid export (catalog + ISRCs) + settle $103.88.** | RouteNote (3.2) and the Goat masters (M3). The critical path for streaming revenue. | Chais — DistroKid app export; the $103.88 needs the locked Cash App Card (Visa ending 9039) unlocked. |
| M6 | **SOL in the Pump.fun wallet** (~0.25 SOL covers Wave 1 + buffer). | Every coin creation (7.1–7.2). | Chais — Cash App → BTC → Coinbase → SOL, or card deposit in the Pump.fun app. |
| M7 | **Written per-asset Howey analysis** — SVRS first, then each coin/NFT in order. | Every mint (6.1–6.8) and every token launch (7.1–7.5). | Free lawyers first (DCLDC, Rutgers, BLIP, NJVLA, VLA NY, Harvard Cyberlaw — 10 outreach emails sent 18 Nov, 0 replies yet), pay-after second, JD Woods $349/token fallback. |
| M8 | **Founder sign-off per coin** (Gate 3) after Gates 1–2 clear. | Each individual launch. | Chais — per coin, after the gates clear. Sign-off given early does not count. |
| M9 | **Coinbase Business — Source of funds statement in the LLC's name.** | The USDC rail (1.6). | Chais — Mercury business account activation, or an Ocean First statement in the LLC's name. Do not keep asking for statements unless a trigger lands. |
| M10 | **Replit Autoscale deployment increase** (support request). | Publishing DecentralizedMelody ×2, Chaisomnitechworld, Quantum Resonance, RecipeSage/Command Hub, GameNight. | Chais or Muse — contact Replit support to request the increase (or free up a deployment). |
| M11 | **Stripe key for OmniLoop** (or accept the key-less path). | Real payments through OmniLoop `/mint`. | Chais — add STRIPE_SECRET_KEY in Replit Secrets himself. The pay-function work routes around it with PayPal + Cash App in the meantime; do not invent a key. |
| M12 | **Marketplace accounts** (Redbubble, TeePublic, Spreadshop EU) + payout methods + tax forms. | Marketplace sales (2.7–2.9). | Chais — create the accounts (or approve creation). |
| M13 | **KDP account** (Amazon login + tax info + royalty bank details). | Book sales on Amazon (4.1). | Chais — his hands only. |
| M14 | **Manifesto licence line** (CC BY-NC-SA vs MIT signals vs the book's own protected line). | The KDP listing + every bundle that includes the Manifesto. | Chais — confirms the licence line. |
| M15 | **Knicks IP decision for tokens/NFTs** (fresh, per coin). | Using any of the 6 Knicks pieces as NFT art or a token image (6.1, 7.1–7.2). The merch as-is decision does not cover it. | Chais + attorney (Howey brief Q6). God Mode (own IP) is the clean lead and needs no such decision. |
| M16 | **Consent text (E4) + signup forms (E3).** | Any email collection; the CRM list; the first-customer record. | Write the opt-in text + unsubscribe flow before the first form goes live. |
| M17 | **Numbered-run mechanism (G4) + gated Library element (L1).** | Numbered tiers (T2–T4) and "Library access" as a real bundle perk. | Run sheet (order → edition number → buyer) + numbered certificate card; define the gated Library element. Do not sell free Atlas access as a paid perk. |

---

## 11. Never — excluded from every option

- **Londyn lullaby** — a child. Never placed, sold, listed, shown, or used as a token image, collection banner, or preview anywhere. Inventory only.
- **Code of Tawḥīd** — free-only, never commercialised. Never a coin, NFT, bundle item, or sales device.
- **Nipsey name/face; prophets; living figures as new coins** — never used.
- **Screenshot-only works** (The Boyz, Brunson Is King, Brunson MVP) — no originals/CIDs; never listed until originals exist.
- **Father's Day Genesis** — a real photo of real people; inventory only, never merch, never an NFT.
- **No token/NFT sale, mint, pre-sale, or token-as-reward** before the written per-asset Howey analysis.
- **No return / yield / appreciation / passive-income / floor-price language** anywhere — including the CHX "passive divine income", $MIRROR 2% dividend / 12% APR, $LONDC 5% "passive income", and DivineEssenceCoin's 8%/12%/18% APY comments.
- **No public "proceeds go to causes" claim or live donation button** before CPA charitable review + each 501(c)(3)'s written naming permission. (The coin descriptions' proceeds line is itself under Howey review, Question 3.)
- **No unverified figures in anything that sells** — no $35.4T, no $10T, no 50M+ users, no 144,000 Guardians, no "LIVE" claims, no repo demo figures ($12,450 revenue / 1,247 listeners, "38 million architects") presented as real.
- **No second Stripe account** to route around the VibeCanvas hold. No new customer money through Stripe while the dispute stands.
- **No Vydia-distributed song sold direct** until the non-exclusive + direct-sale confirmation is in writing.
- **No partial album listed as a full album** — the Goat Bundle does not list until the masters + tracklist are in hand.
- **No invented tracklist, cover, audio quality, price, inventory, or launch claim.** Every public claim needs a source: record, file, or owner instruction.
- **No ScrollCredits sold.** Credits are earned by buying; selling them would turn a loyalty record into a saleable instrument.

---

## Sources

- Direct Exchange site (Route Finder, three rails, six asset families, Pay-in-anything matrix, trade-slip builder, 11-platform cross-promotion) — artifact `direct-exchange`, public link on file.
- Placement plan: `~/workspace/digital-assets/placement-plan-2026-11-18.md` (contracts code-only, chain split, platform research, gates, first move).
- Pump.fun library: `~/workspace/digital-assets/pumpfun-library/pumpfun-library.md` (Wave 1 + Waves 2–5, funding status $0.00).
- Bandcamp Friday pack: `~/workspace/bandcamp/bandcamp-friday-dec4-pack-2026-11-18.md` (listings, money math, blockers B1–B8).
- Bundles pack v1 + v2: `~/workspace/bundles/scrollverse-bundles-2026-11-18.md` (tiers T1–T4, add-ons A1–A5, Stage-1 incentive, gaps G1–G10, L1, customer list).
- CRM plan: `~/workspace/crm/crm-opportunities-plan-2026-11-18.md` (honest baseline 0/0/$0/0, CRM-ready components, top 3 moves).
- Early Coins governance: `~/workspace/early-coins/governance.md` (three gates, Stage-1 head start, IP flags, CF-1–CF-20).
- Howey brief: `~/workspace/legal/howey-brief-wave1-2026-11-18.md` (12 attorney questions, per-asset gate).
- Merch marketplaces pack: `~/workspace/merch/marketplaces-pack-2026-11-18.md` (7 pieces, payout math, IP flag, watermark trap).
- Free platforms: `~/workspace/money-avenues/free-platforms-2026-11-18.md` (Bandcamp, RouteNote, KDP, marketplaces, Pump.fun/Zora, FilmHub, YouTube, Ko-fi/Payhip/Patreon, overseas lanes).
- RouteNote pack: `~/workspace/music-distribution/routenote-pack-2026-11-18.md` (0 songs upload-ready, ISRCs in DistroKid, 5–6 week timeline).
- Shopify audit: `~/workspace/shopify/shopify-advanced-maximization-2026-11-18.md` (96 ACTIVE / 2 DRAFT, 0 orders, $0 sales, 34 sessions/90 days).
- Replit inventory + maximize pass (18 Nov 2026): OmniLoop live at https://python--hillchais1.replit.app/ (Stripe key absent); DecentralizedMelody ×2 + Chaisomnitechworld running in preview (demo fallback / simulated payment); publishes blocked by the Autoscale deployment limit; pay function being added now (PayPal + Cash App, if/then fallback, all Stripe traffic redirected, transaction ledger) — browser task in progress.
- Stripe dispute: evidence pack sent 18 Nov (msg `1a1ef46b3d91f135`), awaiting Mark's answers to 7 questions; account acct_1REAmRFKoPayn2e0; Chais's stated position is that Stripe is holding almost $200,000 of his money.
- Coinbase: Business application ref d6b2fffd-667b-45a1-ac77-3738dc1b8203, paused one document away (Source of funds in the LLC's name); retail web blocked by the application; Commerce closed 31 Mar 2026.

*End of map. Research and plan only — build nothing, contact nobody, send nothing.*

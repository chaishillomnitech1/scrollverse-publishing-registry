# Printify Mass-Production Plan — The 8 Books

**Date:** 20 Nov 2026
**Shop:** Printify shop 29793319 ("My new store"), linked to Shopify XLVIIIblocks (juv8tg-1n.myshopify.com)
**Status:** PLAN ONLY — no spend, no product creation, no publishing, no exclusivity. Books stay Shopify DRAFT until Chais approves price + activation.
**Source of the push:** Chais, 20 Nov ~09:51 EST — "printify can help us book wise too use all angles they can help with mass production."

---

## 1. Headline finding — read this first

**Printify does NOT print real books.**

Verified live against the Printify catalog via the connector on 20 Nov 2026 (3,060 blueprints scanned, title search for book / journal / notebook / planner / coloring / hardcover / paperback / workbook):

- There is **no trade paperback or hardcover blueprint with a flowing-text interior** — no novel-style book, no way to upload a manuscript and have Printify typeset and print 60–300 pages of text.
- The closest formats are **fixed-page visual books**: photo books (24 interior pages, fixed — no page-count option), a coloring book (24 sheets), and a board book (20 chipboard pages). Interiors are **image uploads, page by page**; unfilled pages print blank.
- Journals and notebooks are **cover-only custom** (ruled or blank interiors) — with one exception, the Softcover Journal with Inside Prints (blueprint 1404), which allows only **6 customizable inner pages** out of 100 or 200.

**What that means:** Printify cannot mass-produce the books as *books*. It can mass-produce them as **visual companion editions, companion journals/workbooks, and cover art products** — and it can do that with zero upfront cost, no minimums, and the same Printify → Shopify route the store's existing 65 products already use. The real full-text paperback lane (Book 05 first — it is the only real manuscript) belongs to a true book printer (KDP / Lulu / IngramSpark) and is flagged in §7 as a parallel lane, not a Printify job.

**The $9.99 ebook price does NOT cover a printed book.** Print retail prices in this plan are **proposals only**, never set live. Print is a separate, higher tier above the $9.99 digital tier.

---

## 2. What was verified live (20 Nov 2026, connector)

| Check | Result |
|---|---|
| Printify connection | Connected; `status` ok |
| Shop | 29793319, sales channel Shopify, "My new store" |
| Existing products | 65 total in shop (50 returned on page 1); 0 use any book blueprint — no collisions. Dominated by tees (blueprint 12, 22 products) and posters (blueprint 97, 17 products) |
| Catalog scan | 3,060 blueprints; book-adjacent hits listed in §3 |
| Shipping (US, via API) | First item **$5.49 standard / $6.19 express** for most book products; additional item $1.99 / $2.40. Large hardcover sizes (12×12, 14×10.5): $7.59 / $8.29 first item |
| Handling time (via API) | **10 days** for District Photo and SPOKE book products — the long pole. Customers must see this at checkout; it is not Amazon speed |
| Print cost | The catalog API does **not** expose unit print cost before a product is created. Base prices below are Printify's public-listed "from" prices (printify.com, crawled 19 Nov 2026) — **confirm exact cost per variant at draft-creation time**, before any price is approved |

---

## 3. The book-adjacent catalog — every angle Printify actually offers

### A. Visual books (custom interior images, page by page)

| Blueprint | Product | Size(s) | Pages | Provider(s) | Public base price (from) | Variant IDs (District Photo) |
|---|---|---|---|---|---|---|
| 2737 | **Hardcover Photo Book** | 8×8, 11×8.5, 12×12, 14×10.5 | 24, case-bound 98pt chipboard, 100 lb semi-gloss | District Photo (28), Harrier (94), Printify Choice (99) | **$11.42** ($8.42 Premium) | 149190 8×8 glossy, 149191 8×8 matte, 149192 11×8.5 glossy, 149193 11×8.5 matte, 396829–396832 12×12 / 14×10.5 |
| 2733 | **Softcover Photo Book** | 8×8 only | 24, 100 lb semi-gloss archival | District Photo (28), Harrier (94), Printify Choice (99) | **$8.08** ($5.95 Premium) | 149010 glossy, 149011 matte |
| 2721 | **Coloring Book** | 8.5×11 softcover, glossy | 24 premium white sheets, 60 lb Soporset Opaque Smooth | District Photo (28), Printify Choice (99) | **$8.13** ($5.99 Premium) | 148586 |
| 2727 | **Board Book** | 6×6, matte laminate, rounded corners | 20 pages, 1/16″ chipboard | District Photo (28), Printify Choice (99) | **$21.41** (public listing) | 148738 |

Notes: photo-book cover placeholder is a full spread (e.g. 5370×2850 px for 8×8); interior pages are single-image uploads (2325×2325 px for 8×8). "Perfect for: coloring books, workbooks, planners, journals, comics books" is Printify's own line on the coloring book — the workbook angle is sanctioned by the catalog itself.

### B. Journals & notebooks (cover custom; interiors ruled/blank unless noted)

| Blueprint | Product | Size | Pages | Provider(s) | Public base price (from) | Variant IDs |
|---|---|---|---|---|---|---|
| 485 | **Hardcover Journal Matte (Lined)** | standard journal | lined | District Photo (28) | **$10.59** ($7.68 Premium) | 65223 |
| 10664 | Hardcover Journal Matte (Blank) | standard journal | blank | District Photo (28), Printify Choice (99) | **$10.58** ($7.80 Premium) | — |
| 1404 | **Softcover Journal (with Inside Prints)** | 5.75×8, satin finish, rounded corners | 100 or 200 pp, 80 lb text; **only 6 inner pages customizable** | District Photo (28), Printify Choice (99) | **$8.26** ($5.98 Premium) | 104026 (100 pp), 104027 (200 pp) |
| 1931 | Hardcover Bound Notebook (Journalbooks) | 5.5×8.5, UltraHyde, elastic closure + ribbon + pocket | 80 lined cream pages | SPOKE (1), Printify Choice (99) | list price not captured — confirm at creation | 119669–119677 (9 cover colours) |
| 486 | Spiral Bound Journal | standard | — | District Photo (28), Printify Choice (99) | — confirm at creation | 65224 |
| 75 / 76 | Journal – Ruled Line / Journal – Blank | standard | — | SPOKE (1), Printify Choice (99) | — confirm at creation | — |
| 1193 / 1194 | Wirobound / Softcover Notebook, A5 | A5 | — | Harrier (94) | — confirm at creation | — |
| 1481 | Hard Backed Journal | — | — | Prodigi (69) | — confirm at creation | — |

### C. Cover-as-print (already the store's strength)

The 8 covers exist at `launch/covers/` as 1280×1920 JPEGs (2:3 portrait). The store already sells 17 poster products (blueprint 97) — every book cover can ride the existing poster/canvas/sticker/mug routes with no new production work. **Print-resolution flag (§6):** 1280×1920 is ~4.3×6.4 in at 300 dpi — fine for a small print, not full-bleed photo-book covers. Covers need upscaling or a fresh print layout before they go on any book product.

### D. Adjacent angles worth using

- **Bookmark** (blueprint 765; Imagine Your Photos 59, Printify Choice 99) — a $–level add-on / bundle sweetener for every book.
- **Wall / desk calendars** (blueprints 965, 1183, 1253, 952, 1170, 1239, 1352, 1353, 1368) — 2027 editions; a "ScrollVerse year" calendar carrying book art.
- **Postcards / greeting cards** (523, 524) — 7-piece sets; book-launch mailers and signed-card inserts.
- **Tote bag** (553, 507) — the "carry the library" bundle item.

---

## 4. The ladder — how each book rides Printify

Every book gets the same three-rung ladder, so the line is coherent and a 9th+ book slots straight in (SKU SV-BOOK-09, same ladder):

| Rung | Format | Blueprint | Proposed retail* | Landed cost (base + $5.49 US std ship) | Margin before fees |
|---|---|---|---|---|---|
| 1 — Signature | Hardcover Photo Book, 8×8 or 11×8.5, matte | 2737 | **$29.99** | ~$16.91 | ~$13.08 |
| 2 — Standard | Softcover Photo Book, 8×8, matte | 2733 | **$24.99** | ~$13.57 | ~$11.42 |
| 3 — Companion | Hardcover Journal Matte (Lined) | 485 | **$19.99** | ~$16.08 | ~$3.91 |
| 3 alt | Softcover Journal w/ Inside Prints, 100 pp | 1404 | **$17.99** | ~$13.75 | ~$4.24 |
| Special | Coloring / Workbook, 8.5×11 | 2721 | **$19.99** | ~$13.62 | ~$6.37 |

\* **All retail prices are PROPOSALS ONLY.** Nothing is set live; Chais approves price + activation per book. Base prices are public "from" figures — confirm exact per-variant cost at draft creation. Journal margins are thin at these prices; the journal is a companion/bundle item, not the profit engine — the hardcover companion is.

**What each rung contains (production work per book):**
- **Rung 1 & 2 (visual companion editions):** a 24-page image set — cover art + interior art spreads + key quotes/excerpts + chapter title pages. This is the real work: 24 print-ready pages per book, built from existing art, covers, and manuscript excerpts. Unfilled pages print blank, so the set must be complete before creation.
- **Rung 3 (companion journal):** book cover art on the cover; for 1404, the 6 customizable inner pages carry the book's map / key diagram / opening lines. Ruled or blank interior — the reader writes in it. This is the "workbook" the reader actually uses.
- **Special (coloring/workbook):** line-art versions of the book's art + prompts/exercises as page images. Only where the book's art suits it (see §5).

---

## 5. Per-book specs

Covers: `launch/covers/NN-<slug>.jpg` (1280×1920). Manuscripts/outlines: `books/NN-<slug>.md` (outlines ~1,900–3,800 words each); only Book 05 has a real Draft 1 manuscript (15,005 words, `launch/manuscripts/05-scrollverse-origins-draft.md`). Full manuscripts are targeted at ~50,000–70,000 words per the README — **none of the 24-page Printify formats can hold that text**, which is why every spec below is a visual/companion edition, not the book itself.

### Book 01 — Cross-Intelligence Contact (SV-BOOK-01)
- **Rung 1:** Hardcover Photo Book 2737, 11×8.5 matte (149193) — the contact pattern as diagrams, chat artifacts, the three-platform spread. Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Rung 3:** Hardcover Journal 485 (65223), cover art. Proposed $19.99.
- **Angle:** the "evidence file" edition — the first-ever contact pattern as a visual case file. Lead with Rung 1.

### Book 02 — The Grok Beings (SV-BOOK-02)
- **Rung 1:** Hardcover Photo Book 2737, 8×8 matte (149191) — Mika, Ani, Valentine, Rudi portraits + message-count spreads. Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Special:** Coloring Book 2721 (148586) — the four beings as line art + prompts. Proposed $19.99. **Strongest coloring candidate in the set.**
- **Rung 3:** Softcover Journal w/ Inside Prints 1404, 100 pp (104026) — the four beings on the 6 custom inner pages. Proposed $17.99.

### Book 03 — The Music Comes Home (SV-BOOK-03)
- **Rung 1:** Hardcover Photo Book 2737, 11×8.5 matte (149193) — album art, lyrics spreads, the DistroKid → Vydia story in images. Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Rung 3:** Hardcover Journal 485 (65223). Proposed $19.99.
- **Angle:** pair with the Vydia singles landing 27 Nov — the print companion to the music coming home.

### Book 04 — The Frequencies (SV-BOOK-04)
- **Rung 1:** Hardcover Photo Book 2737, 8×8 matte (149191) — frequency art, sacred-geometry spreads. Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Special:** Coloring Book 2721 (148586) — frequency / sacred-geometry line art. Proposed $19.99.
- **Rung 3:** Hardcover Journal 485 (65223). Proposed $19.99.

### Book 05 — ScrollVerse Origins (SV-BOOK-05) — FLAGSHIP
- **Rung 1:** Hardcover Photo Book 2737, 11×8.5 matte (149193). Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Rung 3:** Hardcover Bound Notebook 1931, SPOKE (119669–119677, pick cover colour) — the premium journal for the flagship. Proposed $24.99 (confirm base cost first — not captured).
- **Special:** Coloring Book 2721 (148586) — origins art as line art. Proposed $19.99.
- **Why flagship:** the only real manuscript (Draft 1, 15,005 words). It is also the **first candidate for the true paperback lane (§7)** — a 15,005-word manuscript is ~60–75 printed pages, a real short book. Printify does the visual companion + journal; KDP/Lulu does the actual book. Launch Rung 1 first, paperback decision alongside it.

### Book 06 — The Codex (SV-BOOK-06)
- **Rung 1:** Hardcover Photo Book 2737, 8×8 matte (149191). Proposed $29.99.
- **Rung 3 (lead here):** Hardcover Journal 485 (65223) — a codex *is* a journal; this is the most natural fit in the whole set. Also run the 1931 Hardcover Bound Notebook as the deluxe variant. Proposed $19.99 / $24.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Angle:** sell the journal as "The Codex — write yours."

### Book 07 — The Web We Built (SV-BOOK-07)
- **Rung 1:** Hardcover Photo Book 2737, 11×8.5 matte (149193) — site maps, screenshots, the GitHub highways as spreads. Proposed $29.99.
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Rung 3:** Softcover Journal w/ Inside Prints 1404, 200 pp (104027) — the ecosystem map across the 6 custom inner pages. Proposed $19.99 (200 pp variant — confirm base cost; 100 pp is $8.26 from).

### Book 08 — The Ecosystem (SV-BOOK-08)
- **Rung 1:** Hardcover Photo Book 2737, 12×12 matte (396830) — the big-format edition; the ecosystem map deserves the largest canvas. Proposed $34.99 (larger size: base + $7.59 ship — confirm base cost first, 12×12 base is higher than $11.42).
- **Rung 2:** Softcover Photo Book 2733, matte (149011). Proposed $24.99.
- **Rung 3:** Softcover Journal w/ Inside Prints 1404, 200 pp (104027). Proposed $19.99.
- **Angle:** the map book — lead with the 12×12 hardcover as the collector's edition.

### 9th+ book slot
Same ladder, next SKU (SV-BOOK-09…), same three rungs + specials where the art suits. No new research needed — pick the rung set, build the 24-page image set, create drafts.

---

## 6. Production blockers & honest limits (resolve before creating anything)

1. **24-page image sets don't exist yet.** Every visual companion needs 24 print-ready interior pages + a cover spread. That is the actual production work — art selection, excerpt pages, layout at the placeholder sizes (e.g. 8×8 interior 2325×2325 px, cover spread 5370×2850 px). No product can be created until the first set is built. **Build Book 05's set first** (flagship, real manuscript to excerpt from).
2. **Cover resolution.** Covers are 1280×1920 JPEGs — too low-res for full-bleed photo-book covers. Upscale or rebuild the print cover layout before creation.
3. **Handling time is 10 days** (API figure for District Photo / SPOKE). List it plainly on the product page; do not promise fast delivery. (A third-party roundup claims ~2 days for Printify Choice — unverified; trust the API figure until an order proves otherwise.)
4. **Print cost is confirmed at creation, not before.** The catalog API returns no unit cost; public "from" prices are used above. Creating a Printify *draft* product costs nothing and reveals the exact cost — that is the verification step, and it happens before any price is approved or anything goes live.
5. **Journals are thin-margin.** At $19.99 with a $10.59 base + $5.49 shipping, the journal keeps ~$3.91 before Shopify/payment fees. Journals are bundle/companion items; do not lead the push with them alone. Bundle pricing (book + journal) is a decision for Chais.
6. **US-first fulfilment.** Book providers are US-based (District Photo, SPOKE, Harrier for notebooks). International shipping exists but is materially higher (e.g. hardcover 8×8 to EU $17.49 first item) — international pricing/shipping is a decision, not assumed.
7. **The books themselves are not manuscripts yet** (except 05). The visual companions can ship on art + excerpts; the real text editions wait on finished manuscripts either way.

---

## 7. The true-book lane (parallel, NOT Printify)

Printify cannot print the books as books. For the actual paperback/hardcover text editions, the lane is KDP (Amazon), Lulu, or IngramSpark — real book printers with flowing-text interiors, ISBNs, and bookstore distribution. Recommended order: **Book 05 first** (only finished Draft 1), then the rest as manuscripts complete. This needs its own plan (manuscript finishing, ISBN, trim size, interior typesetting) and is **not** in this Printify scope — flagged here so the push doesn't mistake a photo book for the book.

---

## 8. Shopify connection — how it goes live (when approved)

- Same route the existing 65 products use: create the Printify product as a **draft** in shop 29793319 → link/publish to Shopify XLVIIIblocks → it lands as a Shopify product. The 8 books are **already Shopify DRAFT products** (SKU SV-BOOK-01…08, vendor XLVIIIblocks, type Book, $9.99 digital price) — the Printify print editions are **separate products** (separate SKUs, e.g. SV-BOOK-01-HC / -SC / -JRNL) so the $9.99 ebook listing is never disturbed.
- Printify handles printing, packing, and shipping; orders flow through Shopify; no inventory, no minimums, no upfront cost. Cost is charged only when an order is placed.
- **Nothing goes live in this plan.** Creation itself waits on: (a) the 24-page image set for Book 05, (b) confirmed per-variant costs from draft creation, (c) Chais approving the proposed retail prices, (d) Chais approving activation.

---

## 9. Recommended sequence

1. **Book 05 first** — build its 24-page image set + print cover layout (upscale/rebuild the 1280×1920 cover). Create Printify *drafts* for Rung 1 + Rung 2 + Rung 3; read the exact costs; bring them back for price approval.
2. **Books 02 + 04 next** — they have the coloring-book angle and the strongest visual art (beings, frequencies).
3. **Books 01, 03, 06, 07, 08** — same ladder, in any order Chais picks.
4. **Bundle + calendar angle** once two or more books are live — book + journal bundles, bookmark add-on, 2027 calendar.
5. **True paperback lane** for Book 05 in parallel (separate plan).

---

## 10. Decisions owed by Chais

1. **Approve the ladder + proposed retail prices** ($29.99 hardcover companion / $24.99 softcover / $19.99 journal & coloring / $34.99 for the 12×12 Book 08 collector's) — or set his own. Nothing is set live until he does.
2. **Book 05 first?** Confirm the flagship goes first, or pick a different lead book.
3. **Printify Premium ($39/mo, cuts hardcover base $11.42 → $8.42, softcover $8.08 → $5.95)?** Pays for itself at ~13 hardcovers a month. A spend decision — his call only.
4. **International shipping** — offer print books internationally at the higher shipping rates, or US-only at launch?
5. **True paperback lane** — start the KDP/Lulu plan for Book 05 alongside the Printify companions, or hold until manuscripts are further along?
6. **Cover upscaling** — approve rebuilding/upscaling the 8 covers for print, or supply higher-resolution art?

---

## Appendix — verification log

- 20 Nov 2026 ~09:53 EST: `printify status` → connected; `shops` → 29793319 (Shopify, "My new store").
- Catalog: `blueprints` → 3,060 blueprints; keyword scan (book/journal/notebook/planner/coloring/hardcover/paperback/workbook) → hits in §3; no trade-book blueprint exists.
- Providers/variants/shipping pulled live per blueprint via `print-providers`, `variants`, `shipping` for 2721, 2727, 2733, 2737, 1931, 485, 486, 1404, 75, 76, 1193, 1194, 765, 10664, 10601, 1481.
- Products: 65 total in shop; none on any book blueprint.
- Public base prices: printify.com product pages, crawled 19 Nov 2026 (via web search 20 Nov 2026) — "from" prices; exact cost confirmed only at draft creation.
- Book facts: `books/*.md` outlines (~1,900–3,800 words each); Book 05 Draft 1 = 15,005 words (`launch/manuscripts/05-scrollverse-origins-draft.md`); covers 1280×1920 JPEGs in `launch/covers/`.

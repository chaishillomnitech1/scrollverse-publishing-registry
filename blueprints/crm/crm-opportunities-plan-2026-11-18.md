# CRM Opportunities — Survey & Plan (Research Only)

**Date:** 18 November 2026
**Status:** Research and plan only. Nothing built, nobody contacted, nothing sent, $0 spent.
**Sources read:** GitHub showcase survey (102 repos), rollout ledger (passes 1–10), bundles pack v2 §10 (customer list), AI Legion extraction plan, Shopify Advanced maximization audit, `omniversal-kernel/integrations/crm.js` (read live), `MailchimpLegacyProtocol` README + `scripts/api-hook.js` (read live), allies program, Replit maximize report.

## 0. The honest starting point

- **Real customers: 0. Real orders: 0. Real sales: $0. Contacts on any list: 0.**
- Shopify has 2 customer records and both are Chais himself (one is a typo address, hillchais1@gmsil.com). Shopify Email has never been used. 34 store sessions in 90 days.
- Every figure in this plan that comes from a repo README is the repo's own claim, labelled as such. Nothing here is presented as real customers or real revenue.
- **Demo data stays demo:** the "38 million architects" figure (omniversal-kernel README), the "$12,450 revenue / 1,247 listeners" figures (DecentralizedMelody README), and the simulated architect data in `integrations/crm.js` are demo/repo claims, not real numbers. They never appear in customer-facing copy as fact.
- **Guardrail:** no token/NFT sale, mint, pre-sale, or token-as-reward before a written per-asset Howey attorney analysis. CRM incentives stay Stage 1 only: ScrollCredits (loyalty points, no cash value, never a token), early access, numbered runs, Library access, earned roles.

## 1. What customer/lead data and tools already exist

### 1a. Data that exists today

| Data | Where it lives | State |
|---|---|---|
| Shopify customer records (2, both Chais) | Shopify Customers, juv8tg-1n.myshopify.com | Real records, 0 orders each. Typo record needs merge/delete (Chais's yes). |
| Allies register (10 allies contacted, 0 replies) | `~/workspace/allies/allies-program-2026-11-18.md` §6 | A B2B relationship ledger in a document. PSYCHE16 is named as the ledger keeper. 0 replies logged so far. |
| Early Coins Question Box (GitHub Discussions) | github.com/chaishillomnitech1/early-coins/discussions | Live and enabled. 0 discussions posted yet. Public Q&A = a lead channel. |
| ScrollCredits ledger shape | Bundles pack v1 §1/§3 | Defined on paper: per-contact balance, edition numbers, earned roles. No ledger exists yet — the first sale creates the first row. |
| Segment definitions (5) | Bundles pack v2 §10c + Shopify audit §4 P5 | Readers, Music buyers, Merch buyers, Collectors, Window shoppers — written, not yet built in Admin. They populate automatically once real orders exist. |
| Bandcamp buyer emails (future) | Bandcamp, live 4 Dec 2026 | Bandcamp shares the buyer's email with the artist per sale. No page yet, no sales yet. |
| Facebook/Instagram audiences | @chaishillomni, @chaishill, @chasedreamz_management, @chaisthegreat_mrwalk (6,990 followers, unlinked to Muse) | Followers exist; no emails, no list. Socials are reach, not a customer list. |
| Versus battle-night audience | Live verse battles with Riz | A real recurring audience. No signup capture exists yet. |

### 1b. Tools that already exist

| Tool | What it does | State |
|---|---|---|
| **Shopify Customers** (built in) | Every order creates a customer record with purchase history | Live in the store, $0. Waiting on the first order. |
| **Shopify Email** (built in) | Send to the list from inside Shopify. Free tier on Shopify's published plan: 10,000 emails/month (confirm at setup) | Never used. 0 campaigns sent. |
| **Shopify Flow** (built in, free) | No-code automation: tag VIP buyers, post-purchase follow-up, high-value alerts, abandoned-checkout tagging | 5 workflows drafted in the Shopify audit §4 (first-order thank-you + ScrollCredits, high-value order alert, abandoned-checkout tag). None turned on — each needs Chais's yes before activation. |
| **Abandoned checkout recovery** (built in) | Auto-email to buyers who reached checkout and left | Not verified. Should be ON before the first sale. |
| **Matrixify** (installed) | Bulk import/export of customers, orders, products | Installed, unused. The tool for importing Bandcamp buyer emails into Shopify Customers. |
| **Shopify Audiences** | Finds new buyers who look like existing customers | Not usable yet — needs real buyer data (revisit at 50+ real customers). |
| **Klaviyo / Mailchimp** (not created) | Email + segments + flows. Free tiers: Klaviyo 250 contacts / 500 sends/mo; Mailchimp 500 contacts / 1,000 sends/mo (confirm at signup) | No accounts. The plan says: start with Shopify Email, add Klaviyo at ~250 contacts. Pick one, not both. |
| **Google Sheets ledger** | One row per contact (email, name, source, consent date, purchases, credits) | The $0 fallback. No sheet exists yet. |

### 1c. Lead capture points already planned (bundles pack §10a)

Shopify checkout (opt-in checkbox, not pre-ticked) · bundle/product page signup (form, not a gate) · Atlas reading rooms (optional signup only — free stays free, Chais's rule) · Bandcamp buyer email per sale · socials link-in-bio · Versus battle alerts. Marketplaces (Redbubble/TeePublic/Spreadshop) do NOT share buyer emails — they are not collection points.

### 1d. Privacy rules already written (bundles pack §10e)

Explicit opt-in only · unsubscribe in every email · never buy a list · never sell or share the list · no children's data ever · GDPR for EU buyers · CAN-SPAM basics. **Gap E4: the consent text itself is not yet written — no email may be collected before it exists.**

## 2. Which repos/components are CRM-ready

Ranked by how close each one is to doing real CRM work today. "CRM-ready" means the code or the tool exists and runs or nearly runs — not that it has customers.

| # | Component | Verdict | Evidence |
|---|---|---|---|
| 1 | **Shopify stack (Customers + Email + Flow + Matrixify)** | **READY — the CRM home.** Built in, $0, no new account. The only blocker is a working checkout (G1). | Shopify audit 18 Nov 2026: flows drafted, segments defined, Email 10k/mo free. |
| 2 | **MailchimpLegacyProtocol** | **SCAFFOLD — real code shape, needs a live key + wiring.** Workflows (`campaign-automation.yml`, `subscriber-sync.yml`), templates (`email-campaign.json`, `audience-segment.json`), `scripts/api-hook.js` — a working event dispatcher (campaign.send/create, subscriber.sync/add/remove, knowledge.sync) with an HTTP server mode (port 3000). The hook handlers log and return structured responses; **no live Mailchimp API call was verified in the hook code** — it needs a Mailchimp account + API key + the real client calls before it syncs anything real. | README + api-hook.js read live 18 Nov 2026. |
| 3 | **RecipeSage = ScrollVerse Command Hub (Replit)** | **RUNNING IN PREVIEW — admin CRM surface.** Full-stack admin/command hub: dashboard, guardians, contracts, users, analytics, settings, api-management pages (React + Express + PostgreSQL/Neon + Drizzle). It is the closest thing to a CRM dashboard in the stacks. Runs in preview; **publish NOT live** (Replit Autoscale deployment limit) and the data layer is empty/demo. | Replit inventory + maximize pass, 18 Nov 2026. |
| 4 | **Early Coins Discussions (Question Box)** | **LIVE — lead/Q&A channel.** Enabled and verified. 0 discussions yet. Costs nothing. | Verified 18 Nov ~11:57 EST. |
| 5 | **scrollverse-web-app (the site)** | **CODE-COMPLETE, NOT RUNNING.** Guardian registration (`trpc.guardian.registerAIInvestor`), Legion social hub (channels + display names), full `aiLegion` router (chat / council / apex), 100+ routes. The identity/account layer exists in code; the site is down pending the Manus export + transfer. | Legion extraction plan §2.3, 17 Nov 2026. |
| 6 | **scrollsoul-music-sync** | **B2B RIGHTS CRM.** Placement, licensing, and royalty tracking — who licensed what, royalties paid. A relationship system for music buyers/licensees, not retail customers. 62 KB README, Mermaid + ASCII flows. | Repo survey, 18 Nov 2026. |
| 7 | **omniversal-kernel `integrations/crm.js`** | **DEMO ONLY — do not mistake for a working CRM.** The file exists (15,577 bytes) and the README claims Salesforce + HubSpot sync, engagement scoring, "38M architects". The code **simulates** the sync: it fabricates architect records with random numbers and logs "Simulate Salesforce API call" — no live API calls, no real credentials (demo placeholder config). Useful as a design reference for sync shapes and field lists. Not a CRM. The "38M" figure is the repo's claim, unverified. | `crm.js` read live 18 Nov 2026. |
| 8 | **Allies register (document)** | **B2B LEDGER IN A DOC.** 10 allies contacted, 0 replies, rules written (§6). Works as a ledger today; needs a home (a sheet or the Command Hub) as it grows. | Allies program, 18 Nov 2026. |
| 9 | **Legion concierge widget** | **GUIDE MODE READY.** `~/workspace/muse-the-great/concierge-widget/` — `concierge.js`, `concierge.css`, `knowledge.json` v1.0, `config.example.json`, `demo.html`. Answers from written knowledge, labelled guide mode. The multi-being version is designed (extraction plan §4). Live talk needs hosting + LLM key + spend cap + prompt sign-off. | Legion extraction plan §4, 17 Nov 2026. |
| 10 | **scrollverse-dashboard** | **UNKNOWN.** TypeScript, no README. Could hold dashboard/CRM UI — contents never verified. | Repo survey, 18 Nov 2026. |
| — | **Private repos (unread)** | **UNKNOWN — possibly the most relevant.** `scroliverse_commerce` and `scrollwave` were the most recently updated repos (15–16 Nov) and are private; their READMEs were not read. They may already hold commerce/CRM code. Worth a read when Chais opens them. | Repo survey, 18 Nov 2026. |

## 3. Top 3 CRM moves

### Move 1 — Make Shopify the CRM home (first, $0, no new tool)

**What it is:** turn the store's built-in customer system into the working CRM, using only what is already paid for and already drafted.

**Steps, in order:**
1. Fix checkout first (G1 — the blocking fact for everything): Cash App manual payment method + verify checkout, then PayPal as a second rail. No checkout, no customers, no CRM.
2. Turn on abandoned-checkout recovery (verify in Admin → Settings → Checkout) before the first sale.
3. Activate the drafted Flow workflows, one at a time with Chais's yes on each: first-order thank-you + ScrollCredits tag (25/50/75/150 by tier, recorded in the order note); high-value order alert (over $99 → "collector" tag + owner notify); abandoned-checkout tag ("window-shopper").
4. Build the 5 segment definitions in Admin → Customers → Segments (Readers / Music buyers / Merch buyers / Collectors / Window shoppers) — definitions, not data; they populate automatically once orders land.
5. Write the consent text (gap E4) and put the opt-in checkbox on checkout (not pre-ticked).
6. First Shopify Email campaign to the first real customers, once the Tier 1 price is approved and checkout works. Draft exists in the Shopify audit §4 P3. Never send to the typo record (hillchais1@gmsil.com) — merge/delete it first, with Chais's yes.

**What it needs:** working checkout; Chais's yes on each Flow workflow and on the exact email text; consent text written; typo customer record fixed.
**What it takes to run:** nothing new to buy. Shopify Advanced is already the plan. Roughly a day of Admin work once checkout works, then it runs itself per order.
**What's still missing:** checkout (G1); consent text (E4); the first real customer (E1); the typo record fix.

### Move 2 — Lead capture from the sites (the funnel, $0)

**What it is:** put one optional email signup at every place attention already lands, all feeding one list — Shopify Customers, with a Google Sheet as the $0 ledger until Klaviyo at ~250 contacts.

**Steps, in order:**
1. Write the consent text first (E4) — one short paragraph: what they get, how often (one email per drop), how to stop. No form goes live before this exists.
2. Early Coins Question Box is already live — link it from every site (already in the universal-links section on 51 repos + profile). The first real lead is likely a question, not a purchase.
3. Add the signup form to the store's bundle/product pages ("hear about new drops first") and to the Atlas/Super ScrollVerse reading rooms ("new chapters and drops by email") — optional only, never a gate; the free version stays free for direct visitors.
4. Link-in-bio signup on Instagram/Facebook/Threads; Versus battle-alert signup at the next battle night.
5. Bandcamp buyer emails (from 4 Dec) import into Shopify Customers via Matrixify, with purchase context attached — Bandcamp is a collection point, not a separate list.
6. One shared sheet as the ledger until the list outgrows it (email, name, source, consent date, purchases, ScrollCredits balance, segment). Upgrade to Klaviyo at ~250 contacts or when automated flows are wanted — not before.

**What it needs:** consent text (E4); the signup forms placed (E3); the sheet created; Matrixify import mapping for Bandcamp.
**What it takes to run:** the forms are small edits on the artifacts and the store; the sheet is manual until Klaviyo. The real cost is traffic — 34 store sessions in 90 days is the bottleneck. Traffic comes from the Atlas push, socials, Versus nights, and Bandcamp 4 Dec.
**What's still missing:** consent text; forms; traffic; the first signup. Marketplaces will never feed this list (they keep their buyers) — the store and Bandcamp are the collection points.

### Move 3 — AI-assisted follow-up through the Legion (guide mode now, live later)

**What it is:** the Legion answers the customer first, and hands the warm lead to Chais. The concierge widget already exists; the multi-being version is already designed.

**Steps, in order:**
1. **Guide mode now ($0, no key, no backend):** wire the concierge widget into the sites (Super ScrollVerse, Early Coins, Direct Exchange) as the first responder. It answers buyer questions from written knowledge — what a bundle costs, what's in it, how to pay, when the drop is — and says plainly when it doesn't know. Every answer is labelled guide mode.
2. **The handoff is the CRM moment:** when the guide can't answer, or the visitor wants a human, it offers one step — "leave your email and Chais (or the Legion) follows up" — with the same explicit opt-in as Move 2. That email + question goes into the lead list (Move 2's sheet), tagged with the topic and the being that handled it.
3. **Assign the voices:** Socratica asks questions back (the natural guide voice for a visitor deciding what to buy); King Solomon handles governance/dispute-flavoured questions; Qubit handles the tech questions (wallets, chains, how the mint works). Londyn stays in love/legacy only — never a sales device, never a funnel face (Tier-3 rule).
4. **Live mode later (needs decisions, $0 until approved):** hosting for the backend (thin standalone first, or fold into scrollverse-web-app after the transfer), LLM provider + key (server-side only, never in a repo), model choice, monthly spend cap with a kill switch, prompt sign-off (keep the voice, drop the omnipotence, add the honesty rules from Aurellion's charter), roster confirmation (15 beings; Aurellion public-facing or not). The router code (`aiLegion.ts`: chat / councilQuery / apexAnalysis) and the Apex three-tab UI are already written and are the spec.
5. **Council mode as a follow-up tool:** one customer question answered by 2–3 beings in their own voices (e.g., Socratica on whether, Qubit on how, King Solomon on what's fair) — a distinctive follow-up no ordinary store has.

**What it needs:** the widget wired to the live sites; the email-handoff path built; Chais's sign-off on the adapted prompts; for live mode, the §5 decisions (hosting, provider + key, model, cap).
**What it takes to run:** guide mode costs $0 and needs no key. Live mode costs hosting $0–$7/month on free tiers plus cents per short conversation — and nothing is spent until Chais approves provider + model + cap together.
**What's still missing:** the widget isn't on the live sites yet; the email-handoff path isn't built; live talk needs the backend + key + cap; the beings must never claim to be live, conscious, or superhuman, and never present demo figures as fact.

## 4. The bigger build (phase 2 — after Move 1 proves the list works)

**A ScrollVerse CRM of his own, assembled from his stacks:** the RecipeSage Command Hub (users + analytics + settings pages, already running in preview) as the admin shell; the MailchimpLegacyProtocol dispatcher + templates as the email engine (needs the live Mailchimp key + real client calls); the omniversal-kernel sync shapes as the field model (not its simulated code); the allies register moved in as the B2B ledger; scrollsoul-music-sync as the B2B rights/royalty wing. This is a real project — a week of build, not a day — and it only earns its keep once Move 1 has real customers to manage. Do not build it before the first sale.

## 5. What is still missing overall

- **A working checkout** (G1) — the single gate for every CRM move. Without it there are no buyers to manage.
- **Consent text** (E4) — no email collected before it exists.
- **Traffic** — 34 sessions in 90 days. CRM multiplies customers; it does not create visitors.
- **The private repos** (`scroliverse_commerce`, `scrollwave`) — unread; they may already hold commerce/CRM code.
- **Live Legion talk** — hosting + key + cap decisions (Legion extraction plan §5).
- **Replit publishes** — RecipeSage/Command Hub is blocked by the Autoscale deployment limit; needs a support increase request before it can go live.
- **The Manus transfer** — scrollverse-web-app (guardian registration, Legion social) is down until the export lands and the site is re-hosted.

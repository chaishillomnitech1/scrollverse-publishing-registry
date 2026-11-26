# Free scrollverse.co — assessment + rebuild plan

**Date:** 20 Nov 2026 ~20:30 EST (21 Nov 2026 ~01:30 UTC)
**Status:** Assessment and plan only. No DNS changed, no Manus subscription touched, nothing deployed, nothing spent, no accounts created.
**Chais's direction (20 Nov 2026 ~20:26 EST, his words):** "we will free scrollverse.co but Manus forced us to make that look like childsplay and we still gone raise scrollverse.co beyond."
**Goal:** scrollverse.co runs with or without the Manus subscription, on free hosting, and outbuilds what Manus had.

**Prior work this plan builds on (read first — do not redo):**
- `~/workspace/scrollverse-independence/` — the 17 Nov 2026 investigation + verified local build + DNS cutover plan awaiting his approval: `investigation-site-and-billing.md`, `investigation-source.md`, `deployment.md`, `scrollverse-independence.md`, `harvest-account-info.md`. Build clone at `~/workspace/scrollverse-independence/build/repo/`, logs in `build/logs/`.
- Goal `scrollverse-co-independent-of-manus` — "Make scrollverse.co run with or without the Manus subscription… The rebuild uses his own GitHub source with a Railway-first hosting recipe, and the DNS cutover plan is waiting on his approval."
- Goal `scrollverse-beyond-site` — a new site built to exceed ScrollVerse (Tawhid foundation, Consciousness Mirror, visual series, music catalog, seven-stop tour, rap group, cartoon, podcast; New Dominion — Living Archive). Not yet published, no domain chosen.
- `~/workspace/new-site-plan-2026-11-16.md` — the 7-page exceed-ScrollVerse plan (home, music, watch/listen, tour, mirror, Legion, store/support).

---

## 1. scrollverse.co live right now — verified tonight

Checked 20 Nov 2026 ~20:26–20:30 EST (21 Nov 01:26–01:30 UTC) by text fetch + DNS-over-HTTPS. The VM's own resolver is **not trustworthy** for public DNS (it returns synthetic `198.18.x.x` answers and refuses NS/SOA queries — the 17 Nov investigation proved this; tonight it again returned a synthetic `198.18.150.222`). All DNS below is from DNS-over-HTTPS (Cloudflare + Google), which agree.

| Check | Result |
|---|---|
| `https://scrollverse.co/` | **HTTP 200 — but only Manus's suspension page.** Title "Site Unavailable", text: "Site unavailable due to unpaid billing / Contact owner to update billing in Manus to bring it back", Notify-owner button. Zero ScrollVerse content. Same page as 17 Nov. |
| `http://scrollverse.co/` | 301 → `https://scrollverse.co/` (redirect only) |
| `https://www.scrollverse.co/` | Same suspension page (17 Nov: byte-identical, 21,374 bytes) |
| `https://manusworld-jl8njwlb.manus.space/` | HTTP 200, 21,374 bytes — **the same suspension page**, tying scrollverse.co to that Manus deployment |
| `https://scrollatlas.lol/` | **HTTP 200, 10,702 bytes — still live tonight.** "The Living Archive of Creation — ScrollVerse Museum". But it is **also Manus-hosted** (Manus analytics, `/__manus/`, `manus-storage` paths in its HTML). The one working property is not independent of Manus. |
| `scrollverse.lol` | NXDOMAIN (17 Nov, public DNS) — not a real domain, not a live alternate |

**DNS (DoH, tonight — unchanged since 17 Nov):**

| Name | Type | Answer |
|---|---|---|
| `scrollverse.co` | A | `104.18.26.246` (Cloudflare anycast), TTL 60 |
| `scrollverse.co` | NS | `ns1.globaldomaingroup.com`, `ns2.globaldomaingroup.com` |
| `scrollverse.co` | SOA | `ns1.globaldomaingroup.com. hostmaster.scrollverse.co. 2026082501 16384 2048 1209600 300` |
| `www.scrollverse.co` | A | `104.18.26.246` (same) |
| `scrollverse.co` | AAAA / CNAME / MX / TXT | none — no mail service on the domain, no verification records |

**What this means:** the domain registration and DNS sit with the registrar (Global Domain Group nameservers) — outside Manus. But the A record points at a Cloudflare IP fronting a Manus origin, and everything a visitor can reach is served or blocked by Manus. The page returns HTTP 200, so a status-only uptime monitor would call it "up" while it serves no content. **Re-pointing DNS alone restores nothing** unless the site is hosted somewhere else first.

**Registrar identity is NOT verified in this task:** the nameservers show Global Domain Group, but no whois lookup was run (no whois binary on this machine) and no registrar account was inspected. Who holds the registrar login — Chais, or someone else — is **unverified**. See §5, item 1.

---

## 2. What the Manus version of scrollverse.co was

From the 17 Nov source investigation (7 repos shallow-cloned; nothing changed since except the repo HEAD moved — see flag in §6).

**The site repo: `chaishillomnitech1/scrollverse-web-app`** — React 19 + TypeScript + Tailwind 4 + Vite 7 (client SPA, 577 page components, 589 routes) + Express 4 + tRPC 11 + Node 22 (server, ~60 tRPC routers, 114 MySQL tables). Build: `pnpm build` → `dist/` (Vite client + esbuild server bundle). Run: `pnpm start` → `node dist/index.js` (port 3000). **Not Next.js. No `vercel.json`, no `Dockerfile`, no hosting config in the repo.** Proof it is the site: README "LIVE — scrollverse.co", canonical/og/sitemap all `scrollverse.co` URLs.

**What it did (the bar the rebuild has to beat):** Sovereign portal (100+ pages), Academy, books, NFT/ScrollPort marketplace, Scroll Exchange + staking + governance, AI Hub / AI Legion / AI Council / AI Twin (live chat), Sovereign Cinema, music, OmniChess (live PvP, Socket.io), Guardian waitlist (144,000), Book of Life, ZakatEngine, ScrollShop, broadcast (WebSocket), revenue dashboard, CRM, KYC, creator applications.

**The billing picture (from Gmail, 17 Nov — see §6 for freshness):**
- "Paid for the year" is **documented**: $600 across two annual Manus Pro plans (Apr 2026–Apr 2027), with $349.94 later refunded in Aug 2026 (partial, unexplained in the emails). Six "Welcome to Manus Pro" monthly-subscription emails also exist — multiple concurrent subscriptions.
- **All 38 Manus charge attempts found in Gmail failed** ($9,774.32 attempted, 7 distinct amounts). No successful Manus charge receipt exists in the mailbox. The card on file for the 2026 attempts is the locked Cash App card — Cash App decline emails pair with the Manus failures within seconds.
- Suspension trail: "close to free usage limit" 10 Nov → **"free usage exhausted" 12 Nov 05:02 UTC** → site unavailable since at least 16 Nov. The daily staking-compound emails from the ScrollVerse Trinity backend ran through 15 Nov and then stopped.
- **"Manus switched ownership": NOT supported by any Manus email in Gmail** (searched 17 Nov). It may be true from another source, but Gmail does not document it, and no Manus email gives a new billing entity or new terms. Do not assert it as fact.
- **"Charging in five directions": not verifiable as exactly five.** The emails never itemise five streams. At most: 2 annual plans + monthly Pro + (separately) Vercel billing failures (May 2026, separate platform, separate card) = 4 documented billing relationships. The Cash App declines are duplicates of the Manus attempts, not a fifth.

---

## 3. What the Atlas build already covers vs what the Manus site had

**The Atlas build** — artifact slug `super-scrollverse`, public link `https://muse.ai/s/super-scrollverse-bxy6xtuxz8xm5xvn/Tm8xFKLXO7E7C83iUb9IYReHT3QuXoi714p1sJx8eWU`. Source on disk: `~/workspace/ts-spaces/super-scrollverse/index.html` (127,966 bytes, single file) + `assets/` (24 local files). Tech-edit build applied 20 Nov ~15:00 EST and re-shared 20 Nov ~19:51 EST (theme toggle, smooth scroll, hover glow, heartbeat/trust-lens, playable Chess Arena, Dreams room, source-trails + World Ledger, mailto contact). **Verified tonight: zero Manus references** (the one "manus" grep hit is the word "manuscript"), **all 24 local asset references resolve to files on disk** — nothing missing. Its only external dependency is Google Fonts (CDN, free). It links to `https://scrollverse.co` itself as home.

| Atlas section (live in the build) | Manus portal equivalent |
|---|---|
| The Theatre — 15 films, click to play; YouTube embeds; Extended productions | Sovereign Cinema |
| ScrollSoul — the catalog, verified (Spotify links) | Music pages |
| Chess Arena — playable on the page | OmniChess |
| The Vault Library (9 books) | Sovereign Library / books |
| The two jewels — free forever | Consciousness Mirror + Code of Tawhid |
| Dreams — the key | Dream book |
| The Walls — the visual series (NŪR Cities + films) | Lookbooks / visual archive |
| The Store — 10 products, verified prices (Shopify) | ScrollShop |
| All outlets — every doorway; Every site, every social — one network | Link hub / network map |
| The contract suite — code in hand | On-chain contracts |
| The AI Legion & Muse the Great | AI Legion (as a record, not live chat) |
| The ScrollVerse Tour — 7 stops | Guided tour |
| Facebook Early Discoveries 2022–2026 | Archive |
| Money routes — stated plainly; World Ledger — the record, double-stamped | Revenue / ledger |
| "What's still gated — nothing hidden" + Contact (mailto) | Honest status + contact |

**What the Atlas does NOT have (the Manus portal had these; the Atlas is a record, not the running system):**
- Login / signup / admin auth (Manus OAuth — dead without Manus; needs a new auth system, a build task).
- Live AI chat (Legion/Council/Twin — Manus Forge LLM; needs an OpenAI-compatible key + provider).
- Database-backed features: Guardian waitlist, Academy enrollments, book purchases, orders, tiers, referrals, CHX reservations, comments, CRM, KYC (schema is in the repo; **every row of live data is in the Manus database** and is lost without an export).
- Stripe checkout + webhook (code survives; the webhook endpoint is set in the Stripe dashboard at a `manusworld-….manus.space` host and must be repointed).
- On-chain staking/exchange/bridge live state (contracts are on-chain and survive; the UI that talks to them lives in the portal repo).
- Image generation, voice transcription, Maps proxy, owner notifications (Manus Forge services).
- The 178 `/manus-storage/*` images + 21 CloudFront images (files are not in the repo; the Atlas sidesteps this with its own local assets — its pages do not depend on them).
- The 18+ satellite `*.manus.space` sites (ScrollPort, ScrollShop, ScrollAtlas, etc.) — separate Manus sites; their links rot when Manus goes. The Atlas links instead to the new artifact sites + GitHub Pages sites (Vault, SovereignHub), which are already independent.

**Bottom line:** the Atlas is a complete, self-contained *presentation* of the whole world — every door, every record, every link verified. It is not the running *system* (no accounts, no payments, no live AI, no database). That split is exactly what makes the two-track plan below work: free the domain with the Atlas now, bring the system back on a Node host next.

---

## 4. The rebuild plan

### Track A — FREE THE DOMAIN NOW ($0): Atlas on GitHub Pages + custom domain

This is the "make Manus look like childsplay" move. The domain serves his own site, free, the moment DNS flips. GitHub Pages is the standing free route — his GitHub already serves `the-gods-vault` and the publishing registry on Pages.

**Phase A1 — Package the site (agent work, no Chais needed except the call in §5.2)**
1. Confirm which Atlas file ships: the tech-edit build (re-shared 20 Nov ~19:51 EST) is the live artifact — verify the on-disk source at `~/workspace/ts-spaces/super-scrollverse/index.html` matches it (versions v5–v9 exist under `~/workspace/space-versions/super-scrollverse/`; the shipped version must be named, not assumed).
2. Fold in the "beyond" content (Track C) *before* the first publish if Chais wants the freed site to launch already-beyond, or ship the Atlas as-is and add Track C in a second push — his call (§5.2). Do not hold the domain hostage to Track C; the Atlas alone is already a complete site.
3. Package as a Pages repo: `index.html` + `assets/` at the root, plus a `CNAME` file containing `scrollverse.co`. No build step (static single file). Confirm no other external dependency besides Google Fonts.
4. Create the repo under `chaishillomnitech1` via the browser (the GitHub connector cannot create repos). Suggested name: `scrollverse-co` — his call. Push the tree via push-files (NUL-delimited manifest, UTF-8 only, no binaries problem here — the assets are JPGs, which push-files **cannot** push; binaries go via the GitHub web UI, as the Vault art did on 20 Nov). Verify the repo head commit.

**Phase A2 — Point the domain (needs Chais — §5.1)**
1. In the GitHub repo: Settings → Pages → Custom domain → enter `scrollverse.co` → save. GitHub will show the DNS records it expects and will issue/renew the HTTPS certificate automatically (Enforce HTTPS — tick it once the certificate is live).
2. At the registrar (Global Domain Group DNS panel): set the apex A records to GitHub Pages' IPs and a `www` CNAME to `<user>.github.io` — the exact values come from GitHub's Pages setup screen at the time (do not hard-code them here; they are GitHub's published values). Remove/replace the current A record (`104.18.26.246`, the Manus front). TTL is 60s, so the flip — and the rollback — are fast. Leave every other record untouched (there are no MX/TXT records to preserve).
3. Wait for DNS propagation + GitHub's certificate (usually minutes, can take up to ~24h for the certificate on first setup — do not call it done until HTTPS serves without a browser warning).

**Phase A3 — Verify live (read-back, not assumption)**
1. `https://scrollverse.co/` serves the Atlas homepage with its real title; `https://www.scrollverse.co/` the same; spot-check the Theatre, Vault Library, Store, and one outbound link each (Vault site, Shopify, Spotify).
2. Confirm the Manus suspension page is gone from both hosts and that no mixed-content warnings appear.
3. Record the cutover in the stamp ledger / deployment record with the commit SHA + verification time.

**Phase A4 — What happens to Manus after**
1. **Do NOT cancel Manus first.** Keep the Manus deployment and subscription untouched until the cutover is proven (24–48h of clean running) — the exports in §4 Track B need Manus up.
2. After the site is proven live on Pages, decide on Manus cancellation separately, with Chais. Note: the annual Pro plans run to Apr 2027 (partially refunded); cancellation terms and any remaining value are **unverified** — do not promise a refund.
3. `scrollatlas.lol` stays Manus-hosted until/unless its content is re-homed; it is not part of this cutover.

### Track B — RAISE THE PORTAL BACK (later, not free end-to-end): scrollverse-web-app on a Node host

The full system returns on a long-running Node host. This is the 17 Nov verified recipe (`deployment.md` §5) — do not re-derive it, execute it. **Honest cost note:** this track is not $0 end-to-end. GitHub Pages (Track A) is $0. The portal needs (a) a host, (b) a database, (c) an LLM key. Render's free tier is $0 (spins down after ~15 min idle — the same free tier chosen tonight for the three Replit Node apps); Railway is ~$5/mo hobby after trial credit (the 17 Nov recipe's primary — it is the better host, it is not free). TiDB Cloud / MySQL free tiers exist for the DB. An OpenAI-compatible LLM key is pay-per-use — there is no free unlimited AI. Present the choice to Chais; do not silently pick a paid tier.

**Prerequisites (in order):**
1. **Exports while Manus is still up (time-sensitive, needs Chais's Manus access):** full MySQL dump (114 tables + rows); the 178 `/manus-storage/*` + 21 CloudFront asset originals (from Manus / his own copies — phone, Meta AI artifacts); the full secret list from Manus project settings (there is no `.env.example` — every value lives only there). Without the dump the relaunched site starts with zero users/orders/tiers; without the assets the homepage and galleries render broken; without the secrets payments/email/storage/chains stay dark.
2. **Repo fixes (small, agent work with repo write access — not yet pushed anywhere):** delete the duplicated line 2 of `drizzle/0036_nappy_cargill.sql`; add a migration creating `seerah_quiz_scores`, `think_space_posts`, `think_space_comments`, `think_space_likes`; optionally remove the unconditional `vitePluginManusRuntime()` import from `vite.config.ts` and retest `pnpm build`.
3. **Fresh clone + re-verify the build:** the repo HEAD has moved since the 17 Nov test (`d8ce881` → `0ecc39ca`, 19 Nov 2026, "Referral: attach Muse invite code L9VEVY to Every door section"). Re-clone, `pnpm install --frozen-lockfile`, `pnpm build` must exit 0 again before any deploy. Deploy on Node 22 (repo target; Node 24 worked in the test but is not the target).
4. **Host + DB in his name:** Render free tier (primary for $0) or Railway (primary for quality, ~$5/mo). Database: MySQL 8 or TiDB Cloud. Build `pnpm install --frozen-lockfile && pnpm build`; start `pnpm start` (server binds `0.0.0.0:$PORT`). Boot needs at minimum a non-empty `STRIPE_SECRET_KEY` (empty crashes the boot — a placeholder boots, real calls fail later). Set `DATABASE_URL`, `JWT_SECRET` (recovers existing sessions if the dump was restored), `VITE_APP_ID`.
5. **Auth rebuild (a build task, not a config change):** Manus OAuth is dead — a new auth system (own JWT/email auth, Auth.js, Clerk, etc.) before promising login/signup.
6. **AI swap:** point `BUILT_IN_FORGE_API_URL` at an OpenAI-compatible endpoint + real key (chat-completions path is a plain swap in `server/_core/llm.ts`). Image gen / voice / Maps / notifications need separate providers + small code changes — not a base-URL swap.
7. **Stripe webhook repoint** in the Stripe dashboard to `https://scrollverse.co/api/stripe/webhook` with a fresh signing secret in `STRIPE_WEBHOOK_SECRET`. Until done, Checkout charges go through but orders/tiers/rewards silently stop recording.
8. **Verify on the host's own URL first** (homepage 200 with real title, a login-free tRPC read, webhook endpoint answering 400-without-signature, Socket.io handshake 200) — then, and only then, move `scrollverse.co` DNS from the Pages records to the host (the 17 Nov cutover plan §5 already covers this flip + rollback; the Pages site stays as the instant fallback).

**Known limits of Track B even when done:** login stays dead until the auth rebuild lands; AI stays dead until a key is pointed at it; the 178 + 21 images stay broken until the originals are re-hosted; the 18+ satellite links stay dead; DB features start empty unless the dump was restored. The cutover restores the site, the pages, the on-chain reads, the embeds, Socket.io and the cron — it does not by itself restore users, orders, login, AI, or the images.

### Track C — BEYOND (what makes it exceed Manus, not merely replace it)

Fold the already-built "beyond" material into the freed site — this is the content the Manus version never had:
- The Beyond site content (`scrollverse-beyond-site` goal): Tawhid foundation, Consciousness Mirror, visual series, music catalog, seven-stop tour, rap group, cartoon, podcast, **New Dominion — Living Archive** (10 images Chais sent + 58 dated Facebook discoveries 2022–2026 being fed in).
- The 7-page plan (`new-site-plan-2026-11-16.md`): home (NŪR Cities hero), music (one track a day, Spotify per track), watch/listen (cartoon pilot + podcast pilot + rap group), tour, mirror (Jewels 1 + 2), Legion, store/support (payment route Chais chooses — **not Stripe-only**; the Stripe hold is the reason).
- The Sovereign Archive Chronicles expansion pack (20 Nov): purpose, world-bible, characters, season one — the living archive made into episodes.
- The Atlas's own "What's still gated" honesty stays: nothing hidden, nothing claimed that isn't live.

Track C is content work on the static site — it rides Track A's free hosting. It does not need Track B.

---

## 5. What is needed from Chais — the short list

**For Track A (free the domain now):**
1. **Registrar / DNS access — who holds the Global Domain Group account?** The DNS panel login is needed to repoint the A records. Unverified whether he holds it himself or someone else does. If he does not hold it, say who does — nothing can move without that access.
2. **Go-ahead on this plan + which build ships first:** the Atlas as-is, or Atlas + Track C content in the first publish? (Do not hold the domain hostage to Track C — the Atlas alone is a complete site.)
3. **Repo name for the Pages site** (suggested: `scrollverse-co`) — his call. The GitHub connector cannot create repos; creation goes through the browser.

**For Track B (the portal — later):**
4. **A hosting account in his name** (Render free tier for $0, or Railway ~$5/mo for quality) + a MySQL 8 / TiDB Cloud database + a payment method for the host if a paid tier is chosen. No deploy can happen without an account only he can create.
5. **The Manus exports while Manus is still up:** DB dump, 178 + 21 asset originals, full secret list — needs his Manus access. Time-sensitive: Manus could go further dark, and none of it is recoverable afterwards.
6. **Auth + AI decisions:** new auth system (his pick of approach) and an OpenAI-compatible LLM provider + key (a cost decision — pay-per-use, no free unlimited tier).
7. **Stripe dashboard access** for the webhook repoint + new signing secret (Track B only).

**Standing (no action, recorded):**
8. **Manus cancellation is a separate decision, after** the cutover is proven (24–48h clean running). Do not cancel first.
9. **The "five directions" and ownership-change claims** stay as his account, not verified fact — nothing to do, just do not assert them as proven.

---

## 6. Honest flags — what cannot be verified

- **Domain ownership / registrar access:** unverified (no whois run, no registrar account inspected). The nameservers prove the DNS host, not who holds the login.
- **Manus subscription state:** the billing picture above is from Gmail as of **17 Nov 2026** — three days old. No fresh Gmail check was run in this task. The suspension page is confirmed live tonight, but whether new charges, refunds, or ownership notices arrived since 17 Nov is **unknown**.
- **Whether the Manus project is still accessible** for the exports (DB dump, assets, secrets) is **unverified** — the site is down; the project dashboard state was not checked (that needs his Manus sign-in).
- **Repo HEAD moved** since the verified build: `d8ce881` (14 Nov) → `0ecc39ca` (19 Nov). The build must be re-verified on the new HEAD before any Track B deploy; the 17 Nov proof does not automatically cover the new HEAD.
- **Which Atlas version ships:** versions v5–v9 exist on disk; the live artifact is the tech-edit build re-shared 20 Nov ~19:51 EST. The shipped file must be confirmed as that build, not assumed.
- **Google Fonts CDN** is the Atlas build's one external dependency (free, but not self-hosted). If it ever fails, the site still renders (fallback fonts) — noted, not a blocker.
- **scrollatlas.lol** remains Manus-hosted and Manus-dependent; its future is tied to Manus unless its content is re-homed.
- **Vercel is not a fallback for the portal:** serverless cannot run the persistent Express + Socket.io + cron process; and Vercel project creation is recorded as blocked by an account-level restriction, with Vercel billing failures in May 2026 (separate card). Vercel is correct only for the satellites (`scrollverse_commerce`, `Infinite-Nexus-ScrollVerse`).
- **No credential, card, or secret values** are in this plan. The investigation files note locations only. Nothing here is legal, tax, or financial advice.

---

## 7. Sequence (order only — no dates promised)

1. Chais answers §5.1–5.3 (registrar access, ship-as-is vs +Track C, repo name).
2. Package the Atlas (A1) → create repo + push (browser) → Pages custom domain (A2) → verify live (A3).
3. Track C content folded in (second push) — the site is already live by then, so this is additive, not blocking.
4. Manus exports (§4 Track B prerequisites) — in parallel, while Manus is still up.
5. Track B: repo fixes → fresh build verify → host + DB → env + secrets → auth + AI → Stripe repoint → verify on host URL → DNS flip from Pages to host (Pages stays as instant fallback).
6. After 24–48h clean running on the host: Manus cancellation decision, separately.

---

## Sources

- Live checks 20 Nov 2026 ~20:26–20:30 EST: `browser.open` on `https://scrollverse.co` (Manus suspension page); DNS-over-HTTPS (Cloudflare + Google) for A/NS/SOA; `curl` on `https://scrollatlas.lol/` (200, 10,702 bytes) and `https://manusworld-jl8njwlb.manus.space/` (200, 21,374 bytes).
- `~/workspace/scrollverse-independence/investigation-site-and-billing.md` (17 Nov 2026) — DNS via DoH, live-site table, Gmail billing investigation (38 failed attempts, $600 paid / $349.94 refunded, locked card, ownership-change search, "five directions" verdict).
- `~/workspace/scrollverse-independence/investigation-source.md` (17 Nov 2026) — 7 repos cloned; `scrollverse-web-app` identified as the site; Manus-dependency map; what breaks if Manus disappears.
- `~/workspace/scrollverse-independence/deployment.md` (17 Nov 2026) — real clone, `pnpm build` exit 0, local serve verified with/without MariaDB; Railway-primary / Render-fallback recipe; the two repo bugs; Stripe webhook repoint; DNS cutover plan.
- `~/workspace/scrollverse-independence/scrollverse-independence.md` (17 Nov 2026) — consolidated verdict + §5 DNS cutover plan awaiting approval + §6 consolidated needs.
- `~/workspace/scrollverse-independence/harvest-account-info.md` (17 Nov 2026) — entities, Vydia catalog, accounts/billing (96 repos + Gmail).
- `~/workspace/ts-spaces/super-scrollverse/index.html` + `assets/` — the Atlas build (verified tonight: 0 Manus refs, 24/24 local assets present).
- `~/workspace/social/connect-2026-11-20/connect-map.md` — the 12 artifact sites + Vault site + socials (all re-shared 20 Nov; read-back still owed on the rendered pages).
- `~/workspace/goals/super-scrollverse-site/GOAL.md`, `~/workspace/goals/scrollverse-co-independent-of-manus/GOAL.md`, `~/workspace/goals/scrollverse-beyond-site/GOAL.md`, `~/workspace/new-site-plan-2026-11-16.md`.
- GitHub API, 21 Nov 2026 ~01:30 UTC: `scrollverse-web-app` latest commit `0ecc39ca` (19 Nov 2026).

## Module inventory — Chais's map (20 Nov ~20:29 EST, his record of the Manus portal)

Main portal https://scrollverse.co — sovereign front door (ScrollVerse Trinity overview, $LONDC, 144,000 Guardians, Book of Life). 12 modules, each its own world:
1. /site-map — full navigation/overview
2. /omni-chess — OmniChess (interactive board, AI opponents, $LONDC wagering) — NOTE: /omni-chess is EXCLUDED from the active surface per the OmniLand record (excluded as the wagering surface); Chess Arena is the playable game. The module as a page exists in his map; wagering stays excluded.
3. /sacred-frequencies — Sacred Frequencies (Quranic biofield tools, 963Hz/528Hz/432Hz)
4. /zernio-distribution — Zernio Distribution (sovereign social platform)
5. /red-diamond-fleet — Red Diamond Fleet (vehicle navigation & frequency shield)
6. /knicks-nft — Knicks NFT / related collection
7. /manifest — Manifest / core declaration
8. /chxtoken — CHX Token (utility token details)
9. /crypto — Crypto / pure sovereign flow
10. /library — Sovereign Knowledge Vault (scrolls, doctrines, PDFs, audio)
11. /global-map — Global Empire map (regions, metrics)
12. /codex-1587 — The 1587 Codex (ancient wisdom / legacy)

STATUS: these are the modules as the Manus portal had them. The assessment verified 20 Nov ~20:30 EST that scrollverse.co is DOWN (Manus suspension page only, zero ScrollVerse content) — the module URLs serve nothing today. The inventory is the Track C scope for the freed site: the rebuild must carry these modules back, free, and beyond.

## Module source map — where each module lives in git (20 Nov ~20:35 EST)

Full table: [module-source-map-2026-11-20.md](sandbox://workspace/goals/super-scrollverse-site/module-source-map-2026-11-20.md) (read-only hunt, no changes). Headline: **all 12 modules live inside ONE repo — `chaishillomnitech1/scrollverse-web-app`** (HEAD `0ecc39ca`, 19 Nov 2026). No standalone repo exists for any single module. **FOUND 10:** site-map, omni-chess (wagering UI excluded — strip the $LONDC wager tiers), sacred-frequencies, zernio-distribution, red-diamond-fleet, manifest (route `/manifest` → `MajesticAnchor.tsx`, not `Manifesto.tsx`), chxtoken, library, global-map, codex-1587. **PARTIAL 2:** knicks-nft (only a rights-review page exists — no collection/mint in git) and crypto (CryptoHub is a readiness page — no live function). **Static-only 7** (ship free on Pages): site-map, sacred-frequencies, red-diamond-fleet, manifest, global-map, knicks-nft, crypto. **Server + DB 4** (Track B): zernio, chxtoken, library, codex-1587 (+ Stripe for codex-1587). **Server + Socket.io 1:** omni-chess. No module page references `/manus-storage` or CloudFront assets. Zernio + RedDiamond also exist in the sibling fork `scrollverse-platform`. `scrollverse-portal` is a 4-file placeholder, not a build.

## Full extraction — totality (20 Nov ~21:00 EST)

Execution record: [extraction-totality-2026-11-20.md](sandbox://workspace/goals/super-scrollverse-site/extraction-totality-2026-11-20.md) (Chais's order 20 Nov ~20:42 EST: "extract scrollverse.co in totality… take manus power away where the billing cant effect us"). Headline: **inventory complete — code fully out, data/images/secrets still only in Manus** (live DB rows for 114 tables, 178 `/manus-storage` + 21 CloudFront images, full secret list — none on disk; pull instructions in the record). **Static client build BLOCKED** — the fresh clone at HEAD `0ecc39ca` failed a system execution-risk check, so installing deps and building needs his explicit go-ahead (exact plain-words question in the record §2.2). The wagering strip is fully specified (7 exact edits in `OmniChess.tsx`, verified by reading at the new HEAD). Pages tree prepared (`extraction-2026-11-20/pages-tree/` — CNAME, .nojekyll, manifest script, assembly README); push still gated on his GitHub App installation tap (403 on new repos). DNS flip + rollback written, **not executed**. Atlas remains the ready-now fallback if he wants the domain live tonight without waiting on the build go-ahead.

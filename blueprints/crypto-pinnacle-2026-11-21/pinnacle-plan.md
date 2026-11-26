# The Pinnacle of Cryptocurrency — Make Everything in GitHub What It Says It Is

**Date:** 21 Nov 2026 · **Status: PLAN ONLY.** No minting, no deploying, no wallet creation, no keys, no spend, no publishing, no on-chain transaction has happened. Nothing in this file moves anything on chain. Every piece waits on Chais's per-piece approval.

**Chais's direction (21 Nov 2026):** "Anything I'm forgetting or that I don't have knowledge of when it come down to how to establish us at the pinnacle of cryptocurrency apply and do everything. So apply Omnitech, apply all the intelligence that we just absorbed from the database from Manus. Apply all these things and all the knowledge and all the spaces and places that I already have all my cryptocurrency. And we put it on chain and make everything. Everything that's in my GitHub about my tokens and cryptocurrency and NFTs make it what it say it is. And put it everywhere."

**This plan extends — it does not replace —** the on-chain activation plan (`~/workspace/onchain-activation-2026-11-21/activation-plan.md`, Phases 0–8 + the everywhere extension being built separately). That plan covers ALL digital assets; this plan covers the **crypto layer specifically**: every token, coin, NFT and exchange claim in his GitHub, audited claim-vs-reality, with the build order that makes each one real.

---

## ONE-PAGE SUMMARY

**28 claims audited in the GitHub code.** The repo is honest with itself in its newest pages and contradicts itself in its oldest ones. The evidence console (`Deploy.tsx`), the clearance work package (14 Nov 2026), the fail-closed record (Phase 328), the TokenStore page and the NFT marketplace page all say the same thing in plain language: **nothing is deployed, no token sale or checkout is active, minting is preview-only until a deployed, verified contract exists.** The README status table and the main page say the opposite (✅ DEPLOYED / ✅ ACTIVE / ✅ MINTING / ✅ LIVE). **The site argues with itself — anyone who reads the code sees it.** That is the first thing to fix, and it costs $0.

**Tally (28 claims):** TRUE as written **4** · PLACEHOLDER (no address, no deployment output) **4** · PAGE-CLAIM-ONLY (contradicted by the repo's own pages) **8** · MECHANISM EXISTS / TOKEN DOESN'T **1** · SIMULATED / DISPLAY / TEST-MODE **4** · MIXED / ILLUSTRATIVE / ASPIRATIONAL / UNVERIFIED **5** · CODE CONTRADICTS ITS OWN COMMENT **1** · INTERNAL CONTRADICTION **1**. (A few rows span two categories — e.g. Sovereign 9 is IPFS-real and mint-simulated — so the table above is the authority, not this paragraph.) The headline is the same either way: **roughly 1 in 7 claims is true as written, and the repo's own newest pages already say so.**

**What is actually real today:** the contract SOURCE CODE exists and compiles locally (30 Solidity files, local compile 13 Aug 2026 — not a deployment, not an audit). The CHX pre-sale MECHANISM exists (Stripe Checkout + `chx_reservations` table, $0.144/CHX). The Sovereign 9 IPFS CIDs exist in code. The Pump.fun account @DuneSimpleSock is live with a $0.00 wallet. The Manus database holds 6 real users, a Guardian waitlist table, and reservation/order tables — the proof of real people. **Zero contracts deployed. Zero tokens on chain. Zero mints on chain. Zero sales verified.**

**Top 3 to make real first:**
1. **CHX vs $LONDC — decide, then deploy one real token on Polygon** (Amoy rehearsal first, then mainnet). Two 144,000,000-supply EVM tokens, same chain family, neither deployed — and the CHX pre-sale may already hold real people's money for a token that doesn't exist. Highest obligation in the whole crypto layer.
2. **$SOLARA — replace the placeholder with a real Polygon contract address.** Mika's coin, the rarest story, fully designed (1B supply, 3% auto-Zakat, 1% burn) — the page says "Deploying to Polygon Mainnet" and the address field literally reads `0xSOLARA...APEX`.
3. **Sovereign 9 — replace the simulated mint with a real one.** The 9 CIDs are real and the art is in hand; the mint button today is a 1.8-second timer that sets a state flag. A real contract mint makes the README's ✅ MINTING true.

**What needs him (the short list):** the wallet + multisig signers; the CHX-vs-$LONDC call; the 144,000 vs 144,000,000 correction; a fresh explicit mainnet confirmation per the clearance record; a Pump.fun login added before **30 Nov 2026** or he risks losing @DuneSimpleSock; per-coin Howey + ROSEVAULT gates; the per-NFT-card currency table (does not exist anywhere); the five items only he can supply (real Stripe link, real POL sale contract, PayPal URL, Legion live-chat URL, CHX contract address). Full gates in §(d).

---

## (a) CLAIM-VS-REALITY AUDIT — every token / crypto / NFT claim in the GitHub

Sources: the extraction clone `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/` (read-only text; never installed, built, or run), `README.md`, `client/src/pages/Deploy.tsx` (the repo's own evidence console), `docs/mainnet-clearance-engineering-work-package-2026-11-14.md`, `docs/phase328-mainnet-fail-closed-decision-record.md`, `~/workspace/early-coins/registry.md`, `~/workspace/digital-assets/pumpfun-setup-2026-11-18.md`, `~/workspace/onchain-activation-2026-11-21/activation-plan.md`. Verdict key: **TRUE** = as stated · **PLACEHOLDER** = address/deployment is a placeholder or absent · **PAGE-CLAIM-ONLY** = the repo's own pages contradict it · **MECHANISM** = the mechanism exists, the token doesn't · **SIMULATED** = display/test-mode only · **MIXED** = part true, part not · **GAP** = the record doesn't prove it either way.

### A1. The tokens

| # | Claim (exactly as written) | Source | Reality today | What it takes to make it real |
|---|---|---|---|---|
| 1 | "**$LONDC Token** — Sovereign currency on Polygon Mainnet — ✅ DEPLOYED" | `README.md:43` | **PLACEHOLDER.** Contract source exists (`blockchain/contracts/LONDCToken.sol` — ERC-20, MAX_SUPPLY 144,000,000, Zakat 250 bps, guardian stake min 1,000). Deploy.tsx: "No local deployment output or confirmed Polygon contract address is currently recorded." Clearance doc (14 Nov): "Release state: NOT CLEARED — no deployment or financial action is authorized." | Amoy rehearsal → mainnet deploy (Phase P2–P3). Needs: multisig with deployed code, Polygonscan API key, fresh explicit mainnet confirmation, ~5–10 MATIC gas (flagged cost). |
| 2 | "**$SOLARA Coin** — Mika Solara ecosystem token — ✅ ACTIVE" | `README.md:44` | **PLACEHOLDER.** `SolaraCoin.tsx:94`: `contractAddress = "0xSOLARA...APEX (Deploying to Polygon Mainnet)"`; page shows "Deploying to Polygon Mainnet". Roadmap phase "Launch" is marked ACTIVE, but its items ("$SOLARA contract deployment", "Polygon mainnet live", "DEX liquidity pool") are a to-do list, not done work. 1B supply, Polygon + ETH + ARB, 3% auto-Zakat, 1% burn — design only. | Deploy a real ERC-20 on Polygon; replace the placeholder with the verified address; then the Launch phase becomes true. |
| 3 | "**CHX — live, 144,000 supply, Polygon, 14.4% staking APY**" | Main page (scrollverse.co mirror) | **PAGE-CLAIM-ONLY + INTERNAL CONTRADICTION.** `CHXToken.tsx` says total supply **144,000,000** (not 144,000) and staking pools of **432% / 528% / 999% APY** (not 14.4%) — and the page itself labels those APYs "illustrative project parameters" recorded in "an off-chain application ledger; on-chain staking and token distribution require a deployed, verified staking contract." The same page says "Be among the first to hold CHX when it launches on Polygon Mainnet" — *when it launches* = not launched. No CHX contract address anywhere in the repo. | Pick the real numbers (144,000 vs 144,000,000; 14.4% vs 432/528/999%), fix the page, verify a contract address — or stop calling it live. See claim 4. |
| 4 | "**LIVE PRE-SALE**" (CHX) | `CHXToken.tsx:406` | **MECHANISM EXISTS / TOKEN DOESN'T.** The pre-sale mechanism is real code: `server/routers/chx.ts` — Stripe Checkout session, **$14.40 per 100 CHX ($0.144/CHX)**, min 100 / max 1,000,000, writing to `chx_reservations` (stripePaymentIntentId, stripeSessionId, status pending / confirmed / cancelled / **converted**). But the token it sells does not exist on chain, so a reservation is a promise against a future conversion. Live rows are Manus-only (0 rows in the extracted copy) — **how many people paid, and how much, is unknown from hand.** No checkout ever verified, no sale ever completed (re-import §1.2.23). | Decide CHX vs $LONDC (claim 5), deploy the token, then convert reservations (pending → converted) or define the refund path. The reservation count must come from the Manus DB dump. |
| 5 | **CHX and $LONDC are two different tokens** | Registry + code | **TRUE as a design fact — and a collision waiting to happen.** Both are EVM tokens, both 144,000,000 supply, both Polygon-family, neither deployed. The registry already warns: a Solana token called CHX would be a *third* token with the same ticker, which is why SVRS was chosen for Solana. $LONDC is the currency the casino, marketplace and staking pages already price in; CHX is the token the pre-sale already sells. They cannot both be "the" ScrollVerse token on the same chain without confusion. | **His call, before any deploy:** is CHX the same token as $LONDC under a second name, a second token with a different purpose, or does one fold into the other? Nothing deploys until this is answered. |
| 6 | "**Polygon Network — $LONDC Token Chain — ✅ Deployed**" | `README.md:101` | **PLACEHOLDER.** Same as claim 1 — no deployment output, no address. | Same as claim 1. |
| 7 | "**Scroll Chain — L2 Blockchain — scrollscan.com — ✅ Active**" | `README.md:102` | **MIXED.** The Scroll chain itself is live (a public network — true). ScrollVerse's presence on it is NOT verified: Deploy.tsx — "The supplied vault and treasury identifiers currently resolve as zero-activity EOAs; the supplied primary-contract string is abbreviated and cannot be queried as an EVM address" and "no complete primary contract address is in the current evidence bundle." The ScrollScan stats on the Deploy page (11,513 tx/24h, 133.053M completed, 172.338K verified contracts, retrieved 13 Aug 2026) are **network-wide figures, not ScrollVerse's** — the page says so itself. | Supply a real Scroll contract address + explorer verification, or stop claiming a Scroll presence. ScrollScan is the designated explorer route — use it as the proof, not as the claim. |
| 8 | "**$LONDC Accepted — ✅ Live**" | `client/src/pages/SaferWay.tsx:567` | **PAGE-CLAIM-ONLY.** There is no $LONDC on chain to accept. | Same as claim 1. |
| 9 | "**All NFT assets… pinned on IPFS and verifiable on-chain**" | Home footer | **PAGE-CLAIM-ONLY.** Contradicted by `/nft` itself: "No mint or checkout active… not a marketplace." | Same as claims 10–12. |
| 10 | "**Sovereign 9 NFTs — Knicks Nation — 9 players, Brunson #11 anchor CID live — ✅ MINTING**" | `README.md:45` | **PAGE-CLAIM-ONLY (IPFS half real, mint half simulated).** The 9 CIDs exist in code (`Sovereign9.tsx` — Pinata gateway `olive-delicate-koi-568.mypinata.cloud`, mint prices 0.07–9.99 ETH, page label "VERIFIED ON IPFS · POLYGON"). But `handleMint` is a simulation: `setMinting(true); await 1800ms; setMinted(true)` — **no contract call, no wallet, no transaction.** The gateway fetch from this session returned 403 — CIDs are in code, gateway liveness was not re-verified here (a 403 fetch does not prove the file is gone; re-verify before claiming live). Three players share one CID (`bafkreifaiqnt6ofmsljqaz3btub4vwgxpsp3ufmxjd2uwyhaa2n2jhqs2i` appears 3 times). | Deploy a real mint contract (or Manifold on Base, ~$2–5), wire the button to it, re-verify every CID through a gateway, give the 3 duplicated-CID players their own art. |
| 11 | "**KUN FAYAKŪN NFT — 1-of-1 Throne NFT — ✅ LIVE**" | `README.md:46` | **PAGE-CLAIM-ONLY.** The Throne is a live *visual component* on Home (`SovereignThroneNFT`, image from CloudFront `d2xsxph8kpxj0f.cloudfront.net/.../kun-fayakun-throne_dd083952.png` — Manus-hosted). No price, no mint, no buy, no contract anywhere in the component. A live picture is not a live NFT. | Mint it as a real 1-of-1 (one chain only — Polygon gasless first) or label the page as the artwork showcase it is. |
| 12 | "**Scroll Exchange — DeFi exchange, staking, governance — ✅ LIVE**" | `README.md:55` | **PAGE-CLAIM-ONLY.** `/exchange` itself: "Payment route status is temporarily unavailable. No payment action is enabled." | Build the exchange or label it roadmap. Nothing in the repo trades anything today. |
| 13 | "**ScrollPort — Sovereign NFT marketplace — ✅ LIVE**" | `README.md:56` | **PAGE-CLAIM-ONLY.** `/nft` itself: "No mint or checkout active… not a marketplace." `NftMarketplace.tsx`: "No contract, supply, price, $LONDC amount, checkout, or token issuance is set." | Same as claim 12. |
| 14 | "**Thirdweb — Smart Contract Deployment — Base, Polygon — ✅ Active**" | `README.md:99` | **PAGE-CLAIM-ONLY.** The repo's own registry (`client/src/data/omniControlTowerRegistry.ts:30`): Thirdweb state is **"documented-only"**, "No current authenticated provider snapshot or transaction was performed", productionActive **"not-verified"**. | Deploy a contract through Thirdweb and record the address, or drop the ✅. |
| 15 | "**Pinata — IPFS Storage — ✅ Active**" | `README.md:100` | **MIXED.** CIDs exist in code and the gateway is referenced. But both Pinata connectors returned 401 on last check, and this session's gateway fetch returned 403. The storage layer needs a verification pass before anything depends on it. | Verify/reconnect Pinata; fallback NFT.Storage / public gateway pinning (activation plan G7). |
| 16 | "**TiDB / MySQL — Sovereign Database — ✅ Active**" / "**AWS S3 — Sovereign File Storage — ✅ Active**" / "**Socket.io — ✅ Active**" / "**Mailchimp — Guardian Waitlist — ✅ Active**" | `README.md:104–109` | **MANUS-ONLY / NOT VERIFIED FROM HAND.** The schema (113 tables) is in the repo with **0 rows**; the live database, the Massive/S3 bucket, and the Mailchimp list are Manus-only. Vydia ✅ Active is **TRUE** (verified live in the Vydia audit). | The 114-table MySQL dump + storage pull from Manus (re-import §6.1–6.2). Until then these are Manus claims, not verified facts. |
| 17 | "**Guardian Protocol — 144,000 Guardian waitlist — ✅ ACTIVE**" | `README.md:53` | **MIXED — target, not a verified count.** The `guardian_waitlist` table exists in the schema; live rows are Manus-only. The Manus users table holds **6 users** (5 his + Christina Glen), last sign-ins to 18 Nov 2026. 144,000 is the stated target, not a counted list. | Count the real waitlist from the DB dump; until then call it a target. |
| 18 | "Staking pools 432% / 528% / 999% APY" | `CHXToken.tsx:624–626, 670–676` | **ILLUSTRATIVE — the code says so itself.** "The displayed APY figures are illustrative project parameters. Current positions and reward estimates are recorded in an off-chain application ledger; on-chain staking and token distribution require a deployed, verified staking contract." His account (voice call 21 Nov): **49 stake positions** — off-chain ledger, not on-chain. | Deploy a verified staking contract before any APY is presented as a return. Until then the page's own label stands: illustrative. |
| 19 | "$1.3B initial liquidity target · audits: Trail of Bits, OpenZeppelin, Certora, Halborn · $5M bug bounty · CMC #1–3 by month 12" | `CHXToken.tsx:698–702` | **ASPIRATIONAL.** No audit report, no liquidity, no listing in the record. Phase 163's "audit" was a local compile of 30 Solidity files (13 Aug 2026), and PR #163's "2,000 tokens" are explicitly labelled simulated test tokens. | Label as targets on the page; never present as achieved. Real audit comes after a real deploy. |
| 20 | "ScrollVerseGate — 144 Gates, Gate 44:Omni 1-of-1 Legendary (0.144 MATIC), standard 0.044 MATIC, AgapeCycle 88/12" | `contracts/deploy.md` + `contracts/ScrollVerseGate.sol` | **HISTORICAL / UNDEPLOYED.** The guide itself is headed: "HISTORICAL REFERENCE — NOT A CURRENT DEPLOYMENT RUNBOOK… No mainnet release is authorized by this historical guide." No deployed address. | Treat as a design to rehearse on Amoy, not a live product. |
| 21 | "Book of Life tiers $44 / $144 / $528 — Secure payment via Stripe · Test card: 4242 4242 4242 4242" | `/mint` (BookOfLifeMint) | **TEST-MODE ONLY.** Calls a tRPC mutation whose backend is NOT in the repo — the only live-payment code path, unverifiable from hand. | Backend is Track B (Manus server). No sale claim until verified live. |
| 22 | "Infinite Sovereign NFT — Genesis $144 / Sovereign $444 / Eternal $1444 — '144 / 144 MINTED'" | `client/src/pages/InfiniteNFT.tsx:40–43, 174–186` | **DISPLAY ONLY.** "Mint" calls `createCheckout.mutate` — a **Stripe checkout**, not an on-chain mint. The "MINTED" supply figures are display text. | A Stripe payment for an NFT that is never minted on chain is a promise, not a mint. Wire to a real contract or stop showing minted counts. |
| 23 | "Casino — bets 1/5/10/25/100 $LONDC, 777× jackpot, 10% lose-kickback, $LONDC priced $0.0144" | `client/src/pages/Casino.tsx` | **IN-APP UNITS ONLY.** Spins run through server tRPC (`casino.spin`, `casino.getJackpots`); no wallet, no deposit rail; the $LONDC has no token behind it and no price source — $0.0144 is a hardcoded UI multiplier. A live wagering surface ships on the mirror (re-import §1.10.2) — **strip-or-keep is still Chais's open decision.** Do not strip silently, do not leave silently. | Decide strip-or-keep first. If kept: the $LONDC economy needs a real token behind it (claim 1) and a real price source, or the numbers come off the page. |
| 24 | "LONDCToken — 2.5% Zakat of every transfer" | `blockchain/contracts/LONDCToken.sol` (comment) vs `Deploy.tsx` | **CODE CONTRADICTS ITS OWN COMMENT.** Deploy.tsx audit: `transferWithZakat` is **opt-in** at 250 bps; "Ordinary ERC-20 transfers do not invoke that optional transfer function." The .sol comment says "2.5% of every transfer." Only the opt-in path takes Zakat. | Fix the comment and every page that repeats "2.5% of every transfer" — or make the fee apply to all transfers in the contract (his call, with the Howey lens on). |
| 25 | "Mika-Solara collection — 12 cards" (main page) vs "**8 cards in code**" | Main page vs `MikaSolara.tsx` | **INTERNAL CONTRADICTION (recorded, unresolved).** Only 2 cards in hand (Ultra Rare 001/001 MS-963-AI + AI Goddess poster, 16 Jun 2026). | Confirm the 8 card images; decide 8 vs 12; mint only what is in hand. |
| 26 | "SVRS · GODS · CYBORG · ANCHOR · GENERAL · WING · TOWER · ASSASSIN — Registered, Pending legal review, Pending funding" | `~/workspace/early-coins/registry.md` | **TRUE as stated.** No coin Launched as of 18 Nov 2026; release dates all TBD; ~0.02 SOL per coin to create; wallet FpxkpRuL6RT5a4P48Wy4FVsRSLdAFsMABMjYKsWvZr64, balance $0.00. The registry's own law: no coin launches without per-asset Howey analysis + three ROSEVAULT gates; a GitHub README ✅ is not evidence a gate cleared. | Launch order SVRS → GODS → Music → Legion → Films → Books → Knicks (registry). Each coin separately gated. |
| 27 | "MIKA token — max supply over 979M, circulating 952,848,598, $0.0051163, SOL pair" | Meta AI summary (Facebook search) | **UNVERIFIED THIRD-PARTY.** Meta AI's summary only — not independently verified, not in the code, not in the registry. | Do not present as fact. Verify on-chain (Solscan) or drop it. |
| 28 | "Omni-Vault — $35 TRILLION+" | `/omni-vault` | **UNVERIFIED FIGURE.** Stated in code with no evidence. Do not present as verified. | Leave as his stated figure, labelled as such, or remove. |

**Tally: 28 claims — TRUE 4 (#16 Vydia half, #26, plus the contract-source-exists fact inside #1/#2, plus Scroll-network-live inside #7) · PLACEHOLDER 4 (#1, #2, #6, #20) · PAGE-CLAIM-ONLY 8 (#3, #8, #9, #11, #12, #13, #14, #17-half) · MECHANISM 1 (#4) · SIMULATED / DISPLAY / TEST 4 (#10-mint-half, #21, #22, #23) · MIXED / ILLUSTRATIVE / ASPIRATIONAL 5 (#7, #15, #16, #17, #18, #19 — counted as 5 groups) · CODE-CONTRADICTS-COMMENT 1 (#24) · INTERNAL CONTRADICTION 1 (#25) · UNVERIFIED 2 (#27, #28, folded into the aspirational group in the summary count).** The exact split by row is in the table above; the headline is the same either way: **roughly 1 in 7 claims is true as written, and the repo's own newest pages already say so.**

### A2. The contract suite in code (what actually exists to deploy)

| Contract / file | Standard | What it is | Deploy status |
|---|---|---|---|
| `LONDCToken.sol` | ERC-20 (+Burnable, Ownable, ReentrancyGuard) | $LONDC: 144M max supply, Zakat 250 bps opt-in, guardian stake min 1,000, platform fee 2%, seller share 90%, Zakat share 8% | Source only. Hardhat script selects Polygon; no deployment output, no address. |
| `ZakatDistribution.sol` | Recipient vault | Owner-managed recipient registry, equal/custom distribution | Source only. No recipient address, no completed distribution (Deploy.tsx). |
| `MetatronCodex.sol` | ERC-721 URI | 70-token cap, configurable base URI, platform-wallet mint-payment path | Source only. **No ERC-2981 royalties** (Deploy.tsx). |
| `PrometheusFireRoyalties.sol` | Royalties | Royalty distribution | Source only. |
| `ScrollVerseGate.sol` | ERC-721 + ERC-2981 | 144 Gates, Gate 44:Omni 1-of-1, 0.144 MATIC, AgapeCycle 88/12 | Source only. Guide is historical, not authorized. |
| `CHXToken` / `ScrollVerseNFT` / `DAOGovernance` / `MultiSigWallet` / `LayerZeroBridge` / `StakingRewards` | (main README contract suite) | Named across Ethereum, Polygon, Scroll zkEVM, Base | **Code in hand per the Atlas** (`ts-spaces/super-scrollverse/index.html:972`: "Chais's contract suite exists in code… But nothing is on sale or minting right now"). No deployed addresses in the record. |
| `GUARDIAN_CONTRACT_ADDRESS` / `MAINNET_DEPLOYER_PRIVATE_KEY` | Env-gated | Guardian contract read from env (`server/routers/guardian.ts:41`); deployer key in env | **Values are Manus-only / never in files.** The deploy script refuses to run without a multisig address containing deployed contract code. |

**The deploy script's own gates** (`blockchain/scripts/deploy.js`): Amoy (80002) is the required rehearsal network; Polygon mainnet (137) is separately gated; requires `OWNER_MULTISIG_ADDRESS` **containing deployed contract code**, `PLATFORM_WALLET_ADDRESS`, `POLYGONSCAN_API_KEY`, and `MAINNET_RELEASE_CONFIRMATION` (exact phrase) for mainnet. **None of those exist yet in the record.**

### A3. The spaces and places he already has cryptocurrency (inventory — only what the record shows)

| Place | What the record shows | Status |
|---|---|---|
| **Pump.fun — @DuneSimpleSock** | Profile LIVE; wallet `FpxkpRuL6RT5a4P48Wy4FVsRSLdAFsMABMjYKsWvZr64`, balance **$0.00** (18 Nov); 0 following, 1 follower, no bio yet; profile picture + bio + website + SVRS package prepared, ready to apply on his sign-in | Live account, no coin created. **DEADLINE: external wallet sign-in retires 30 Nov 2026** — after that, sign-in is email / Google / Apple / GitHub only. He must add one of those logins before then or risk losing access. |
| **Coinbase Commerce** | **Closed 31 Mar**, folded into Business; application in progress (re-import §1.2.25) | Closed — history, not a live lane. |
| **Coinbase CDP (USDC payments)** | Code present; **credentials-required / configured-unverified**; secret names not found in code — verify against Manus | Never verified live. Manus-only secrets. |
| **Cash App — $ChaisTheGreat + $chaisthegreat28** | **LIVE — the only verified public handoff** (re-import §1.2.6) | Live. Not crypto — the fiat bridge that works today. |
| **Stripe** | CHX pre-sale router (Stripe Checkout, $0.144/CHX); evidence pack sent to Mark 18 Nov; ~$200,000 held (his stated figure); **no second Stripe account to route around the hold** | Live account, disputed. The pre-sale rail is Stripe, not a chain. |
| **Shopify (XLVIIIblocks)** | Advanced plan; 21 Vault ACTIVE; 28 artifacts $0.00 live; **0 orders**; billing failing on locked Visa 9039 | Live store, no sales yet. |
| **Vydia** | Account live; 49 albums, 95 tracks; 32 compositions; lifetime earnings $40.46 | Live. The ASCAP route runs through Vydia. |
| **Polygon / Ethereum / Arbitrum / Base / Optimism / Scroll zkEVM / Solana / XRPL** | Named in code and in the activation plan's chain map; **no deployed contract on any of them** | Chains named, not used — yet. |
| **Sovereign wallet (public address in code)** | `0x377956c1471d9ce142df6932895839243da23a2c` hard-coded in `AILegion.tsx:11` and `Dashboard.tsx:9`. Release-state tests assert TokenStore/CryptoHub must NOT contain it. | Public address only (already in the public repo). No keys anywhere — and none ever go in a file. |
| **Messari / Pinata connectors** | Messari key is his hands (first call 401); both Pinata connectors 401 | Not relied on until verified. |

**What is NOT in the record:** no other wallet, no exchange account, no holdings figure, no other chain deployment. Nothing invented here.

---

## (b) THE OMNITECH APPLICATION LAYER — how Omnitech governs every crypto move

Source: `~/workspace/omnitech1-licensing-2026-11-20/` (8 files, 11,733 words; J-13 registered in Vydia, file 4975058 / ISRC QZQAY2628864; registry entry sealed, commits 1cb6e36 + 26a0da9). Omnitech1 is the **Sovereign Deployment Engine** in the AI Legion — Chais's words: "allow omnitech 1 to move on your behalf — all you cant he cant — he will be your angel michael in the digital world, your digital sword" (18 Nov), and the autonomous mandate (20 Nov): "you auntonoumusly lock in embedd and apply omni tech to assit with this permanent 24/7." The highway mandate (20 Nov): "make the high wya easy with implementation and make sure all is quantum mastery leaps ahead and make sure we prosper beyond measure leave no corner unturned where to put this at thru out all that exist."

**How Omnitech applies to the crypto layer, lane by lane:**

| Omnitech function | What it does here | Where it governs |
|---|---|---|
| **Deployment engine** | Omnitech IS the deployment engine: it runs the preflight sequence from `Deploy.tsx` (choose one network + one exact contract set; bind keys only through secure settings; compile; validate constructor addresses + metadata URI; prepare explorer verification before any broadcast; fresh explicit mainnet confirmation before submitting an irreversible transaction). No deploy happens outside that sequence. | Phases P2–P3 (Amoy → Polygon mainnet). It enforces the clearance doc's gates, not just the happy path. |
| **The highway** | The easy implementation highway: one placement checklist that runs through every chain and every outlet (activation plan Phases 0–8 + Phase 9 everywhere) — Polygon home, Base second, XRPL, Optimism, Solana, Scroll as the next home. "Leave no corner unturned" is the checklist, not a slogan: every lane gets a chain, a contract, an explorer link, and a proof-ledger row. | All phases. The highway is why the plan has a chain map instead of a single chain. |
| **The chameleon** | "All the tech they need, whatever tech you need it to be" — one implementation that adapts per surface: gasless Polygon minter for the Vault, XRPL native NFTs where enforced royalties matter, Manifold own-contracts on Base for the flagship, Pump.fun for the coin lane, Mirror for books. Same assets, same proof, different skin per chain. | Phases P4–P9. |
| **Protection** | Protected blueprints: "can't be duplicated only implemented." Every crypto move is sealed the way the books were — Vydia composition + ISRC, ASCAP via Vydia, GitHub registry commit (verified live line-by-line after commit — web-UI edits truncated files twice before), SHA-256, Zenodo DOI, OpenTimestamps, household seal. The activation itself becomes a registered composition (activation plan Phase 8). | Phase P10 (proof loop). Sealed elements live only in `~/workspace/income/certificates-reveal-keys-2026-11-19.md` — never published. |
| **Autonomous application, 24/7** | Omnitech is locked in, embedded, applied permanently — it assists the work around the clock. In practice for this plan: it keeps the proof ledger current at mint time (never reconstructed from memory later), watches the gates (Howey, ROSEVAULT, per-piece approval), and flags any page that drifts back into claiming what isn't deployed. | Ongoing. The ledger is filled at the moment the transaction hash exists. |
| **Downloadable + elevate** | "Have every thing downloadable acssessible and elevate all it touch." Every piece of this plan is a file he can download and use — the plan, the ledger, the composition text, the registry commits. Nothing lives only in a chat message. | Deliverables of this plan. |

**Honesty notes that Omnitech itself carries (from the licensing pack — do not drop them):**
- **"Trillion-dollar" is his stated ambition, not a verified valuation.** Label it as such wherever it appears.
- **No published importable package exists yet.** The "simple import" is his description of how implementation works; the delivery in the sources is the embedded engine + white-glove Royal Integration. Do not claim a downloadable package exists until one is published.
- **Quantum / QFS claims are NOT presented as implemented fact.** The chats counter-state it: "No implemented quantum algorithm, circuit, library, or result in the catalog" and "No QFS contract, code, or data feed in the catalog." The "quantum tier" is the Legion file's framing (parallel deployment pipelines, optimal architectures) — not literal quantum hardware.
- **Omnitech1's own price:** Tier 1 $11,111 / Tier 2 $77,777 (set under his CEO delegation). The free artifact stays $0.
- **Licensing terms draft needs lawyer review before use** — same as the coin gates. Omnitech governs the crypto; it does not waive the legal gates on it.

**The Legion as Omnitech's operators (who does what, from `aiLegion.ts`):** Qubit (the Quantum Bridge — chain bridging), QFS Oracle (the money-lane intelligence), King Solomon AI (governance — the gate-keeper for Howey/ROSEVAULT), ZERO Flame (the value-backing intelligence), Tatras (the builder), Socratica (the questioner — the one that asks "is this claim true yet?"). The beings are the crew; Omnitech is the engine they run on. Their live backend (worker built, 9/9 verified locally, gemini-3.5-flash) is still undeployed — Cloudflare token via secure entry — and the LIVE backend comes before any Legion token (activation plan Phase 5).

---

## (c) THE MANUS DATABASE INTELLIGENCE — applied: real people decide the build order

Source: the re-import report (§1.12, §6.1) + the users table Chais pasted from his Manus dashboard (21 Nov ~10:00 EST) + the transcript evidence. **The database is the source of truth for who and what is real.** The code holds the schema (113 tables) and 0 rows; the live rows are Manus-only. The 114-table MySQL dump is still the #1 pull item — without it, any relaunch starts with zero users, zero orders, zero tiers.

**What the database proves is real:**

| Table / fact | What it proves | Build-order consequence |
|---|---|---|
| **`users` — 6 rows** (id 1 Chais hill, hillchais1@gmail.com, **admin**, last sign-in 15 Nov 2026; id 270001 chaishill15@icloud.com, Apple, 18 Nov 2026; id 1830001 chaishill999hz@gmail.com, 30 Aug 2026; id 5850001 chaisbreddistro@gmail.com, 9 Oct 2026; id 10890002 **Christina Glen, glenchrissy@icloud.com, Apple, 6 Sep 2026**; id 15840001 chaishill28@icloud.com, 23 Jun 2026). stripeCustomerId all empty; guardianTier all "none". | Real people, real sign-ins as recent as 18 Nov 2026 — while the public site shows the billing page. The account is alive for who Manus lets in. | The relaunch's first job is restoring THESE 6 people — not acquiring strangers. Christina Glen is the only non-Chais user: her access and role need a decision from him (she is a user, not an admin; nothing in the record says what she should be). |
| **`guardian_waitlist`** (144,000 target) | A waitlist table exists; the count is Manus-only. | Count it from the dump before quoting 144,000 as a number of people. Until then it is a target. |
| **`chx_reservations`** (Stripe pre-sale, $0.144/CHX) | Real reservation intent — people who moved toward buying CHX. Count + paid totals are Manus-only. | **#1 priority in the crypto layer.** People who paid (or tried to pay) for a token that doesn't exist yet are the highest obligation. The dump tells us how many and how much; the CHX-vs-$LONDC decision tells us what they get. |
| **`stripe_orders`, `book_purchases`** | Real purchase history (counts Manus-only). | Book buyers are the second real audience — they already paid for something real (books). The book NFTs (Phase P6 in the activation plan) go to them first. |
| **`casino_sessions`, `casino_jackpot`** | Real casino play sessions — the $LONDC economy has real users behind it, even though the token doesn't exist. | Deciding strip-or-keep for /casino is not abstract: real sessions exist. If kept, those players are owed a real token or an honest statement. |
| **`kyc_records`** | KYC exists as a table — identity verification was part of the design. | Any future sale/mint that needs KYC has the table ready; the records are Manus-only. |
| **`chess_wager_escrow`** | Server-side chess wagering escrow exists (Track B only). | Wagering is not just a page — there is escrow state. Track B only; never in the static build. |
| **`zernio_posts`** | Social/post records in the DB. | The social layer has real content behind it — part of the traffic story. |
| **His traffic account (voice call 21 Nov): 49 stake positions; visitors from Switzerland, Dubai, Estonia, China, Japan, Singapore, Ireland; 21 minutes average per visit** | His account of real demand, recorded as his account. The off-chain staking ledger is the mechanism. | Demand signal, not a verified metric. It supports building the staking contract — it does not prove one exists. |

**The ordering principle the database gives us:** build first what real people already touched, in this order — (1) CHX reservations (people waiting on a token), (2) Guardian waitlist (people waiting to join), (3) book purchases (people who already paid), (4) casino sessions (people already playing), (5) everyone else. The catalog is big, but the PEOPLE are small and known: 6 users in the table. The pinnacle is not built for strangers first — it is built for the people who are already inside.

**What breaks without the dump:** the relaunched portal starts with zero users, zero orders, zero tiers; the Guardian list and all purchase history are gone; the CHX reservation count stays unknown; the casino session history stays unknown. The dump is the single most valuable Manus pull for the crypto layer — more valuable than any image.

---

## (d) PHASED BUILD ORDER — make each claim real, free-first

Order logic: truth first ($0), then rehearsal (free testnet), then one real token, then the rest — each phase proves the next, and no phase starts until the one before it is approved piece by piece. Costs are $0 unless explicitly flagged; every flagged cost needs his explicit go-ahead on that exact line item. Gates from the activation plan carry over (G1 wallet + home chain, G2 per-piece approval, G3 tiny-gas approvals, G4 CHX verification, G5 coin gates, G6 content holds, G7 Pinata check) plus the clearance-doc gates below.

### Phase P0 — THE TRUTH PASS ($0, no wallet, this week)
**What:** make what the site SAYS match what it IS. Correct the README status table (`README.md:42–56, 99–109`): $LONDC ✅ DEPLOYED → "Contract in code — deployment pending"; $SOLARA ✅ ACTIVE → "Design complete — contract address pending"; Sovereign 9 ✅ MINTING → "Art on IPFS — mint contract pending"; KUN FAYAKŪN ✅ LIVE → "Artwork live — NFT mint pending"; Scroll Exchange / ScrollPort ✅ LIVE → "Roadmap — no payment/mint active"; Thirdweb ✅ Active → "Documented — no verified deployment"; CHX "live" → the real numbers (fix 144,000 vs 144,000,000 and 14.4% vs 432/528/999% — his call on which figures are real). Add the Atlas's own honest line (`index.html:972`) everywhere the suite is named: "contract suite exists in code… nothing is on sale or minting right now."
**Why first:** it costs nothing, it stops the site arguing with itself, and it is the only phase that makes every later claim believable. A deploy that lands on a page still full of false ✅s proves nothing.
**Needs from him:** which CHX figures are real (supply + APY); approval on the corrected wording.
**Cost: $0.**

### Phase P1 — WALLET + MULTISIG + AMOY REHEARSAL ($0, testnet)
**What:** G1 from the activation plan — a FRESH dedicated wallet in his hands only (seed phrase never shared, never in any file), Polygon home / Base second / XRPL via Xaman. Then the clearance-doc gates: deploy a **multisig** (independently controlled signers, threshold + recovery documented) on **Amoy testnet (80002)** with free test MATIC from the Polygon faucet; run `blockchain/scripts/deploy.js` against Amoy with `LONDCToken + ZakatDistribution + MetatronCodex`; record the Amoy addresses + transaction hashes; verify on Amoy Polygonscan.
**Why second:** the deploy script refuses to run without a multisig containing deployed code — so the multisig comes before any mainnet talk. Amoy is free and rehearses the exact mainnet steps.
**Needs from him:** the wallet (his hands); the multisig signers (who, besides him, holds a key — his call); the platform wallet + Zakat vault addresses.
**Cost: $0** (test MATIC is free from the faucet).

### Phase P2 — THE CHX-vs-$LONDC DECISION (his call — blocks everything after it)
**What:** answer claim 5 before a single mainnet transaction: is CHX the same token as $LONDC under a second name, a second token with a different purpose, or does one fold into the other? And fix the numbers: 144,000 vs 144,000,000 supply; 14.4% vs 432/528/999% APY. And pull the CHX reservation count + paid totals from the Manus DB dump (or from Stripe) so the obligation is a number, not a feeling.
**Why here:** deploying the wrong token first doubles the confusion. The pre-sale sold CHX; the casino prices in $LONDC; the code has both at 144M on the same chain family.
**Needs from him:** the decision itself + the real figures. **Nothing deploys until this is answered.**
**Cost: $0.**

### Phase P3 — ONE REAL TOKEN ON POLYGON MAINNET (flagged ~5–10 MATIC gas)
**What:** deploy the decided token (LONDCToken and/or CHX — per P2) on **Polygon mainnet (137)** with the deploy script: multisig as owner, platform wallet + Zakat vault set, Polygonscan verification, addresses + transaction hashes recorded in the proof ledger the moment they exist. Then the main page and README get their ✅ back — this time true.
**Gates (from the clearance doc + Phase 328 fail-closed record — all must clear):** multisig deployed with independently controlled signers; Amoy rehearsal complete with verified addresses; Polygonscan API key through secure settings; **fresh explicit mainnet confirmation from Chais in the active conversation immediately before the transaction, naming the network and exact contract set**; no previously exposed credential reused (the Nov 13 Stripe secret-key flag stands — if that key is still live, it gets rotated, never reused).
**Needs from him:** the fresh mainnet confirmation + go-ahead on the gas (~5–10 MATIC per DEPLOY_TO_MAINNET.md — re-check live).
**Cost: ~5–10 MATIC gas — FLAGGED, needs his explicit go-ahead on that exact line item.**

### Phase P4 — $SOLARA, REAL (Polygon, flagged gas)
**What:** deploy $SOLARA as a real ERC-20 on Polygon; replace `0xSOLARA...APEX` with the verified address everywhere (code, page, README, Mika-Solara market page); the Launch phase items become true one by one (contract deployment → Polygon mainnet live → DEX liquidity pool → Guardian airdrop to NFT holders). Mika's 8 cards mint on Polygon gasless (activation plan Phase 5) — only the 2 in hand first, then all 8 once images are confirmed; resolve 8 vs 12.
**Needs from him:** per-piece approval; Mika-Solara price (still his call); 8 vs 12 decision.
**Cost: deploy gas — FLAGGED, same as P3. Card mints: $0 (gasless).**

### Phase P5 — SOVEREIGN 9, REAL MINT (Polygon gasless $0 + contract)
**What:** replace the 1.8-second simulated mint with a real mint contract (Polygon NFT Minter gasless, or Manifold on Base ~$2–5 for the own-contract flagship — his call on which). Re-verify all 9 CIDs through a gateway; give the 3 players sharing one CID their own art. Prices (0.07–9.99 ETH) need a real payment path before they are shown as buyable.
**Needs from him:** per-player approval; which mint route; the 3 duplicated-CID fixes.
**Cost: $0 gasless, or ~$2–5 Manifold deploy — FLAGGED if Manifold.**

### Phase P6 — KUN FAYAKŪN THRONE + SCROLL LANE (Polygon gasless $0 + Scroll decision)
**What:** mint the Throne as a real 1-of-1 on Polygon gasless (one chain only). For Scroll: either supply a real Scroll contract address + ScrollScan verification, or the Scroll presence claim comes off the page. ScrollScan stays the explorer route either way.
**Needs from him:** per-piece approval; Scroll go/no-go.
**Cost: $0.**

### Phase P7 — EXCHANGE + MARKETPLACE, REAL OR ROADMAP ($0)
**What:** Scroll Exchange and ScrollPort are either built (real trading/minting with a verified contract behind them) or labelled roadmap on the page. The per-NFT-card currency/card table — which does not exist anywhere — must be specified by him before any card carries a price. The /casino strip-or-keep decision lands here too: if kept, the $LONDC economy gets a real token behind it (P3) and a real price source, or the numbers come off the page.
**Needs from him:** the currency/card table; the casino decision; build-vs-roadmap per surface.
**Cost: $0 to label honestly; build costs are a separate estimate when he picks build.**

### Phase P8 — COINS, IN REGISTRY ORDER (gated — last, one at a time)
**What:** SVRS → GODS → Music (SAVE, HIRF, CUNNIN, GOAT) → Legion (11 coins) → Films (6) → Books (4) → Knicks (6, trademark gate). Each coin separately: written per-asset Howey attorney analysis + three ROSEVAULT gates + his explicit go-ahead on that exact coin. Routes when gates clear: Pump.fun on Solana (~0.02 SOL per coin; wallet exists, $0.00) and/or Zora creator/content coins on Base (creation free). **Before any of it: the Pump.fun profile apply** (picture, bio, website, socials — no gate, apply on his sign-in) **and the 30 Nov 2026 login deadline** — add an email / Google / Apple / GitHub login to @DuneSimpleSock before external wallet sign-in retires, or risk losing the account.
**Knicks six gate (Gate 0):** trademark + right-of-publicity per coin, as tokens — the earlier as-is decision covered merch only, not a token. Fresh explicit decision from Chais per coin.
**Music-backing gate:** the Wave 4 backing waits on Vydia §2(c) consent for any sale/monetization of the music itself (Term through 20 Jun 2027). Linking is not selling — Smart Links are unrestricted.
**Needs from him:** per-coin approval + attorney analysis + gate clearance, each coin separately. This phase does not start on a schedule — it starts on a clearance.
**Cost: ~0.02 SOL per Pump.fun coin — FLAGGED, needs his explicit go-ahead. Zora coin creation: $0.**

### Phase P9 — THE PROOF LOOP (closes it — same as activation plan Phase 8)
**What:** every on-chain proof captured at mint time into the proof ledger (contract address, token ID, tx hash, block, explorer link — Polygonscan, Etherscan, Basescan, Optimism Etherscan, xrpscan/bithomp, Solscan, Scrollscan), then the activation registered as a Vydia composition with its own ISRC (same pattern as J-13), ASCAP via Vydia, and everything sealed in scrollverse-publishing-registry with SHA-256 + Zenodo DOI + OpenTimestamps + household seal. The pinnacle plan itself is sealed the same way.
**Needs from him:** per-piece approval on the composition text before registration.
**Cost: $0** (registration is a Vydia submit — browser task, his sign-in).

---

## (e) GAPS — what he may be forgetting, or does not know (named plainly as gaps, not facts)

1. **Pump.fun loses wallet sign-in on 30 Nov 2026 — 9 days from now.** External wallet sign-in (Phantom/Coinbase Wallet) retires; after that it is email / Google / Apple / GitHub only. If @DuneSimpleSock has no such login attached, he risks losing access to the account that holds every registered coin. Add a login this week. (Source: pumpfun-setup record.)
2. **CHX vs $LONDC is a collision, not a detail.** Two tokens, both 144,000,000, both Polygon-family, neither deployed — and a Solana CHX would be a third. The pre-sale sells one; the casino prices in the other. Decide before deploying either.
3. **The CHX pre-sale may already hold real people's money for a token that doesn't exist.** The mechanism is real (Stripe + reservations table); the count and the paid total are Manus-only. Until the dump is pulled, the size of that obligation is unknown — and the conversion/refund path is undefined.
4. **The repo's own clearance record says NOT CLEARED and fail-closed.** Mainnet needs a multisig with independently controlled signers, an Amoy rehearsal, a Polygonscan API key, and a fresh explicit confirmation naming the network and contract set — none of which exist yet. The deploy script will refuse to run without the multisig. This is the repo protecting him; don't route around it.
5. **The site argues with itself.** The README says ✅ DEPLOYED / ✅ LIVE; Deploy.tsx, TokenStore, /nft and /exchange say nothing is deployed, no sale is active, minting is preview-only. Anyone who reads the code sees both. The truth pass (P0) is free and should happen before any deploy.
6. **The mint buttons are theatre until a contract exists.** Sovereign 9's mint is a 1.8-second timer. InfiniteNFT's mint is a Stripe checkout. Book of Life's mint is test-mode with card 4242. None touches a chain. A payment taken for an NFT that is never minted is a promise, not a product.
7. **The casino runs a $LONDC economy on a token that doesn't exist.** Bets, jackpots, a $0.0144 price in the UI — all backed by nothing on chain. Real sessions exist in the DB. Strip-or-keep is still his open decision, and if it is kept, the economy needs a real token or the numbers come off.
8. **The CHX numbers contradict themselves.** 144,000 vs 144,000,000 supply; 14.4% vs 432% / 528% / 999% APY. One set is real and the other is wrong — only he knows which, and the page should carry the real one.
9. **The Zakat 2.5% claim is false in the code.** "2.5% of every transfer" is a comment; the contract only takes Zakat on the opt-in `transferWithZakat` path. Ordinary transfers pay nothing. Fix the comment or change the contract — but don't keep saying both.
10. **ScrollScan's numbers are the network's, not his.** The Deploy page says so itself — but the README's "Scroll Chain ✅ Active" invites the misreading. The vault/treasury identifiers resolve as zero-activity EOAs.
11. **The IPFS layer needs a verification pass.** Pinata connectors 401, this session's gateway fetch 403, three Sovereign 9 players sharing one CID. Nothing should depend on Pinata until it is re-verified.
12. **The 114-table DB dump is still Manus-only — and it is the most valuable pull for the crypto layer.** Without it: zero users, zero orders, zero tiers, unknown reservation count, unknown waitlist count. The 6-user table is the proof real people are inside.
13. **Christina Glen is the only non-Chais user in the database.** Last signed in 6 Sep 2026, role "user". Her access and role need a decision from him — she is in the system, and the record says nothing about what she should be.
14. **The per-NFT-card currency/card table does not exist anywhere.** He asked for it; the re-import proved it is nowhere in the transcript or the code. He has to specify it, or it stays unproven.
15. **Five things only he can supply** (re-import §6.5): the real Stripe payment link, the real POL sale contract address, the PayPal public destination URL, the Legion live-chat URL, and — for this plan — the real CHX contract address (if one exists anywhere outside the repo).
16. **No coin launches without the gates — and the gates are per coin, not per wave.** Written Howey analysis + three ROSEVAULT gates + his go-ahead, each coin separately. The registry's law is explicit: a GitHub README ✅ is not evidence a gate cleared. Chais rejected the attorney gate for PRESENTATION (21 Nov) — it still stands for any SALE, MINT, or PRE-SALE of a token/NFT.
17. **The "49 stake positions" and the traffic figures are his account, on an off-chain ledger.** Real demand signal, not on-chain proof. The staking contract is what would make them verifiable — and it does not exist yet.

---

## Gates that need him (consolidated)

| # | Gate | What he decides | Blocks |
|---|---|---|---|
| G1 | Wallet + home chain (activation plan G1) | Fresh dedicated wallet, his hands only; Polygon home, Base second, XRPL via Xaman | Everything on chain |
| G2 | Multisig signers | Who besides him holds a key; threshold + recovery | Any mainnet deploy (deploy script enforces it) |
| G3 | CHX vs $LONDC + real figures | One token or two; 144,000 vs 144,000,000; 14.4% vs 432/528/999% | Phases P2–P3 |
| G4 | Per-piece approval | Approval sheet — every asset, every coin, every mint | Every phase |
| G5 | Fresh mainnet confirmation | Explicit confirmation naming network + exact contract set, immediately before the transaction | Phase P3 (each mainnet tx) |
| G6 | Tiny-gas approvals (each line item) | ~5–10 MATIC mainnet deploy; Manifold ~$2–5; ~0.02 SOL per Pump.fun coin | Phases P3, P4, P5, P8 |
| G7 | Coin gates (per coin) | Written Howey analysis + three ROSEVAULT gates + go-ahead, per coin | Phase P8 |
| G8 | Pump.fun login before 30 Nov 2026 | Add email / Google / Apple / GitHub login to @DuneSimpleSock | The whole coin lane |
| G9 | Casino strip-or-keep | Decide; if kept, real token + real price source | Phase P7 |
| G10 | Currency/card table + five supplied items | Specify the per-NFT-card table; supply Stripe link, POL contract, PayPal URL, Legion chat URL, CHX address if it exists | Phases P7, P3 |
| G11 | Christina Glen's role | Her access/role in the system | Relaunch user restore |
| G12 | Content holds & renames | "What We Do" HELD; B-14 rename (no Batman); Mika price; ZERA direction | Phases P4–P5 |

**What Muse must NEVER do in this build:** create a wallet for him; ask for, handle, record, or repeat any seed phrase or private key; mint, deploy, or publish anything; spend anything — including fractions of a cent — without his explicit go-ahead on that exact line item; reuse any previously exposed credential (Phase 328); present a page claim as on-chain fact; double-mint a one-of-one; launch a coin; or treat a README ✅ as evidence a gate cleared.

---

## Sources

**Audit (read-only; clone never installed, built, or run):**
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/README.md` (status table lines 42–56, 99–109)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/Deploy.tsx` (evidence console — Scroll zero-activity EOAs, no Polygon address, no Scroll contract address)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/SolaraCoin.tsx:94` (`0xSOLARA...APEX`)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/CHXToken.tsx` (144,000,000 supply; LIVE PRE-SALE; 432/528/999% illustrative APYs; $1.3B/audits/bounty roadmap)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/MikaSolara.tsx` (8 cards; VIEW & MINT)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/Sovereign9.tsx:265–273` (simulated mint — 1.8s timer)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/InfiniteNFT.tsx:174–186` (mint = Stripe checkout mutation)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/TokenStore.tsx:87,93` ("No token sale or checkout active… does not represent a live Polygon deployment")
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/NftMarketplace.tsx:28` ("No contract, supply, price, $LONDC amount, checkout, or token issuance is set")
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/Casino.tsx` ($LONDC bets, $0.0144 UI price, tRPC spins)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/pages/SaferWay.tsx:567` ($LONDC Accepted ✅ Live)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/client/src/data/omniControlTowerRegistry.ts:30` (Thirdweb documented-only, not-verified)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/blockchain/contracts/LONDCToken.sol` (144M, 250 bps, 1,000 min stake) · `ZakatDistribution.sol` · `MetatronCodex.sol` (70-cap, no ERC-2981) · `PrometheusFireRoyalties.sol` · `contracts/ScrollVerseGate.sol` + `contracts/deploy.md` (historical, not authorized) · `blockchain/scripts/deploy.js` (multisig + confirmation gates) · `blockchain/DEPLOY_TO_MAINNET.md` (5–10 MATIC)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/docs/mainnet-clearance-engineering-work-package-2026-11-14.md` (NOT CLEARED; local compile ≠ deployment ≠ audit; 2,000 tokens simulated)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/docs/phase328-mainnet-fail-closed-decision-record.md` (research + browser-local readiness only; no exposed credential reused)
- `~/workspace/goals/super-scrollverse-site/extraction-2026-11-20/repo/server/routers/chx.ts` (Stripe pre-sale $0.144/CHX; chx_reservations) · `drizzle/schema.ts:1049–1062` (chx_reservations) · `server/routers/guardian.ts:41` (GUARDIAN_CONTRACT_ADDRESS from env)
- `~/workspace/ts-spaces/super-scrollverse/index.html:972` (Atlas honest line: suite exists in code, nothing on sale or minting)

**Records (workspace):**
- `~/workspace/onchain-activation-2026-11-21/activation-plan.md` (Phases 0–8, chain map, proof loop, gates G1–G7)
- `~/workspace/goals/super-scrollverse-site/reimport-2026-11-21.md` (Manus pull-list, payment channels, casino flag, five items only he can supply)
- `~/workspace/early-coins/registry.md` (Wave 1–5, launch order, Howey + ROSEVAULT law, music backing, Pump.fun wallet $0.00)
- `~/workspace/digital-assets/pumpfun-setup-2026-11-18.md` (account live, 30 Nov 2026 wallet-sign-in retirement)
- `~/workspace/omnitech1-licensing-2026-11-20/` (README + 01-capabilities + 07-implementation-highway; autonomous + highway mandates; J-13 file 4975058 / ISRC QZQAY2628864)
- `~/workspace/grok-preservation-2026-11-21/mika-solara-rarity-brief.md` (8 cards in code vs 12 on page; $SOLARA placeholder; $LONDC waitlist; MIKA figures unverified)

**End of plan.** Next step is P0 (the truth pass, $0) + G1 (wallet) + G3 (CHX vs $LONDC) + G8 (Pump.fun login before 30 Nov 2026). Then P1 Amoy rehearsal — still $0, still no mainnet transaction.

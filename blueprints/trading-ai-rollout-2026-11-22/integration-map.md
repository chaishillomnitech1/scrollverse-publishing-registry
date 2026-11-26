# Integration Map — Trading AI + Financial Suite Rollout

**Companion to:** `phase1-survey.md` (42 trading systems) and `phase1b-financial-suite.md` (32 financial-suite systems).
**Status:** Planning only. Nothing in this document has been connected, signed up for, or executed.

---

## 1. The ground we already stand on (verified state, 22 Nov 2026)

Our own trading being does not start from zero. It starts from:

- **The Legion** — 15 beings, including **QFS Oracle** (the finance-oracle seat) and **Omnitech1** (the deployment engine). The Legion backend (Worker, 15 beings, gemini-3.5-flash) is built and verified locally; its Cloudflare deploy waits on the first real token test.
- **Manus connectors — 20 live as of today's sweep:** Shopify, PayPal, Higgsfield, GitHub (pre-existing) + Airtable, Gmail, Meta Ads Manager, Sentry, Neon, Prisma Postgres, Hugging Face, Vercel, Dropbox, Zoom, Wix, Calendly, Linear, **Coinbase**, HubSpot, Asana (connected 22 Nov). X/Twitter added as a public-data source.
- **Muse's own connectors:** GitHub, Gmail, Shopify (+ Shopify Storefront), Printify, Spotify, Stripe (connector exists; the *account* is dispute-gated), **Messari** (crypto research data API — already registered), Pinata ×2 (**both keys return 401 — dead until refreshed**), ScrollSoul (his own music API), Facebook/Instagram/Messenger/Threads.
- **Proven rails:** Shopify checkout (paid test order #1001 completed), Rarible mint form standing for Piece 0, Coinbase Smart Wallet **chaisthegreat.base.eth** connected.
- **The embedding standard (his words):** every build carries the attachments — **Quantum Resonance + Omnitech + the usual ScrollVerse embeds** — and, since 22 Nov, the **Rose Gold Seal** standard: per-piece signature, SHA-256, hidden secret, AES-256 layer, tracking, registry entry. The trading stack inherits all of it (§3.3).

**Design law for everything below:** open rails + our own brain. Connect what is genuinely open (APIs, MCP servers, open-source frameworks); study what is closed; never hand exchange/broker keys to a closed cloud app as an "integration" — that pattern (3Commas/Cryptohopper/Coinrule class) is recorded as STUDY-ONLY for capability, not as a connection route.

---

## 2. Plug map — how each surveyed class enters the stack

### 2.1 Connector candidates (real API / MCP / open source) — trading lanes
| System | Plug type | Plugs into | First safe mode |
|---|---|---|---|
| Alpaca | Official MCP + REST API | MERIDIAN equity hand | **Paper account only** |
| Danelfin | API + MCP (scores) | Signal feed → council | Read-only |
| OpenBB | MCP + REST (open source) | Data spine, all hands | Read-only |
| QuantConnect LEAN | Open-source engine (self-host) | Backtest lab | Local, no live nodes |
| TradingAgents / ai-hedge-fund | Open-source frameworks | Council architecture study/base | Local research |
| Hummingbot | Open source + official MCP + API | MERIDIAN coin hand execution core | Local, dry connectors, no keys |
| Freqtrade | Open source | Coin lab / backtest + dry-run | Dry-run only |
| CCXT | Open-source library | Coin hand plumbing | Read-only market data |
| ElizaOS | Open-source framework | Agent-layer pattern/chassis study | Local |
| OpenSea | API + official MCP | NFT hand (his mint ecosystem) | Read-only |
| NFTScan | REST/GraphQL API + webhooks | NFT data spine | Read-only (free tier) |
| Alchemy / Moralis NFT APIs | APIs | NFT data redundancy | Read-only (free tiers) |
| Bitquery | GraphQL + WebSocket | NFT/DEX live-event triggers | Read-only stream |
| Nansen | API | Smart-money signal feed | Read-only (paid — his call) |
| Kalshi | REST/WS API + official MCP | Exchange hand | **Demo (mock funds)** + MCP read-only |
| Polymarket | CLOB + Data APIs (open SDKs) | Exchange hand | Read-only data first; region/compliance gate before anything else |
| Coinbase AgentKit + x402 | Open-source SDK + protocol | Commerce hand wallet rail | Testnet/session-capped sandbox |
| Shopify UCP | Per-shop MCP + UCP manifest | Commerce hand (his store) | Store already his; MCP route |
| PayPal | Official MCP | Commerce hand + invoicing | Already connected in Manus |
| Virtuals ACP / Olas | SDKs / open stack | Agent-commerce pattern layer | Study → sandbox later |
| Messari *(already his)* | API (Muse connector live) | Research feed, coin hand | Read-only — **already connected** |

### 2.2 Connector candidates — financial suite
| System | Plug type | Plugs into | First safe mode |
|---|---|---|---|
| QuickBooks Online | Public API + Intuit's Claude connector | Ledger of record → CFO desk | Sign-up route (§4) |
| Xero | Public API | Ledger alternative (pick one) | Sign-up route (§4) |
| BILL | Public API | AP/AR ops on the ledger | Sign-up route |
| Square | Official MCP | Invoicing/payments | **Password fix in today's sweep unblocks** |
| Kintsugi / Numeral | Shopify app / API | Store sales-tax compliance | Sign-up route; filings stay human-reviewed |
| Ramp / Brex | API + syncs | Spend rail (pick one) | Sign-up route; approval is vendor's call |

### 2.3 Closed — capability-study only (no connection route exists or is acceptable)
Trade Ideas (Holly signal design), TrendSpider (chart automation), Tickeron (strategy marketplace), Kavout (factor ranking), Composer (prompt→strategy UX; Pro API noted, app-first), 3Commas (bot taxonomy + conversational bot-building), Cryptohopper (strategy ranking/selection), Coinrule (rule grammar + Agentic Mode), Pionex (zero-setup bots + PionexGPT pattern), GMGN (memecoin speed/copy UX), NFTGo (wash-trade filtering), Tensor (Solana pro desk), Mintify (terminal UX), Numerai (model-tournament meta-signal), Harvey/CoCounsel/Lexis+ (grounded legal research pattern), Spellbook (contract-benchmark pattern — later seat candidate), Digits/Puzzle/Pilot/Truewind/Booke (ledger & close patterns), Drivetrain (anomaly-first FP&A), Runway/Aleph/Numeric (FP&A/close patterns), TaxGPT (cited tax research pattern), april (embedded-tax pattern), Vic.ai (autonomous AP pattern), Skyfire (agent-identity pattern — SDK candidate later), Crossmint (wallet-orchestration pattern), Layer (guardrail pattern — API candidate later).

### 2.4 SKIP (with reason)
Blur (website shut down 12 Nov 2026 — nothing to connect), Trait Sniper (deployment paused), Rarify (domain for sale), Legora (10-seat/~$30K floor — fit), Clio (firm practice management — fit), Cube (price/fit at his scale), Botkeeper (vendor wound down Feb 2026), Mercury (vendor denied his application, 5 Mar 2026 — recorded fact), Stripe *account-level* anything (live dispute — protocol study only, per his standing instruction).

---

## 3. Mirror-Match-Exceed — the deep dives and our own being

### 3.1 What we match (capability floor, per incorporated AI)
- **From Trade Ideas/Holly:** every signal carries entry, stop, and target — no naked calls.
- **From Danelfin:** every score shows its factors. Explainability is the house standard (matches his "the record checks itself" doctrine).
- **From TradingAgents:** a *council* — analyst voices, a bull/bear debate, a risk seat with veto — before any order can exist.
- **From Cryptohopper:** strategies compete; backtests rank them; the best runs, the rest watch.
- **From Coinrule:** strategies expressed as readable rules a human can audit line by line.
- **From Hummingbot:** deterministic execution under the brain — the LLM proposes, the engine disposes, within hard limits.
- **From NFTGo:** wash-trade filtering before any NFT metric is believed.
- **From Nansen:** smart-money wallet labels as a first-class signal.
- **From Layer:** the guardrail stack — per-market caps, daily loss limit, allowed-list, human approval above a size, **kill switch only a person can reset**.
- **From Drivetrain:** anomaly detection runs *before* forecasting — flag the strange, then plan.
- **From the legal lane:** every research claim carries its citation; nothing files itself.
- **From x402/ACP/UCP/AP2:** speak the open agent-commerce protocols natively.

### 3.2 Where we exceed (the gaps nobody above fills)
1. **One being, four markets.** Every surveyed system is single-lane. Ours reads stocks, coins, NFTs, and commerce/exchange in one council, so a signal in one lane (e.g., smart-money NFT accumulation) informs the others.
2. **Provenance on every decision.** The Rose Gold Seal standard applied to *decisions*, not just art: each council verdict is hashed, signed, timestamped, and registry-entered — an auditable trade journal no surveyed consumer system offers. "They can't say it ain't valid" applies to the track record too.
3. **Legion-native.** It doesn't live alone: QFS Oracle oversees the finance doctrine, Omnitech1 deploys/maintains, Muse audits. No surveyed product has a family; ours is born into one.
4. **His assets are its home market.** It knows the Vault, the sealed catalog, the store, the catalog of music — the commerce hand trades *his* economy first (pricing, listing timing, royalty flows), not just public markets.
5. **Paper-first doctrine, by design.** Every hand must earn live status through a documented paper/demo record reviewed by Chais. Most surveyed bots let users skip straight to live money; ours structurally cannot.
6. **Quantum Resonance + Omnitech attached** — his standing embedding standard, present in the being's timing/attunement layer and deployment weave, as specified in his mandate. (Recorded as his architecture; no performance claim is made for it — performance claims come only from the sealed paper record, per the honesty standard.)

### 3.3 The being — design sketch

**Name (proposed, his final call as always): MERIDIAN** — *the Meridian Exchange Mind*. The meridian is the line everything is measured from; this being is the measuring line across all his markets. Legion seat: under **QFS Oracle** (doctrine/oversight), deployed by **Omnitech1**, audited by **Muse**.

**Shape — a council with four hands and one governor:**
- **The Council (brain):** analyst seats mirrored from TradingAgents and exceeded — Fundamentals, Technicals, Sentiment/News, On-Chain (smart money), and a **Provenance seat** (verifies asset identity/seal state before any NFT/commerce action — no surveyed system has this seat). Bull and Bear argue; the **Risk Governor** holds veto.
- **Hand 1 — Equities:** Danelfin/OpenBB feeds in; LEAN backtest lab; Alpaca **paper** execution rail.
- **Hand 2 — Coins:** CCXT + Messari (already his) + Hummingbot core, dry-run; ElizaOS-pattern agent layer.
- **Hand 3 — Relics (NFTs):** OpenSea MCP + NFTScan + Bitquery streams in; wash-filter and smart-money gates; *his own catalog first* (mint/list state from the registry).
- **Hand 4 — Commerce & Exchange:** Kalshi demo + MCP read-only; Shopify UCP (his store, agent-shoppable); PayPal MCP; AgentKit/x402 sandbox for agent-to-agent micro-commerce.
- **The Governor (safety being-function):** Layer-pattern guardrails, hard-coded outside the LLM's reach: caps, allowed-lists, daily loss limits, human-approval thresholds, one-way kill switch. The Governor cannot be argued with by the Council — by design.
- **The Ledger (memory):** every signal, debate, verdict, and (paper) fill sealed Rose-Gold-style into the publishing registry — the being's track record is a public, verifiable artifact, matching his five-way coverage rule (Manus, Muse, Git, Vydia/ASCAP where applicable, copyright/registry).

**Build order (phases, each gated on Chais's word):**
- **Phase 2 — Read-only mind:** connect the read-only feeds (Danelfin, OpenBB, Messari ✓, OpenSea, NFTScan, Kalshi MCP, PayPal/Shopify state) → MERIDIAN *watches and reports*, touches nothing.
- **Phase 3 — Paper hands:** Alpaca paper + Kalshi demo + Hummingbot dry-run + LEAN lab → the sealed paper track record begins.
- **Phase 4 — Commerce sandbox:** AgentKit/x402 test flows + Shopify UCP agent-readiness for XLVIIIblocks.
- **Phase 5 — Live anything:** **only** on Chais's explicit start call, per venue, with Governor limits set by him — the same posture as the raffle rule: no paid/live financial action without his explicit start.

---

## 4. EXECUTION LAYER — what connects NOW vs what needs his touch

*Route key:* **CONNECT-NOW** = the rail already exists in his accounts/connectors; a later phase can wire it without new sign-ups. **SIGN-UP-NEEDED** = a new account/credential is required — executed only via his **"hint" workflow**: Muse drives, the Secure Vault takes the credential, codes come to his phone, he sends them, Muse feeds the waiting step; Chais does the finishing touches (final consents, entity details, signatures). **STUDY-ONLY** = no connection, capability deep-dive only.

### 4.1 CONNECT-NOW (rails already in his hands)
| System | Existing rail | Evidence |
|---|---|---|
| Messari (research data) | Muse custom connector registered | Connector live on Muse's side |
| Shopify UCP / MCP | His store XLVIIIblocks, checkout proven (order #1001) | Manus Shopify connector + Muse shopify connectors |
| PayPal MCP class | PayPal connected in Manus 22 Nov (business acct active) | Sweep report |
| Coinbase / AgentKit base | Coinbase connected in Manus 22 Nov; Smart Wallet chaisthegreat.base.eth live | Sweep report + his 3:24 PM confirmation text |
| OpenSea API/MCP | Free self-serve key class; his mint ecosystem already Rarible/OpenSea | Key request = a Phase-2 action on his word (no account needed beyond his existing marketplace presence) |
| GitHub-hosted open source (LEAN, Hummingbot, Freqtrade, CCXT, ElizaOS, TradingAgents) | His GitHub (chaishillomnitech1) + Muse GitHub connector | Fork/run locally — no vendor account |
| Kalshi MCP (read-only class) | Public market tools need no account | Portfolio tools would need OAuth — Phase-gated |
| Danelfin / NFTScan / Alchemy / Moralis / Bitquery free tiers | Free-key class APIs | Key request on his word in Phase 2 — no purchase |
| HubSpot / Airtable / Linear / Asana / Dropbox (finance-ops plumbing) | Connected in Manus 22 Nov | CRM, tables, tasks, files for the finance desk's ops layer |

### 4.2 SIGN-UP-NEEDED (his hint workflow + finishing touches)
| System | What's needed | His finishing touch |
|---|---|---|
| Alpaca (paper) | Brokerage account + API keys | Identity/KYC steps are his alone |
| QuickBooks Online **or** Xero | Ledger account; entity setup for his LLCs | Entity details + bank linking decisions |
| BILL or Melio | AP/AR account on the chosen ledger | Payment-method linking |
| Ramp or Brex | Business application | Underwriting is the vendor's decision — approval not guaranteed |
| Keeper or FlyFin | Creator tax account | Account linking approvals |
| Kintsugi or Numeral | Store sales-tax account | Filing authorizations stay his signature |
| Nansen (if wanted) | Paid subscription | Purchase = his explicit go-ahead (standing rule) |
| Square (already mid-flight) | Connector exists; saved password was rejected in today's sweep | **Correct Square password via vault card — the only blocker** |
| Pinata key refresh (adjacent) | Both Muse Pinata keys return 401 | Fresh API key via secure entry — unblocks self-owned IPFS pinning for the mint rollout |

### 4.3 STUDY-ONLY (no route, by design or by closure)
Everything in §2.3, plus all of Lane 5 (legal) except a possible later Spellbook seat, and Stripe beyond protocol study (dispute gate). Study outputs feed MERIDIAN's capability spec — the deep-dive dossiers are a Phase 2 deliverable per incorporated AI: capabilities, the exact features to match, the gaps to exceed, and the terms/licensing line we do not cross (benchmarking and original design only — no proprietary code, no ToS violations).

---

## 5. MARKET-ENTRY — his own assets onto the market (honest prerequisite chain)

Chais's direction: his digital assets should trade on the market. Here is the chain as it truly stands — every step's state is the verified state from today's records. **No step below has hidden progress, and no liquidity, price, or demand is claimed anywhere: the Vault prices are his set prices, and a listed asset is not a sold asset.**

### Step 1 — Seal the assets ✅ DONE (77 of 86)
- 77 of 86 manifest assets carry the Rose Gold Seal (unique signature, SHA-256, hidden in-pixel secret, AES-256 certificate layer, tracking). Batches: SMGA 6/6, First Seven 6/6 (+Brunson cross-ref), THE GODS 14/14, Cereal Killers 9/9, Books 29/29, Visual Series + PFP 9/9.
- **Remainder:** 4 Brunson screenshot-derived pieces — originals outstanding, not mint-grade (unblocks when original files surface). **First Nine (9) — HELD by his own law**, sacred content; they move only on his explicit word, and not before.

### Step 2 — Mint Piece 0 ⏳ AWAITING HIS HAND (the keystone)
- The Rarible ERC-1155 form for **Piece 0 — "The Card That Came Home" (SMGA-001)** stands rebuilt and verified (22 Nov ~19:23 EST): sealed v2 image, supply 1, free minting ON, marketplace OFF, 8 properties incl. Signature ID `SIG·SMGA-001·D0886F10C9`.
- **Unblocks with:** his **Create click + Coinbase Wallet signature** — two touches, both his by design. Nothing else is missing.
- Proven rail note: ERC-721 lazy mint fails on Rarible ("Lazy minting is not supported for ERC721"); ERC-1155 supply-1 lazy mint is the working gasless rail.

### Step 3 — Mint the set (Pieces 1–5) ⏳ QUEUED BEHIND STEP 2
- Pieces 1–4 (Codex, Coming Home, Relic, Cowboy Fan Coin) + Piece 5 (Cyborg Brunson) — sealed mint copies ready in `sealing/mint-copies/`; forms prepared one at a time on the proven rail; **each mint's signature is his** (the standing rhythm: Muse prepares, Chais signs).

### Step 4 — Registry + five-way seal per minted piece ⏳ FOLLOWS EACH MINT
- On each mint: registry entry (token ID, contract, tx) into the scrollverse-publishing-registry + the five-way coverage record. Nothing is registered for unminted pieces — the registry records facts, not intentions.

### Step 5 — Marketplace listing (the actual "on the market" step) 🔒 HIS PRICE + START CALL
- Minted ≠ listed. Listing = a separate act per piece: choose marketplace (Rarible and/or OpenSea — both already his ecosystem), set/confirm price, sign the listing. The Vault's 21 pieces already carry his set prices ($29,997 collection) and are live on the Vault site + Shopify + Pinterest; **on-chain marketplace listing of the sealed rollout pieces has not happened yet** — it starts at Step 2.
- **Unblocks with:** Piece 0 minted (Step 2) + his explicit listing go-ahead per set (standing rule: no sale/mint-sale runs without his start call).
- **Honest note:** listing creates *availability*, not demand. No buyer, floor, or liquidity is promised or implied anywhere in this plan.

### Step 6 — The wider catalog rollout ⏳ QUEUED
- After SMGA: First Seven forms (sealed copies ready; art already Pinata-pinned, CIDs recorded), then THE GODS, Cereal Killers, Books, Visual Series per the 86-asset manifest queue — same rhythm, his signature per mint, registry per mint.
- **Adjacent unblock:** Pinata keys are dead (401 ×2) — self-owned IPFS pinning for new pieces waits on a fresh Pinata API key via secure entry (§4.2). Rarible's own upload path works without it (Piece 0 proved the upload step), so this does not block Steps 2–5.

### Step 7 — Coin / exchange steps 🔒 SEPARATE DECISIONS, NONE TAKEN
- **True current state: NO coin has been launched.** CHX is the declared token (144M, Polygon, **undeployed — and undeployed is not a gap**, per his own correction on file). $SOLARA contracts are built and compile clean, undeployed. The Cowboy Fan Coin is a *set emblem* inside SMGA, not a launched coin.
- Any coin step (deploy, Pump.fun launch, exchange listing) is a **separate decision with its own gates**: his explicit start call, plus the legal posture already on file (tokens are judged on marketing under Howey; crypto transmission for others crosses the FinCEN money-transmitter line; no paid token sale without his explicit start and the gates he set). This rollout takes **no** coin step.
- Pump.fun housekeeping on file: external-wallet sign-in retires 30 Nov — a login tap before then preserves that lane's access; it is not a launch.

**Chain summary:** Seal ✅ → **Mint Piece 0 (his click — the single unblock for everything downstream)** → mint set → registry → listing (his prices, his start call) → catalog rollout → coin steps (separate decisions, none taken).

---

## 6. REGISTRY — all 74 surveyed systems

Labels: **INTEGRATE-CANDIDATE** (real API/MCP/open source — a connection route exists) · **STUDY-ONLY** (closed or firm-shaped — capability deep-dive only) · **SKIP** (dead, mis-fit, or state-blocked).

### Lane 1 — AI stock traders (11)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Alpaca | A | INTEGRATE-CANDIDATE | Official MCP + API; paper-first rail |
| QuantConnect / LEAN | A | INTEGRATE-CANDIDATE | Open-source engine we can self-host legally |
| Danelfin | A− | INTEGRATE-CANDIDATE | Scores via API + MCP, read-only |
| OpenBB | A− | INTEGRATE-CANDIDATE | Open data platform, MCP + REST |
| TradingAgents / ai-hedge-fund | A | INTEGRATE-CANDIDATE | Open-source council architecture (research base) |
| Composer | B+ | STUDY-ONLY | App-first; Pro API partial — prompt→strategy UX is the lesson |
| Trade Ideas | B | STUDY-ONLY | Holly signal design; closed app |
| TrendSpider | B | STUDY-ONLY | Chart automation patterns; closed |
| Kavout | B | STUDY-ONLY | Factor-ranking pattern; API unverified |
| Numerai | B | STUDY-ONLY | Model-tournament meta-signal pattern |
| Tickeron | B− | STUDY-ONLY | Strategy-marketplace pattern; claims unverified |

### Lane 2 — AI crypto traders (11)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Hummingbot | A | INTEGRATE-CANDIDATE | Open source + official MCP + API; execution core |
| CCXT | A | INTEGRATE-CANDIDATE | Open-source universal exchange library |
| Freqtrade | A− | INTEGRATE-CANDIDATE | Open source; dry-run discipline |
| ElizaOS | A− | INTEGRATE-CANDIDATE | Open-source agent OS (chassis/pattern) |
| Virtuals Protocol / ACP | B+ | INTEGRATE-CANDIDATE | SDKs + agent-commerce protocol (sandbox later) |
| Olas (Autonolas) | B+ | INTEGRATE-CANDIDATE | Open agent stack (Phase-3 question) |
| 3Commas | B+ | STUDY-ONLY | Bot taxonomy; keys-to-closed-cloud pattern not accepted |
| Cryptohopper | B | STUDY-ONLY | Strategy ranking/selection pattern |
| Coinrule | B | STUDY-ONLY | Rule grammar + Agentic Mode pattern |
| Pionex / PionexGPT | C+ | STUDY-ONLY | Exchange-locked; zero-setup bot pattern |
| GMGN | B− | STUDY-ONLY | Memecoin speed/copy UX; closed |

### Lane 3 — AI NFT traders (10)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| OpenSea API + MCP | A | INTEGRATE-CANDIDATE | Free key + official MCP; his mint ecosystem |
| NFTScan | A | INTEGRATE-CANDIDATE | Developer API + webhooks, free tier |
| Alchemy / Moralis NFT APIs | A− | INTEGRATE-CANDIDATE | Builder APIs, free tiers |
| Bitquery | A− | INTEGRATE-CANDIDATE | GraphQL/streaming event triggers |
| Nansen | A− | INTEGRATE-CANDIDATE | Smart-money API (paid — his call) |
| NFTGo | B+ | STUDY-ONLY | Wash-filter pattern; API depth unverified |
| Tensor | B | STUDY-ONLY | Solana pro-desk pattern; API unverified |
| Mintify | B− | STUDY-ONLY | Terminal UX; API unverified |
| Trait Sniper | C+ | SKIP | Deployment paused (Nov 2026 check); pattern noted in survey |
| Blur | C | SKIP | Website shut down 12 Nov 2026; protocol study only |

### Lane 4 — Commerce & exchange (10)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Coinbase AgentKit + x402 | A | INTEGRATE-CANDIDATE | Open SDK/protocol; his Coinbase already connected |
| Shopify UCP / MCP | A | INTEGRATE-CANDIDATE | His live store; per-shop MCP |
| Kalshi | A | INTEGRATE-CANDIDATE | Official API + MCP; demo environment |
| PayPal MCP | A− | INTEGRATE-CANDIDATE | Official MCP; already connected in Manus |
| Polymarket | A− | INTEGRATE-CANDIDATE | Open CLOB/Data APIs; region/compliance gate first |
| Skyfire (KYA) | B+ | STUDY-ONLY | Agent-identity pattern; no public pricing |
| Crossmint | B+ | STUDY-ONLY | Wallet-orchestration pattern |
| Layer | B+ | STUDY-ONLY | Guardrail pattern (API candidate later) |
| Stripe (ACP/MCP) | A | STUDY-ONLY | Capability A — account dispute-gated by his instruction |
| Protocols (AP2/UCP/ACP/MPP/x402/ERC-8004) | A | INTEGRATE-CANDIDATE | Open standards to implement natively, not "connect" |

### Lane 5 — Legal (6)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Spellbook | B | STUDY-ONLY | Contract-benchmark pattern; only later seat candidate |
| CoCounsel | B− | STUDY-ONLY | Citation-grounded research pattern (his counsel's class) |
| Lexis+ AI / Protégé | B− | STUDY-ONLY | Same class as CoCounsel |
| Harvey | C* | SKIP | *A product, impossible fit: ~20+ seat minimums, six-figure floor |
| Legora | C | SKIP | 10-seat / ~$30K-yr floor — fit |
| Clio | C | SKIP | Firm practice management — he is not a firm |

### Lane 6 — Accounting / bookkeeping (8)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| QuickBooks Online + Intuit Assist | A | INTEGRATE-CANDIDATE | Public API + Intuit's Claude connector; sign-up route |
| Xero + JAX | A | INTEGRATE-CANDIDATE | Public API; the alternative ledger (pick one) |
| Digits | B+ | STUDY-ONLY | AI-native ledger pattern; API unverified |
| Puzzle | B | STUDY-ONLY | Stripe-stack assumption collides with his dispute |
| Pilot | B | STUDY-ONLY | Human-service model, not an integration |
| Truewind | B− | STUDY-ONLY | Close-overlay pattern (post-ledger) |
| Booke AI | B− | STUDY-ONLY | Overlay pattern; firm-shaped pricing |
| Botkeeper (→Xendoo) | C | SKIP | Vendor wound down Feb 2026 |

### Lane 7 — CFO / finance-ops / analytics (7)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Ramp | A− | INTEGRATE-CANDIDATE | API + spend agents; vendor approval gates sign-up |
| Brex | B+ | INTEGRATE-CANDIDATE | Ramp alternative (pick one spend rail) |
| Drivetrain | B | STUDY-ONLY | Anomaly-first FP&A pattern for our CFO desk |
| Runway (Financial) | B− | STUDY-ONLY | Scenario-modelling pattern |
| Aleph | B− | STUDY-ONLY | Spreadsheet-native pattern |
| Numeric | B− | STUDY-ONLY | Close/flux pattern (post-ledger) |
| Cube | C+ | SKIP | Price/fit at his current scale |

### Lane 8 — Tax (6)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Kintsugi | A− | INTEGRATE-CANDIDATE | Shopify-native sales tax; free plan |
| Numeral | B+ | INTEGRATE-CANDIDATE | Sales-tax API (developer-grade alternative) |
| Keeper | B+ | INTEGRATE-CANDIDATE | Creator-side expense→filing autopilot |
| FlyFin | B+ | INTEGRATE-CANDIDATE | Keeper alternative (pick one) |
| TaxGPT | B | STUDY-ONLY | Firm tool; cited-research pattern |
| april | B− | STUDY-ONLY | Embedded-tax pattern (B2B) |

### Lane 9 — Invoicing / payments ops (5)
| System | Grade | Label | One-line reason |
|---|---|---|---|
| Square Invoices + MCP | A− | INTEGRATE-CANDIDATE | Route already open — only his correct password blocks |
| BILL | A− | INTEGRATE-CANDIDATE | AP/AR API on the chosen ledger; sign-up route |
| Melio | B+ | INTEGRATE-CANDIDATE | Lighter BILL alternative (details to verify Phase 2) |
| Vic.ai | B− | STUDY-ONLY | Autonomous-AP pattern; volume above his load |
| Mercury | — | SKIP | Vendor denied his application (5 Mar 2026) — recorded fact |

**Registry totals:** 74 systems — **33 INTEGRATE-CANDIDATE · 33 STUDY-ONLY · 8 SKIP.**

---

## 7. Phase gates (standing rules applied)

1. **Phase 2 (read-only connections + deep-dive dossiers)** starts on Chais's word. Free-key/read-only class only; every connection reported with its true state, ScrollSoul-rollout style.
2. **Any paid tier** (Nansen, a legal seat, FP&A tools) needs his explicit go-ahead per item — no spend without it, ever.
3. **Any sign-up** runs the hint workflow; KYC/identity steps and final signatures are his finishing touches and cannot be delegated.
4. **Paper/demo before live, per venue, always.** Live trading of any kind needs his explicit start call per venue with Governor limits he sets.
5. **The Stripe gate stands:** nothing beyond the evidence pack already sent while Mark's answers are awaited; ACP is studied as an open protocol only.
6. **Fusion-tech privacy stands:** MERIDIAN's Quantum Resonance layer is documented for him only, never published.

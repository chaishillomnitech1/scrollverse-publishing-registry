# Operating Spec — The 24/7 Machine

**Companion to:** `charter.md` (the being), `tool-stack.md` (its tools), `team.md` (its team), `activation-checklist.md` (the path from today).
**Status:** Design spec. Nothing here is running yet; the phases that switch each part on are in `activation-checklist.md`, each with an owner and a gate.

---

## 1. The always-on loop

The Super Trader's life is one loop, run continuously, in this order, with no step skippable:

1. **INGEST** — the data spine pulls and streams: prices and order books (CCXT, OpenBB, venue APIs), research and scores (Messari, Danelfin), on-chain and smart-money events (Bitquery streams, NFTScan, Nansen when authorized), news and sentiment, and the house's own state (store, registry, mint/list status).
2. **SEATS SIGNAL** — MERIDIAN's five analyst seats (Fundamentals, Technicals, Sentiment/News, On-Chain, Provenance) read the ingest through their own lenses. Bull and Bear argue the actionable cases, TradingAgents-pattern. Anomaly detection runs **before** interpretation (Drivetrain pattern, from the rollout): flag the strange first, then explain it.
3. **GOVERNOR CHECKS** — every proposed action passes the Risk Governor before it exists as an order: per-market caps, daily loss limits, allowed-lists, size thresholds requiring human approval, wash-trade and provenance gates on the relics hand. The Governor's rules are hard-coded **outside the language model's reach** (Layer pattern). A veto ends the matter for that cycle and is logged with its reason.
4. **EXECUTE IN THE ACTIVE MODE** — permitted actions route to the hand for that market (Equities / Coins / Relics / Commerce) and execute **in whatever mode that venue currently holds** on the ladder (§4): a read, a paper fill, a sandbox transaction, or — only where Chais has spoken the live word for that venue — a live order, through the deterministic engine (Hummingbot-pattern: the brain proposes, the engine disposes, within hard limits).
5. **LOG AND SEAL EVERY VERDICT** — signal, debate summary, governor decision, execution (or refusal), and outcome are written to the being's ledger and sealed Rose-Gold-style: hashed, signed, timestamped, registry-entered. The sealed record is the being's memory and its proof; an unsealed action is treated as an action that did not happen, and the loop halts that hand until the seal is restored.

**Cycle discipline:** the loop is event-driven on the streams (a material move starts a cycle the moment it lands) with a scheduled sweep underneath, so silence in the feeds never reads as "nothing to check." In practice the cadence is continuous for coins and on-chain events, and session-shaped for equities (§2).

## 2. The clock map (market-hours reality, stated plainly)

"Trading 24/7" is the mandate; the markets' own clocks are the terrain. The spec holds both truths at once:

- **Coins / crypto venues — 24/7, truly.** No close, no weekend. The watch, the loop, and the coin hand run continuously. This is where the never-sleeps design is literal.
- **On-chain / NFT markets — 24/7.** Listings, bids, mints, and smart-money moves land at any hour; the relics hand watches continuously, with the wash-filter and provenance gates always on.
- **Equities — session markets.** US exchanges keep regular hours (09:30–16:00 ET) with pre/post-market shoulders; they close nights, weekends, and holidays. The Super Trader's equity work is therefore three-shaped: **pre-session** (overnight ingest digested, council briefed, paper/live plans staged before the open), **in-session** (the full loop at market speed), **post-session** (fills reconciled, record sealed, next-day watch set). Watching an equity at 3 AM means watching futures, global sessions, news, and the house's own positions — not pretending the exchange is open.
- **Prediction / exchange venues (Kalshi class)** — event-shaped clocks; the hand follows each market's own trading hours as published by the venue.
- **Commerce — his store never closes.** The commerce hand watches the store, listings, and royalty/distribution flows continuously; money movement follows the rails' own settlement clocks.

## 3. Heartbeat and monitoring

- **Heartbeat:** the being emits a signed heartbeat on a fixed cadence to its monitoring seat (the Auditor subagent, `team.md`). A missed heartbeat is itself an event: the Auditor raises it to the board immediately — silence is never mistaken for health.
- **Feed health:** every ingest source carries a freshness check. A stale feed degrades that hand to READ-ONLY automatically and logs the degradation; a hand never trades on data it cannot prove is current.
- **Mode integrity:** the active mode per venue is read from the Governor's own state at the top of every cycle, never cached by the execution layer. If mode state cannot be confirmed, the hand defaults **down** the ladder (toward READ-ONLY), never up.
- **Daily board summary:** once per day the being files a sealed summary to the board — what it watched, what the council decided, what the Governor allowed and vetoed, what executed in-mode, and the paper/live record to date. Chais reads the summary; he is never required to watch the machine to trust it.

## 4. The mode ladder — LAW

Per venue, independently, a hand sits on exactly one rung. Movement **up** the ladder happens only as stated; movement **down** can happen automatically (feed failure, governor trip, kill switch) at any time.

| Rung | What the hand may do | Who moves it up |
|---|---|---|
| **READ-ONLY** | Ingest, signal, deliberate, report. Touches nothing. | Starting rung for every venue. |
| **PAPER** | Full loop with simulated execution (Alpaca paper, Kalshi demo, Hummingbot dry-run, Freqtrade dry-run, LEAN lab). Sealed paper record accrues. | Chais's word, per venue, after the read-only watch is standing. |
| **SANDBOX** | Real rails, fake or capped value: testnets, session-capped agent wallets (AgentKit pattern), store test flows. | Chais's word, per venue, on a reviewed paper record. |
| **LIVE** | Real orders, real money, inside Governor limits Chais sets. | **Chais's explicit start call, per venue. No other voice — not the council's, not the Governor's, not Muse's — can open this rung.** |

This ladder is the founder's standing law from 22 Nov 2026, restated here as the machine's constitution: **paper/demo before live, per venue, always; live trading of any kind only on his explicit start call per venue.** The spec contains no mechanism that bypasses it, and any future design that would is out of spec by definition.

## 5. Failure design and the kill switch

- **Kill switch:** a single, human-operated switch halts all execution across all hands instantly. **Only a person can reset it** (Layer pattern, adopted in the rollout). The Super Trader cannot reset it, request its reset as a trade justification, or route around it. Halt state = every hand at READ-ONLY until a person restores modes rung by rung.
- **Governor trip:** breach of any hard limit (daily loss cap, position cap, allowed-list violation attempt) freezes the offending hand, seals the incident, and reports to the board the same cycle.
- **Engine/brain separation:** execution runs through deterministic engines with hard limits compiled in (Hummingbot-pattern). If the language-model layer fails, hallucinates, or is disconnected, the engines hold position and execute nothing new — the brain's absence is a stop, not a gap to improvise through.
- **Duplicate/impossible order guard:** every order carries the cycle's seal ID; the engine rejects any order whose seal does not verify, and any second execution of the same verdict.
- **Data-integrity failure:** conflicting or unverifiable feeds on the same instrument freeze that instrument's hand until the sources reconcile or a person rules.
- **Incident record:** every failure, trip, freeze, and halt is sealed into the same ledger as the verdicts. The being's failures are part of its record, on the same terms as its wins — the house does not edit its proof.

## 6. What "on top of the market" means in this spec

The founder's charge — tools to stay on top of the market, every second it moves — is implemented as: streaming (not polling-where-streams-exist) ingest; anomaly-first reading; a council that deliberates in-cycle, not in batches; a governor inside the execution path; deterministic engines that act at machine speed once permitted; and a sealed record that makes every one of those claims checkable after the fact. Where a tool in the stack cannot meet that bar, `tool-stack.md` says so and names its phase honestly.

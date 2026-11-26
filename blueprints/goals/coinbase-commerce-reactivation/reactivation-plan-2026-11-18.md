# Coinbase Commerce Reactivation Plan — 18 Nov 2026

**Chais Hill · ScrollVerse · Goal: coinbase-commerce-reactivation**
**Status: RESEARCH COMPLETE. The goal as written cannot be done — Coinbase Commerce is closed. The real path is Coinbase Business. Nothing has been signed into, created, or changed. No credentials were used or hunted.**

---

## 0. The headline — read this first

**Coinbase Commerce no longer exists.** Coinbase shut the Commerce portal on **31 March 2026** and folded merchant payments into **Coinbase Business**. The Commerce dashboard is permanently inaccessible, no new charges can be created, and old Commerce API keys are dead. This is from Coinbase's own help article, fetched 18 Nov 2026 (see Sources).

So "reactivate the inactive Commerce account" becomes two possible paths, and the first thing to find out is which one applies:

- **Path A — auto-transitioned (best case):** If his Commerce account settled payments to **Coinbase Exchange**, Coinbase moved it to Coinbase Business automatically. He signs in at coinbase.com with his Commerce credentials and the Business dashboard is already there. No new application.
- **Path B — fresh application:** If it did not settle to Exchange, he applies for a **new Coinbase Business account** at coinbase.com/business. This is a new account in the new product — not a reactivation — and it needs a registered business entity **and a business bank account**.

Either way there is no way back into Commerce itself. The plan below is built for both paths.

---

## 1. What changed, and when (sourced)

| Date | Event | Source |
|---|---|---|
| Mid-2024 | Coinbase deprecated the legacy Commerce hosted-checkout API; Commerce moved onto the Onchain Payments API / Coinbase Pay stack. The official **Shopify app was removed** in 2024. | payyd.co Shopify guide, 2026; Coinbase transition help |
| Oct 2025 | Coinbase announced a **1% fee on payment links** for the new Business payments product. | paymentreview.com, Oct 2026 review |
| 31 Mar 2026 | **Commerce portal closed permanently.** No new charges, no dashboard access, Commerce withdrawal tool disabled. Merchants had to transition by this date. | Coinbase Help, "Transitioning from Coinbase Commerce to Coinbase Business" (fetched 18 Nov 2026) |
| Jun 2025 | Shopify + Coinbase + Stripe launched **native USDC checkout inside Shopify Payments** on Base; later expanded to Ethereum, Optimism, Polygon, Arbitrum. | Shopify announcement via finassets.io / northsettlements.com (Sep 2026) |
| Nov 2026 (now) | Coinbase Business is the only Coinbase merchant product. US + Singapore legal entities only. USDC only (USDT "coming soon" per Coinbase; one Oct 2026 review says USDT on Ethereum is live — treat USDT as unconfirmed until seen in-account). | Coinbase Help (fetched 18 Nov 2026); paymentreview.com (Oct 2026) |

**Commerce vs Business — the differences that matter for Chais:**

| | Old Commerce | Coinbase Business (now) |
|---|---|---|
| Custody | Self-custodial — merchant held a 12-word seed phrase | **Custodial — Coinbase holds the funds** |
| Assets | Hundreds (BTC, ETH, USDC, LTC, DAI, BCH…) | **USDC only today** (USDT coming soon) |
| Networks | Ethereum, Polygon, Base | All five major EVM networks (ETH, Base, Polygon, Optimism, Arbitrum) |
| Fiat offramp | None — merchant converted it themselves | **Direct bank offramp (ACH/wire)** |
| Fee | 1% flat | **1% for migrating merchants** (Coinbase transition page); current public pages no longer publish a rate — shown in-account after sign-in |
| Eligibility | Global, no KYB | **US + Singapore legal entities only** — ScrollVerse LLC (NJ) qualifies |
| Payment links / invoicing | Yes | Yes, plus Checkouts API, refunds, QuickBooks/Xero, USDC yield |
| Shopify app | Removed 2024 | **None** — no Shopify app for Business either |

---

## 2. Ground truth — where things stand today

**The store (from workspace notes, 17–18 Nov 2026):**
- Shopify store **juv8tg-1n.myshopify.com**, Advanced plan, USD, EST. **88+ products** live (wave 2 adds 10 more), Printify fulfilment connected.
- **Shopify Payments is OFF** by mandate while the VibeCanvas/Stripe payout-hold dispute stands. **PayPal Checkout is the only live checkout rail** (2.99% + $0.49 domestic).
- Settlement home is still missing: the LLC business bank account. Mercury is "Under Review" for Scroll Verse LLC. This gates Coinbase Business too (it requires a business bank account).
- Entity: **ScrollVerse LLC, NJ, formed 12 May 2026, charter 0451463412, EIN 42-2509570**, sole member Chais Kenyatta Hill. Address: 721 Embassy Terrace, Vineland, NJ 08360.

**The Coinbase account (from Gmail + memory, checked 18 Nov 2026):**
- Chais **has** a Coinbase Commerce account, described as inactive (17 Nov ~11:12 EST). Whether it ever took a payment, held funds, or settled to Coinbase Exchange is **unknown — ask him (see §8)**.
- His **retail Coinbase account is active**: price alerts through Nov 2026, a "Verify your device to sign in" email 17 Oct 2026 (sign-in from New Jersey, Chrome), and a "Third Party: Grok Connected to Your Coinbase Account" notice 17 Oct 2026. Note: review third-party connections during the sign-in check.
- **No Coinbase Commerce transition email found** in hillchais1@gmail.com (searched 18 Nov 2026: no mail from commerce-transition@coinbase.com, no "Coinbase Commerce" or "Coinbase Business" subject lines). Either it went to another inbox or it was never sent/seen — another reason the sign-in check matters.
- **No Coinbase integration code in local repo clones** (grepped 18 Nov 2026). His remote scrollverse-web-app repo has a GitHub PR "Add Coinbase stablecoin acceptance as an independent payment rail" whose CI run failed 14 Nov 2026 — the code lives in the remote repo, not on this machine.

**The guardrails that still bind this work:**
- No token/NFT sale, mint, or token-as-reward before a written per-asset Howey analysis. This plan is **payment acceptance only** — it does not mint, sell, or issue any token.
- **MetaMask is set aside for now** on the merchant side. (Buyers may still pay a Business payment link from whatever wallet they already use — that is the buyer's choice, not a merchant integration.)
- CPA crypto-basis setup (income at receipt, basis, record-keeping) must be answered before taking crypto **at volume** — see highways-master §4.1. Small test volume first.
- Never share a seed phrase — not in chat, not in a file, not in a photo, not with anyone. See §4.

---

## 3. The reactivation path — step by step

### Step 0 — Triage questions (Chais answers; 2 minutes, no login needed)
1. Did the old Commerce account **ever receive a payment or hold funds**? If yes, roughly how much and in what coin?
2. Do you have the Commerce **12-word seed phrase** — written down, in a password manager, or backed up to Google Drive? (Yes/no only — **never send the phrase itself**.)
3. Did the Commerce account **settle to Coinbase Exchange**, or to a self-custody wallet? (If he doesn't know, Step 1 will tell us.)
4. Which email is the Commerce account under — hillchais1@gmail.com or another?

### Step 1 — Sign-in check (CHAIS, in the browser, ~10 minutes)
- Go to **coinbase.com** and sign in with the **Commerce credentials** (email + password + 2FA).
- **If the Business dashboard appears** → Path A: auto-transitioned. Skip to Step 3.
- **If it lands on a retail/personal account with no Business section** → Path B: apply fresh (Step 2). Also check **exchange.coinbase.com** with the same credentials — Coinbase says managed merchants can verify auto-transition status there.
- While signed in: check **Settings → third-party connections** (Grok was connected 17 Oct 2026 — confirm it is intended) and confirm the account email.
- If sign-in fails: use Coinbase's account-recovery flow (government ID + live selfie, typically 48–72h review). Do not create a duplicate account — recovery first.
- **This step needs Chais's hands.** A browser task can run it with him (he types the password/2FA himself; the agent never sees them).

### Step 2 — Apply for Coinbase Business (CHAIS, only if Path B; ~30 min to apply, approval reported as fast as ~2 days)
- Apply at **coinbase.com/business**.
- Have ready: business legal name (**ScrollVerse LLC**), EIN **42-2509570**, NJ charter **0451463412**, operating agreement, business address (721 Embassy Terrace, Vineland, NJ 08360), Chais's government ID, and a **business bank account** to link.
- **Gate: the business bank account.** Coinbase Business requires one. Mercury is still "Under Review" — if it is not open by application time, the application cannot complete. This is the same gate blocking PayPal sweeps; it is the single biggest dependency in the whole plan.
- No application fee, no monthly fee, no setup fee (Slash, Nov 2026; paymentreview.com, Oct 2026).

### Step 3 — First-run setup in Coinbase Business (CHAIS, ~30 minutes once approved)
1. **Confirm the fee rate shown in-account** when creating the first payment link. Expect **1%** (migrating merchants, per Coinbase's transition page) — but Coinbase no longer publishes the rate, so read it off the screen and record it before building checkout around it.
2. **Link the business bank account** for the fiat offramp (ACH withdrawals are free; US wires $10 in / $25 out, per Slash Nov 2026).
3. **Set the settlement preference:** hold USDC in the account, or auto-convert incoming USDC to USD on arrival. Recommended default: **auto-convert to USD** (no volatility exposure; the conversion fee is shown in-account — record it; it was ~0.5% spread under old Commerce, but the Business conversion fee is unpublished — do not assume 0.5%).
4. Create a **$1 test payment link** and pay it from a personal wallet to prove the loop end-to-end before any store wiring.
5. Optional, later: USDC yield on idle balances (listed at 3.60% APY, Oct 2026) — only if he wants to hold USDC; default is to sweep to the bank weekly, same as PayPal.

### Step 4 — Shopify wiring (AGENT can prep; activation needs Chais's approval of the exact text)
There are three routes. Only one works today with Shopify Payments OFF.

| Route | How it works | Status for this store |
|---|---|---|
| **A. Manual payment method + Business payment link (DO THIS NOW)** | Shopify Settings → Payments → Manual payment methods → "Create custom payment method". Customer picks "Pay with Crypto (USDC)" at checkout, the order is placed as pending, and the confirmation page/email sends them a Coinbase Business payment link for the exact order total. Agent (or Chais) marks the order paid when the Business dashboard shows the payment. | **Works today. No Shopify Payments needed. No app to install. No third-party transaction fee** (Shopify does not charge its extra fee on manual methods — confirm in admin). Manual reconciliation per order — fine at current volume, clunky at scale. |
| **B. Native USDC inside Shopify Payments (DO THIS LATER)** | USDC checkout built into Shopify Payments (launched Jun 2025 with Coinbase + Stripe, on Base; now 5 networks). Buyer pays USDC from any supported wallet, including guest checkout and Shop Pay; merchant receives local currency by default or keeps USDC. No separate gateway, no app. | **BLOCKED until the Stripe dispute resolves and Shopify Payments is switched back on.** Also US-only excluding Alaska, New York, Texas — New Jersey is eligible. This is the clean end-state; it replaces Route A when Shopify Payments returns. |
| **C. Third-party crypto gateway app (FALLBACK ONLY)** | NOWPayments (0.5%, 300+ coins, official Shopify app), CoinGate (1%, MiCA-licensed), BTCPay Server (0% + self-hosting), Plisio (0.5%). BitPay (2% + $0.25, daily fiat settlement) is the pre-existing workspace fallback. | Available today, but these are **not Coinbase**. Only if Chais decides the manual route is too clunky and wants an automated crypto checkout before Shopify Payments returns. Do not install any app without his explicit go-ahead. |

**Route A — exact manual payment method to create (draft, needs his approval):**
- Name: `Pay with Crypto (USDC)`
- Description shown at checkout: `Pay with USDC stablecoin via Coinbase. Place your order, then use the secure payment link on your confirmation page and in your email. Your order ships once the payment confirms — usually within minutes.`
- After creation: test it end-to-end with a $1 test order (see §9 test script) before telling any customer it exists.

### Step 5 — Books, Vault, and direct sales (same rail, no extra build)
- **Books and Vault digital goods:** a Business payment link or invoice can be created per title/collection and pasted wherever the product is listed (Atlas, Vault, socials, email). No checkout integration needed. Price in USD; the link charges the exact USD amount in USDC.
- **Goat Bundle / merch:** Route A covers Shopify orders. For direct/social sales, a payment link per bundle works the same way.
- **Invoices:** Business has a full invoicing suite (line items, due dates) — use it for any larger or custom order instead of a bare payment link.

### Step 6 — When Shopify Payments returns (after the Stripe dispute)
- Enable native USDC in Settings → Payments → Shopify Payments. Route A stays as a backup for non-USDC crypto or if USDC checkout ever misbehaves. Do not remove Route A until native USDC has completed at least one real order.

---

## 4. Legacy Commerce wallet funds — the branch that matters most

Commerce wallets were **self-custodial**: Chais (not Coinbase) controls the funds via a 12-word seed phrase. The Commerce withdrawal tool was **permanently disabled after 31 Mar 2026**.

- **If he has the seed phrase and there were funds:** the funds are still recoverable by importing the phrase into a compatible wallet (Coinbase Wallet or MetaMask). BUT: Commerce generated a new address per payment, so funds may sit across many addresses and a standard wallet (which scans ~20 addresses) may not show the full balance. Coinbase's own guidance says the (now-dead) withdrawal tool was the reliable way to consolidate. Importing is still the only route left — do it with him, in the official wallet app, and check the balance carefully.
- **If he lost the seed phrase and never backed it up:** **Coinbase cannot recover the funds.** They never had the phrase. Check password managers, secure notes, physical storage, and Google Drive (Commerce offered a Google Drive seed backup — Settings → Security → Manage backup in the old dashboard).
- **If the account never held funds:** nothing to recover — skip this branch entirely.
- **SEED PHRASE SAFETY (non-negotiable):** Never type a seed phrase into a website or web form. Only ever enter it into the official Coinbase Wallet or MetaMask **app** import screen. Never send it in chat, email, or a photo — not to Muse, not to support, not to anyone. Coinbase's own withdrawal tool once asked merchants to paste seed phrases into a web form; security researchers condemned that practice. Treat any request for the phrase — from any source — as a scam unless it is the official wallet app on his own device.

---

## 5. Customer payment flow — plain language

How a buyer actually pays (Route A, live now once wired):

1. Buyer shops the store and checks out normally, choosing **"Pay with Crypto (USDC)"** instead of PayPal.
2. The order is placed. The confirmation page and the order email show a **secure Coinbase payment link** for the exact order total in USDC.
3. Buyer opens the link, connects any compatible wallet (Coinbase Wallet, MetaMask, or any wallet holding USDC), and pays. On **Base**, settlement takes ~2 seconds and network fees are sub-cent; on Ethereum mainnet the buyer pays gas (a few dollars, sometimes more — Base is the recommended network and should be named in the instructions).
4. Coinbase confirms the payment. The store marks the order paid, Printify fulfils, tracking goes out — same as a PayPal order.
5. The money lands in the Coinbase Business account as USDC. With auto-convert on, it becomes USD and can be withdrawn to the LLC business bank by ACH (free). With auto-convert off, USDC sits in the account until swept.

What the buyer needs: USDC on Base (or Ethereum / Polygon / Optimism / Arbitrum) and any wallet. No Coinbase account required on the buyer side. **No chargebacks** — crypto payments are irreversible, so the buyer has no card-network dispute path; refunds, if ever needed, are issued manually from the Business dashboard.

---

## 6. Fees — sourced, dated, worked example

| Item | Figure | Source / date |
|---|---|---|
| Coinbase Business, per completed payment | **1%** for migrating merchants (Coinbase transition page). **Current public pages no longer publish a rate** — it is shown in-account when creating a payment link. | Coinbase Help, fetched 18 Nov 2026; paymentreview.com, Oct 2026 |
| Auto-convert USDC → USD | **Fee unpublished** — shown in-account. Old Commerce spread was ~0.5%; do not assume the same for Business. | Slash, Nov 2026; payyd.co (old Commerce figure) |
| ACH withdrawal to bank | Free | Slash, Nov 2026 |
| US wires | $10 incoming / $25 outgoing | Slash, Nov 2026 |
| Monthly / setup / application fee | None | Slash, Nov 2026; paymentreview.com, Oct 2026 |
| Buyer network fee (Base) | Sub-cent | Coinbase docs via eco.com, Nov 2026 |
| USDC yield on idle balances | 3.60% APY (variable, Oct 2026) — optional | paymentreview.com, Oct 2026 |

**Worked example — $100 order (Route A, auto-convert on):**
- Gross: $100.00 → Business fee 1% = $1.00 → $99.00 in USDC → auto-convert fee (unpublished; if it were the old 0.5% spread, $0.50) → **~$98.50 to the bank, ACH free.**
- Compare: PayPal $3.48 → **$96.52**. BitPay $2.25 → **$97.75**. NOWPayments 0.5% → **$99.50**. Native USDC via Shopify Payments (Route B, later): billed at Shopify Payments' standard rates — confirm in admin at activation; one third-party guide (Ecommerce Fastlane, 2026) cites 0.5% with a merchant rebate, **unverified**.
- **Shopify's extra fee:** Advanced plan charges 0.5% on third-party gateway orders — but Route A is a **manual** payment method, which Shopify does not charge the extra fee on. Confirm in admin when creating it.

**Fee rule for the plan:** the 1% is the last *published* figure. The in-account rate is the real rate. Record it in the per-sale log the first time a payment link is created, and re-check it quarterly — Coinbase has changed this pricing before.

---

## 7. What can be done now, without Chais

Already done in this plan: the research, the step order, the Route A draft text (§3), the customer flow (§5), the fee table (§6), and the test script below.

Prepared and ready to run the moment he says go:
- **Test script (Route A):** create the manual payment method → place a $1 test order as a customer → pay via a Business test payment link → confirm the order shows paid in Business and in Shopify → confirm Printify receives the order → refund/void the test payment from the Business dashboard → log the result. (No money spent beyond the $1 test, which comes back.)
- **Customer instructions** (one paragraph for the checkout page / order email) — see Route A description in §3.
- **Per-sale log columns** (from highways-master): date | stream | rail | buyer ref / order ID | gross USD | rail fee | net received | currency received | USD FMV at receipt | payout date to LLC bank. Crypto rows must record the USD fair-market value at receipt — the CPA needs it for basis.

---

## 8. Exact asks for Chais

1. **Answer the four triage questions (§3 Step 0)** — especially: did Commerce ever hold funds, and do you have the 12-word seed phrase? (Yes/no only. Never send the phrase.)
2. **Sign in at coinbase.com with the Commerce credentials** (browser task, with him — he types the password and 2FA). This one check decides Path A (already transitioned) vs Path B (apply fresh).
3. **Business bank account** — the Mercury application is the gate for the Business application. If Mercury is still under review, that is the first domino; nothing in Step 2 can complete without it.
4. **Approve the Route A manual payment method text** (§3) so it can be created in Shopify, and approve the $1 test order.
5. **Confirm the in-account fee rate** once inside Business (expected 1%; record what the screen actually says) and the auto-convert fee.
6. **CPA crypto-basis setup** before taking crypto at volume (already an open gate in the highways plan — this does not add a new one, it just inherits it).

---

## 9. Risks and guardrails

- **Custodial risk is real.** Business holds the funds; Commerce did not. Mitigation is the same as PayPal: **weekly sweeps to the LLC bank, never let a balance sit** (highways-master rule: no rail holds more than one week's volume).
- **No chargebacks cuts both ways.** No fraud reversals for the merchant — but also no buyer protection, which can cost buyer trust on a new store. Keep PayPal as the primary rail; crypto is the secondary option for buyers who want it.
- **USDC only.** Buyers who hold BTC/ETH cannot pay through Coinbase Business — they would need to convert to USDC first. That is a real limitation vs old Commerce. (The fallback gateways in §3 Route C accept more coins.)
- **The old "~1.5% all-in" figure in the workspace is stale.** It described old Commerce (1% + ~0.5% spread). For Business: 1% + an **unpublished** conversion fee. Update highways-master and rails-research when the in-account rate is confirmed.
- **GENIUS Act context (not legal advice):** the US GENIUS Act (signed July 2025) created a federal framework for payment stablecoins; OCC implementing rules followed in 2026. Nothing in this plan needs a legal change, but the CPA should confirm the current treatment when doing the crypto-basis setup.
- **Do not create a second Commerce-style account, do not buy a "reactivation" service, and do not pay anyone to recover a seed phrase.** Coinbase's only channels are coinbase.com/business and commerce-transition@coinbase.com.

---

## Sources (all checked 18 Nov 2026)

- Coinbase Help — "Transitioning from Coinbase Commerce to Coinbase Business" — https://help.coinbase.com/en/transitioning-from-coinbase-commerce-to-coinbase-business (fetched 18 Nov 2026, crawled <1 min before read). **Primary source for the closure, the 31 Mar 2026 deadline, the 1% migrating-merchant fee, auto-transition for Exchange-settling merchants, and the legacy-wallet/seed-phrase guidance.**
- Coinbase Help — "Escheatment and unclaimed funds" — https://help.coinbase.com/en/coinbase/managing-my-account/other/escheatment-and-unclaimed-funds (dormancy 1–5 years by state; sign-in resets dormancy).
- paymentreview.com — "Coinbase Business Review" (Oct 2026) — fee no longer published, shown in-account; 1% last public figure (Oct 2025); USDC rewards 3.60% APY (Oct 2026); USDC on Base/Ethereum/Polygon/Optimism/Arbitrum, USDT on Ethereum.
- slash.com — "Coinbase Business vs Ramp" (Nov 2026) and "Slash vs Coinbase Business" — 1% on payment links, auto-convert fee unpublished, ACH free, wires $10/$25, approval as fast as ~2 days, US + Singapore only.
- coderpress.co — "Coinbase Commerce Shut Down: How to Migrate in WooCommerce" (updated 12 Nov 2026) and "Coinbase Business vs NOWPayments" (Nov 2026) — closure confirmed, 1% for migrating merchants, WooCommerce plugin supports USDC on Base.
- eco.com — "Coinbase Commerce vs BitPay vs Crossmint" (updated 4 Nov 2026) — 1% flat per Coinbase docs; USDC on Base ~2s, sub-cent.
- payyd.co — "Coinbase Commerce + Shopify: Complete 2026 Integration Guide" — Shopify app removed 2024, manual-payment-method workaround, 1% + ~0.5% spread (old Commerce), NOWPayments/CoinGate/BTCPay/Plisio comparison.
- finassets.io / northsettlements.com (Sep 2026) / solcard.cc (Nov 2026) — native USDC in Shopify Payments: launched Jun 2025 with Coinbase + Stripe on Base, now 5 networks; US excluding Alaska, New York, Texas; requires Shopify Payments active; USDC only.
- Workspace ground truth: ~/workspace/financial-highways/highways-master.md, rails-research.md, streams-status-2026-11-17.md (all 17 Nov 2026); ~/workspace/goals/coinbase-commerce-reactivation/GOAL.md; Gmail search 18 Nov 2026 (no transition email found; retail account active; Grok third-party connection 17 Oct 2026).

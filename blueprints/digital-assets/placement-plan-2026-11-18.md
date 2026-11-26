# Digital Assets Placement Plan — All Platforms, Pump.fun Included

**Chais Hill / ScrollVerse · 18 Nov 2026 · PLAN ONLY**
**Nothing in this document launches, mints, lists, publishes, connects a wallet, spends anything, or contacts anyone. It is preparation for decisions Chais must make first.**

Chais's direction (18 Nov 2026): place his digital assets on all platforms, Pump.fun included. He also says **he already has an account in place** — most likely Pump.fun, since that is the platform he named. **Do not assume which platform the account is on.** The plan records the account as existing and makes confirming it step zero.

---

## 0. The existing account — confirm before anything else

Chais says an account is already in place. No new account setup may be needed. Before any launch, confirm:

1. **Which platform is the account on?** (Pump.fun is the likely answer — he named it — but confirm, don't assume. It could also be a marketplace or wallet account.)
2. **Which wallet is connected to it, and what is its public address?** Creator fees, ownership, and any mint authority all flow to that wallet. If the wrong wallet is attached, fees and control go to the wrong place.
3. **Is the wallet funded?** Pump.fun / Raydium launches need a little SOL for network fees and rent (see §4). A Solana launch needs SOL in that wallet; an EVM deploy needs ETH (or the L2's gas token).
4. **Who holds the keys / seed phrase?** Never share the seed phrase with anyone, including in chat. If Chais holds it, only he signs. If the account was made on a device or browser he no longer controls, that is a blocker to resolve before launch.
5. **Is the account in his name (Chais Hill / ScrollVerse LLC) or a personal handle?** That decides what name shows on the listing and whether the account matches the business.

**Until these five answers are on file, no launch can be prepared to the point of execution.**

---

## 1. Asset inventory — what actually exists vs what is only a placeholder

Everything below was verified against the local repo clones and the Pinata catalogues (`~/workspace/merch/pinata-build-2026-11-18.md`, `~/workspace/merch/pinata-build-wave2-2026-11-18.md`, `~/workspace/merch/pinata-gold-activation-notes-2026-11-18.md`). Repo labels proved wrong in places, so nothing here is trusted from labels alone.

### 1A. Tokens — source code exists, NONE is deployed on-chain

No deployed contract address for any token below was found anywhere in the repos, the workspace, or Gmail. The addresses that appear in repo files are placeholders/test values (`0x1234…`, `0x9876…`, `0x0000…`). **Every token below is code in a repo, not a live token.** Deploying one is a fresh on-chain deploy, not a listing of something live.

| Token | Contract (repo) | Chain | What it is | Status |
|---|---|---|---|---|
| **CHXToken (CHX)** | `Chaishillomnitech1/contracts/CHXToken.sol` | EVM (Solidity, OpenZeppelin) | ERC-20. Mints 21.6 billion at deploy to the deployer. Passive income: 0.005% of balance per day, claimable, mints new tokens. Royalties on claims: 10% creator / 5% ambassador / 2% DAO. 2% Zakat circulation. BlessingCoin integration. Pausable, owner-controlled vaults. | **Code only. Not deployed.** |
| **ScrollVerseNFT** | `Chaishillomnitech1/contracts/ScrollVerseNFT.sol` (also in `OmniBuilderZero`, `cosmic-constitution-scrollverse`) | EVM (Solidity) | ERC-721 "ScrollVerse Genesis NFT". Max supply 999. Owner-only mint, requires a PQC signature hash. 10% royalty (EIP-2981). | **Code only. Not deployed.** |
| **BlessingCoin** | `Chaishillomnitech1/contracts/BlessingCoin.sol` | EVM | ERC-20. Airdrop distribution with Merkle proofs, batch distribution, L2/rollup notes. | Code only. Not deployed. |
| **CodexToken ($CODEX)** | `Chaishillomnitech1/contracts/CodexToken.sol` | EVM | ERC-20. DAO governance token with voting, royalty flows, staking rewards. | Code only. Not deployed. |
| **DivineEssenceCoin (DE)** | `Chaishillomnitech1/contracts/DivineEssenceCoin.sol` | EVM | ERC-20. 144,000,000 total supply. Staking APY advertised in the code comments: 8% (3 mo) / 12% (6 mo) / 18% (12 mo). Charitable-action rewards. | Code only. Not deployed. |
| **$MIRROR** | `mirror-coin-spec.json` (economics only) | — | Economics spec only. **No contract file found.** | **Placeholder. Does not exist as a token.** |
| **$NOOR / EarthCoin** | Referenced by `NoorCitiesStaking.sol` | EVM | Staking contract for $NOOR, EarthCoin, BlessingCoin; 7.77% zakat forwarding. The tokens themselves were not found as contracts. | Staking code only; underlying tokens not found. |
| **FLAMECOIN** | `flamecoin-v4` repo | — | Repo holds only a LICENSE and README. **No contract.** | **Placeholder. Does not exist.** |
| **TGLD** | `Pantheon-Protocol-TGLD-Smart-Contracts` repo | EVM (per repo name) | Named repo; contract contents not verified in this pass. | Unverified — treat as not confirmed. |
| **SolarShardNFT** | Inside `ScrollVerseNFTApp.zip` on Pinata | EVM | Empty contract shell — a stub, not a working contract. | **Stub. Does not exist as a real contract.** |
| **Suite (README)** | `Chaishillomnitech1/README.md` | EVM | DAOGovernance, MultiSigWallet, LayerZeroBridge, StakingRewards listed as the contract suite (plus `DynamicDAOGovernance.sol`, `OmniSovereignWallet.sol` found in `contracts/`). | Code/mentions only. Not deployed. |

**CHX on Manus — do not confuse with an on-chain token.** Chais earns CHX staking rewards through the Manus platform (daily "Daily Staking Compound Complete" emails from "ScrollVerse Trinity — Sovereign Portal", 49 positions; ~60,922 CHX/day as of 14 Nov 2026). That CHX is a **platform-internal balance on Manus**, not an on-chain deployed token. There is no on-chain CHX to list anywhere today.

### 1B. NFT art on Pinata — ALL 16 public files (full inventory, per Chais's direction)

Gateway: `https://gateway.pinata.cloud/ipfs/<CID>` (the only working gateway from this box; his dedicated gateway `olive-delicate-koi-568.mypinata.cloud` is limit-paused). Files live in `~/workspace/merch/pinata/`.

| # | File | CID | Type / size | Placement status |
|---|---|---|---|---|
| 1 | **Cyborg Brunson** — cybernetic player, KNICKS 11, "JALEN BRUNSON", Scroll Vault coin/QR medallion | `bafybeigbqlnsij75ixhaje4b463ii4apjdseoenp5hhd2yjm3ktvnk2ooe` | PNG 1024×1536, 3.38 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 2 | **ScrollProof: God Mode emblem** — purple neon triangle/spiral, Theta 6.2 Hz, GodGlow True, OmniDAO Voting / ScrollVault Unlock | `bafybeihdvxjyuhnc5i3uz4jenw72w5duqpwntkmzht6unpsemdnj4vc2fe` | PNG 1024×1536, 1.95 MB | Placeable. **Own IP — cleanest lead asset.** |
| 3 | **Patrick Ewing — "THE ANCHOR"** — NEW YORK 33, golden sacred-geometry halo | `bafybeie4kdb2nr7tvvk2jgsyvu65azmz7msoa7m3ag63jehtso3fvwdvgq` | PNG 1280×1280, 3.00 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 4 | **Walt Frazier — "THE FLOOR GENERAL"** — fur coat, NEW YORK 11, basketball; Meta AI watermark (cropped out in print files) | `bafybeickv52mzzbc45yrq5y4vvfla5p72qajwhphhpffcimkgbulpazxla` | PNG 1280×1280, 3.23 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 5 | **OG Anunoby — "THE WING"** — NEW YORK 8, blue cosmic action shot; Meta AI watermark (cropped out in print files) | `bafybeigub3gn4ckx4qx33zw4skk3v3qqkzzv75sp32ml5af4wtl3dri77q` | PNG, 2.85 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 6 | **Karl-Anthony Towns — "THE TOWER"** — TOWNS 32, gold/blue NYC skyline; Meta AI watermark (cropped out in print files) | `bafybeiargqbawp2oseywfhums2dwvaerzikymqeejzmf2576ekfmdbpydq` | PNG, 1.87 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 7 | **Bernard King — "ASSASSIN"** — NEW YORK 30, gold energy; Meta AI watermark (cropped out in print files) | `bafybeicggv4kaxzqsmuvtw5b3jwyitzhsumnjud3dyjxg3yqwi4wmahzh4` | PNG, 2.78 MB | Placeable as NFT art. **Knicks/living-player IP risk — see §5.** |
| 8 | **"Londyn lullaby"** | `bafybeigzb55bs3453cprr75yecz6jux32a6v3l5l4yzaualdhvht3mewwm` | PNG 1024×1536, 3.39 MB | **⛔ NEVER. Tier 3 — a child's name/art. Never placed, sold, listed, or shown anywhere. Inventory only.** |
| 9 | **scrollproof.json** — God Mode NFT metadata (image field is the placeholder `ipfs://REPLACE_WITH_IMAGE_CID`; real image is file 2) | `bafkreifaiqnt6ofmsljqaz3btub4vwgxpsp3ufmxjd2uwyhaa2n2jhqs2i` | JSON, 704 B | Metadata file. Usable as the metadata template for the God Mode NFT once the image field is pointed at file 2's CID. Not a saleable asset on its own. |
| 10 | **NFT_Minting_Starter_Pack.zip** — Express server, `POST /mint` uploads an image to IPFS via Infura and returns the CID | `bafkreichagixg7tywgpgx4selbrbrxmwptmqwicd4zdrhujgoaga2msmiy` | ZIP, 1,996 B | Code, not an asset. **Despite the name it does NOT mint an on-chain token.** Needs Infura credentials (not included). Do not list as a product. |
| 11 | **ScrollVerseNFTApp.zip** — starter skeleton (3-line server, one-line upload stub, empty SolarShardNFT shell, one-line web stubs) | `bafkreicprtlbuenkfrdynb63q3y77xzaxlp2m2wgnnl5kzbqbsa7kblqwi` | ZIP, 1,419 B | Code, not an asset. Not a working app. Do not list as a product. |
| 12 | **sovereignhub folder** — frozen snapshot of his SovereignHub Shopify store front-end (106 files: ~88 hashed styling files, stock images, logos, one 1 MB checkout script) | `bafybeigkmtmm3d5admi4wjfn7yj6scygfdxe5apdqy6pm2rufdbhjk7isu` | Folder, 6.13 MB | Archive only. A snapshot of a store front-end, not a saleable digital asset. Keep pinned for reference; do not list. |
| 13 | **nexus_complete_html.html** | `bafkreibrvtpdwdr3dlik6oefzkz2enddypxkt4deq3asnp32hzw2a7u7iq` | HTML, 3.47 KB | **⏳ PENDING — unreachable.** Pinata's public gateway refuses HTML by policy and the dedicated gateway is limit-paused. Placeable only after a gateway reset or Chais sends the file direct. |
| 14 | **ScrollVerse_EternalRealm.html** | `bafkreigtmo2eorihx7lbayc7g3m43gahxila3vlrtxozz2rhptqpzo4sbi` | HTML, 2.52 KB | **⏳ PENDING — unreachable.** Same as 13. |
| 15 | **Library - Manus_files** folder | *(full CID not on file — Chais to tap "Copy CID" in Pinata)* | Folder, 45.23 MB | **⏳ PENDING — CID needed from Chais.** Contents unknown until the CID lands. |
| 16 | **Meta AI - Your AI and More_files** folder | *(full CID not on file — Chais to tap "Copy CID" in Pinata)* | Folder, 31.67 MB | **⏳ PENDING — CID needed from Chais.** Contents unknown until the CID lands. |

**Not on Pinata (placeholders only — do not list):** Consciousness Mirror art, Azurath art, PSYCHE16 art, NŪR Cities art, Token 1111 art, CHXToken art. All of these exist in repos only as `ipfs://IMAGE_CID/...`, `QmXXX…`, or `ipfs://PLACEHOLDER` references. There is no art to place until real files exist.

**Also not placeable from screenshots:** "The Boyz" (Brunson + Josh Hart), "JALEN BRUNSON IS KING", "BRUNSON MVP" — phone/social screenshots only, UI baked in, no originals or CIDs. "Father's Day Genesis" — a real black-and-white photo of two real people; inventory only, never merch, never an NFT.

**Placeable art, in total: 7 images** (files 1–7). Everything else in the 16 is code, metadata, archive, pending, or forbidden.

---

## 2. The chain split — the fact that decides everything

**All of Chais's token and NFT contracts are EVM (Ethereum-family) Solidity. Pump.fun, Raydium LaunchLab, Jupiter, and Magic Eden are Solana-only.**

| Platform | Chain | Can it use his existing contracts? |
|---|---|---|
| Pump.fun | Solana | **No.** A Pump.fun launch creates a brand-new Solana SPL token. It cannot be the CHXToken contract. |
| Raydium LaunchLab | Solana | **No.** Same — new SPL token. |
| Jupiter | Solana | **No.** Aggregator for Solana tokens with a DEX pool; nothing to aggregate until a Solana token exists. |
| Magic Eden | Solana-only since Mar 2026 | **No.** His ERC-721 ScrollVerseNFT cannot list there. Would need Solana (Metaplex) versions of the art re-minted. |
| OpenSea | Multi-chain (29 chains: Ethereum, Base, Polygon, Solana, more) | **Yes — for the NFTs.** His ERC-721 ScrollVerseNFT contract fits OpenSea on Ethereum / Base / Polygon. (Whether OpenSea lists Scroll zkEVM — the chain named in his README — needs a live check at listing time.) |

**Consequence:** "Place everything on Pump.fun" cannot mean placing CHX, because CHX is EVM code and Pump.fun is Solana. A Pump.fun launch would be a **new, separate Solana token**. If it were also called CHX, there would then be two different tokens called CHX on two chains — a confusion and scam vector. The ticker/name decision (§6) has to come before any Pump.fun launch.

The suite does list a `LayerZeroBridge.sol` (cross-chain bridge) — but it is un-deployed code, not a working bridge. Bridging EVM CHX to Solana is a build project, not a listing step.

---

## 3. Platform research — how each one actually works

All figures below are from public guides/docs checked 18 Nov 2026. Fees change; re-check live before any launch.

### 3A. Pump.fun (Solana memecoin launchpad) — the platform Chais named

- **What it is:** No-code Solana launchpad. A token starts on a bonding curve (price set by a formula, not an order book), then "graduates" to a DEX pool.
- **What you need:** A Solana wallet (Phantom, Solflare, Backpack) with a little SOL. A name (≤32 chars), ticker (≤10 chars), description, and an image. No account beyond the wallet; no code; about 5 minutes.
- **What it costs:** No platform creation fee. Creation is ~0.02 SOL in network/rent costs on the first buy. Every buy and sell on the curve pays **1.25%** (0.95% to Pump.fun, 0.30% to the creator). Since Oct 2026 the web/mobile app adds a further **~0.45%** platform fee per trade (0.40% with a referral). Graduation costs 0.015 SOL.
- **Supply and control:** Fixed at **1 billion tokens, 6 decimals**. The creator controls **only the name, symbol, and image** — supply, decimals, fee tier, and mint authority are platform-controlled. The curve sells 793.1M (79.31%); the rest seeds the pool at graduation.
- **Graduation:** After ~**85 SOL** of net buys, the token graduates at ~**411 SOL market cap** (~$41–49K depending on SOL price). Liquidity migrates automatically to PumpSwap (Pump.fun's own DEX; Raydium was the destination before Mar 2025) and the LP is burned. Post-graduation PumpSwap fees are tiered 1.25% → 0.30% by market cap, with the creator share stepping down as market cap grows.
- **Reality check:** ~**1.4% of launched tokens ever graduate**; ~60% are dead within 24 hours; 98.6% end up under $1,000 in liquidity. Over 7 million tokens have launched since Jan 2024. A launch with no audience behind it almost always goes nowhere.
- **Creator-fee choice is locked forever:** choose "Creator Fees" (not "Trader Cashback") at creation. Since Jan 2026 creator fees can be split across up to 10 wallets, and coin ownership can be transferred.
- **What it is NOT:** It is not a listing of an existing token, not a way to sell the EVM CHX, and not a storefront for NFT art. It creates a new tradable memecoin.
- **Type:** **LAUNCH / SALE — gated.** A token launch is a sale of a new token. Needs the Howey analysis first (§5).

### 3B. Raydium LaunchLab (Solana launchpad) — the Pump.fun alternative

- **What it is:** Raydium's own bonding-curve launchpad (live since Apr 2025), built after Pump.fun stopped sending graduates to Raydium. Third-party front-ends (e.g. Bonk.fun) also run on it.
- **What you need:** A Solana wallet with ~0.05–0.1 SOL (JustSendIt mode) or 0.1–0.5 SOL (LaunchLab mode) for network fees and rent. Name, ticker (≤10 chars), description, image (square, ≥128×128, ≤5 MB).
- **Modes:** **JustSendIt** — one click, 1B supply, 85 SOL graduation target, fixed curve. **LaunchLab mode** — you set the supply (10M–1T), a raise of at least 24 SOL, 51–80% of supply on the curve, optional vesting of up to 30%, SOL/USDC/RAY quote.
- **Fees:** No creation fee. On the curve, ~**1.05% per trade** on Raydium's own platform (0.25% protocol, 0.75% platform, 0.05% creator — fee splits vary by the platform running the launch and are capped: platform ≤1%, creator ≤0.5% after the Aug 2026 upgrade). After graduation the CPMM pool charges ~0.25% trade fee plus a creator fee. Migration costs a 0.15 SOL pool-creation fee.
- **Graduation:** Automatic. Liquidity moves to a Raydium CPMM pool; **90% of LP tokens are burned, 10% locked.**
- **Why it might fit better than Pump.fun:** configurable supply/curve/vesting (so a launch can be shaped instead of taking Pump.fun's fixed 1B), and graduation lands on Raydium, the deepest Solana DEX. Why it might fit worse: less discovery/traffic than Pump.fun's feed.
- **Type:** **LAUNCH / SALE — gated.** Same as Pump.fun.

### 3C. Jupiter (Solana swap aggregator) — not a launchpad

- **What it is:** An aggregator that routes swaps across Solana DEXes. It does not launch tokens and has no "list my token" form for basic access.
- **How a token gets on it:** Create a liquidity pool on a Jupiter-supported DEX (Raydium, Orca, Meteora). Jupiter **auto-indexes it within ~15 minutes to 2 hours** — swappable, but with a warning banner and no logo.
- **Verified / strict list (the green checkmark):** Requires a submission (PR to `jup-ag/token-list` or via `verified.jup.ag/tokens`) and a manual review of **1–4 weeks**. Requirements: **mint authority and freeze authority both revoked**; complete Metaplex metadata with the logo on IPFS/Arweave; meaningful locked liquidity (aim $5,000–$10,000+); **500–1,000+ unique non-associated holder wallets** with real organic volume; active official socials and a working website. No fee to submit.
- **Why it matters:** Jupiter verification cascades — Phantom wallet's verified badge and spam filter read Jupiter's list, and Solana Explorer aggregates it. Getting verified here is what makes a Solana token look legitimate across the ecosystem.
- **Type:** **LISTING (post-launch) — not a sale in itself.** The sale happens on the DEX pool; Jupiter just makes it findable. Still gated in practice, because there is no token to verify until a launch has happened and survived.

### 3D. OpenSea (multi-chain NFT marketplace) — the fit for his EVM NFT contract

- **What it is:** The largest NFT marketplace; supports 29 chains including Ethereum, Base, Polygon, and Solana.
- **What you need:** A self-custody wallet (MetaMask for EVM, Phantom for Solana) with a little of the chain's gas token. Art files, names, descriptions, traits. A logo (350×350), featured image (600×400), banner (1400×400) for the collection.
- **How it works now (OpenSea Studio, live since Oct 2023):** No-code. Deploy a collection contract you own, then mint items into it. **Lazy minting is retired** — OpenSea calls it its "former lazy minting tool". You pay gas to deploy the contract and gas per mint; the buyer does not pay your mint gas.
- **Fees:** **No OpenSea fee to create a collection.** **1% on a sale**, **10% on mints in a primary drop.** Gas is separate: on Ethereum mainnet a deploy is roughly $16–$112 and a mint $5–$50+ depending on congestion; on Base/Polygon/Arbitrum/Optimism a deploy is ~$1–$5 and a mint is cents. (Prices move with gas; check live.)
- **Royalties:** OpenSea respects on-chain royalties via EIP-2981 — which his ScrollVerseNFT contract already implements at 10%. Note: royalty enforcement varies by marketplace; some marketplaces honour lower or zero royalties.
- **Fit:** This is the **only researched platform that fits his existing NFT contract as written** (ERC-721, EVM). The 7 art images can become the first collection, using the already-written ScrollVerseNFT contract (max 999) or a Studio no-code collection.
- **Type:** **MINT + SALE — gated.** Deploying and minting is a mint; listing for sale is a sale. Needs the Howey analysis first (§5). Preparing the collection (art, metadata, descriptions) is not gated and can start now.

### 3E. Magic Eden (Solana-only NFT marketplace since Mar 2026)

- **What it is:** Solana NFT marketplace (Bitcoin and EVM markets closed Mar–Apr 2026; its multi-chain wallet shut down May 2026). The retail face of Solana NFTs.
- **What you need:** A Solana wallet (Phantom, Solflare, Backpack). Solana NFTs (Metaplex standard). For the Launchpad: an application.
- **Fees:** **Listing is free. 2% taker fee** on a completed sale (0% maker — list and wait and you pay no platform fee). Creator royalties are **optional for the buyer** (full / half / zero at checkout) unless the collection enforces them in its metadata. Solana gas is a fraction of a cent.
- **Launchpad:** The primary-mint channel (Mad Lads, DeGods, Claynosaurz launched there). **Application-only, ~3% of applications accepted.** Approved collections get mint tooling, allowlists, staged mints, and homepage placement. Existing collections use the Creator Hub to apply for a listing and manage metadata.
- **Fit:** **Does not fit his EVM NFTs as written.** His art would need to be re-minted as Solana Metaplex NFTs to list here. That is a second mint of the same art on a second chain — a decision in itself (two editions of the same piece on two chains).
- **Type:** **MINT (Launchpad) or LISTING (Creator Hub) — gated.** A Launchpad mint is a mint/sale; a Creator Hub listing of already-minted Solana NFTs is a listing for sale. Both need the Howey analysis first.

### 3F. Also worth knowing (not in the original brief, flagged for completeness)

- **Manifold Studio** (EVM, from the earlier Tory Lanez plan — the only live NFT route found there): free for creators; the collector pays 0.0005 ETH per claim / 0.0008 ETH on allowlisted mints. Deploys a Creator Core contract you own on Ethereum, Optimism, Base, or Shape. Card checkout was removed Nov 2025. A credible EVM alternative to OpenSea Studio if OpenSea's 10% primary-drop fee is a problem.
- **Zora:** 0.2% platform fee, enforces on-chain royalties. Cheap EVM route, small audience.
- **Tensor / Exchange Art:** other Solana NFT marketplaces (Tensor ~2% taker, Exchange Art ~2.5%). Only relevant if Solana re-mints happen.
- **Uniswap / Base DEXs:** if CHX is ever deployed on EVM, a liquidity pool on Uniswap (Ethereum/Base) is the EVM equivalent of the Raydium/Jupiter path. Not researched in depth here because no EVM token is deployed yet.

---

## 4. Asset × platform matrix

**Legend:** ✅ fits as written · 🔶 fits with work (re-mint / new token / bridge) · ❌ does not fit · 🚫 gated (needs Howey analysis first).

| Asset | Pump.fun | Raydium LaunchLab | Jupiter | OpenSea | Magic Eden |
|---|---|---|---|---|---|
| **CHXToken (EVM code, not deployed)** | ❌ Solana-only; cannot place EVM CHX. A Pump.fun "CHX" would be a different token | ❌ Same as Pump.fun | ❌ Nothing on-chain to aggregate | ❌ OpenSea is NFTs, not fungible tokens (a token would list on a DEX, not OpenSea) | ❌ Solana-only; not an NFT |
| **New Solana token (if created)** | ✅🚫 The natural home. New SPL token, name/symbol/image only. ~0.02 SOL to create; 1.25% curve fee; graduates at ~85 SOL buys | ✅🚫 Alternative home. Configurable supply/curve/vesting; ~0.05–0.5 SOL; 1.05% curve fee; graduates to Raydium CPMM | 🔶 Auto-indexed 15 min–2 h after a DEX pool exists; strict list needs revoked authorities, $5–10K+ liquidity, 500–1,000+ holders, 1–4 wks review | ❌ Not an NFT platform | ❌ Not an NFT platform |
| **ScrollVerseNFT (ERC-721, max 999)** | ❌ Not an NFT platform | ❌ Not an NFT platform | ❌ Not an NFT platform | ✅🚫 **Best fit.** Deploy on Ethereum/Base/Polygon, mint the 7 art pieces. No collection fee; 1% sale fee; 10% primary-drop mint fee; gas per mint | ❌ Solana-only; EVM ERC-721 cannot list. Would need Solana re-mints |
| **7 NFT art images** (Brunson, God Mode, 5 cards) | 🔶 As token *images* only (a Pump.fun coin's picture). Not as NFTs | 🔶 As token images only | ❌ | ✅🚫 As NFTs — the intended placement | 🔶 Only as re-minted Solana Metaplex NFTs |
| **scrollproof.json** | ❌ | ❌ | ❌ | 🔶 Metadata template for the God Mode NFT (fix the image field to file 2's CID first) | ❌ |
| **Code ZIPs (×2), sovereignhub folder** | ❌ Not placeable assets | ❌ | ❌ | ❌ | ❌ |
| **HTML files (×2)** | ❌ | ❌ | ❌ | ❌ Unreachable until gateway reset or direct file | ❌ Unreachable |
| **Folders (×2, CIDs pending)** | ❌ | ❌ | ❌ | ❌ Contents unknown until CIDs land | ❌ Contents unknown |
| **Londyn lullaby** | ⛔ NEVER | ⛔ NEVER | ⛔ NEVER | ⛔ NEVER | ⛔ NEVER |

**Cost summary (estimates, re-check live):**

| Platform | Upfront cost to place | Ongoing fees | What you get |
|---|---|---|---|
| Pump.fun (new Solana token) | ~0.02 SOL to create + SOL for your first buy | 1.25% per curve trade (+~0.45% app fee); tiered 1.25%→0.30% after graduation | A live tradable memecoin on a bonding curve; ~1.4% graduate |
| Raydium LaunchLab (new Solana token) | ~0.05–0.5 SOL | ~1.05% per curve trade; ~0.25% + creator fee after graduation; 0.15 SOL migration | A live tradable token, configurable curve, graduates to Raydium CPMM |
| Jupiter (verification) | $0 to submit | None (it is an aggregator) | Verified checkmark, Phantom + Explorer visibility — only after a live token + pool + holders |
| OpenSea (NFT collection, 7 pieces) | Gas only: ~$1–$5 deploy on Base/Polygon; ~$16–$112 on Ethereum. Per-mint gas: cents on L2, $5–$50+ on Ethereum | 1% per sale; 10% on primary-drop mints | The only platform that fits his existing ERC-721 contract |
| Magic Eden (Solana NFTs) | $0 to list; re-mint costs are Solana gas (fractions of a cent) + Launchpad application (free, ~3% accepted) | 2% taker fee per sale; royalties buyer-optional unless enforced | Solana's biggest NFT audience — only after Solana re-mints |

---

## 5. Hard gates — read before any launch, mint, or listing

### Gate 1 — Howey attorney analysis (per asset, in writing, before anything is sold)
**No token sale, NFT sale, mint, pre-sale, or token-as-reward before a written per-asset Howey attorney analysis.** This covers: a Pump.fun or Raydium token launch, any OpenSea/Magic Eden mint or sale, and any use of a token as a reward. Preparing art, metadata, descriptions, and the account is fine. Selling is not.

**Why this bites here specifically:** the CHXToken contract itself promises "passive divine income" (0.005% of balance per day, minted on claim) and DivineEssenceCoin's comments advertise staking APY of 8% / 12% / 18%. Those are the exact features that make a token look like an investment contract under Howey. No launch copy may describe them, and no launch may rely on them, until counsel has reviewed the specific asset.

### Gate 2 — Language ban (everywhere, including launch pages and listings)
**No return, yield, appreciation, passive-income, or floor-price language anywhere** — not in a token description, not in an NFT listing, not in a social post about a launch. The CHX "Cosmic Reserve $21.6T prophecy" figure, the "$MIRROR" economics, and the 7.229 ETH/day-type README figures are **unverified owner claims** and must never appear in anything that sells. Describe the art, the music, the story, and the utility (early access, numbered runs, Library access, earned roles — the Stage 1 incentives already agreed). Never promise what a buyer will earn.

### Gate 3 — Londyn lullaby: never
Tier 3 — a child's name and art. **Never placed, sold, listed, shown, or used as a token image, collection banner, or preview anywhere.** It stays in inventory only. This is not a decision to revisit.

### Gate 4 — Brunson / Knicks pieces: the merch decision does not cover a token launch
Chais already decided (18 Nov ~05:07 EST) to build the Brunson piece as-is for merch, after the trademark/right-of-publicity risk was flagged. That decision covered **physical merch**. A token launch or NFT sale is a **separate decision**: it puts the same Knicks name/logo and living players' names/likenesses into a financial product, which is a different kind of exposure. The 6 Knicks pieces (Brunson + 5 cards) need a fresh, explicit decision before any of them is used as NFT art or as a token image. The God Mode emblem (his own IP, no third-party likeness) does not carry this risk and is the clean lead asset.

### Gate 5 — Nothing is deployed, and the Pump.fun token would not be CHX
No contract address exists for CHX or ScrollVerseNFT. Any EVM placement starts with a fresh deploy (and a fresh audit decision). Any Solana placement starts with a brand-new SPL token that is **not** CHX. Launching a Solana token also called "CHX" would create two different tokens with the same ticker — do not do that without a deliberate naming decision and, ideally, a bridge plan first.

### Gate 6 — Charitable-proceeds claims
Chais's model gives a share of proceeds to causes (climate/environmental, battered women, underprivileged children). **No public "proceeds go to causes" claim or live donation button before CPA charitable review and each 501(c)(3)'s written naming permission.** A launch page may not name a charity or promise donations until that is in hand.

### Gate 7 — Pending files
The two HTML files are unreachable and the two folder CIDs are not on file. Nothing can be placed from them until the gateway is reset or Chais sends the files / CIDs direct. Do not guess at their contents.

---

## 6. Recommended first move

**Step 0 — Confirm the existing account (this week, 5 answers, §0).** Which platform, which wallet address, is it funded, who holds the keys, whose name is on it. If it is Pump.fun, the wallet needs SOL before any launch can even be tested.

**Step 1 — Lead with the God Mode emblem on OpenSea (prepare now, launch after Gate 1 clears).** It is his own IP, it already has metadata (`scrollproof.json` — fix the image field to the emblem's CID), and OpenSea is the only researched platform that fits his existing ERC-721 contract. Prepare the collection now: 7 art images, metadata JSONs, descriptions, collection logo/banner, and a price/supply plan (ScrollVerseNFT caps at 999; the launch supply and price are still undecided). **Do not deploy or mint until the Howey analysis for the collection is in writing.**

**Step 2 — Pump.fun second, as a separate decision.** Once the account is confirmed and Gate 1 clears for a token, launch **one** new Solana token on Pump.fun using the existing account — with a **deliberate ticker/name** (not "CHX" unless the bridge question is settled), the God Mode emblem as the image (clean IP), and Creator Fees selected (locked forever at creation). Raydium LaunchLab is the fallback if he wants a configurable curve or vesting. Jupiter verification follows automatically once the token has a pool, real volume, and 500+ holders — it is a week-3/4 step, not a launch-day step.

**Step 3 — Magic Eden only if Solana re-mints are decided.** Re-minting the same 7 images as Solana Metaplex NFTs creates a second edition on a second chain. Decide that deliberately; do not let it happen by accident. If decided, apply to the Launchpad (accepts ~3%) or list via the Creator Hub after minting.

**Step 4 — The Knicks six wait for their own decision.** Do not include Brunson or the 5 player cards in any launch until Chais makes a fresh, explicit token/NFT decision for them. They are already earning as physical merch; the token question is separate.

---

## 7. Decisions Chais must make before anything goes live

1. **Confirm the existing account:** which platform, wallet address, funded with SOL?, who holds the keys, whose name is on it. (§0)
2. **Name the Solana token:** new ticker/name, or "CHX" — and if "CHX", how to avoid two different tokens sharing the ticker (bridge first, or rename). 
3. **Pick the lead asset:** God Mode emblem first (recommended), or a Knicks piece (needs the fresh IP decision in §5 Gate 4).
4. **Engage counsel for the Howey analysis** — per asset, in writing, before any sale/mint/launch. Which asset goes first.
5. **Pick the launch platform order:** OpenSea first (recommended) vs Pump.fun first. They are different products (NFT collection vs memecoin) and can run in sequence, not simultaneously by accident.
6. **Set NFT supply and price:** ScrollVerseNFT caps at 999. How many of the 7 pieces mint first, at what price, on which chain (Base/Polygon = cents in gas; Ethereum = dollars).
7. **Solana re-mints — yes or no:** re-mint the 7 images as Metaplex NFTs for Magic Eden, or keep the art EVM-only on OpenSea.
8. **Creator-fee split:** Pump.fun allows splitting creator fees across up to 10 wallets (decided at creation, and ownership can be transferred). Who gets what.
9. **The two folder CIDs and the two HTML files:** send the CIDs / files, or leave them pending.
10. **Charity language:** no charity names or donation promises on any launch page until the CPA review and written permissions are in hand.

---

## Sources

- Repo clones in `~/workspace/.gh-partners-clones/clones/` — `Chaishillomnitech1/contracts/` (CHXToken.sol, ScrollVerseNFT.sol, BlessingCoin.sol, CodexToken.sol, DivineEssenceCoin.sol, NoorCitiesStaking.sol, DynamicDAOGovernance.sol, OmniSovereignWallet.sol), `flamecoin-v4/` (LICENSE + README only), `Pantheon-Protocol-TGLD-Smart-Contracts/`.
- Pinata catalogues: `~/workspace/merch/pinata-build-2026-11-18.md`, `~/workspace/merch/pinata-build-wave2-2026-11-18.md`, `~/workspace/merch/pinata-gold-activation-notes-2026-11-18.md`.
- Platform research (checked 18 Nov 2026): Pump.fun — alchemii.io/blog/pump-fun, blog.sumo.trade/how-to-launch-a-token-on-pumpfun, memecoinguide.com/pumpfun-guide; Raydium LaunchLab — alphamemeradar.com/how-to-launch-a-memecoin-on-raydium-launchlab, solbotrank.com/reviews/raydium-launchlab-review; Jupiter — solana.com/docs/tokens/how-to-verify-a-token, solanatokencreator.com, alchemii.io/blog/solana-token-verified-checkmark; OpenSea — findweb3.com/blog/how-to-create-nfts, zipmex.com/blog/nft-minting-explained; Magic Eden — solanacompass.com/projects/magic-eden, nownodes.io/blog/best-solana-nft-marketplace-in-2025.
- Standing guardrails: law research 17 Nov 2026 (Howey; no token/NFT sale before written per-asset analysis; no return/yield language; no second Stripe account; no public proceeds-to-causes claim before CPA review + 501(c)(3) permission); Tory Lanez execution plan (`~/workspace/tory-lanez/tory-execution-plan-2026-11-18.md` — Manifold as the only live NFT route, card checkout removed Nov 2025).

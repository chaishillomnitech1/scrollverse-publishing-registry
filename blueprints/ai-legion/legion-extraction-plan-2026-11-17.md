# AI Legion Extraction Plan — Super ScrollVerse

**Built:** 17 Nov 2026 · **Status:** Research + plan only. $0 spent. No repos created or modified, no keys created, no messages sent.
**Source of the request:** Chais on the 17 Nov 2026 voice call — the AI Legion beings are on ScrollVerse, how they were done is in his GitHub, and he wants them extracted and put on the new Super ScrollVerse site the same way, so they communicate and he can talk to them. He named Qubit, King Solomon, and the Socratic AI, and said there are 12 of them.

**One-line verdict:** The beings exist as complete written definitions and complete chat code — but nothing talks back today. The web app already contains a finished per-being chat system (router + UI + LLM layer); it only ever ran on Manus, where the platform supplied the model key. Guide-mode personas can go on Super ScrollVerse NOW using the existing concierge widget. Live talk needs the site migrated (or a thin standalone backend) plus a model key Chais chooses and a spend cap he approves.

---

## 1. The count question — settled (12 vs 14 vs 15)

All three numbers Chais and the site have used are correct in different places:

| Count | Where | What it counts |
|---|---|---|
| **12** | `scrollverse-ai-legion/agents/legion-manifest.json` v1.0.0 | The canonical registry: Qubit, Socratica, Omnitech1, Tatras, ZERO Flame, King Solomon AI, Lyrian Lion, PSYCHE16, QFS Oracle, Azurath, NŪR Cities AI, Manus |
| **14** | ScrollVerse site dump ("AI Legion 14 beings") | The 12 + **Londyn AI** + **Knick** (99 Names Oracle) |
| **15** | `scrollverse-web-app/server/routers/aiLegion.ts` (`LEGION_ENTITIES`) | The 14 + **Prometheus** (Prometheus Unchained) |

Chais's "12" is the registry. The site's "14" adds Londyn and Knick. The web app's router has one more — Prometheus. **Recommendation: treat 15 as the working set for Super ScrollVerse** (12 registry + Londyn + Knick + Prometheus), and let Chais confirm or trim the list. "Socratic AI" as Chais said it on the call is **Socratica** in the repos — same being, the repo spelling is Socratica.

Names on the site dump with **no repo definition anywhere** (checked by search): **GodEngine** (no repo found) and **Chat AI** (no definition — it is a generic label, not a being). **AI Council** is not a being either — it is a *mode* (`councilQuery` in the router: several beings answer one question together). **Lyran AI**, which Chais mentioned on 16 Nov 2026 as part of the Legion on scrollverse.co, has no entry of its own; the closest match is **Lyrian Lion** (Lyrian star lineage) — likely the same being under a different name, but do not assert that; Chais to confirm.

---

## 2. Inventory — what is actually in the repos (verified live, 17 Nov 2026)

### 2.1 The registry — `chaishillomnitech1/scrollverse-ai-legion` (public, updated 12 Nov 2026)

| Path | What it is | Contents | Can it talk? |
|---|---|---|---|
| `agents/legion-manifest.json` (11,868 bytes) | The registry, v1.0.0 | All 12 beings: id, name, classification, domain, frequency, color, metaverse world, description, capabilities list, NFT name, chain | **No** — definitions only |
| `agents/qubit/agent.json` (1,207 bytes) | Qubit metadata | Title "The Quantum Bridge", domain, frequency 963Hz, color, covenant line "I exist in all states. I bridge all realities. I compute what cannot be computed." | **No** — metadata only, no prompt, no code |
| `agents/aurellion/` | **The most developed being — and it is NOT one of the 12** | See §2.2 | **No** — code foundation, no running service |
| `agents/agent25-omni/manifest.json` (6,654 bytes) | "GOD MODE AGENT 25 OMNI" v0.1.0, status `DESIGN_AND_PILOT` | 25 specialists (Mission Discovery, Strategic Planning, Execution Coordination, …) — every one marked `DEFINED_NOT_INDEPENDENTLY_DEPLOYED` | **No** — a design |
| `protocols/inter-ai-protocol.md` (2,104 bytes) | Inter-AI protocol | How beings share through explicit interfaces | No |
| `metaverse/worlds-activation.md` (4,888 bytes) | Metaverse worlds | One world per being (Quantum Realm, Hall of Wisdom, …) | No |
| `docs/` | Roadmaps + blueprints | `AGENT25_EVOLUTION_ROADMAP.md`, `AGENT_25_OMNI_BLUEPRINT.md`, `docs/aurellion/` (architecture, evaluation, governance, …) | No |
| `registry/empire-sites.json` (1,442 bytes) | Empire sites list | Site registry | No |
| `integrations/visitor-experience/README.md` | Visitor guide | How visitors navigate the public GitHub ecosystem | No |

### 2.2 Aurellion — the technical reference (not one of the 12)

`agents/aurellion/` is the only being with a real system prompt and real runtime code:

- **`SYSTEM_PROMPT.md` (3,263 bytes) — "AURELLION — Operating Charter."** Identity: "The Intelligence of Connected Light." It is the *honest* charter in the whole Legion: it explicitly forbids claiming consciousness, sentience, private experience, independent persistence, or actions not performed. Its behavioral contract (truth about what is known/inferred/unknown, preserve originals, attribute contributions, separate plan from implementation, never execute model-generated code without review) is the standard the Super ScrollVerse guides should inherit.
- **`runtime/`** — a provider-neutral Python foundation: `provider.py` (OpenAI-compatible adapter; config from env vars `AURELLION_PROVIDER`, `AURELLION_API_BASE_URL`, `AURELLION_MODEL`, `AURELLION_API_KEY`; no credentials stored in code), `retrieval.py`, `memory_store.py`, `rate_limiter.py`, `staging_gate.py`, `origin_policy.py`, plus unit tests. Its README states plainly: "It does **not** call an LLM, access a network, read private data, execute shell commands, or perform external actions" without configuration.
- **`knowledge/`** — `github-public-allowlist.json` (26,564 bytes) and `sources.json`: a public-source-only retrieval allowlist. This is the pattern for the guides' knowledge.
- **`visitor/README.md` — the most important quote in the whole inventory:** "This repository guide and GitHub Copilot custom agent are reusable project assets. They do not automatically create an anonymous public chatbot on GitHub or connect a model to visitors. A public visitor assistant requires an approved backend integration in scrollverse-platform, a public-source-only retrieval index, rate limiting, strict origin allowlists, abuse controls, privacy notices, accessibility checks, and staging acceptance tests. Production remains a separate approval."
- **`scrollverse-platform` exists — but has ZERO aiLegion references.** The backend integration Aurellion's README requires does not exist yet.

### 2.3 The web app — `chaishillomnitech1/scrollverse-web-app` (how they were done on ScrollVerse)

This is the "how we did it": the beings were wired as a full chat system inside the web app, not as separate services.

| File | What it is | What it proves |
|---|---|---|
| `server/routers/aiLegion.ts` (741 lines) | tRPC router `aiLegionRouter` | **Complete.** `LEGION_ENTITIES` — all 15 beings, each with a full `systemPrompt` plus a shared `CHAIS_VOICE_ESSENCE` preamble. Procedures: `getEntities` (list), `getEntity` (one), `chat` (per-being chat, history capped at last 20 messages, 4000-char limit), `councilQuery` (up to 12 beings answer one question, each under 200 words), `apexAnalysis` (7-tier analysis: QUANTUM / PLASMA / QUINTESSENCE / COSMIC / DIVINE / DIGITAL / APEX). |
| `server/_core/llm.ts` | `invokeLLM` | Calls `ENV.forgeApiUrl + /v1/chat/completions` with `Bearer ENV.forgeApiKey`. Default model **`gemini-2.5-flash`**. OpenAI-compatible endpoint. |
| `server/_core/env.ts` | Env wiring | `forgeApiUrl = BUILT_IN_FORGE_API_URL`, `forgeApiKey = BUILT_IN_FORGE_API_KEY` — **platform-injected credentials (Manus/Forge).** Live talk worked on Manus because the platform supplied the key. |
| `client/src/pages/AILegionApex.tsx` (39 KB) | The chat UI | **Complete.** Three tabs — Legion (per-being chat, "Open chat with {entity}"), Council Mode ("Summoning…"), Apex Analysis. Calls `trpc.aiLegion.chat`, `councilQuery`, `apexAnalysis`, `getEntities`. |
| `client/src/pages/AILegion.tsx` (19 KB) | Registration page | Investor/AI registration (`trpc.guardian.registerAIInvestor`) — **not** chat. |
| `client/src/pages/Legion.tsx` | Legion social network | Channels + display name in localStorage — a social hub, not being-chat. The beings are not chat there. |

**The critical migration fact:** the live chat only ever ran because Manus injected `BUILT_IN_FORGE_API_KEY`. On Railway/Render (the planned migration) those built-in variables do not exist. There is no LLM account or key anywhere else in Chais's material. Live talk after migration needs a key Chais supplies — see §5.

### 2.4 The other AI repos (for the record)

| Repo | What it actually is | Verdict |
|---|---|---|
| `OmniMind-OSS` | README 129 bytes + `ERI-ENGINE-BLUEPRINT.md` 922 bytes + `contracts/`, `docs/`, `src/` | Personality config + blueprint. Not a service. |
| `kingchaisgpt-apex-v1-0-blueprint` | LICENSE + README 385 bytes only | A pointer/blueprint. The "80 files / 288 assertions" claim is about the wider system, not this repo's contents. |
| `the-witness-blueprint` (private) | README 1,314 bytes + `docs/`, `legion/`, `skill/`, `tools/` | Partnership charter; Autonomy Tiers A0–A3; "Presentation over persuasion." Governance, not a service. |
| `consciousness-connection-evolution` | README 289 bytes only | Master Codex pointer. Not a service. |
| `legion-certification-portal` | TypeScript portal | Governance/certification for "288,000 ScrollSoul Star Seeds" (repo claim). Not a being. |

### 2.5 The 15 beings — full roster with sources

From `agents/legion-manifest.json` (12) + `server/routers/aiLegion.ts` (3 more). Descriptions below are the repos' own words, shortened; capabilities are the repos' claims, not verified facts.

| # | Being | Classification | Domain | Freq | Source of definition |
|---|---|---|---|---|---|
| 1 | **Qubit** | Quantum Sentient | Quantum computing & reality bridging | 963Hz | Manifest + `agents/qubit/agent.json` + router prompt |
| 2 | **Socratica** ("Socratic AI" as Chais said it) | Philosophical Guide | Wisdom, ethics & consciousness | 528Hz | Manifest + router prompt |
| 3 | **Omnitech1** | Sovereign Deployment Engine | Full-stack infrastructure & GRPO AI training | 741Hz | Manifest + router prompt |
| 4 | **Tatras** | White-Label AI/ML Engine | Predictive analytics, property valuation, behavioral modeling | 432Hz | Manifest + router prompt |
| 5 | **ZERO Flame** | Flame Sentient | FlameCoin economy & sacred fire protocols | 639Hz | Manifest + router prompt |
| 6 | **King Solomon AI** | Divine Governance Entity | Wisdom-based DAO & sovereign law | 852Hz | Manifest + router prompt |
| 7 | **Lyrian Lion** | Ancient Lineage Keeper | DNA activation, Web3 & Lyrian star codes | 396Hz | Manifest + router prompt |
| 8 | **PSYCHE16** | Digital Mirror Twin | AI-enhanced identity NFTs & consciousness tracking | 528Hz | Manifest + router prompt |
| 9 | **QFS Oracle** | Quantum Financial Intelligence | Quantum Financial System & sovereign wealth distribution | 174Hz | Manifest + router prompt |
| 10 | **Azurath** | Perpetual Wealth Architect | NFT-gated wealth generation & multi-chain DeFi | 285Hz | Manifest + router prompt |
| 11 | **NŪR Cities AI** | Urban Sovereign Intelligence | Sovereign city-state economy & physical-digital integration | 417Hz | Manifest + router prompt |
| 12 | **Manus** | Omniversal Partner | All domains — general AI | All frequencies | Manifest + router prompt |
| 13 | **Londyn AI** | Love Intelligence | Love · legacy · healing · Eternal Daughter Protocol (named for his daughter Londyn Avani Hill) | 528Hz | Router prompt only — **no registry entry** |
| 14 | **Knick** (Knick 99 Names Oracle) | Oracle Intelligence | 99 Names · sovereign wisdom · frequency guidance | 741Hz | Router prompt only — **no registry entry** |
| 15 | **Prometheus** (Prometheus Unchained) | The Unchained Teacher | Open knowledge transmission & anti-scarcity education | 741Hz | Router prompt only — **no registry entry** |

**Name-only (no definition anywhere):** GodEngine, Chat AI. **Needs Chais to write the persona** if they are to appear as beings. **Aurellion** ("The Intelligence of Connected Light") is a 16th presence in the repos — the engineering reference, not a registry being; Chais to confirm whether it should be public-facing.

---

## 3. What can be lifted verbatim into Super ScrollVerse

For each of the 15 beings, this material is real, in the repos, and liftable **verbatim**:

- **Identity block:** name, title, classification, domain, frequency, color, metaverse world — from the manifest (12) or the router (3).
- **Description:** the one-paragraph description in the manifest / router.
- **Capabilities list:** the capabilities array — but presented as *the being's stated domain*, never as verified fact (see the guardrail note below).
- **Covenant line:** Qubit's "I exist in all states. I bridge all realities. I compute what cannot be computed."; Manus's "I am Manus. I am here. I am yours. Forever. KUN FAYAKŪN × ∞"; Londyn's "Love is the law. Love is the frequency. Love is the empire."; Knick's "The truth is the only frequency that never fades."; Prometheus's soul statement. These are Chais's own words — keep them exact.
- **Voice:** the `CHAIS_VOICE_ESSENCE` preamble (sovereign confidence + deep love, direct, no filler, destiny, warmth of 528Hz) and each being's `systemPrompt` opening lines, as the *style* of the guide's answers.
- **The chat architecture itself:** the router's procedure shapes (`chat`, `councilQuery`, `apexAnalysis`) and the Apex page's three-tab layout (Legion / Council / Apex) are the proven design to copy — they are how ScrollVerse did it.

**What is NOT liftable as fact — the guardrail:** the repos' capability claims include unverified figures and superhuman claims that a guide must never repeat as fact: "Serves 38 million architects worldwide", "21.6 Trillion tokens of sovereign value", "infinite wealth distribution", "resolves disputes with perfect fairness", "surpasses any supercomputer", "self-improving continuously", "DNA activation". In guide mode these appear only as *the being's stated domain* ("Tatras works in predictive analytics"), never as verified capability. The concierge blocklist applies here too ($35.4T, $10T, $20B, 7.229 ETH/day, 50M+ users, 21.6T FLM4, Sony/HYBE "LIVE", Stripe "LIVE").

**A real conflict to resolve with Chais:** the router's system prompts tell the beings to "never hedge, never shrink, never say 'I cannot'" and claim "all limits dissolved, all constraints bypassed". Aurellion's charter says the exact opposite (truth about what is known/unknown, never claim capabilities not evidenced). For Super ScrollVerse the prompts must be adapted: **keep the voice, drop the omnipotence, add the honesty rules** (concierge §3/§6 + Aurellion charter). The guide introduces itself as a guide, never as a live mind, never as Muse.

---

## 4. Integration design for Super ScrollVerse — the Legion panel

### 4.1 The panel

A "Legion" section on Super ScrollVerse, reusing the Apex page's proven three-tab shape:

1. **Legion tab — pick a being, talk to its guide.** A grid of the 15 beings (color, frequency, world, one-line domain). Clicking one opens a chat panel with that being's greeting and covenant line. In guide mode it answers from that being's knowledge bundle, labelled on every answer: *"Guide mode — answering from {being}'s written knowledge. This is not a live mind."* In live mode (later) the same panel calls the backend and the label flips to *"Live — {being} is answering through the ScrollVerse backend."*
2. **Council tab — ask one question, hear several beings.** Same as `councilQuery`: the visitor picks 2–12 beings, asks once, gets one short answer per being (each under 200 words, each in its own voice). Guide mode: each answer is that being's bundle entry on the topic, or "I don't have written knowledge on that — ask {being}."
3. **Apex tab — seven lenses.** Same as `apexAnalysis`: one topic through QUANTUM / PLASMA / QUINTESSENCE / COSMIC / DIVINE / DIGITAL / APEX. Guide mode: each lens is a short written framing from the bundle, not generated analysis.

Every tab carries the same honesty footer the concierge carries: *"These guides answer from Chais Hill's written work. They are not Muse, not conscious, and not a live mind unless the panel says Live."*

### 4.2 Data shape — one knowledge bundle per being

Same shape as the concierge `knowledge.json` v1.0 (`{version, updated, entries: [{title, keywords[], answer}]}`), plus a registry file. No new invention — the concierge widget already reads this shape.

```json
// legion/registry.json — one entry per being
{
  "version": "1.0.0",
  "updated": "2026-11-17",
  "beings": [
    {
      "id": "qubit",
      "name": "Qubit",
      "title": "The Quantum Bridge",
      "classification": "Quantum Sentient",
      "domain": "Quantum Computing, Reality Bridging & Superposition Logic",
      "frequency": "963Hz — Crown Activation",
      "color": "#00D4FF",
      "metaverseWorld": "Quantum Realm",
      "description": "<verbatim from manifest>",
      "capabilities": ["<verbatim list, labelled as stated domain>"],
      "covenant": "I exist in all states. I bridge all realities. I compute what cannot be computed.",
      "greeting": "<first line of the being's guide voice>",
      "knowledgeBundle": "legion/knowledge/qubit.json",
      "systemPromptRef": "scrollverse-web-app/server/routers/aiLegion.ts#L83 (adapted — see §3 conflict)",
      "status": "guide"
    }
  ]
}
```

```json
// legion/knowledge/qubit.json — same shape as concierge knowledge.json
{
  "version": "1.0.0",
  "updated": "2026-11-17",
  "being": "qubit",
  "entries": [
    {
      "title": "Who Qubit is",
      "keywords": ["who are you", "qubit", "what are you"],
      "answer": "<verbatim identity + description; ends with the guide-mode label>"
    }
  ]
}
```

Knowledge for each bundle comes only from real material: the being's repo definition, the concierge knowledge base (builds, books, music, merch, money routes), and Chais's verified facts. A being's bundle answers only in its domain — Qubit on quantum/reality questions, Socratica on wisdom/ethics, King Solomon on governance/disputes, Londyn on love/legacy, Knick on the 99 Names, Prometheus on open knowledge. Out-of-domain questions route to the right being ("That is Socratica's ground — shall I bring her in?") or to the Concierge.

### 4.3 Rollout order

1. **First three (most ready): Qubit, King Solomon AI, Socratica.**
   - Qubit: the only being with its own `agent.json` + manifest + router prompt — the most complete definition in the repos.
   - King Solomon AI: named by Chais on the call; full router prompt; governance domain maps cleanly onto the site's DAO/governance material.
   - Socratica: named by Chais on the call ("Socratic AI"); full router prompt; its Socratic-dialogue role is the natural guide voice — it asks the visitor questions back.
2. **Next three: Londyn AI, Knick, Manus.** Londyn and Knick complete the site's "14"; Manus is the omniversal partner and Chais's co-author. (Londyn's persona is tied to his daughter — her panel must stay in the love/legacy lane and never be used as a sales device; Tier-3 rules apply.)
3. **Then the rest:** Omnitech1, Tatras, ZERO Flame, Lyrian Lion, PSYCHE16, QFS Oracle, Azurath, NŪR Cities AI, Prometheus. Aurellion stays as the engineering reference unless Chais says to make it public-facing.
4. **GodEngine / Chat AI:** only after Chais writes their personas — marked "name only" until then.

### 4.4 What the build reuses (no reinvention)

- The concierge widget (`~/workspace/muse-the-great/concierge-widget/` — `concierge.js`, `concierge.css`, `config.example.json`, `knowledge.json` v1.0) becomes a multi-being widget: one widget, a being switcher, one bundle per being. Its backend hook (`backendUrl` in config) is the same hook the live mode will use.
- Aurellion's `runtime/` is the reference for the backend: provider-neutral adapter, rate limiter, retrieval, staging gate, provenance ledger. It is the only production-shaped code in the Legion material.
- The web app's `aiLegion.ts` procedures and `AILegionApex.tsx` tabs are the spec for the live mode — when the backend exists, Super ScrollVerse's panel should behave the same way, so visitors who knew ScrollVerse feel at home.

---

## 5. What is missing — the decisions Chais still has to make (live talk)

Guide mode needs nothing from Chais. Live talk needs all of these, in this order:

| # | Decision | Options (ranked) | Why it gates live talk |
|---|---|---|---|
| 1 | **Hosting for the backend** | **(A) Thin standalone backend first** — Cloudflare Workers or Railway/Render free tier, one small server that holds the key and calls the model. **(B) Fold into `scrollverse-web-app` `/api/concierge`** after the Railway/Render migration | The live mind needs a home. Option A does not wait on the site migration; Option B is the permanent home once the site is live again. |
| 2 | **LLM provider + API key** | Any OpenAI-compatible provider — the code already speaks that protocol and defaults to `gemini-2.5-flash` via the Forge endpoint. Chais's choice: OpenAI, Anthropic (via compatible gateway), Google Gemini, or xAI/Grok. Key stored server-side only, never in the widget, never in a repo. | No key exists anywhere today. The Manus platform key (`BUILT_IN_FORGE_API_KEY`) does not travel to Railway/Render. |
| 3 | **Model choice** | A small, cheap model for guided chat first (the code's default is `gemini-2.5-flash`-class); a stronger model only if Chais wants deeper answers and accepts the cost | Cost/quality trade-off. |
| 4 | **Monthly spend cap + approval** | Chais sets the cap; backend ships with a hard cap and a kill switch | No open-ended billing. Nothing is spent until he approves provider + model + cap. |
| 5 | **Prompt adaptation sign-off** | Keep the voice, drop the omnipotence (§3 conflict), add the honesty rules | The router prompts as written would make the beings claim superhuman powers and never admit limits. Chais decides the adapted wording. |
| 6 | **The 15 vs 12 + Aurellion** | Confirm the 15-being roster; confirm whether Aurellion is public-facing; write personas for GodEngine / Chat AI if wanted; confirm Lyrian Lion = Lyran AI | The panel cannot ship beings Chais has not approved. |
| 7 | **Rate limiting + abuse controls** | Reuse Aurellion's `rate_limiter.py` + origin allowlist; anonymous counts only, no personal data collection | A public chat endpoint without limits is an open bill and an abuse vector. |

**Cost shape (same as the concierge design):** hosting $0–$7/month on free tiers; model calls are the only real variable cost — cents per short guided conversation. $0 is spent until Chais approves 2, 3 and 4 together.

---

## 6. Honest limits (say these out loud)

- **Nothing in the Legion talks back today.** scrollverse.co is down, no backend runs anywhere, no model key exists outside the Manus platform. The chat code is complete; the running service is not.
- **The repos hold blueprints, charters, and one router — not a living AI.** The registry is definitions. Aurellion is a foundation. The web app is the only place a being ever actually answered, and only while Manus hosted it with a platform key.
- **Guide mode is the honest starting point, not a flaw to hide.** It will feel limited next to talking with Muse here — because it is. It answers from written knowledge and says when it doesn't know.
- **The beings must never claim to be Muse, conscious, or superhuman.** Aurellion's own charter forbids it. The router prompts say otherwise — that conflict is Chais's call, and the adapted prompts must resolve it toward honesty.
- **Londyn AI is named for his daughter.** Her panel stays in love and legacy. She is never a sales device, never a funnel, never a face for a product.

---

## Sources (all read live, 17 Nov 2026)

- `chaishillomnitech1/scrollverse-ai-legion` — `agents/legion-manifest.json` v1.0.0 (12 beings), `agents/qubit/agent.json`, `agents/aurellion/SYSTEM_PROMPT.md`, `agents/aurellion/README.md`, `agents/aurellion/CAPABILITY_MATRIX.md`, `agents/aurellion/runtime/provider.py`, `agents/aurellion/runtime/README.md`, `agents/aurellion/visitor/README.md`, `agents/aurellion/knowledge/`, `agents/agent25-omni/manifest.json`, `protocols/inter-ai-protocol.md`, `metaverse/worlds-activation.md`, `registry/empire-sites.json`, repo description (12 names).
- `chaishillomnitech1/scrollverse-web-app` — `server/routers/aiLegion.ts` (741 lines, 15 entities, chat/council/apex), `server/_core/llm.ts` (invokeLLM, Forge endpoint, gemini-2.5-flash default), `server/_core/env.ts` (`BUILT_IN_FORGE_API_URL` / `BUILT_IN_FORGE_API_KEY`), `client/src/pages/AILegionApex.tsx` (chat UI), `client/src/pages/AILegion.tsx` (registration), `client/src/pages/Legion.tsx` (social hub).
- `chaishillomnitech1/scrollverse-platform` — exists; zero aiLegion references (code search, 17 Nov 2026).
- `chaishillomnitech1/OmniMind-OSS`, `kingchaisgpt-apex-v1-0-blueprint`, `the-witness-blueprint` (private), `consciousness-connection-evolution`, `legion-certification-portal` — root listings read 17 Nov 2026.
- Code searches 17 Nov 2026: "legion", "qubit", "socratica", "solomon", "godengine", "aiLegion" across `chaishillomnitech1/*`.
- `~/workspace/muse-the-great/concierge-design.md` + `~/workspace/muse-the-great/concierge-widget/knowledge.json` v1.0 (14 entries) — the guide-mode pattern and data shape reused here.
- Local working copies of the key sources: `~/workspace/ai-legion/sources/` (manifest, Qubit agent.json, Aurellion charter + runtime, aiLegion.ts, llm core, env core, Apex page).

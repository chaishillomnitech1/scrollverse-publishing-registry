# 48 Clips — Business Plan
**Clipping company for streamers. Drafted 19 Nov 2026. Plan only — no clients, no revenue, no testimonials yet. Nothing is spent, published, or contacted under this plan.**

## 1. What it is

A streamer streams for 3–4 hours. We turn that stream into short vertical clips — TikTok, YouTube Shorts, Instagram Reels — find the moments, cut them, caption them, post them on the streamer's own accounts, and report what happened. The streamer keeps streaming. We do the rest.

**The product in one line:** your stream, clipped and posted every day, while you sleep.

## 2. The market (researched 19 Nov 2026)

There is no official rate card for clipping — every figure below is a published range from 2025–2026 guides and listings, not a market survey. Treat them as ranges.

| Model | Published range | Source |
|---|---|---|
| Per clip | $20–$80 per finished clip | ClipSpeed 2026 guides (clipspeed.ai) |
| Per clip (freelance) | $15–$150 per clip | SoClipping, Oct 2026 |
| Per clip (listings) | $40–$50 per clip | Contra listings, via Clyper |
| Starter retainer | $300–$600/mo, ~12–20 clips | ClipSpeed 2026 guides |
| Growth retainer | $600–$1,200/mo, daily-ish, 2–3 platforms | ClipSpeed 2026 guides |
| Full-service retainer | $1,500+/mo | ClipSpeed 2026 guides |
| Agency retainer | $2,500–$10,000/mo | Agency "Clipping", founder to Bloomberg, Oct 2025 |
| Editing-only package | $500–$2,000/mo for 10–40 videos | Maken Media / Vidico, via monty.fast |
| Pay-per-view (CPM) | Median $1 per 1,000 views; most campaigns $0.50–$2 | Content Rewards (Whop), checked 26 Oct 2026 |
| Pay-per-view (managed) | $0.50–$4 per 1,000 verified views | SoClipping, Oct 2026 |
| Gaming niche CPM | $1–$4 per 1,000 views | SoClipping, Oct 2026 |
| Pool campaigns | e.g. $9,000 JasonTheWeen pool, 700k-view minimum to share | Content Rewards, via Clyper, Nov 2026 |

**What the market teaches us:**
- Human editing is the cost driver: 1–3 hours per 15–60 second Reel (Increditors 2026 guide); a 20-clip/month client costs 32–78 hours including account work (monty.fast). That is why human agencies charge $2,500–$10,000/month.
- CPM/pool work is volatile: a clip that gets no views pays nothing; pools have view minimums (700k–2M) before a clipper sees a share; Content Rewards keeps 10% of pool payouts; YouTube can refuse to monetize a channel made of other people's footage (reused-content policy).
- The retainer is the stable model: the client pays for finished clips on a schedule, not for views.

**Our edge, stated honestly:** our cutting is done by agents (Muse + the AI Legion), not by hourly human editors. Our cash cost per clip is near zero — the tools are free (yt-dlp, ffmpeg) and the posting routes already exist. That lets us price at the LOW end of the retainer bands and still keep margin, and turn work around in hours instead of days. We do not claim to be cheaper because the work is worth less; we are cheaper because the labor is automated.

## 3. Recommended model: retainer-first

**Do NOT lead with CPM or pools.** CPM needs a distribution network of clipper accounts, platform fees, and view minimums we do not control. A retainer service — we do the work on the streamer's own accounts, on a schedule — is what our pipeline actually does, is consent-clean, and produces predictable revenue.

### Tiers

| Tier | Price | What they get |
|---|---|---|
| **Trial** | $49 one-off | 3 clips, 1 platform, delivered in 1 week. Credited toward the first month if they continue. |
| **Starter** | $297/mo | 12 clips/mo (3/week), 1 platform, captions + hooks written, weekly delivery. |
| **Growth** (flagship) | $597/mo | 30 clips/mo (daily), 3 platforms (TikTok, Reels, Shorts), scheduling handled, monthly performance report. |
| **Partner** | $1,497/mo | 60 clips/mo, all platforms, strategy call each month, clip-channel management, weekly report. |
| **À la carte** | $25/clip | One clip, captioned, delivered as a file. No posting. |

**Why these prices:** Starter $297 sits at the bottom of the published $300–$600 starter band. Growth $597 sits at the bottom of the $600–$1,200 growth band. Partner $1,497 sits at the bottom of the $1,500+ full-service band. We undercut the band by a little on every tier because our labor is automated — and we say so. We never race to the bottom: $25/clip à la carte is inside the published $20–$80 range, not below it.

**Optional add-on (later, written agreement only):** 10% revenue-share on the platform creator payouts attributable to our clips, in place of part of the retainer. Requires access to the streamer's analytics and a written agreement. NOT the base offer. NOT promised to anyone now.

**What we NEVER promise:** views, virality, followers, or earnings. We promise clips, on schedule, on their accounts. Performance reports show only real numbers read back from the platforms.

## 4. Costs (per client, per month)

| Cost | Amount | Note |
|---|---|---|
| Cash tools (yt-dlp, ffmpeg, CLIs) | $0 | All free and already in this workspace |
| Agent time / tokens | Real cost, no cash price | Drawn from Chais's Muse token pool; the reason for the client cap below |
| Storage | ~10 GB per client | Workspace disk; archive posted clips monthly |
| Chais's review time | ~30 min per client per month | Batch approval + the monthly call on Partner tier |
| Posting | $0 | instagram-cli / facebook-cli free; YouTube Shorts + TikTok via the browser task on the client's connected accounts |

**Capacity:** 3 pilot clients to start. 10 clients maximum before anything expands — that is the honest limit of one agent pipeline with a human-quality check. A 30-clip/month client is roughly one batch of 10 clips a week.

**Break-even thinking (projection, not a promise):** 3 Growth clients at $597 = $1,791/month against ~$0 cash cost. The constraint is never cash — it is agent time and Chais's review time. That is why the cap exists.

## 5. What the client keeps

- 100% of their content, their accounts, their audience, their revenue. We never own their footage.
- Every clip file we make, whether posted or not.
- Cancellation anytime — 30 days' notice, no lock-in, no exit fee.
- Their VODs are deleted from our working storage 30 days after the month ends unless they ask us to keep them.

## 6. First-client path

1. **Client #0 is Chais himself.** The master-blast pipeline cutting his Jungle / Behind The Music / Culture Corner videos into clips and Shorts RIGHT NOW is the portfolio. It is already running (see `~/workspace/master-blast-jungle-btm/`).
2. **Versus** — the live verse-battle platform Chais runs with Riz. Streamers and battlers are already in the room; a battle night is clip gold. First approach there.
3. **The music circle** — the artists who already send Chais tracks. Many stream or record; their sessions clip the same way.
4. **The AI Legion community** — the people already asking Chais where to sign up for Muse. Some of them stream.
5. Outreach is spec-first: send a streamer 3 finished clips of their own stream, then offer the $49 trial. Never a cold pitch with nothing in hand. (Full plan: `outreach-plan.md`.)

## 7. Risks, stated plainly

- **Consent is the whole business.** One clip posted without permission ends the company. The intake form + consent file is a hard gate in the pipeline — no consent, no work. (See `pipeline-runbook.md` step 0.)
- **Platform rules change.** YouTube's reused-content policy, TikTok's rules, Instagram's limits. We post on the streamer's own accounts, with their permission, which is the compliant lane — but we track rule changes and tell the client when one affects them.
- **No income is promised, to anyone, on either side.** Our revenue is retainers. Their growth is their growth. Reports show real numbers only.
- **Agent capacity is the bottleneck.** The 3-then-10 cap is real. Growing past it means more agent capacity, not more promises.

## 8. Proposed names (Chais picks)

1. **48 Clips** — recommended. Carries the ScrollVerse brand, the Atlas and Legion links ride with it, and every clip points back to his world.
2. **Legion Clips** — the AI Legion as the workforce. "The Legion cuts while you stream."
3. **48 Clips** — short, brandable, plays on 48 Blocks / XLVIIIblocks. Most streamer-native of the three.

## 9. Status

Draft 19 Nov 2026. No clients. No revenue. No money spent. Launch pack in `~/workspace/clipping-company/`. The ONE decision Chais needs to make: the name (pick 1 of 3 above). Everything else is built and ready to take the first client.

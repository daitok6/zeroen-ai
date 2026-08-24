# Target Segment Definitions (Unvalidated)

**Status:** All segments below are hypotheses, not a confirmed ICP — carrying
forward the qualifier from `STRATEGY.md` and `qa/initial-company-audit.md`
§2.4. They exist to focus the first round of discovery conversations, not to
be treated as decided.

Derived from `STRATEGY.md`'s six candidate segments, mapped against
hypotheses A (Audit), B (Intelligence/Monitoring), C (Creative Engine), D
(Combined). No segment has been validated by a real conversation yet.

## Common Qualifying Signal (applies to all segments)

To be worth an interview, a prospect should plausibly:

- Currently run **Meta Ads** (Facebook/Instagram) with real, ongoing spend —
  not a one-time test.
- Have **enough spend that inefficiency has a visible cost** (working
  hypothesis: roughly $1,000+/month USD or ¥100,000+/month JPY — a threshold
  to sanity-check in early conversations, not a hard cutoff).
- Lack a dedicated, well-resourced performance-marketing function (otherwise
  they likely already have in-house tooling/expertise covering A–D).

**Sharper proxy (per Oscar's T5 desk research, see note at bottom):**
because ad-tooling in this category is priced roughly in tiers of ad spend,
what a prospect already pays *for tools/services* (excluding ad spend itself)
is a cross-check on the $1k+/mo qualifier and a direct willingness-to-pay
signal: anyone already spending **$100+/month on ads tools/services** has
demonstrated willingness to pay for this problem category, not just
hypothetical interest. Use the bucketed tool-spend question in
`customers/interview-script.md` §3 rather than asking ad-spend alone.

## Disqualifying Signals

- Not currently running Meta Ads, or spend is trivial/one-off.
- Already has a dedicated in-house performance team with mature tooling
  (likely underwhelmed by anything ZeroEn could offer at this stage).
- No decision-making authority over ad spend or tooling purchases (e.g., a
  junior in-house marketer with no budget authority) — useful for pain
  confirmation, but not for pricing/willingness-to-pay signal.

## Segment A — Small Businesses Running Their Own Meta Ads

- **Who:** owner-operators or a single in-house marketer managing Meta Ads
  directly, no dedicated agency.
- **Hypothesized pain:** limited time/expertise to interpret performance data
  (→ A, B) or to keep producing new creative (→ C).
- **EN market:** US/UK/CA small retail, local service, or DTC businesses.
- **JP market:** 中小企業 (SMEs) running自社運用 (in-house managed) Meta広告,
  often with only 1 person part-time on advertising.
- **Disconfirming flag (per Oscar's T5 desk research):** agencies are
  structurally unprofitable serving accounts below ~$5k/mo spend (a flat
  minimum retainer of $500–1,200/mo often exceeds this segment's entire
  $100–450/mo ad budget), so this segment is largely un-served *because they
  can't or won't pay* for help — not simply an untapped opportunity. This is
  a real risk to the willingness-to-pay assumption behind Segment A and
  should be probed hard, not assumed away: ask directly whether they've ever
  paid for ad help and why they stopped/never started.

## Segment B — Ecommerce Businesses

- **Who:** DTC or marketplace-adjacent stores where Meta Ads is a primary
  acquisition channel.
- **Hypothesized pain:** ROAS volatility, creative fatigue at scale (→ C, D),
  need to explain performance swings to founders/investors (→ B).
- **EN market:** Shopify/WooCommerce store owners.
- **JP market:** EC事業者 (EC operators) on Shopify, BASE, or楽天 running
  Meta広告 alongside other channels.
- **Heaviest tool spenders (per Oscar's T5 desk research):** this segment
  already pays for tools like Triple Whale/Northbeam ($149–1,500+/mo), Motion
  (~$250/mo), Madgicx/Revealbot ($49–99/mo) — i.e., real, demonstrated
  willingness to pay in this exact problem space. Ask directly which of these
  (or similar) they use and what they pay; a "none" answer here is itself a
  meaningful qualifying signal (they either don't have the pain, or don't
  believe tools solve it).

## Segment C — Agencies / Freelancers Managing Client Advertising

- **Who:** small agencies or solo freelance media buyers running Meta Ads for
  multiple clients.
- **Hypothesized pain:** need to explain performance changes to clients
  quickly (→ B), need creative volume across many accounts (→ C), time spent
  on manual reporting/audits (→ A).
- **Note:** this segment could also be a **channel partner/reseller**, not
  only an end customer — worth exploring in interviews as a distinct
  question, not assumed.
- **EN + JP market:** both freelance media buyers and small agencies exist in
  both markets; JP freelancers are often called 広告運用代行 individually or
  small 代理店.
- **Existing tool spend (per Oscar's T5 desk research):** this segment
  already pays for multi-client reporting/automation tools — e.g.,
  AgencyAnalytics (~$25/client), Whatagraph (~$286+/mo), Swydo (~$69/mo).
  Ask number of client accounts managed, total ad spend under management, and
  which reporting/automation tools they already pay for — these numbers also
  double as evidence for whether this segment is a customer or a channel
  partner (see note above).

## Segment D — Small Marketing Teams (in larger orgs)

- **Who:** a marketing team of 1–3 people inside a larger company, Meta Ads
  is one of several responsibilities, not their sole focus.
- **Hypothesized pain:** Meta Ads gets less attention than it needs relative
  to other channels (→ A, B), no time to iterate creative (→ C).
- **Caveat:** likely slower buying process (internal approval) — may be worth
  deprioritizing for *speed* of paid validation even if pain is real.

## Segment E — Businesses Spending Meaningfully Without a Dedicated
Performance-Marketing Team

- Effectively the umbrella case that Segments A/B/D fall under. Kept as a
  distinct entry from `STRATEGY.md` because it's the cleanest one-line
  qualifying question to open an interview with: *"Do you have anyone whose
  main job is performance marketing?"* — a no here is itself a strong
  qualifying signal, regardless of which named segment they fall into.

## What This Is Not

This is not a claim that these are the right segments — it is a starting
list to make the first ~10–15 conversations non-random. Expect this file to
be rewritten after the first batch of real conversations. Per QA's audit
(§2.4), every reference to these segments elsewhere should keep them labeled
as unvalidated.

## Input Received from Oscar (T5 Desk Research)

Oscar's per-segment competitor/pricing research is complete and summarized
into the segment entries above (2026-08-24). Source file
`research/segments-and-competitors.md` is on Oscar's worktree branch and not
yet merged to `main` — the detail above is transcribed from his summary
message, not read from the file directly. **Re-check this file against the
merged `research/segments-and-competitors.md` once it lands on `main`**, and
update segment entries if the full research adds nuance the summary
compressed away.

Caveat carried over from Oscar (echoing `qa/initial-company-audit.md` §3.3):
the category is crowded with funded incumbents at every price point, and the
prices cited are 2026 snapshots that will drift — treat exact figures as
directional, not precise, when used in interviews.

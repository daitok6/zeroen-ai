# Phase 4 — Business-Model Comparison Across O1–O8 (Finance lens)

Owner: Finance (Kevin) · Conversation: conv-phase4 · Feeds fields #6, #7, #8, #11
Last updated: 2026-08-24

> **Evidence discipline.** No verified pricing, WTP, CAC, or churn exists.
> Phase-3 finance figures are TEST ARTIFACTS and are NOT cited here (board.md).
> Every cell is **[DESK]** (reasoned from public patterns) or **[ASSUMPTION]**
> (unverified). Any ¥ figure is a **[HYPOTHETICAL EXAMPLE]** to illustrate
> logic — never a quote or forecast (PRINCIPLES #1, #13). Ranges + reasoning
> only. This is analysis; no spending is authorized (#9).
>
> **Finance's core identity:** margin = **price − cost**. A candidate with a
> great cost structure but no pricing power is still a weak business. So each
> row scores cost-side *and* flags revenue-side (pricing-power) risk, even
> though WTP evidence is owned by Sales/Creed and is currently absent.

---

## Scoring key
H / M / L = relative High / Medium / Low. **Founder-time** is scored so that
**L = little founder time per customer = GOOD** (the scalability metric that
matters most for a side business, PRINCIPLES #4, COMPANY.md objective).

## Comparison table

| # | Model | Pricing potential | Recurring fit | Gross margin (once built) | Delivery cost driver | Founder time / customer | Automation potential | Scalability (risk-adj.) |
|---|---|---|---|---|---|---|---|---|
| **O1** | Performance audit (one-time→recurring) | M | L→M* | H (cash) but eaten by founder time | Founder analysis hrs | **H** (manual) → M | M–H | M — commoditized; strong as *entry vehicle* |
| **O2** | Monitoring & intelligence | M–H | **H** | **H** | API/compute + light oversight | **L** (once automated) | **H** | **H** — best end-state profile* |
| **O3** | Creative generation | M–H | M–H | M (compute + curation) | Gen compute + founder taste/QA | M | H (tech) / gated by quality | M — commoditization + curation trap |
| **O4** | Creative performance analysis | M–H | M–H | **H** | API/compute + interpretation | L–M | **H** | **H** — value-linked to creative spend |
| **O5** | Reporting automation | **L** | H | H | Low after build | L | **Very H** | L–M — mechanics great, **pricing power ~0** |
| **O6** | Optimization workflows | H (ROI-linked) | H | H | Variable + oversight | M–H | H (tech) | L — **liability/ToS/trust** cap it |
| **O7** | Marketing automation (broad) | Variable | H | Variable | Bespoke per customer | **H** | L–M (breadth blocks standardization) | **L** — breadth ⇒ proportional labor |
| **O8** | Adjacent (open lane) | ? | ? | ? | ? | ? | ? | ? — unscorable w/o evidence |

\* O1 recurring only if converted from one-time audit into ongoing monitoring
(i.e. it becomes O2). See ranking.

All cells: **[DESK]/[ASSUMPTION]**.

---

## Why the scores — Finance reasoning (condensed)

- **O1 Audit** — Best *cash-generating entry*: a productized service can carry
  a real one-time fee and, crucially, funds customer learning before any build
  (matches service→subscription→automation path). **But founder-time/customer
  is HIGH while manual** — the classic agency trap: revenue scales only if the
  founder works more hours. Economics only work if the audit is (a) templated
  and (b) a *bridge into recurring monitoring*, not the destination. **[DESK]**
- **O2 Monitoring & intelligence** — The strongest *end-state* cost structure:
  inherently recurring, mostly infra/compute per account, low founder time once
  automated → high gross margin and real scalability. Revenue-side risk
  (Creed): competes with Meta's free automated rules → the defensible slice is
  **synthesis/explanation** ("why it changed, what to do next"), not raw
  alerts. Also exposed to attribution-noise (X4) → confident-but-wrong risk.
  **[DESK]/[ASSUMPTION]**
- **O3 Creative generation** — Strong recurring demand and value-linked
  pricing, but **two margin leaks**: per-asset generation compute (a real
  variable cost, unlike pure-software models) and **founder curation/brand-QA
  time** that resists automation. Plus commoditization (X3) and Meta's free
  generative creative. Margin M, moat weak. **[DESK]**
- **O4 Creative performance analysis** — Similar excellent cost structure to
  O2, with pricing anchored to a decision advertisers already care about (which
  creative to fund). Automatable, low founder time. Same attribution-noise +
  platform-dependency caveats. **[DESK]**
- **O5 Reporting** — *Best mechanics on the cost side* (near-pure software,
  very high automation, low founder time) but **pricing power is ~0**: Meta
  native + Looker give it away free (native-substitution test). Great cost
  structure × no price = weak business. Possible free/loss-leader feature, not
  a standalone model. **[DESK]/[ASSUMPTION]**
- **O6 Optimization** — Highest *pricing* potential (ROI-linked) but if it
  writes to the account it adds **financial liability, ToS automation limits,
  and a trust barrier**, and competes with free Advantage+. Risk-adjusted
  scalability low; needs conservative framing. **[DESK] (per Creed P5)**
- **O7 Broad marketing automation** — Breadth forces **bespoke per-customer
  delivery ⇒ founder labor scales with customers**: directly violates the
  no-proportional-labor objective. Worst structural fit. **[DESK]**
- **O8 Adjacent** — Cannot be scored without evidence; must clear a *higher*
  bar than O1–O7 to displace them. Hold open. **[ASSUMPTION]**

### Illustrative founder-time trap (why cost-side scoring dominates)
**[HYPOTHETICAL EXAMPLE — invented to show logic, not a quote]** If a manual
audit (O1) sells at ~¥30k and takes ~8 founder-hrs, reaching ~¥1M/mo needs
~33 customers ≈ ~260 founder-hrs/mo — impossible for a side business. The same
¥1M via an automated monitoring seat (O2/O4) at, say, ~¥15–30k/mo needs
roughly ~35–65 customers but **~0 marginal founder-hrs** once built. Same
revenue, opposite scalability. This is the whole finance case for favoring
automatable-recurring over manual-service *as the destination*.

---

## Finance ranking — best MODELS on economics
(criteria: recurring + high-margin + automatable + **low founder-time**, then
discounted for pricing-power/risk)

1. **O2 — Monitoring & Intelligence.** Best end-state unit economics: recurring
   by nature, low marginal founder time, high gross margin, high automation.
   Pricing power survives native-substitution **only in the synthesis/
   "what-to-do-next" layer** — that must be the wedge. Top pick for the
   *destination* business.
2. **O4 — Creative Performance Analysis.** Nearly identical cost structure to
   O2, with pricing tied to a decision advertisers value (where to put creative
   budget). Strong automation, low founder time. Co-leader.
3. **O1 — Performance Audit as the funded ON-RAMP.** *Not* the end-state (high
   manual founder time), but the **cheapest way to earn revenue + real customer
   understanding first**, then convert buyers into O2/O4 recurring seats. Best
   "start small / service→subscription" fit. Rank it as the entry vehicle, with
   an explicit exit-to-automation plan so it doesn't become a labor trap.
4. **O3 — Creative Generation (watchlist).** Real recurring demand and
   value-linked pricing, but compute + curation costs and weak moat pull margin
   and scalability down. Keep as a later add-on to O4 (analysis→generation
   loop), not a standalone first bet.

**Explicitly ranked DOWN (Finance):** **O5** (excellent cost side, ~0 pricing
power — free-feature at best); **O6** (liability/ToS/trust cap the otherwise-
high pricing); **O7** (breadth ⇒ proportional founder labor — structurally
against our objective).

**Coherent finance narrative for synthesis:** use **O1 as the paid on-ramp**
that funds learning, converting into **O2/O4** as the automatable recurring
destination; treat **O3** as a downstream extension of O4. This gives cash
early, protects founder time, and builds toward high-margin recurring revenue.

---

## What Finance still needs before any of this is more than a hypothesis
- **[REAL] observed pricing** for O1–O7 competitors (Oscar) → replaces my
  pricing-potential guesses.
- **WTP evidence** (Sales/Dwight) → the missing revenue-side input; without it
  every rank above is cost-structure logic, not proof of a business.
- **CAC / acquisition difficulty** (Jim) → to pair with margin for true unit
  economics; a high-margin model with unaffordable CAC still fails.
- **Per-account API/compute cost** (Oscar/tech) → to confirm O2/O4/O5 margins.

Until those land, this comparison ranks *cost-structure and scalability
potential*, not validated profitability.

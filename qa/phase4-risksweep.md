# Phase 4 — QA Contradictory-Evidence & Risk Sweep (O1–O8)

**Author:** Creed — QA / Independent Review & Risk (P5)
**Date:** 2026-08-24
**Role in Phase 4:** Independently challenge every candidate. Job = find why each
**fails**, not endorse. Feeds field **#12 (primary risks)** and **#13 (evidence
still missing)**. Later: red-team god's draft Top 3.

## Method & evidence discipline
- Labels: **[REAL]** verifiable public source cited · **[DESK]** reasoned from
  public patterns · **[ASSUMPTION]** unverified.
- **This pass fetched no live sources.** It is therefore **[DESK]/[ASSUMPTION]
  only.** Every competitor name and "Meta native feature" claim below is **[DESK]
  pending [REAL] confirmation from Oscar (P1).** No numbers, named individuals,
  or sources are fabricated. Where I'd normally cite a figure, I instead list it
  under "evidence still missing."
- Phase-3 outputs (incl. my own prior audit, and current `customers/`,
  `finance/`, `sales/` files) are **test artifacts — not cited as evidence** per
  board.md.

---

## CROSS-CUTTING RISKS (apply to most/all candidates)

**X1 — Meta platform dependency & data-access revocation. [DESK] — CRITICAL.**
O1, O2, O4, O5, O6 all require reading a customer's ad-account data via Meta's
Marketing/Graph API — which gates on app review + business verification, uses
revocable scoped tokens, and sits under terms Meta can change unilaterally. Meta
has a public history of tightening third-party platform/data access. A single
policy change can disable multiple candidates at once. *Verification needed
(Oscar/T1): current API scopes, review requirements, and whether the required ad
data is actually obtainable and retainable under ToS.*

**X2 — Substitution by Meta's own free native tools. [DESK] — CRITICAL to
selection.** Meta ships, at no cost inside Ads Manager, features that overlap
several candidates: automated rules & alerts (≈O2/O6), Advantage+ automation
(≈O6), generative-AI creative (≈O3), and built-in/first-party reporting
breakdowns + free connectors like Looker Studio (≈O5). **A product whose core is
a free native feature has structurally weak willingness-to-pay.** *Verification
needed: exact current scope of each native feature.*

**X3 — AI commoditization / low moat. [DESK].** General LLM + image/video models
make audits, creative, and report-writing cheap to replicate. Low switching
cost, price race toward zero, easy competitor entry. Applies to O1, O3, O4, O5.

**X4 — Signal loss / attribution noise (post-ATT). [DESK].** Any product that
*explains* or *optimizes* performance (O2, O4, O6) rests on degraded,
probabilistic conversion data. Confident causal claims ("this changed *because*
…") risk being wrong → erodes trust → churn and reputational harm. Especially
acute at SMB spend levels where sample sizes are small.

**X5 — Founder-time & focus. [DESK].** Side business, limited hours, EN+JP split.
Every manual-delivery/service model risks consuming the scarcest resource;
serving two languages/markets at once dilutes the validation signal.

**X6 — No demand evidence exists yet. [REAL, internal].** All Phase-3 "evidence"
is void; `research/` and `customers/` hold no validated demand or WTP. **Zero
candidates currently have evidence a customer will pay.** Every candidate's #13
therefore includes "primary demand + WTP." Any Top 3 must be labelled hypotheses.

---

## PER-CANDIDATE SWEEP

### O1 — Meta Ads performance auditing
**#12 Primary risks / why it fails:**
- One-time audit = **no recurring revenue** → conflicts with the company's own
  stated preference (recurring). [DESK]
- Audits are commonly given away **free by agencies as a lead-magnet** to win
  retainers → market reference price trends toward ~0. [DESK — verify with Oscar]
- X3 (AI makes audits near-free to produce) → price compression.
- "Audit → recurring monitoring" upsell assumes findings are *actionable by the
  buyer*; an SMB that can't/won't execute fixes gets no recurring value.
[ASSUMPTION]
**#13 Evidence still missing:** paid (not free) audit WTP; audit→recurring
conversion rate; whether typical buyers can act on findings; who feels the pain
(owner-operator vs agency).

### O2 — Monitoring & intelligence (change/anomaly detection & explanation)
**#12:** Direct substitute = Meta native alerts/automated rules (free, X2).
"Explain *why* it changed" collides with X4 (attribution noise) → unreliable
causal claims. Continuous read = high X1 dependency. Dashboard-fatigue: SMBs may
not log in → retention risk. Incumbent tools likely exist in this space. [DESK —
Oscar to name/verify]
**#13:** Do targets currently *pay* for monitoring? Retention/churn of such
tools; can "why" be answered accurately enough to be trusted; alert-fatigue
tolerance.

### O3 — Advertising creative generation
**#12:** **Most crowded + best-funded lane** (multiple established AI-creative
vendors) AND Meta's own free in-platform generative creative (X2) → existential
substitute. X3 commoditization; brand-safety/IP/misleading-claims risk on
generated output; creative that underperforms → immediate churn; low switching
cost. [DESK — Oscar to verify vendors + native scope]
**#13:** WTP *over* free native tools; evidence ZeroEn creative outperforms
baseline; retention; IP/compliance posture.

### O4 — Creative performance analysis
**#12:** **Double data-dependency** (creative + performance) → 2× X1. Statistical
validity problem: at SMB spend/volume there's rarely enough data to attribute
performance to specific creative elements → spurious conclusions (X4). Overlaps
O2. Native creative breakdowns already exist (X2). [DESK]
**#13:** Do target SMBs have sufficient volume for valid creative analysis? WTP;
whether insights change behavior.

### O5 — Reporting automation
**#12:** Heavily commoditized; competes with free connectors (Looker Studio) +
native reporting (X2) → price compression. **Segment mismatch:** reporting pain
is felt mainly by *agencies reporting to clients*, not owner-operator SMBs → the
buyer with the pain may not be the hypothesized customer. Low margin. [DESK]
**#13:** Which segment actually feels reporting pain and pays; WTP vs free
tools; is it a standalone product or a feature.

### O6 — Optimization workflows
**#12 — highest-liability candidate:**
- If it **writes to the account** (budgets/bids), it carries direct financial
  liability (bad automation loses the customer money → churn + reputational +
  possible dispute) AND likely extra Meta ToS/automation constraints. [DESK] —
  **flagged Critical.**
- Direct substitute = Meta Advantage+ / automated rules, free, and Meta owns the
  algorithm + data ZeroEn would compete on (X2). Hardest technically. Requires
  trust (write-access to spend) a new vendor won't easily earn. [DESK]
**#13:** Will customers grant a new tool write-access to spend? Does it beat
Meta native? ToS limits on programmatic changes; liability/consent model.

### O7 — Marketing automation (broader)
**#12:** **Scope too broad** → violates "start small / focus"; dilutes the
Meta-ads competence that is the founder's only claimed edge. Faces large
entrenched incumbents (general automation platforms). Undifferentiated; unclear
single pain; typically longer sales cycles. [DESK]
**#13:** A *specific narrow* pain worth isolating; why ZeroEn vs incumbents;
whether it even belongs in a Meta-ads-focused validation.

### O8 — Adjacent problems (open lane)
**#12:** The open lane is itself a **confirmation-bias / scope-creep risk**: a
novel adjacent idea arrives with the *least* evidence, yet novelty can masquerade
as opportunity. Straying outside Meta-ads also erases the founder's only stated
domain edge. **Anything surfaced here must clear a *higher* evidence bar, not a
lower one.** [DESK]
**#13:** For any O8 idea: same discipline as O1–O7 — demand, WTP, competition,
founder-edge — before it can rank.

---

## CRITICAL FLAGS FOR GOD (raised immediately, per brief)
1. **X2 (Meta native-feature substitution) should drive Top-3 selection.** O2,
   O3, O5, O6 each compete against a *free* Meta-native feature — a structural
   WTP problem. Prefer candidates that do something Meta does **not** give away.
2. **O6 is categorically higher-risk** than read-only candidates: write-access to
   customer spend = financial liability + likely ToS-automation limits. If it
   makes the Top 3, its validation must be framed accordingly.
3. **No candidate has any demand/WTP evidence (X6).** Every Top-3 entry must be
   labelled a hypothesis, and the cheapest experiment (#14) must test **WTP
   before any build**, per PRINCIPLES #2/#3.

## Ranking of *risk* (not attractiveness — highest existential risk first)
O6 ≈ O3 (Meta substitute + liability/commoditization) > O7 (too broad) > O5 ≈ O1
(commoditized / low WTP) > O2 ≈ O4 (dependency + attribution reliability) >
O8 (evidence-unknown by definition). **All remain unproven on demand.**

## Handoff notes
- When Oscar (P1) lands [REAL] competitor/native-feature/API findings and Kevin
  (P4) lands WTP/margin assumptions, I will attack those claims specifically and
  update #12/#13.
- Ready to red-team god's draft Top 3 on request.

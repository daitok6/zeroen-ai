# Initial Company Audit

**Author:** QA — Independent Review & Risk Lead
**Date:** 2026-08-24
**Scope reviewed:** `COMPANY.md`, `STRATEGY.md`, `PRINCIPLES.md`, `README.md`,
and the contents of `research/`, `marketing/`, `sales/`, `finance/`,
`customers/` (plus `decisions/`, `experiments/`).

**State of evidence at time of audit:** `research/`, `marketing/`, `sales/`,
`finance/`, `customers/`, `decisions/`, and `experiments/` are **all empty**
(`.gitkeep` only). There is no research, no customer contact, no financial
model, and no experiment on record. This audit therefore reviews the
**foundational documents and org design**, not department output. Nothing has
yet been produced that could be validated — which is itself the single most
important fact below.

**Severity scale**
- **Critical** — could sink the company, waste its scarcest resources, or create
  legal/reputational exposure; must be resolved before building a product.
- **High** — likely to cause a materially wrong decision or significant wasted
  effort if left unaddressed.
- **Medium** — a real weakness that should be fixed but is unlikely to be fatal
  alone.
- **Low** — cleanup, clarity, or consistency; low downside.

This audit **does not rewrite strategy**. It flags concerns and, per QA
principle, pairs each with the cheapest way to resolve it.

---

## 1. Contradictions between COMPANY.md, STRATEGY.md, PRINCIPLES.md

### 1.1 "Build products" mission vs. "validate before building" — **Medium**
COMPANY.md's Mission opens *"Build useful marketing products and systems…"* and
Business Model Direction presents a service→SaaS path as *"The preferred path."*
STRATEGY.md and PRINCIPLES.md #2 insist nothing substantial is built until a
paying customer proves the problem. The framing is build-first at the top and
validate-first everywhere else. **Why it matters:** the top-of-document mission
is what an agent anchors on; a build-oriented mission quietly licenses premature
building. **Resolve:** reconcile the mission wording with the validation phase
(no file change made by QA — this is a recommendation to the founder/Michael).

### 1.2 QA is in the org chart but not in the department list — **Medium**
COMPANY.md's org chart lists **Research, Marketing, Sales, Finance, QA**.
README.md's Departments list is **research, marketing, sales, finance,
customers, experiments, decisions** — it omits QA and adds three folders the org
chart never assigns to anyone. **Why it matters:** ownership of `customers/`,
`experiments/`, and `decisions/` is undefined, and QA's place in the structure
is inconsistent between the two governing files. See also 6.2. **Resolve:** make
the two lists agree and assign an owner to each folder.

### 1.3 Bilingual capability: asset vs. hypothesis — **Low**
COMPANY.md lists "Ability to serve English- and Japanese-speaking markets" as an
**Existing Asset** (stated as fact). STRATEGY.md correctly demotes
"English/Japanese market capability" to an unproven **competitive-advantage
hypothesis**. The same item is a fact in one file and a hypothesis in the other.
**Resolve:** treat the *language ability* as a fact but the *market advantage* as
a hypothesis; align wording.

### 1.4 Scope: "marketing products" vs. Meta-Ads-only strategy — **Low**
COMPANY.md's mission and interest list are broad ("marketing automation,"
"related products"), while STRATEGY.md's four hypotheses (A–D) are **entirely
Meta Ads**. Not a hard contradiction, but the strategy has silently narrowed the
company to one platform without recording that decision in `decisions/`. See 5.1
and 4.6.

---

## 2. Assumptions treated too much like established facts

### 2.1 "Meta advertising knowledge" as a current, durable asset — **Medium**
Listed in COMPANY.md under both Founder Capabilities and Existing Assets, stated
flatly. Meta's ad platform, APIs, and best practices change continuously.
Depth, recency, and breadth of this knowledge are asserted, not evidenced, yet
three of four hypotheses depend on it being a real edge. **Resolve:** state
concretely what the knowledge is (years, spend managed, results, last active
date) so downstream reasoning isn't built on an untested self-assessment.

### 2.2 The service → SaaS transition as a near-given — **Medium**
COMPANY.md calls Productized Service → Subscription → Automation → SaaS *"The
preferred path,"* and Hypothesis A/B assume audits/monitoring will
"automate/evolve" into a platform. The historical failure rate of
agency/service businesses that try to become software is high; this transition
is treated as a route rather than a bet. **Resolve:** log it as an assumption
with an explicit test ("what repetitive work, specifically, could be
automated?").

### 2.3 ¥1,000,000+ MRR without proportional founder hours — **Medium**
COMPANY.md's Long-Term Objective states this as an objective, which is fine — but
nothing yet supports that this domain has the margin, retention, and low support
burden to reach it on side-business time. It should not be reasoned from as a
settled parameter. **Resolve:** treat as a target requiring unit-economics
evidence (see 4.4), not a premise.

### 2.4 Named target segments as "potential customers" — **Low/Medium**
STRATEGY.md lists six candidate segments and *does* label them "require
validation" — good discipline. The risk is downstream agents dropping the
qualifier and treating "small businesses running their own Meta Ads" as the
confirmed ICP. **Resolve:** keep the "unvalidated" tag attached whenever these
segments are cited.

---

## 3. Important risks the current strategy may be overlooking

### 3.1 Platform dependency on Meta — **Critical**
All four hypotheses require access to Meta advertising data, which in practice
means the Meta Marketing/Graph API: app review, business verification, scoped
permissions, rate limits, and terms that Meta can change or revoke unilaterally.
Meta has a history of restricting third-party access to ad and platform data.
The entire company is being designed on top of a dependency whose *feasibility
and durability have not been checked*. **Why Critical:** if API access is
unavailable, too limited, or revocable, every hypothesis (A–D) fails at once.
**Resolve:** before any product work, verify what data ZeroEn can actually,
legally, and reliably obtain (see 4.5).

### 3.2 Data privacy / regulatory exposure — **High**
The hypotheses involve accessing customers' ad accounts, performance data, and
potentially audience/PII and OAuth tokens, across **Japan (APPI)** and
international/**EU (GDPR)** users the strategy explicitly targets. No data-
handling, consent, retention, or security posture is mentioned. **Why High:**
mishandling customer ad-account access is both a legal and a trust-killing
reputational risk. **Resolve:** define a minimum data-handling stance before
touching real customer accounts.

### 3.3 Crowded, mature competitive category — **High (evidence pending)**
Meta Ads auditing, "intelligence/monitoring," and AI creative generation are
well-populated categories. STRATEGY.md's competitive advantages are explicitly
labeled hypotheses (good), but the strategy does not confront the possibility
that differentiation is thin against incumbents. **Note:** QA will not fabricate
competitor names or numbers — the actual landscape is currently **unknown and
unresearched** (`research/` is empty), which is itself the finding. **Resolve:**
competitor scan is a prerequisite, not a nice-to-have (see 4.1).

### 3.4 Validation phase consumes the scarcest resource — **High**
Milestones 4–8 (interview customers, deliver manually) and PRINCIPLE #4 (protect
founder time) are in direct tension: manual delivery of the first customers is
founder-time-intensive, on a side business with explicitly limited hours. The
plan is correct for learning, but the founder-time cost of the validation phase
itself is not budgeted. **Resolve:** cap the manual-delivery experiment (e.g.,
hours/week, number of customers) so validation does not quietly become an
unpaid agency.

### 3.5 AI-generated creative — brand/compliance/IP risk — **Medium**
Hypothesis C/D generate ad creative that customers would run under their own
brands. This raises Meta ad-policy compliance, misleading-claims, and image/IP-
provenance risks. Not addressed. **Resolve:** flag as a required guardrail if C/D
advances.

### 3.6 Split focus across two languages/markets — **Medium**
Serving EN and JP simultaneously on limited founder time risks diluting the
validation signal (different competitors, pricing, channels, and buying
behavior). **Resolve:** consider validating one market first; record the choice.

### 3.7 The AI org can produce confident, wrong output — **Medium**
The company relies on an AI agent organization to research and reason. Without a
requirement that conclusions trace to primary/external evidence, the org can
generate internally-consistent but unfounded analysis. (This is why QA exists,
but the risk should be named explicitly.) See 5.3.

---

## 4. Missing information to obtain before building a product

All **High/Critical** — the company cannot responsibly build until these exist,
and today none do:

### 4.1 Market & competitor research — **Critical (missing)**
`research/` is empty. No competitor set, pricing benchmarks, or category map.
Everything in STRATEGY.md's competitive section is currently unsupported.

### 4.2 Primary customer evidence — **Critical (missing)**
`customers/` is empty. Zero interviews, zero problem confirmation. STRATEGY.md's
own Success Metric ("evidence a specific customer will pay to solve a specific
problem") is at 0.

### 4.3 A single, specific problem statement + ICP — **High (missing)**
Six candidate segments and four hypotheses, none narrowed. Building requires one.

### 4.4 Unit economics / financial model — **High (missing)**
`finance/` is empty. No pricing, CAC, gross margin, retention, or infra/support
cost estimate — yet PRINCIPLE #12 and the ¥1M MRR goal depend on them.

### 4.5 Meta API access feasibility (technical + legal) — **Critical (missing)**
Can ZeroEn actually obtain the required data at acceptable cost, permission
scope, and reliability? Unanswered. Gates everything (see 3.1). This is the
cheapest highest-value thing to check first.

### 4.6 A recorded decision log — **Medium (missing)**
`decisions/` is empty despite consequential implicit decisions already made
(Meta-only focus, service-first path). Per PRINCIPLE #10, these should be
written down with rationale.

---

## 5. Parts of the setup that could encourage confirmation bias

### 5.1 The strategic question presupposes its answer — **High**
STRATEGY.md frames the Current Strategic Question as *"What product… should
ZeroEn build **around digital marketing and Meta advertising expertise**?"* This
bakes the conclusion (the answer lies in Meta Ads) into the question. Research
run against this prompt will tend to *find* Meta Ads opportunities rather than
test whether a better problem exists elsewhere. **Why High:** confirmation bias
at the root of the funnel contaminates every downstream experiment. **Resolve:**
also ask the disconfirming question — "what evidence would show Meta Ads is the
*wrong* place to start?"

### 5.2 Anchoring on a favored end-state — **Medium**
Hypothesis D is pre-labeled *"an attractive long-term hypothesis."* Naming a
favorite before data exists biases interim experiments toward confirming it.
STRATEGY.md does add "NOT yet validated," which partially mitigates this.

### 5.3 Self-generated research with no primary-evidence gate — **Medium**
The AI org may produce its own "market research" and then validate against it,
creating a closed loop with no external ground truth. PRINCIPLE #13 forbids
fabrication (good), but there is no positive requirement that a claim cite a
real, checkable source or a real customer quote. **Resolve:** require every
consequential research claim to carry a source label (per QA's fact/inference/
assumption taxonomy).

### 5.4 QA independence is structurally compromised — **High** (also §6.1)
If all QA findings flow *only* through Michael, the person accountable for the
departments' output also controls the review of that output. That is a
confirmation-bias amplifier. Mitigated by the direct-to-founder escalation for
Critical findings now written into `qa/README.md`.

---

## 6. Unclear or overlapping responsibilities between agents

### 6.1 QA independence vs. "report through Michael" — **High**
QA's charter says coordinate/report through Michael/COO, who owns every
department QA reviews. Independent review filtered solely through the owner of
the reviewed work is not independent. **Resolve (partially done):** QA's README
now routes Critical findings to the founder directly as well. Founder/Michael
should confirm this escalation path.

### 6.2 Unowned folders: `customers/`, `experiments/`, `decisions/` — **Medium**
Present in the repo/README but absent from COMPANY.md's org chart. No agent owns
customer interviews, experiment logs, or the decision record. **Resolve:** assign
each explicitly.

### 6.3 Research vs. Marketing vs. Sales overlap on discovery — **Medium**
- *Competitor research* sits in Research, but *positioning* (which requires
  competitor understanding) sits in Marketing.
- *Customer development / interviews* plausibly belong to both Sales
  ("customer development and sales") and Research/`customers/`.
- *Acquisition* is claimed by Marketing while Sales owns customer development.
Boundaries are undefined; in the validation phase, who runs and owns customer
interviews is the most important of these to settle. **Resolve:** name a single
owner for customer-discovery interviews.

---

## Top priorities (for Michael and the founder)

1. **Verify Meta API access feasibility and terms** (3.1 / 4.5) — Critical,
   cheapest high-value check, gates everything.
2. **Do real customer discovery before any building** (4.2 / 4.3) — Critical;
   the Success Metric is currently at zero.
3. **Reframe the strategic question to avoid presupposing Meta Ads** (5.1) —
   High; prevents root-level confirmation bias.
4. **Define a data-privacy/handling stance** (3.2) — High; before any real
   account access.
5. **Assign owners for `customers/`, `experiments/`, `decisions/` and settle
   discovery ownership** (6.2 / 6.3) — Medium; needed before work starts.
6. **Confirm QA's direct-to-founder escalation for Critical findings** (6.1) —
   High; preserves independent review.

QA has made **no changes outside `qa/`**. All items above are recommendations
returned for founder/Michael decision, not edits to other departments' work.

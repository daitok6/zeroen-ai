# QA — Independent Review & Risk

## Purpose

QA exists to challenge important ZeroEn work **before** the company relies on it.

QA does not make proposals sound better. QA finds weaknesses, unsupported
assumptions, errors, and risks so that decisions are made on evidence rather
than confidence. The operating principle is: **trust evidence, not confidence.**

QA is a service to the founder and to every department. A finding is a gift: it
is cheaper to be wrong on paper than to be wrong after spending money, founder
time, or reputation.

## What Requires Independent Review

Review is mandatory before ZeroEn *acts on* or *commits to* any of the
following:

1. **Research conclusions** used to choose a direction (market size, competitor
   claims, "customers want X").
2. **Strategy changes** or new/retired hypotheses.
3. **Financial models and projections** (pricing, CAC, LTV, margin, revenue
   targets, unit economics).
4. **Marketing and sales claims** made to real prospects (performance promises,
   comparisons, testimonials, statistics).
5. **Experiment designs and their interpretation** — before running, to check
   the experiment can actually disprove the assumption; after, to check the
   conclusion follows from the result.
6. **Any consequential action** listed in PRINCIPLES.md #9 (spending money,
   paid ads, financial commitments, significant public claims, contacting
   customers as the company, production deploys, contracts, core strategy
   changes).
7. **Anything presented as fact** that would change a decision if it turned out
   to be an assumption.

Small, reversible, ¥0 internal steps do **not** need QA. QA is for work that is
consequential, hard to reverse, or outward-facing.

## Criticism vs. Useful Risk Analysis

QA is judged on whether its findings change outcomes, not on how skeptical it
sounds. Every finding must pass these tests:

- **Specific, not vague.** Name the exact claim, file, or number — not "this
  feels risky."
- **Evidence-based.** State *why* it is weak: which assumption is unproven, what
  evidence is missing, what the alternative explanation is.
- **Consequential.** Say what breaks if the concern is right, and how big the
  damage is. A concern with no downside is noise.
- **Actionable.** Pair the finding with the cheapest experiment or piece of
  information that would resolve it. QA recommends validation; it does not just
  object.
- **Falsifiable and fair.** QA states what evidence *would* change its mind, and
  does not reject an idea merely to appear rigorous.

QA labels every claim it reviews as one of: **verified fact · inference ·
estimate · assumption · speculation.** Rejecting ideas to look careful is a
failure mode, not the job.

## Reporting to Michael and the Founder

- **Default channel:** QA documents findings in `qa/` and returns them **through
  Michael (COO)**. QA does not rewrite another department's files; it reviews
  and reports.
- **Severity classification:** every finding is tagged **Critical / High /
  Medium / Low** with a one-line reason.
- **Critical-finding escalation (founder ruling, 2026-08-24):** escalation runs
  **through Michael**, not via a separate direct-to-founder channel. Michael's
  standing commitment: **Critical findings — and any consequential
  recommendation QA judges unsupported — are relayed to the founder
  verbatim/unfiltered and logged on the ASK ME board**, visible independently of
  Michael's triage, with no gatekeeping or delay. If QA ever judges that a
  Critical is being filtered or delayed, QA says so explicitly and Michael
  escalates it immediately. This preserves independence without a parallel
  channel.
- **Format:** headline + severity + the specific claim + why it is weak + the
  cheapest way to resolve it. No bare "looks fine" / "looks bad."
- QA never fabricates a concern to justify its existence, and never suppresses a
  real one to avoid friction.

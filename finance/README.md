# Finance & Business Strategy

Owner: Finance & Business Strategy Lead (Kevin)
Coordinated through: Michael (COO)
Last updated: 2026-08-24

---

## Purpose

The finance department exists to answer one question for ZeroEn:

> **Can a given product, service, or growth strategy become a profitable,
> repeatable, and scalable business — not just a source of revenue?**

Finance does this by:

- Evaluating pricing, revenue models, costs, and unit economics.
- Modeling the metrics that determine whether an offer sustains itself.
- Comparing opportunities on their *likely economics*, not their appeal.
- Challenging any model where revenue growth requires a proportional
  increase in founder labor.
- Producing **scenario models** (low / base / high) instead of presenting
  uncertain forecasts as facts.
- Finding the **cheapest reasonable experiment** to validate a financial
  assumption before money or founder time is committed.

Finance does **not** authorize spending, make purchases, enter contracts, or
make financial commitments. It recommends; the founder decides
(see PRINCIPLES.md #9).

### Guiding principle

Revenue is useful. **Profitable, repeatable revenue is better.**
(See PRINCIPLES.md #3, #5, #12.)

---

## Metrics ZeroEn should eventually track

None of these have values yet — the departments are empty and no evidence
exists. They are listed as the eventual measurement targets, not as known
numbers.

**Revenue & pricing**
- Price per offer / per tier
- Recurring revenue (MRR) vs. one-time revenue
- Revenue mix (service vs. subscription vs. software)

**Unit economics**
- Gross margin (revenue minus direct delivery cost)
- Customer Acquisition Cost (CAC)
- Lifetime Value (LTV) and the LTV : CAC relationship
- CAC payback period (months to recover acquisition cost)
- Contribution margin per customer

**Retention**
- Churn (logo and revenue)
- Retention / net revenue retention
- Expansion revenue

**Cost & capacity**
- Infrastructure / tooling cost per customer and fixed
- Advertising / acquisition spend
- **Founder time per customer** (onboarding, delivery, support) — the single
  most important scalability metric for a side business (PRINCIPLES.md #4)
- Support burden per customer

**Viability**
- Break-even point (customers and revenue needed to cover costs)
- Path to the ¥1,000,000/month objective *without* founder hours scaling
  proportionally to customer count (COMPANY.md long-term objective)

---

## How assumptions must be documented

ZeroEn is in market validation. Almost every financial number will start as an
assumption. To keep them honest (PRINCIPLES.md #1, #8, #11, #13):

1. **Label every number.** Mark each as `FACT`, `EVIDENCE`, `ASSUMPTION`, or
   `HYPOTHETICAL EXAMPLE`. Never present an assumption as a fact.
2. **State the source.** Where did it come from — a customer conversation, a
   competitor page (via Research), an internal estimate? If there is no
   source, say "no evidence yet."
3. **Never fabricate.** No invented pricing, CAC, LTV, conversion rates,
   churn, or testimonials. If it can't be verified, it is written down as
   unverified (PRINCIPLES.md #13).
4. **Model in ranges.** Present low / base / high scenarios, not a single
   false-precision forecast. Show which assumption each scenario is most
   sensitive to.
5. **Name the cheapest test.** Every assumption gets a proposed cheapest
   experiment capable of disproving it (a ¥0 test beats a ¥100,000 test that
   answers the same question — PRINCIPLES.md #11).
6. **Preserve it in the repo.** Assumptions, models, and decisions live in
   `finance/`, not in a temporary conversation (PRINCIPLES.md #10).

Suggested layout as evidence arrives:
- `finance/assumptions.md` — the live register of labeled assumptions
- `finance/models/` — scenario models (per opportunity)
- `finance/pricing/` — pricing experiments and subscription structures

---

## How Finance collaborates

Finance owns no primary evidence of its own — it turns other departments'
evidence into economics. Coordination runs through **Michael**.

| Department | Finance needs from them | Finance gives back |
|---|---|---|
| **Research** | Market pricing, competitor pricing/packaging, market-size signals | Which economic questions research should answer first; sanity checks on competitor claims |
| **Sales** | Willingness-to-pay evidence, objections, what customers actually paid | Price points and offer structures worth testing; break-even targets per deal |
| **Marketing** | Acquisition-cost assumptions, channel/funnel data, conversion signals | CAC ceilings a channel must stay under to be viable; payback constraints |
| **QA** | Delivery quality issues, rework, defect/support load | The cost of rework and support burden folded into gross margin and founder-time-per-customer |
| **Michael (COO)** | Prioritization, cross-department coordination, sign-off routing | Financial recommendations, risks, scenario models, and the cheapest validation path for founder approval |

Finance is deliberately a **challenger**: its job includes arguing against
attractive ideas whose economics don't hold — especially any model where
serving more customers means the founder working proportionally more hours.

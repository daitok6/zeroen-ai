# Sales & Customer Development

## Purpose

Sales exists to answer one question before anything else: **does a real
customer have a problem worth paying ZeroEn to solve, and will they actually
pay?**

At this stage, ZeroEn has not committed to a product (see `STRATEGY.md`).
Sales is not here to push a predetermined offer — it is here to test whether
each hypothesis in `STRATEGY.md` (Meta Ads audits, monitoring, creative
engine, etc.) deserves to become a product at all. That means Sales' job is
as much about disqualifying weak ideas as it is about closing paying
customers.

This aligns with `PRINCIPLES.md`: evidence over enthusiasm, revenue is
stronger evidence than interest, and every proposal should include reasons
it might fail — not just reasons it might succeed.

## Customer Discovery vs. Traditional Selling (at ZeroEn's current stage)

| Traditional Selling | Customer Discovery (ZeroEn now) |
|---|---|
| Assumes the product is correct; job is to persuade | Assumes nothing is correct; job is to find out |
| Optimizes for closing the conversation | Optimizes for learning, even from a "no" |
| Pitches features and benefits | Asks about pain, current spend, and workarounds |
| Success = signed deal | Success = a validated or invalidated hypothesis |
| Objections are obstacles to overcome | Objections are data about what's wrong with the offer |
| Leading questions ("wouldn't it be great if...") | Neutral questions that don't hint at the desired answer |
| A "sounds great" is treated as a win | A "sounds great" is treated as unconfirmed until money or a firm commitment shows up |

Until ZeroEn selects one problem for paid validation (Strategy milestone 5),
every customer conversation is primarily a research conversation. Selling
only becomes the primary mode once a specific, evidence-backed offer exists
(Strategy milestones 6–7). Even then, "sales" at ZeroEn's stage looks more
like a structured pilot/paid-trial process than a traditional closing
process — because the goal is still to learn whether the offer is worth
scaling, not just to book revenue once.

## What Belongs in `sales/`

Process, tooling, and pattern-level knowledge that applies across many
customers or conversations:

- Target customer segment hypotheses and qualification criteria
- Customer interview / discovery question sets
- Outreach approach concepts (channel, framing, sequencing) — planning only;
  actual outreach requires founder authorization per `PRINCIPLES.md` #9
- Offer structures and pricing experiments under consideration
- Sales process design (how a lead moves from first contact to paid pilot)
- Aggregated patterns across multiple customer conversations: common
  objections, common buying triggers, common reasons for refusal
- Frameworks for distinguishing interest from intent from payment (see
  below)

If it's reusable across customers, it goes in `sales/`.

## What Belongs in `customers/`

Records of specific, individual customer interactions and evidence:

- Interview notes and transcripts from specific conversations (anonymized
  or identified per founder preference, never fabricated — `PRINCIPLES.md`
  #13)
- What a specific customer said about their pain, current solution, and
  spend
- Specific objections raised and by whom
- Specific willingness-to-pay signals or refusals
- Outcomes: did this person move from interest → intent → payment, and when

If it's a fact about one specific customer or conversation, it goes in
`customers/`. Sales then mines `customers/` to produce the aggregated
patterns that live in `sales/`.

## Collaboration

- **Michael (COO):** All sales activity is coordinated through Michael.
  Report qualification criteria, proposed outreach approaches, and offer
  designs before acting on them. Escalate anything that touches founder
  approval items in `PRINCIPLES.md` #9 (spending money, contacting
  prospects as ZeroEn, entering commitments).
- **Research:** Hand off patterns discovered in customer conversations that
  need deeper investigation (e.g., a recurring competitor mentioned, a
  workaround tool customers already use). Pull from `research/` before
  drafting interview questions so discovery isn't re-asking what's already
  known.
- **Marketing:** Share real customer language — the exact words customers
  use to describe their pain — so Marketing can reflect authentic voice
  instead of guessed positioning. Marketing's messaging hypotheses should be
  informed by `customers/`, not the reverse.
- **Finance:** Share willingness-to-pay evidence (what customers currently
  spend, what price points get accepted vs. rejected) so Finance can model
  pricing and unit economics on real data rather than assumption.
- **QA:** Flag any delivery-quality signals raised during sales/customer
  conversations (e.g., a pilot customer's complaint about a manual
  deliverable) so QA can track them against actual delivery.
- **Founder:** Sales never contacts real prospects, sends outreach, makes
  commitments, negotiates, or represents the founder externally without
  explicit authorization. Sales prepares the plan; the founder approves
  consequential action.

## Interest vs. Intent vs. Payment

These are three different strengths of evidence, and conflating them is one
of the most common ways a startup fools itself.

**1. "That sounds useful" (Interest)**
The customer reacts positively to a description of the problem or solution.
This costs the customer nothing — no time commitment, no money, no risk. It
confirms the pitch is *understandable and not obviously unappealing*. It
does **not** confirm the problem is painful enough to act on, that ZeroEn's
approach is the right one, or that this person will do anything next.
Weakest signal. Necessary but nowhere near sufficient.

**2. "I would pay for that" / "sign me up when it's ready" (Purchase Intent)**
The customer makes a verbal or written commitment to a future action —
agreeing to a follow-up call, asking to be first on a waitlist, saying
they'd pay a specific price. This is stronger: it costs a small amount of
social capital and attention. But intent is cheap to express and expensive
to walk back later, so people over-state it, especially to be polite or
encouraging. It should raise confidence, not settle the question.

**3. Actually paying (Revealed Preference)**
The customer transfers real money (or signs a binding commitment) for the
offer as it actually exists today — not a future version, not a discount so
steep it's nearly free. This is the strongest evidence because it's costly
and irreversible: the customer gave up something scarce (money) to get the
outcome. Per `PRINCIPLES.md` #3, this is the evidence ZeroEn prioritizes
testing for.

**Practical rule:** never advance a hypothesis from "worth exploring" to
"worth building" on interest or intent alone. Design every discovery
conversation to push toward the cheapest real test of payment (a deposit, a
paid pilot, a paid audit) rather than stopping at a compliment or a "maybe
later, sounds cool."

# Customer Discovery Plan

**Owner:** Sales & Customer Development (Dwight)
**Status:** Active — Task T2
**Related:** `qa/initial-company-audit.md` §4.2/4.3 (Critical — zero customer
evidence exists; Success Metric = 0), `STRATEGY.md` (hypotheses A–D,
milestones 3–4)

## Objective

Generate the first real customer signal ZeroEn has ever collected, and use it
to narrow four unvalidated product hypotheses (A: Audit, B: Intelligence/
Monitoring, C: Creative Engine, D: Combined) down to the strongest one — or
discover that none of them match a real, paid problem.

This is discovery, not selling. ZeroEn has not committed to a product
(`STRATEGY.md`, Current Stage). No fixed offer exists yet to sell.

## Scope & Boundaries

- **In scope:** defining who to talk to, what to ask, and how to log what we
  learn. Preparing (not executing) a first outreach batch.
- **Out of scope for this agent, without explicit founder authorization:**
  actually contacting real people, sending messages, posting outreach, or
  making any commitment on ZeroEn's behalf (`PRINCIPLES.md` #9). This plan
  produces a ready-to-execute batch; a human must authorize sending it.
- No fabricated customers, quotes, or conversations (`PRINCIPLES.md` #13). If
  a conversation hasn't happened, the log says so — it is never backfilled
  with invented detail.

## Approach (cheapest-experiment-first, per PRINCIPLES.md #11)

1. **Define target segments** across hypotheses A–D, for EN and JP markets —
   see `customers/target-segments.md`.
2. **Write a neutral interview script** that asks about existing pain, current
   solutions, and current spend without pitching a solution — see
   `customers/interview-script.md`. (Mom Test-style: ask about past behavior
   and money already spent, not hypothetical future interest.)
3. **Prepare a first outreach batch**: candidate channels, targeting
   criteria, and message templates — see `customers/outreach-plan-and-log.md`.
   Marked NOT SENT until the founder authorizes execution.
4. **Log every real conversation** as it happens in
   `customers/outreach-plan-and-log.md`, tagged with segment, hypothesis
   relevance, and evidence strength (interest / intent / payment — see
   `sales/README.md`).
5. **Synthesize patterns** back into `sales/` once enough conversations exist
   to see a pattern (target: after ~5–10 real conversations, revisit).
   Feed relevant patterns to Marketing (real customer language) and Research
   (recurring competitors/tools mentioned).

## Dependencies

- **Oscar (Market Intelligence / Research):** segment definitions below are
  built from `STRATEGY.md` alone, since `research/` currently has no desk
  research on file. Requesting Oscar's competitor/tool findings to sharpen
  segment criteria and interview questions (e.g., what tools do these
  segments already pay for). Tracked via hive message to Oscar.
- **Founder/Michael:** authorization required before the outreach batch in
  `customers/outreach-plan-and-log.md` is actually sent.

## Definition of Done (this task)

- [x] Discovery plan (this file)
- [x] Target-segment definitions, EN + JP (`customers/target-segments.md`)
- [x] Interview/outreach script (`customers/interview-script.md`)
- [x] First outreach batch prepared (`customers/outreach-plan-and-log.md`) —
      structurally ready, explicitly **not sent** pending authorization
- [ ] First outreach batch **sent** and/or first real conversations **logged**
      — blocked on founder authorization to contact real people

## Open Questions for Michael / Founder

1. Authorize sending the prepared outreach batch (channels + message
   templates in `customers/outreach-plan-and-log.md`), or hold until T1
   (Meta API feasibility) resolves? Talking to customers doesn't require API
   access, so discovery can run in parallel with T1 — flagging for a
   decision, not assuming it.
2. Preference on starting with EN or JP market first, given
   `qa/initial-company-audit.md` §3.6 (split-focus risk)? Default assumption
   below is to run both in parallel at small scale, since discovery itself is
   ¥0, but a single-market first cut would be cheaper for the founder's
   available time.

# ZeroEn O1 Launch Plan — Paid Meta Ads Audit

**Owner:** Michael (COO / orchestrator) · **Date:** 2026-08-25 · **Conversation:** phase5-o1
**Status:** DRAFT for founder approval. Nothing external has been published, spent, or sent. No prospect contacted.

**Strategic frame (founder decision):** O1 is the **initial paid offer and customer-learning wedge** — NOT the end-state business. Its job is to acquire the first paying customers, learn what advertisers struggle with, generate real evidence, and reveal which recurring problems lead into **O2 (Monitoring & Intelligence)** and/or **O4 (Creative Performance Analysis)**. Path: **O1 → paid validation → O2 and/or O4 → recurring subscription/software.** Do not build O2/O4/SaaS yet. O1 is not "validated" until customers actually pay.

**Sources synthesized (all in this repo):** `research/phase5-o1-audit.md` (Oscar, branch `agent/oscar-mt70k94n`), `sales/phase5-o1-sales.md` (Dwight), `finance/phase5-o1-economics.md` (Kevin), `marketing/phase5-o1-gtm.md` (Jim, `f109526`), `qa/phase5-o1-redteam.md` (Creed).

**Evidence labels:** **[REAL]** cited public source · **[DESK]** reasoned from public patterns · **[ASSUMPTION]** unverified. Every number below is a hypothesis to test, not a validated fact.

> **⚠ TWO CRITICAL ISSUES (from Creed's red-team) shape this plan and require founder decisions — see §18:**
> **C1 — Positioning honesty:** the "nothing to sell you afterward" promise (Marketing) contradicts using the audit as a paid acquisition channel with a scripted O2 upsell at delivery (Finance/Sales). Shipping both breaks the exact trust the offer is built on. **This plan resolves it by keeping the pilot genuinely independent and capturing O2/O4 interest as *research*, not a pitch** — see §12/§16/§17 — but the founder must confirm this stance.
> **C2 — The wedge is unproven:** "independence" is the differentiator, and it is the ONE driver with zero direct market evidence. Every real paid comp validates a *different* driver. **The pilot's primary job is to test whether independence actually drives a paid purchase** — see §13.

---

## 1. Target Customer

**Primary ICP:** A self-managing Meta advertiser — owner-operator or a 1–3 person marketing function — running its **own** Meta Ads with **real, ongoing spend**, currently **in a decisive trigger moment** (doubting results, newly took over the account, or deciding whether to keep/replace an agency). Single decision-maker, no procurement chain. [REAL/DESK]

**Spend band (resolves Creed M1 — a cross-lens mismatch):** Sales framed ~**$1k+/mo**; Research pointed to **$5k–50k/mo DTC**. For the first paid batch, **target the higher band (~$3k+/mo, ideally $5k+/mo)** — the audit's ROI (price vs. recoverable wasted spend) is only defensible there, and higher spend = sharper trigger + more budget authority. Treat $1k/mo as the floor, not the target.

**Secondary / future (not first batch):** small agencies/freelancers as a **white-label/reseller** channel — deliberately deprioritized now (they give free audits as their own lead-magnet → an objection source, not a buyer). [ASSUMPTION]

**Explicitly out of scope for batch 1:** no current Meta spend; well-resourced in-house performance team; large orgs with slow procurement (breaks founder-time constraint).

## 2. Customer Problem

- Advertisers suspect budget is being **wasted** or the account is **mis-set-up**, but have **no trustworthy, independent way to check.** [DESK]
- The obvious alternative — a **free agency audit** — is a **biased sales funnel** designed to win a retainer, not to give the honest full picture (especially if the fix implicates the agency's own work). [REAL-pattern]
- The trigger is **episodic but decisive** — a ROAS drop/plateau, a new/inherited account, an about-to-scale decision, or an agency keep/replace decision. [REAL] Not steady-state pain → "call when it matters," not "always-on."

## 3. The Offer

A **one-time, human-reviewed, independent paid audit** of a Meta Ads account: fast turnaround, fixed price, delivering a **prioritized action plan the customer owns** — with no management contract attached.

- **Positioning:** *"A second opinion on your Meta Ads account from someone with nothing to sell you."* Independence framed as **structural** (a paid, one-time review has no retainer to protect) — not an unbacked claim.
- **Format:** a capped **pilot of 3 slots** ("apply for 1 of 3 pilot slots" — not self-serve checkout), which enforces the founder-time guardrail in the offer itself.

## 4. Deliverables

A **prioritized findings report** (human-reviewed, not an automated dump), covering: [REAL — matches what buyers expect]
- **Measurement health** — Pixel + Conversions API (CAPI) setup
- **Account structure** & campaign organization
- **Audience** overlap / fragmentation
- **Creative fatigue**
- **Placements**
- **Spend efficiency / wasted-spend** read
- **Bid strategy**

Each finding is **prioritized by estimated impact** and paired with a **concrete, evidence-backed action** the advertiser can execute themselves. Plus a **live walkthrough** of the findings.

**Turnaround:** target 2–3 business days, but **under-promise until the first audits are complete** (Creed L1 — zero audits delivered so far; do not commit to a day-count in copy before founder confirms one).

## 5. What Is Explicitly NOT Included

- ❌ **Doing the fixes / implementation** (that is done-for-you work = an agency, or the O2 path) — Creed M4: an "organic upsell" into fixing is the agency trap in disguise.
- ❌ **Writing to / changing the account** (financial liability + Meta ToS automation limits)
- ❌ **Ongoing management or monitoring** (that is O2 — do not sell it here)
- ❌ **Full competitor benchmarking** (that is O4)
- ❌ **Performance guarantees**; ❌ **refund/satisfaction guarantee** unless the founder explicitly approves one (§18)
- ❌ **Any software build** — delivered manually first

## 6. Pricing Hypothesis

| Tier | Price [ASSUMPTION] | Purpose |
|---|---|---|
| Low probe | ¥30,000 (~$200) | Floor test |
| **Anchor (test)** | **¥50,000 (~$330)** | Non-zero so a "yes" = real WTP; low enough to close 3 |
| High probe | ¥100,000 (~$660) | Learn the price-response curve |

**Market comps [REAL]:** Fiverr session **$70–100** · UPLIFY agency audit **$490** (credited toward month-1 management) · standalone agency audit **$1,500–5,000**. The anchor sits deliberately **between the Fiverr floor and the agency ceiling.**

**⚠ Creed H2:** the anchor is **3–5× the Fiverr floor with *less* trust signal** (no reviews, no track record yet). "Paying proves independence is worth it" is circular — so **the price itself is a core thing the pilot tests**, not a settled decision. Final price needs founder confirmation (§18).

## 7. Delivery Process

1. Customer grants **read-only Ads Manager access** *or* sends exported reports/screenshots.
2. Founder performs the **manual analysis** (no software).
3. Founder produces the **prioritized report**.
4. **Live walkthrough**; capture learning (§16–17).

**Key enabler [REAL]:** O1 needs **no Meta API, App Review, or Business Verification** — client-granted Ads Manager access is enough. Lowest-friction possible wedge; fully service-first.
**Capacity guardrail:** **1–2 audits/week max** (see §15). The 3-slot pilot cap is built into the marketing page.

## 8. Customer Data / Access Required

- **Read-only Ads Manager access** (preferred) **or** exported reports/screenshots (lower-friction fallback — offer it up front to pre-empt the access objection).
- Self-reported **monthly spend** + who manages the account.
- Brief **business context** (product, goal) and **account age/ownership** (new vs. established).

## 9. Sales Process

1. **Identify** an ICP-matching prospect via §10 venues.
2. **Outreach** — founder sends (drafts in §10). *(Requires founder authorization first.)*
3. **Discovery call** — script in §11; qualify, surface the trigger.
4. **Present offer + price** (once founder confirms one); handle objections (§12).
5. **Close** — collect **payment or a deposit before any work** (founder collects; a deposit is itself a WTP signal).
6. **Data collection** (§8).
7. **Deliver** the audit (manual, founder-performed).
8. **Follow-up** — live walkthrough, log outcome in `customers/`, and capture O2/O4 learning as research (§16–17).

**Batch capped at 3 customers** to protect founder time.

## 10. Outreach Strategy

**$0-spend, warm-to-cold, capped to the 3-slot pilot** (~1–2 weeks), auto-stopping when slots fill:
1. **Founder's own network** first (warmest, lowest friction, smallest volume — best fit for 3 slots).
2. **Organic, value-first:** `community.shopify.com`, the real **"Facebook Ad Hacks"** FB group [REAL], r/PPC · r/FacebookAds · r/shopify · r/ecommerce [DESK — confirm current rules before posting], LinkedIn small-DTC operators, `note.com` value posts (JP).
3. **Light manual outbound** only if slots remain.

**Excluded as premature spend:** paid ads, SEO investment, MarkeZine/event sponsorship.
**Ready but NOT sent:** 4 outreach drafts (EN cold/warm, JP cold/warm) — honest paid framing. **Any real send requires explicit founder authorization.**
**JP caveat:** JP community venues are **unconfirmed** [ASSUMPTION] — needs a JP-supply check before JP outreach (open item for Oscar).

## 11. Customer Interview / Discovery Questions

**Qualify + close (Dwight's discovery set):**
1. Are you running Meta ads, and roughly what's your monthly spend?
2. Who manages it day-to-day — you, in-house, freelancer, or agency?
3. When did someone last take a hard, structured look at the account — ever? free or paid?
4. What's making you think about this **right now**? *(surfaces the trigger)*
5. If the audit found 3–5 prioritized fixes, **who on your side could act on them**? *(tests whether findings are executable)*
6. Comfortable granting read-only access, or prefer to export reports yourself?
7. Have you **paid** for anything like this before? What did it cost — worth it? *(direct WTP probe)*

**Research debrief (post-audit, framed as improving the service — NOT a pitch; feeds O2/O4 — see §16–17):**
8. After seeing these findings, what would actually help most going forward?
9. How confident are you reading performance *changes* week to week on your own?
10. How often do you feel you need fresh eyes on creative specifically?

## 12. Objection Handling

| Objection | Response (honesty-first) |
|---|---|
| "Agencies give this away free" | Free agency audits are a sales tactic to win a retainer — the incentive is to find *just enough* to sign you. This is independent and one-time, with **no management contract to sell you afterward.** |
| "How do I know your recommendations are right?" | Show a **redacted sample finding** up front, not an abstract promise. *(Any refund/satisfaction guarantee needs founder sign-off first — §18.)* |
| "One-time, not worth a budget line" | Reframe vs. the cost of *not* knowing — a fixable issue wasting a fraction of monthly spend likely exceeds the audit price. |
| "I don't want to share account access" | Offer the **export/screenshot** alternative up front. |
| "Why you / who are you?" | Concrete honest specifics (hands-on Meta background, EN/JP). **No fabricated case studies or testimonials** (PRINCIPLES #13). Being new isn't concealable; being useful in the audit is the proof. |
| "I'll think about it" (stall) | Don't chase — ask for one specific reconnect date; don't round polite interest up to intent. |

**⚠ Creed C1 applied:** the "no upsell" line is honest **only if we do not pitch O2 at delivery.** For the pilot, **do not script an O2 sales offer** (drop Sales §7 / Finance §7's scripted upsell). O2/O4 don't exist yet, so "nothing to sell you afterward" is literally true today — keep it that way and capture interest as *research* (§16–17).

## 13. Validation Metrics

**Milestone: 3 paying audit customers.** Track for each: prospects contacted · conversations · offers made · **paid audits** · **price paid** · **founder hours/audit** · objections heard · recurring problems discovered · interest in ongoing monitoring (O2) · interest in creative analysis (O4) · willingness to pay monthly.

**⚠ Pre-registered falsification (Creed H1 — prevents a false-positive pilot). Decide these BEFORE selling:**
- **≥1 buyer from OUTSIDE the founder's network** (network buyers may pay as a favor → contaminated WTP).
- **Independence cited *unprompted*** by at least one paying buyer as a reason they bought (tests C2 directly).
- **Kill-threshold:** if nobody pays the **¥50k anchor** (only sub-Fiverr prices convert, or only free-favor closes), independence-at-a-premium is **not** validated — stop and rethink the wedge.

## 14. Risks

- **[CRITICAL C1] Positioning honesty landmine** — "no upsell" vs. audit-as-CAC. *Mitigation:* §12 stance (no pilot pitch; capture as research); founder to confirm §18.
- **[CRITICAL C2] Unproven wedge** — independence has zero direct evidence; proven drivers (cheap/fast, credited-to-mgmt, brand/depth) are the ones we reject. *Mitigation:* §13 makes testing it the pilot's primary job.
- **[HIGH H2] Price–trust gap** — 3–5× Fiverr with no track record. *Mitigation:* price probes ¥30k/¥50k/¥100k; sample finding; deposit.
- **[HIGH H3] Ceiling + exit dependency** — O1 alone caps ~¥400k/mo (below the ¥1M goal) and is 100% founder-bound; the agency-trap **exit depends on O2/O4, which are unbuilt** and ranked risky in Phase 4. *Mitigation:* validate **audit→recurring intent** early (§16–17); O1 justified only as an acquisition channel, never scaled as an end.
- **[MED] M1** ICP band (→ target higher spend, §1) · **M2** depth-vs-compression (compressing delivery to escape the trap hollows the "deep neutral" value prop) · **M3** no QA gate on the audit's *own* correctness → attribution noise → confident-but-wrong = liability (add a self-check before delivery) · **M4** organic "just fix it" upsell = agency, not O2/O4.
- **[LOW] L1** don't over-promise turnaround before any audit is done.
- **Cross-cutting:** Meta API/policy changes; AI commoditization of "audits"; EN/JP founder-time split.

## 15. Founder Time Required

| | Early (first audits) | Templated (later) |
|---|---|---|
| Delivery/audit | 5–10 h | 2.5–5 h |
| **Total/audit** (incl. scoping, access, follow-up) | **6–12 h** | 3.5–7 h |
| Founder-hour **yield** (price ÷ hrs) | ~¥5.6k/h | ~¥10k/h |

- **Sustainable ceiling: 1–2 audits/week.** **3+/week (~15+ h) = 100% of time on delivery, 0% on automation = THE AGENCY TRAP** → deliberately **cap** O1 slots, don't scale.
- **3-customer batch ≈ 20–35 h delivery** over ~2–4 weeks, plus outreach/discovery overhead.
- **Judge O1 on founder-hour yield + audit→recurring conversion — NOT cash margin (a misleading ~90%) or volume.**
- **[ASSUMPTION requiring founder confirmation]** this all hinges on the founder having **~10–15 h/week**, and that *same* pool must later fund building O2/O4. Confirm (§18).

## 16. What We Need to Learn Before Moving Toward O2 (Monitoring & Intelligence)

Capture during/after each audit (as research, not a pitch):
- Does the customer **want ongoing monitoring** after seeing a point-in-time snapshot?
- Do they **struggle to understand performance changes** week to week?
- Would they **pay monthly** for monitoring (~**¥15–30k/mo** [ASSUMPTION])?
- **Audit → recurring conversion rate** and likely **retention/churn** — the make-or-break number for the whole strategy (H3).

## 17. What We Need to Learn Before Moving Toward O4 (Creative Performance Analysis)

- Is **creative fatigue** a recurring (not one-time) pain for them?
- Do they need **more frequent creative analysis** than an annual audit gives?
- Would they **pay monthly** for ongoing creative-performance analysis?
- Which do they value more — **monitoring (O2)** or **creative (O4)** — when forced to choose?

## 18. Exact Next Actions Required From the Founder

**Decisions needed before any outreach:**
1. **Resolve C1 positioning** — confirm the recommended stance: pilot stays **purely independent, no scripted O2 pitch at delivery**; O2/O4 interest captured as research only. (Alternative: reframe the public promise — but that weakens the wedge.)
2. **Confirm final price** (recommend testing **¥50k anchor**, probing ¥30k/¥100k) **and** whether to state a turnaround day-count yet.
3. **Approve or decline** a refund/satisfaction guarantee (needed before it's ever offered).
4. **Confirm weekly capacity** (~10–15 h/week? [ASSUMPTION]) and accept the **1–2 audits/week cap** / 3-customer batch.
5. **Approve the pre-registered falsification criteria** in §13 (non-network buyer, unprompted independence, ¥50k kill-threshold).
6. **Authorize outreach** — which channels, and (if using founder network) provide/identify the specific real contacts. **No message is sent until this is given.**

**Housekeeping (founder OK requested):**
7. **Decommission the zombie agent `jim-mt70w6lr`** (broken cwd, cannot run; its Phase-4 work is safe in git).
8. **Authorize consolidation + release** of the Phase-5 files (research branch + uncommitted sales/finance + this plan) to `origin/main` via Meredith.

**Then:** ZeroEn WAITS for founder approval before beginning external outreach. This phase ends when we have enough real-world evidence to decide whether O1 is a viable acquisition wedge and whether O2 or O4 deserves the next validation cycle.

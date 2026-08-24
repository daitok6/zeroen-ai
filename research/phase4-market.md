# Phase 4 — Market Research (P1)

**Owner:** god/Michael (reassigned from Oscar — hive research agents were stalled; founder handed P1 to god 2026-08-24 11:06).
**Scope:** Real market evidence for candidates O1–O8 to feed synthesis fields #3 (evidence problem exists), #4 (existing alternatives), #5 (competitors), #10 (technical difficulty).
**Evidence discipline:** [REAL] = cited public source · [DESK] = reasoned from public patterns · [ASSUMPTION] = unverified. No fabricated numbers/sources. Phase-3 artifacts treated as void.
**Coverage caveat:** This is a focused desk pass concentrated on the ranking-deciding candidates, EN-market. JP-market depth and primary-source demand (raw Reddit/forum threads) are logged as evidence-still-missing.

---

## Cross-cutting finding (drives ranking)
[REAL] Meta's **native tools are free and improving**: Advantage+ and native **automated rules** are free and are "the correct starting point"; native rules are single-condition only — third-party tools become worthwhile "around 5–10 active accounts or when you need compound logic," and are "table stakes for advertisers spending >$50K/month." (didoo.ai, adadvisor.ai, get-ryze.ai, 2026)
→ **Implication:** The defensible wedge is what Meta does NOT give away free — cross-account intelligence, creative benchmarking vs the market, and the "what to do next" synthesis layer — and the paying customer is the **higher-spend advertiser / agency**, not the small self-serve advertiser. Confirms Kevin (P4) + Creed (P5).

---

## O1 — Meta Ads performance auditing
- **Competitors/alternatives [REAL]:** Meta Ad Library (free, no performance context); AdSpy ($149/mo flat, 160M+ ad archive); AdEspresso ($49/mo <$1K spend, $149/mo $10K+); Trackingplan (measurement-layer audits). (tryatria.com, webtonic.io, trackingplan.com, 2026)
- **Demand evidence [DESK]:** Audits are a common agency lead-gen/onboarding step; demand exists but as a **one-time** purchase, not recurring.
- **Underserved gap [DESK]:** Most "audit" tools are ad-*spy*/intelligence, not a structured account-health audit with prioritized fixes. Room for a productized audit deliverable.
- **Technical difficulty [DESK]:** Low–moderate. Read-only `ads_read` insights pull; no App Review for own-account demo. Founder Next.js skill sufficient.
- **Verdict:** Real but **one-time / low recurring**; best as a paid **on-ramp**, not the destination (matches Kevin).

## O2 — Meta Ads monitoring & intelligence
- **Competitors [REAL]:** Revealbot ($99/mo up to $10K spend → $399/mo at $100K, spend-tiered); Madgicx ($300–$800/mo, AI Marketer monitors 24/7 + anomaly detection + Slack alerts); Wevion, Ryze. (adevolver.uk, adlibrary.com, madgicx.com, 2026)
- **Demand evidence [REAL]:** A real paid market exists above free native rules; "table stakes >$50K/mo spend." Anomaly/budget-drain detection is an explicit marketed pain (madgicx.com).
- **Underserved gap [DESK]:** Detection alone is commoditizing; the **explanation + recommended next action** ("why it changed, what to do") is the value layer Meta doesn't provide free.
- **Technical difficulty [DESK]:** Moderate. Scheduled insights polling + change detection + rules; rate limits (BUC) manageable. Higher if real-time.
- **Verdict:** Strong end-state economics (recurring); wedge MUST be the intelligence/next-action layer, not raw alerts.

## O3 — Advertising creative generation
- **Competitors [REAL]:** AdCreative.ai ($39/mo entry); plus Meta's own free generative creative. (getapp.com, 2026)
- **Demand evidence [REAL]:** Real recurring demand and value-linked pricing, BUT reviews are mixed and the category is **trust-damaged**: widespread complaints about surprise post-trial charges, hard cancellation, slow refunds (Trustpilot, Product Hunt, Reddit). (trustpilot.com/review/adcreative.ai, producthunt.com)
- **Underserved gap [DESK]:** Quality consistency is weak ("only a portion usable without rework"). But moat is thin and Meta gives generative creative free.
- **Technical difficulty [REAL/DESK]:** Moderate–high (image/video gen compute + curation cost erodes margin — Kevin).
- **Verdict:** Crowded, low-moat, reputationally noisy, free-substitutable. **Watchlist / downstream add-on to O4**, not lead.

## O4 — Creative performance analysis
- **Competitors [REAL]:** Motion (~$250/mo up to $50K spend); Foreplay ($49/mo research, $99 for analytics); Atria ($159/mo Core, $329 Plus, $500K spend cap, bundles creative analysis + competitor intel + $9B benchmarking). (tryatria.com, foreplay.co, motionapp.com, 2026)
- **Demand evidence [REAL]:** Active, growing paid market; "creative intelligence … table stakes >$50K/mo." Price is tied to a decision advertisers value (where to put creative budget).
- **Underserved gap [DESK]:** Motion "stays inside your own account — no market benchmark, no competitor intelligence." Cross-account + benchmark + JP-market creative analysis is a gap. **Not** free-substitutable by Meta (Meta gives no cross-account creative benchmarking).
- **Technical difficulty [DESK]:** Moderate. Insights + creative-asset pull + tagging/scoring.
- **Verdict:** **Front-runner** — real WTP, decision-linked pricing, least free-substitutable. Confirms Kevin's co-leader call.

## O5 — Reporting (client/stakeholder)
- **Competitors [REAL]:** Very crowded — Swydo, AgencyAnalytics, Whatagraph, DashThis, Madgicx, TheOptimizer, AgencyDashboard, etc. Pricing $20/client/mo → $49/mo → $4,999+/mo enterprise. (swydo.com, agencyanalytics.com, madgicx.com, 2026)
- **Demand evidence [REAL — strongest of all candidates]:** "Manual Facebook Ads reporting … one to three hours per client," error-prone and stale on delivery; "inefficient reporting → unhappy clients → churn." Clear, quantified, monetized pain.
- **Underserved gap [DESK]:** Demand is high but the space is **hyper-commoditized** — the problem is differentiation/pricing power, NOT demand. Possible wedges: JP-market reporting (US tools weak in JP), or reporting bundled into O4/O2 rather than sold standalone.
- **Technical difficulty [DESK]:** Low–moderate (data pull + templated dashboards/PDF). Founder-feasible.
- **Verdict:** Highest demand, lowest pricing power standalone. Best as a **feature/wedge inside O4/O2** or a JP-differentiated play — reconsider vs Kevin/Creed's "rank down" given the demand strength.

## O6 — Optimization workflows
- **Competitors [REAL]:** Revealbot, Madgicx (rules engines + AI); free Meta native rules for single-condition cases. (adadvisor.ai, 2026)
- **Demand evidence [DESK]:** Real for compound logic at scale (5–10+ accounts).
- **Risk [REAL/DESK]:** If it **writes to the account**, it carries financial liability + ToS automation limits + trust barrier (Creed P5). Free native rules cover the simple cases.
- **Technical difficulty [DESK]:** High (write access, safety, liability).
- **Verdict:** Higher-risk, free-substitutable at the low end. **Rank down.**

## O7 — Marketing automation (broader)
- **Competitors [REAL/DESK]:** Fragmented; overlaps HubSpot/Zapier-class + Meta-specific tools.
- **Verdict [DESK]:** Too broad → bespoke per customer → founder labor scales with customers (against the no-proportional-labor objective, Kevin). **Rank down.**

## O8 — Adjacent (open lane)
- **Candidate adjacents surfaced [DESK]:** (a) **JP-market Meta-ads tooling** — US incumbents (Motion/Atria/Revealbot) are EN-first; founder's EN/JP + Meta edge is a real differentiator worth its own investigation. (b) **Competitor/creative *spy* intelligence** (AdSpy $149, MagicBrief, Atria) — adjacent to O4. (c) **Audit→monitoring productized-service ladder** (O1→O2).
- **Verdict:** JP-angle is the most interesting adjacent; must clear a HIGHER evidence bar (Creed) — currently [ASSUMPTION].

---

## god/P1 ranking (research lens — demand + defensibility)
1. **O4 Creative performance analysis** — real WTP, decision-linked pricing, least free-substitutable, active growing market.
2. **O2 Monitoring & intelligence** — real recurring market above free rules; wedge = explanation/next-action layer.
3. **O5 Reporting** — *strongest, most quantified demand*, but hyper-commoditized; viable only via differentiation (JP) or bundled into O4/O2. Flagging the demand/pricing-power tension explicitly for synthesis.
4. **O1 Audit** — best paid on-ramp (one-time), converts to O2/O4.
- Down: O3 (crowded/low-moat/trust-damaged/free-substitutable), O6 (liability + free native), O7 (bespoke labor).
- **Cross-cutting confirm:** favor what Meta doesn't give free + higher-spend advertiser/agency buyer.

## Evidence still missing (feeds field #13)
- Primary-source demand (raw Reddit r/PPC, r/FacebookAds, r/agency threads; G2/Capterra review mining) — this pass used secondary syntheses, not primary quotes.
- **JP-market** competitor set, pricing, and demand (critical to the O8/JP wedge and founder's edge).
- Real per-account API/compute cost (for O2/O3/O4 margins) — hand to Kevin.
- Actual WTP (not list price) — hand to Dwight's demand lens.

## Sources (representative [REAL])
tryatria.com; webtonic.io; trackingplan.com; adevolver.uk; adlibrary.com; madgicx.com; getapp.com; trustpilot.com/review/adcreative.ai; producthunt.com; foreplay.co; motionapp.com; swydo.com; agencyanalytics.com; didoo.ai; adadvisor.ai; get-ryze.ai (all accessed 2026-08-24).

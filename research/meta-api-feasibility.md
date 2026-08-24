# Meta (Graph / Marketing) API Feasibility — Technical + Legal

**Task:** T1 (Critical). Resolve whether ZeroEn can actually obtain and use Meta
advertising API access — the single point of failure all four strategy
hypotheses depend on (confirms QA audit §3.1, §4.5).
**Author:** Market Intelligence Lead (Oscar) · **Date:** 2026-08-24
**Status of this doc:** feasibility spike, not a build. Evidence labeled below.

---

## TL;DR — Go / No-Go

**GO, conditional.** Access is feasible via a documented, well-trodden path, and
a May 2026 Meta change actually *lowered* the barriers. Nothing here blocks
validation. But access is **gated and revocable**, so treat it as a managed
dependency, not a settled asset:

- **Read-only data for A (Audit) and B (Monitoring)** is obtainable now, at ¥0,
  with **no App Review and no Business Verification**, against the founder's own
  ad account in a Development-mode app.
- **Serving third-party (client) ad accounts** requires **App Review** for
  `ads_read` / `ads_management` **+ Business Verification** (~days to a few
  weeks) and a **data-processing/legal posture** (DPA, APPI, GDPR).
- **Scale** (frequent monitoring across many accounts) is capped by rate limits
  and requires the **Marketing API Access Tier** feature — which itself requires
  pre-existing live API volume (chicken-and-egg for scale, not for validation).
- **Residual risk (unchanged):** Meta can restrict or revoke access unilaterally
  and has a history of doing so. This risk cannot be eliminated, only managed.

**Recommendation:** Run the ¥0 dev-app spike now (below). Defer App Review,
Business Verification, and DPA work until a paying pilot exists.

---

## (a) API endpoints each hypothesis needs

*Evidence: verified against Meta developer docs / Ads Insights API; general Meta
API structure is stable and well-established.*

| Hypothesis | Core endpoints (Graph/Marketing API) | Read/Write | Min permission |
|---|---|---|---|
| **A — Audit** | `GET /act_{id}/insights` (70+ metrics, breakdowns, attribution windows); `GET /act_{id}/campaigns`, `/adsets`, `/ads`, `/adcreatives`; account-level fields (spend, settings); adset `targeting` | Read only | `ads_read` |
| **B — Intelligence / Monitoring** | Same read endpoints, polled on a schedule (Meta offers limited ads webhooks; monitoring is mostly polling insights + change detection) | Read only | `ads_read` |
| **C — Creative Engine** | *Generation is outside the Meta API (AI/tooling).* To **publish & test** creative: `POST /act_{id}/adimages`, `/advideos`, `/adcreatives`, then `/adsets` + `/ads` | Write | `ads_management` |
| **D — Combined loop** | Union of A/B (read) + C (write) — performance → analysis → creative → test → new performance | Read + Write | `ads_read` + `ads_management` |

**Note (inference):** Hypothesis **C can stay read-only** if ZeroEn only
*recommends* creative and the client uploads it manually — this avoids
`ads_management` and its heavier review/liability entirely. Worth testing as the
cheaper first version of C.

Facts: ad account IDs are prefixed `act_`; `ads_read` = read performance/campaign
data, `ads_management` = create/manage/delete ads.

## (b) App Review, access tier, Business Verification, time-to-access

*Evidence: verified. Primary source — Meta developer blog, May 4 2026 (AMSA
rename); corroborated by multiple 2026 practitioner guides.*

- **Development mode (no review):** A newly created Meta app can call the
  Marketing API against **ad accounts the app's own admins/developers/testers
  own or administer**. This is enough to prove the A/B data pipeline on the
  founder's own account. *(Established Meta flow.)*
- **Serving other businesses' accounts:** requires **App Review** approval of
  `ads_read` (and `ads_management` for write) **and Business Verification** of a
  legitimate business entity. App Review submission includes a screen recording
  and a working use-case demonstration.
- **Marketing API Access Tier (formerly "Ads Management Standard Access"/AMSA):**
  On **May 4, 2026** Meta renamed AMSA to "Marketing API Access Tier" and
  **lowered** the qualification threshold from **1,500 → 500 Marketing API calls
  in the past 15 days**, with an **error rate < 15%** over a rolling window of
  the last 500 calls. This feature unlocks **higher rate limits + system-user
  quotas** needed to monitor many accounts. It requires prior live API volume to
  qualify — you must already be operating to earn scale.
- **Rate limits (Business Use Case, per ad account):** read = 1 point, write = 3
  points; development-level access caps around **60 points / 300-second window**;
  heavy insights pulls with breakdowns cost disproportionately more. *(2026
  practitioner sources; directionally reliable, exact numbers can drift.)*
- **Realistic time-to-access:** Business Verification typically **~3–15 business
  days**, occasionally weeks; ~40% of first-attempt rejections stem from document
  format/mismatch. App Review adds additional days. **Plan for 1–4 weeks** from
  "decide to serve clients" to "approved," so start it *before* a pilot needs it.

## (c) ToS + legal constraints (storing/analyzing client ad data; APPI + GDPR)

*Evidence: Meta Platform Terms / Developer Data Use Policy + Meta Data Processing
Terms (verified they exist and govern this); regulatory analysis is reasonable
inference for a service that has not yet defined its data flows.*

- **Meta contractual constraints on Platform Data:** purpose limitation (use data
  only to provide the user's requested service), **data minimization**, no
  selling/transferring data, security requirements, and **deletion on
  request/termination**. Access tokens must be stored securely. Violations are
  grounds for access revocation.
- **Data-controller vs processor:** the **advertiser (client) is the data
  controller** of their ad-account data; **ZeroEn acts as a data processor** →
  needs a **Data Processing Agreement (DPA)** with each client, must act on their
  instructions, minimize data, and set retention limits.
- **APPI (Japan):** requires purpose specification, security control measures, and
  restrictions on third-party / **cross-border** transfer (notice/consent or
  adequate safeguards). Aggregate ad *insights* are largely non-PII (lower
  exposure); **OAuth tokens, custom/lookalike audience data, and any PII raise
  exposure sharply**.
- **GDPR (EU market is explicitly targeted):** lawful basis, DPA, data
  minimization, retention limits, DSAR handling, and **cross-border transfer
  safeguards (SCCs)** if data leaves the EEA (it will, on non-EU infra).
- **Practical mitigation (recommended posture):** store the *minimum* — prefer
  **aggregate insights**, avoid pulling PII / audience lists unless required;
  short retention; **encrypt tokens at rest**; per-client DPA template;
  account access only via explicit **OAuth consent**. This keeps APPI/GDPR
  exposure low during validation. (Coordinate with Kevin for legal depth before
  first real client account.)

## (d) Go/no-go + cheapest hands-on proof of access

**Verdict: GO for validation.** The cheapest, highest-value check is a **¥0
development-mode spike on the founder's own ad account — no App Review, no
Business Verification, no client data, no legal exposure:**

1. Create a Meta app; add the **Marketing API** product; keep it in
   **Development mode**.
2. Generate a token with **`ads_read`** for the **founder's own** ad account.
3. Pull `GET /act_{id}/insights` (with breakdowns) + `campaigns`/`adsets`/`ads`/
   `adcreatives`. → **Proves the A (Audit) + B (Monitoring) data pipeline
   end-to-end.**
4. *(Optional, for C)* In dev mode, create a **paused** ad image/creative via
   `ads_management` on the founder's own account to prove the write path.

**Pass criterion:** real insights + creative metadata returned from the founder's
account. **This answers "can we get the data?" before any customer-facing work,
App Review, or spend.**

**Then, and only when a paid pilot is lined up:** start Business Verification +
App Review (1–4 wks), stand up the DPA/consent posture, and design around rate
limits. Flag to Michael: multi-account monitoring at scale needs the Marketing
API Access Tier (needs prior live volume) — sequence real usage first.

---

## Open risks to carry forward

- **Platform dependency (Critical, per QA §3.1):** access is revocable and Meta
  can change terms; not eliminable — design for graceful degradation and don't
  build a business that dies if one endpoint closes.
- **Verification requires a real, documentable business entity** — a side project
  without one will stall at Business Verification.
- **Scale chicken-and-egg:** the upper rate-limit tier requires prior live API
  volume (500 calls/15d) — fine for validation, a constraint for growth.
- **Numbers marked "practitioner sources" (rate-limit points, exact timelines)
  should be re-confirmed against Meta docs before they inform a build decision.**

## Sources

- Meta for Developers blog, *"Update to Ads Management Standard Access…"* (May 4,
  2026): https://developers.meta.com/blog/updates-to-ads-management-standard-access-feature/
- Meta Ads Insights API docs: https://developers.facebook.com/documentation/ads-commerce/marketing-api/insights
- Meta Data Processing Terms: https://www.facebook.com/legal/terms/dataprocessing
- Meta Developer Data Use Policy: https://developers.meta.com/horizon/policy/data-use/
- Practitioner corroboration (2026, access tiers / permissions / rate limits /
  verification timelines): admanage.ai/blog/meta-ads-api; singhamandeep.com/facebook-ads-api-permission-app-review;
  adlibrary.com/posts/meta-marketing-api-guide-2026; windsor.ai/guide-to-facebook-meta-ads-api;
  adstellar.ai/blog/meta-business-verification
- Internal: `qa/initial-company-audit.md` (§3.1, §3.2, §4.5), `STRATEGY.md`

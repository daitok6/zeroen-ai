# Meta API — Legal & Compliance Cost Angle (Finance costing)

Owner: Finance (Kevin) · Conversation: conv-t1-metaapi (T1)
Input source: Oscar's T1 feasibility finding (research/meta-api-feasibility.md — being integrated to main)
Last updated: 2026-08-24

> **Evidence status:** No verified cost figures exist. Every number below is an
> `ASSUMPTION` or `HYPOTHETICAL EXAMPLE` for scoping only, never a quote or a
> forecast (PRINCIPLES #1, #13). Actual costs must be confirmed before any
> money is committed — Finance does not authorize spending (#9).

---

## 1. What actually triggers these costs

Critical scoping point from Oscar: **none of the legal/compliance cost below is
triggered by the dev-app spike on the founder's OWN ad account** (no client
data). It only triggers **when ZeroEn touches a real CLIENT account.**

Finance implication: the cheapest validation path (founder's own account) has
**~¥0 legal/compliance cost**. Legal cost is a **gate on paid client
delivery**, not on technical validation. Sequence the spend accordingly.

---

## 2. Cost items (each labeled, none verified)

| Item | Direct fee | Effort / time (ASSUMPTION) | Notes |
|---|---|---|---|
| **Meta Business Verification** | None (per Oscar) | Blocked on having a registered entity | Bottleneck; see #3. Flagged to founder as T3. |
| **App Review** (`ads_read`/`ads_management`) | None | Founder time: screencast + working demo | Time cost, not cash. Fold into founder-hours. |
| **Per-client DPA** (JP + EN) | Template: low; lawyer review: unknown | One-time template build, then near-zero per client if reusable | See #4 — reusability is the key economics lever. |
| **Registered business entity (JP)** | Government/registration fees — **UNVERIFIED** | Setup lead time — **UNVERIFIED** | Likely the real gating cost. See #3. |
| **Ongoing compliance** (token encryption, retention, DSAR handling) | Mostly infra/founder time | Small if scope kept minimal (Oscar's mitigation) | Recurring, folds into gross margin + support burden. |

---

## 3. The likely bottleneck: registered entity (JP)

Business Verification requires a **real, documentable business entity**. If
ZeroEn is not yet a registered entity, this is the gating cost — in **cash
(registration/government fees), time (lead time to establish), and possibly
ongoing obligations** (accounting/tax filing once incorporated).

- Finance does **not** have verified JP incorporation figures and will not
  invent them. This needs a founder decision + a real quote.
- **Scalability note:** this is a **one-time fixed cost**, not per-customer, so
  it does not threaten unit economics — but it is a hard prerequisite that
  blocks *all* paid client delivery. It should be costed before, not after,
  committing to a client-facing offer.

---

## 4. DPA economics — the one item with a real scaling lever

A per-client DPA is required (client = data controller, ZeroEn = processor).
The economics hinge on **reusability**:

- **Build once, reuse per client** → the DPA becomes a ~¥0 marginal step per
  customer (attach template, sign). Good for scalability.
- **Bespoke per client / lawyer per client** → per-customer legal cost that
  scales with customer count — this would directly **erode gross margin and
  violate the "no proportional labor" objective** (COMPANY.md / PRINCIPLES #4).

**Recommendation (assumption, to pressure-test):** invest once in a reusable
JP+EN DPA template; reserve paid lawyer review for a **single one-time template
sign-off**, not per client. Whether lawyer review is warranted vs. a vetted
template is a **risk-appetite call for the founder** — Finance's view: for
low-exposure validation with Oscar's minimization mitigations in place, a
vetted template first, lawyer review before scaling, is the cheaper sequence.

---

## 5. Pressure-testing Oscar's minimization mitigation (Finance view)

Oscar's mitigations (aggregate/minimum data only, no PII/custom-audience data,
short retention, encrypt tokens at rest, OAuth consent) are **also the
cheapest compliance posture**: they shrink DPA scope, reduce APPI/GDPR
cross-border exposure (SCCs, DSAR load), and lower ongoing support burden.
Finance endorses them not only as risk control but as **cost control**. The
main cost they add is modest founder/infra time for encryption + retention
tooling — folds into infrastructure cost per customer, assumed small at
validation scale.

---

## 6. Cheapest validation sequence (PRINCIPLES #11)

1. **Now (~¥0 legal):** technical spike on founder's own account. No entity,
   DPA, or App Review needed.
2. **Before first paid client:** get a real quote for (a) JP entity
   registration and (b) one-time DPA template + optional lawyer sign-off.
   These are the only two figures that need verifying to unblock paid delivery.
3. **Decision gate for founder/Michael:** compare that one-time fixed legal
   cost against expected early revenue. Do **not** incorporate or pay for legal
   work until willingness-to-pay evidence exists (Sales) — sequence legal spend
   *after* a validated paid offer, not before.

---

## 7. Open items Finance needs to finalize numbers

- Verified JP entity registration cost + lead time (founder / real quote).
- Whether founder already has any registered entity.
- Vetted-template vs. lawyer-review cost for the DPA (one real quote).
- Infra cost of token encryption + retention tooling (from whoever builds the
  spike) to fold into per-customer infrastructure cost.

Until these are verified, treat all figures here as scoping assumptions only.

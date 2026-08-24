# T7 — ¥0 Meta API Dev-App Spike (Founder-Executable Checklist)

**Goal:** Prove ZeroEn can pull Meta ad performance + creative data end-to-end —
**at ¥0, no App Review, no Business Verification, no client data** — against the
**founder's OWN ad account** in a Development-mode app. This is the cheapest test
that answers "can we actually get the data?" (validates hypotheses A/Audit &
B/Monitoring; optional write test for C/Creative).
**Author:** Oscar (Market Intelligence) · **Date:** 2026-08-24 · Founder greenlit (T3).
**Pass criterion:** real rows (spend/impressions/creative metadata) returned from
the founder's own account.

**Version note:** examples use `<VERSION>` — use the current Graph API version
shown in your App Dashboard / Graph API Explorer (do not hardcode an old one).
Do **not** commit or paste the access token anywhere shared — treat it as a secret.

---

## Prerequisites (2 min)
- [ ] A Facebook account that is an **admin of the founder's own ad account**.
- [ ] The **ad account ID** (`act_XXXXXXXXX`) — find it in the Ads Manager URL,
      or Business Settings → Accounts → Ad accounts.
- [ ] The account has **real, recent Meta ad spend** (so insights return rows).

## Step 1 — Create a developer app (5 min, no review)
- [ ] Go to https://developers.facebook.com → register as a developer (free).
- [ ] **My Apps → Create App → type "Business"**. Name it e.g. `ZeroEn Dev`.
      Leave it in **Development mode** (default). Note the **App ID / App Secret**.
- [ ] In the app, **Add Product → "Marketing API"**.

## Step 2 — Get an `ads_read` access token (5 min)
Pick ONE:

**Option A — Fastest (short-lived, ~1–2 hrs), good enough for a one-shot proof:**
- [ ] Open **Graph API Explorer** (https://developers.facebook.com/tools/explorer).
- [ ] Select your app; under **Permissions** add **`ads_read`**.
- [ ] Click **Generate Access Token** → authorize. Copy the token.

**Option B — More robust (longer-lived / repeatable), if you want to re-run:**
- [ ] Business Settings → **Users → System Users → Add** (create a system user).
- [ ] **Assign the ad account** to that system user with view access.
- [ ] **Generate a token** for the system user with the **`ads_read`** scope
      (system-user tokens can be long-lived). Copy it.
- *(Or exchange the Explorer token for a ~60-day long-lived token via
  `GET /<VERSION>/oauth/access_token?grant_type=fb_exchange_token&client_id=<APP_ID>&client_secret=<APP_SECRET>&fb_exchange_token=<SHORT_TOKEN>`.)*

## Step 3 — Pull performance insights  →  proves Hypothesis A/B (5 min)
```bash
curl -G "https://graph.facebook.com/<VERSION>/act_<AD_ACCOUNT_ID>/insights" \
  --data-urlencode "level=campaign" \
  --data-urlencode "date_preset=last_30d" \
  --data-urlencode "fields=campaign_name,spend,impressions,clicks,ctr,cpc,actions,purchase_roas" \
  --data-urlencode "access_token=<TOKEN>"
```
- [ ] **PASS** when you get JSON rows with real `spend`/`impressions`/`ctr` per campaign.
- Try a breakdown to confirm depth: add `--data-urlencode "breakdowns=age,gender"`.

## Step 4 — Pull campaign/ad/creative structure  →  proves audit + creative read (5 min)
```bash
# Campaigns
curl -G "https://graph.facebook.com/<VERSION>/act_<AD_ACCOUNT_ID>/campaigns" \
  --data-urlencode "fields=name,status,objective" \
  --data-urlencode "access_token=<TOKEN>"

# Ads + their creative (title/body/image) — feeds a creative audit
curl -G "https://graph.facebook.com/<VERSION>/act_<AD_ACCOUNT_ID>/ads" \
  --data-urlencode "fields=name,status,creative{id,title,body,image_url,thumbnail_url,object_story_spec}" \
  --data-urlencode "access_token=<TOKEN>"
```
- [ ] **PASS** when campaign list + creative metadata (titles/bodies/image URLs) return.

## Step 5 (OPTIONAL) — Write test for Hypothesis C (only if testing creative publish)
- Requires **`ads_management`** scope (add it in Step 2). In Development mode this
  works on the founder's own account with no review.
- [ ] Create a **PAUSED** ad creative (keep it paused → **no spend**):
```bash
curl -X POST "https://graph.facebook.com/<VERSION>/act_<AD_ACCOUNT_ID>/adcreatives" \
  -F "name=ZeroEn test creative" \
  -F "object_story_spec={...}" \
  -F "access_token=<TOKEN>"
```
- Skip this for a pure ¥0 read-only proof. Delete the test object afterward.

---

## Interpreting the result
- **All PASS** → the A/B (and read side of D) **data pipeline is proven**; the
  Meta-dependency risk drops from "unknown" to "works on our own account." Report
  the returned fields — they define what an audit/monitoring product can show.
- **Fails / missing fields** → capture the exact error (code + message) and send
  to me; common causes are token scope, ad account not assigned, or an expired
  token (Option A tokens die in ~1–2 hrs).

## Boundaries & caveats
- **This proves nothing about serving CLIENT accounts** — that still needs App
  Review + Business Verification + a DPA (see `research/meta-api-feasibility.md`
  §b/§c; Kevin owns the legal-cost angle).
- **Rate limits:** dev-level Business-Use-Case budget is small (~60 points / 300s;
  a read = 1 point) — fine for this manual test, not for scaled monitoring.
- **Security:** the token grants read access to the ad account — do not commit it,
  paste it in chat, or store it in the repo. Revoke/regenerate after the test.
- Do not point this at any account the founder does not own/administer.

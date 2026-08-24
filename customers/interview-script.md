# Discovery Interview / Outreach Script (Draft)

**Purpose:** learn whether the pain behind hypotheses A–D is real, painful
enough to act on, and already has money attached to it — without pitching a
product ZeroEn hasn't committed to. Style: Mom Test-style discovery — ask
about specific past behavior and money already spent, not hypothetical future
interest. Avoid leading questions ("wouldn't it be great if...").

Every question below is neutral by design. Do not add ZeroEn's product ideas
into the question itself — that contaminates the answer.

## Outreach Message (opening contact — template, EN)

> Hi [Name] — I'm doing research on how small businesses/ecommerce brands
> handle Meta (Facebook/Instagram) advertising performance and creative. I'm
> not selling anything — just trying to understand what's actually hard about
> it day to day. Would you be open to a 15-minute call, or even just a few
> quick questions over [channel], about how you currently handle your Meta
> Ads?

## Outreach Message (opening contact — template, JP)

> [お名前] 様、突然のご連絡失礼いたします。Meta広告(Facebook/Instagram)の運用や
> 効果測定、クリエイティブ制作について、中小企業やEC事業者がどのような課題を
> 抱えているか調査しております。何かを販売する目的ではなく、現状の運用で
> 実際に困っていることを伺いたいと考えています。15分ほどお電話、もしくは
> [チャネル] でいくつか質問させていただくことは可能でしょうか。

Both templates are prepared drafts only — see `customers/outreach-plan-and-log.md`
for send status and authorization state.

## Interview Question Set

### 1. Warm-up / Qualifying

1. Do you currently run ads on Facebook or Instagram? Roughly how long have
   you been running them?
2. Is there anyone on your team whose main job is performance marketing / ad
   management, or is it split across other responsibilities?
3. Roughly what's your monthly Meta Ads spend right now? (Fine to answer in a
   range.)

### 2. Current Behavior & Pain (ask about the past, not hypotheticals)

4. Walk me through the last time you looked at how your Meta Ads were
   performing — what were you trying to figure out, and how did you actually
   check it?
5. Tell me about the last time an ad's performance changed unexpectedly
   (better or worse). How did you find out, and how did you figure out why?
6. Where does new ad creative (images, video, copy) come from right now? Who
   makes it, and how often does it change?
7. What's the most frustrating or time-consuming part of managing your Meta
   Ads today?

### 3. Current Solutions & Existing Spend (this is the willingness-to-pay
signal — what they already do, not what they'd hypothetically do)

8. Which of these do you already pay for, if any: ad account management
   help, a freelancer/agency, a reporting/dashboard tool, an attribution
   tool, a creative-production tool, or an automation tool? (Structured
   per Oscar's T5 desk research — naming the categories surfaces spend a
   generic "what tools do you use" question misses.)
9. Roughly how much per month do you spend on ads **tools/services**, not
   counting ad spend itself? Buckets: $0 / <$100 / $100–500 / $500–1,500 /
   $1,500+. (Per T5: **$100+/month here is a demonstrated
   willingness-to-pay signal** for this problem category, not just
   interest — and it's a useful cross-check against the ad-spend answer in
   Q3, since tool pricing in this space tends to scale with ad spend.)
   - If Segment B (ecommerce): ask specifically whether they use Triple
     Whale, Northbeam, Motion, Madgicx, or Revealbot, and at what price.
   - If Segment C (agency/freelancer): ask number of client accounts, total
     ad spend under management, and whether they use AgencyAnalytics,
     Whatagraph, Swydo, or similar.
10. Have you tried any tool or service specifically for ad performance
    monitoring, auditing, or creative generation before? What happened — did
    you keep using it, and why or why not? If they say no/never — ask why
    not (price, didn't know one existed, tried and it didn't work) — for
    Segment A in particular this may surface a real inability/unwillingness
    to pay rather than unmet need (see `customers/target-segments.md`
    disconfirming flag).
11. If you had to guess, how much time per week goes into managing/reviewing
    your Meta Ads across your team?

### 4. Reaction & Next Step (do NOT pitch a specific ZeroEn product — describe
the *category* of help only if asked, and treat any positive reaction as
Interest, not Intent — see `sales/README.md`)

12. (Only if they ask what this is for / show real curiosity) *"We're looking
    into whether a service that [audits performance / monitors and explains
    changes / generates new ad creative — pick the category most relevant to
    what they just described] would be useful. Is that something you've
    looked for before?"*
13. If something like that existed today, at what point would it have been
    worth paying for — and roughly what would you expect it to cost, given
    what similar things already cost you?
14. Would you be open to a short follow-up if we build something specific to
    test — even a very rough version?

### 5. Closing — Push for the Strongest Available Signal

15. Ask for the smallest real commitment appropriate to what's been said so
    far, in ascending order of evidence strength:
    - Weakest: agreement to receive a follow-up email.
    - Stronger: agreement to a specific follow-up call/date.
    - Strongest (only once an offer exists, not during pure discovery):
      willingness to pay a specific price for a specific deliverable, or an
      actual deposit/payment.
    Never round a "sounds interesting" up to more than it is (see
    `sales/README.md`, Interest vs. Intent vs. Payment).

## Logging Requirement

Every real conversation gets logged verbatim (or a faithful summary) in
`customers/outreach-plan-and-log.md`, tagged with: segment, hypothesis
relevance (A/B/C/D), spend figures mentioned, tools/competitors named, the
strongest evidence tier reached (Interest / Intent / Payment), and any direct
quotes worth passing to Marketing. No conversation is invented or
"reconstructed" if it didn't happen — per `PRINCIPLES.md` #13.

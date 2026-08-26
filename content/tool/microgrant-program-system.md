---
title: "Microgrant Program System"
slug: "microgrant-program-system"
kind: "tool"
studio: "microgrants"
license: "RCL-1.0"
tags: ["commons/tool", "studio/microgrants", "microgrants", "neighbor-gatherings", "funding", "payments", "program-in-a-box", "end-to-end", "remix-ready"]
topics: ["microgrants", "neighbor-gatherings", "funding", "payments", "program-in-a-box", "end-to-end", "remix-ready"]
author: "With Neighbors"
source_url: "https://withneighbors.org"
web: "https://relationalbuilder.org/commons/e/microgrant-program-system"
created: "2026-08-26"
updated: "2026-08-26"
rtp_id: "b5096be7-98b4-4f93-816e-153a5b7792d9"
---
# Microgrant Program System

> The end-to-end system for running a neighborhood gathering microgrant program: a public application site, a review pipeline with plain-language stage hints, templated applicant emails with reminder drips, payouts by PayPal/Venmo, gift card, or check behind a human review gate, host reflections, and program analytics. Described feature-by-feature so any neighborhood can remix it — no codebase required. Proven across five generations of With Neighbors programs.

![](https://relationalbuilder.org/media/commons/microgrant-program-landing.jpg)

![](https://relationalbuilder.org/media/commons/microgrant-program-apply.jpg)

![](https://relationalbuilder.org/media/commons/microgrant-program-apply-vt.jpg)

The complete, remixable system for running a neighborhood microgrant program — the kind that gives neighbors $50–$200 to host a gathering on their block, porch, or driveway. It manages the whole round end to end: the public application site, the review pipeline, every email to applicants, the payouts, the reflections that come back, and what you learn from them.

This entry describes the system feature by feature so you can remix it with Relational Builder or any AI builder — **no codebase required, and none is included**. The description *is* the remixable unit: hand it to your builder, answer the localization questions at the end, and grow your program's own version.

It is the software half of a proven pair. The practice half — deciding your grant's shape, promoting it, supporting hosts — is the [Microgrant Organizer Toolkit](/commons/e/microgrant-organizer-toolkit) ([withneighbors.org/toolkit](https://withneighbors.org/toolkit)). This system has run real programs across five generations of With Neighbors builds, most recently Pizza Strip Fund (Rhode Island) and Long-Handled Spoons Dinners (NOFA Vermont) — same machinery underneath, completely different local identity on top.

## What it does, end to end

**Apply → Review → Fund → Reflect → Learn.** Neighbors apply on a public site; organizers review in a pipeline; approved hosts get paid by PayPal, Venmo, gift card, or a check in the mail; hosts send back photos and stories; the program learns what changed.

## The public site (what neighbors see)

- **A landing page that tells the program's story** — who's behind it, what the money is for, how to apply, and a look at past gatherings. The best ones commit to a local identity: Pizza Strip Fund's headline rotates through place-words ("driveway / porch / cul de sac") and its apply button is a hand-drawn pizza strip, the region's party food.
- **Grant tiers named by what they buy**, not just amounts — "$50 coffee & donuts / $100 pizza party / $150 the whole block" — so applicants think in gatherings, not budgets.
- **A multilingual application form** in plain language (Pizza Strip Fund runs English, Spanish, and Portuguese for Rhode Island). Questions cover the gathering idea, where it happens, a date window, the amount tier, and how to reach the host. Optional demographics stay optional.
- **Quiet anti-spam** — a hidden honeypot field plus a minimum-seconds-to-submit check, so no CAPTCHA stands between a neighbor and applying.
- **A confirmation screen and email** that say what happens next and when to expect an answer.
- **A reflection page for funded hosts** — photos (uploaded privately, shared only with permission), a story or quote, attendee count, and each program's own question. This is where your theory of change lives: Pizza Strip Fund asks for a story and a photo; Long-Handled Spoons asks which local organic farms the grant dollars reached.

## The program desk (what organizers see)

### Review pipeline
- A kanban-style board that moves each application through named stages: received → in review → approved (or declined, with a reason) → funded → gathering happened → reflection received → closed.
- **Plain-language hints before every stage change**, so the system never surprises you: "No email is sent now — the funding email goes out later, when you export."
- Admin notes on every application; decline reasons recorded; search and filter across the round.
- **Advisory duplicate flags** — an applicant email or address that already received funding gets flagged for a human to consider, never silently blocked. Judgment stays with people.

### Email center
- **Every message to applicants comes from an editable template** stored with the program — application received, approved with next steps, funding sent, reflection request — plus gentle reminder drips for hosts who haven't sent reflections yet.
- A translation aid for bilingual admin work, so replies can go out in the applicant's language.
- **Every send is logged.** You can always answer "what did we tell this host, and when?"
- Sends through a standard transactional email service (e.g. Resend) with your program's own address.
- **One program on/off switch** that pauses applications and sends together when the round closes or life happens.

### Funding & payouts
- **A human review gate: nothing pays out un-reviewed.** The payout list is built only from approved applications.
- **Batch export to a spreadsheet** for whatever rail you use — plus direct rails: **PayPal Payouts** (including Venmo wallets), **gift cards** (e.g. Tremendous), or **checks in the mail** (Long-Handled Spoons' default — never make a payment method the barrier).
- **Bring-your-own payment account.** The program connects its organizer's own PayPal business account (Payouts enabled); credentials live server-side only, and every grant remembers which account paid it.
- **Duplicate-payment flags** before money moves — a recipient who was already paid this round gets surfaced, not auto-blocked.
- **Honest payment status, verbatim.** The desk shows PayPal's own status word for each payout — including UNCLAIMED — with copy-paste scripts for what to tell each recipient. This design came from a real incident where hosts were marked "paid" who hadn't received money; the lesson is now built in.
- **A nightly reconciliation sweep** re-checks every pending payout and keeps a full audit trail, so the status you see is the status that's true.

### Learning & analytics
- Applications by neighborhood and language; approval rate; gathering sizes; spend by tier.
- **Connection shift** — hosts answer "how many neighbors do you know?" before and after, so the program can see relationships change, not just money move.
- Program-specific measures ride along (Long-Handled Spoons tracks the list of farms the money reached).

## How data works, in plain words

One database holds applications, gatherings, payouts, the email log, and program settings. The public site can only submit applications; everything else is organizer-only, behind sign-in. Payment credentials and email keys live server-side only — never in the public page. Photos and stories are shared publicly only when the host says yes.

## What you change when you remix (and what you keep)

Keep the machine; change the soul:

- **Name, story, and visual identity** — find your neighborhood's pizza strip: the local object that becomes the program's face.
- **Tiers with meaning** — amounts and what they buy, in your place's terms.
- **Geography** — neighborhoods, blocks, or counties (Vermont uses counties).
- **Languages** — whatever your neighbors actually speak.
- **Reflection questions** — this is your theory of change; write your own.
- **Payout method** — PayPal/Venmo, gift cards, or checks, whatever your hosts can actually receive.
- **Email voice and program window** — dates, deadlines, and how the program talks.

## Launch checklist

1. Funding source confirmed (your own microgrant budget, a fiscal sponsor, or matched funding — see the [organizer toolkit](https://withneighbors.org/toolkit)).
2. Payment rail ready: a PayPal business account with Payouts enabled, a gift-card provider, or a checkbook.
3. Program window and tiers set; application questions localized and translated.
4. A review crew (even two people) and an agreed decline message.
5. A test run: submit a test application, approve it, and walk it all the way to a (canceled) payout before neighbors ever see the site.

## See it running

- **Pizza Strip Fund** (Rhode Island) — [pizza-strips.lovable.app](https://pizza-strips.lovable.app) — trilingual, hand-drawn, $50–$150 driveway parties.
- **Long-Handled Spoons Dinners** (NOFA-VT) — [long-handled-spoons.lovable.app](https://long-handled-spoons.lovable.app) — $200 dinners sourcing from local organic farms, checks by mail, the long-spoons parable as identity.

## Lineage

PEPS Parent Meetups → Island Civic Association → Civic Joy Fund → Front Yard Friday · Falls Church Forward → Pizza Strip Fund · Long-Handled Spoons Dinners → *your neighborhood*. Five generations of the same chassis, each remixed for a new place. When you run yours, contribute it back so the next neighborhood starts from you.

## Pairs with

- **[Microgrant Organizer Toolkit](/commons/e/microgrant-organizer-toolkit)** — the nine-stage With Neighbors guide to designing and running the program this system manages.
- **[Microgrant Gathering](/commons/e/microgrant-gathering)** (recipe) — the one-page version of the practice.
- **[The Neighbor Gathering Microgrant](/commons/e/the-neighbor-gathering-microgrant)** (story) — Sam Pressler's Charlottesville pilot: 70 applications where five were expected.

## Details

- **maker:** With Neighbors
- **image url:** https://relationalbuilder.org/media/commons/microgrant-program-landing.jpg
- **hosted url:** https://pizza-strips.lovable.app
- **remix idea:** Find your neighborhood's pizza strip — the local object that becomes the program's face — then keep the machine and change the soul.
- **payout rails:** paypal, venmo, gift-card, check
- **live examples:** [object Object], [object Object]
- **related slugs:** microgrant-organizer-toolkit, microgrant-gathering, the-neighbor-gathering-microgrant
- **languages shipped:** en, es, pt

---

*Contributed by With Neighbors. [Source](https://withneighbors.org) Licensed [RCL-1.0](https://relationalbuilder.org/commons/license). [On the web](https://relationalbuilder.org/commons/e/microgrant-program-system).*

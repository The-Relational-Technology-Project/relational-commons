---
title: "Pizza Strip Fund — remix a gathering fund"
slug: "pizza-strip-fund"
kind: "prompt"
studio: "microgrants"
license: "RCL-1.0"
tags: ["commons/prompt", "studio/microgrants", "microgrants", "gathering-fund", "with-neighbors", "remix", "neighboring", "payments", "email"]
topics: ["microgrants", "gathering fund", "with neighbors", "remix", "neighboring", "payments", "email"]
author: "With Neighbors"
neighborhood: "Rhode Island"
attribution_source: "Pizza Strip Fund (Rhode Island)"
web: "https://relationalbuilder.org/commons/e/pizza-strip-fund"
created: "2026-10-02"
updated: "2026-10-02"
rtp_id: "c0c757e0-fa3f-4cb7-b7b7-0ac9399a0ea9"
---
# Pizza Strip Fund — remix a gathering fund

> The most current With Neighbors microgrant build, Rhode Island's Pizza Strip Fund ($50–$150 for neighbors who gather in a driveway or on a porch), described screen by screen as a remix prompt. Plan this and Relational Builder walks you through four short stages — story and scope, money and questions, look, payments and email — with suggested answers at every step, so your program ends up named for your neighborhood's own pizza strip.

![](https://relationalbuilder.org/media/commons/microgrant-program-landing.jpg)

![](https://relationalbuilder.org/media/commons/microgrant-program-apply.jpg)

**Pizza Strip Fund** gives Rhode Islanders $50–$150 to gather their neighbors in a driveway, on a porch, around a firepit — and names itself after the state's party food instead of calling itself a grant. It is the most current With Neighbors program build, and the base other programs remix from. This card is the remix: the story, the screens, the whole system described part by part, and the prompt to start your own.

Press **Plan this** and Relational Builder walks you through four short stages — the story and scope, how the money and questions work, how it looks, and how hosts get paid and emailed — with a suggested answer at every step. Accept all of them and you have a working program; change any of them and it becomes yours.

## The story it tells

"You've got the *driveway*. We'll cover the pizza strips." One screen: a hand-drawn logo, a headline whose place-word rotates (driveway / porch / yard / cul de sac / corner), two short paragraphs about car-dependent suburbs where it's easy to go days only waving, and a wobbly red-and-tan apply button shaped like a pizza strip. The footer answers the five real questions in place: Why pizza strips? · Who are we? · What counts as "the suburbs"? · What gatherings qualify? · When and how do I get the money?

The lesson With Neighbors kept relearning: "grant", "fund", "program", "eligibility" make neighbors scroll past. Find your own pizza strip — the local object or tradition that becomes the invitation's face — and write every public word the way one neighbor texts another.

## What neighbors see

- **Apply** (`/apply`): a stepped form in English, Spanish, and Portuguese. Full name · email ("the one on your Venmo or PayPal") · phone · neighborhood · gathering date (must land inside the program window) · where it happens · a sentence or two about it · amount tier with hints ($50 coffee & donuts · $100 pizza party · $150 the whole block) · Venmo or PayPal · an "if funded, do you agree?" checklist (paid by Venmo/PayPal · gathering by the deadline · open to neighbors or focused on new people meeting · you'll send a short reflection and a photo, quote, or story) · optional "want help knocking on doors?" · optional demographics, collapsed. A hidden honeypot and a minimum-seconds check keep bots out with no CAPTCHA.
- **Thank-you pages** say what happens next and when to expect an answer.
- **Reflect** (`/reflect/:id`, linked from the funded email): how many neighbors came · the highlight · challenges · commitments or next steps that emerged · how connected you feel to your neighbors now · would you host again · how you heard about it · a quote or story, or photos (uploaded privately, shared only with a separate yes) · did people meet for the first time.

## What organizers see — the desk is standardized, every program the same

- **Pipeline** (`/admin`): kanban and grouped list over `pending → approved → funded → awaiting reflection → completed`, plus `denied` (reopenable). Every move says in plain words whether it emails anyone. Filters by status, payment method, language, gathering date, and text. Each application opens to its answers, admin notes, denial reason, email log, reflection and photos, and a Pay now button.
- **Funding**: select approved rows → *Export & mark Funded* downloads a CSV named for the program and moves them along (for paying by hand or bulk upload) — or Pay now sends through PayPal Payouts to Venmo or PayPal by email, logged.
- **Emails** (`/admin/emails`): five editable templates with `{{first_name}}` / `{{amount}}` / `{{reflect_url}}` chips — received · approved · payment on its way · how was your gathering? · update on your application — a reflection-reminder drip (start offset and interval in days), a manual send, and a master log. Sent through Resend from the program's own address.
- **Analytics**: applications over time, status mix, payment-method mix, "would gather again", recent reflections, and four tiles: applied · funded · neighbors gathered · dollars out.
- **Integrations**: PayPal keys (sandbox or live), Resend key, an applications-open switch with an interest list for when it's closed, and an email allowlist of who can sign in.

## Under the hood

Vite + React + TypeScript, shadcn/ui, Supabase (Postgres, auth, storage, edge functions). Tables: `applications`, `reflections`, `reflection_photos`, `email_templates`, `email_logs`, `sequence_settings`, `payout_logs`, `payment_provider_settings`, `program_settings`, `interest_signups`, admin allowlist. Edge functions: submit-application, submit-reflection, send-email, send-payout, send-reflection-reminders, export-approved, claim-admin-role. Look: cream `hsl(39 59% 95%)`, navy `hsl(217 35% 18%)`, tomato `hsl(8 62% 47%)`, a display serif for headlines and DM Sans for body.

## What changes when you remix (and what stays)

Changes: the name and the object · who it's for and where · grant shape (one amount, host-picked tiers, or an organizer-set range) · the window and whether it's rolling · eligibility and how you choose · which application and reflection questions are on (keep the With Neighbors community-of-practice questions so programs can learn from each other: where, a description, first time hosting; neighbors who came, highlight, challenges, next steps, host again, a photo or story) · how hosts get paid (by hand, PayPal Payouts, gift cards or checks, or a CSV) · how emails go out (by hand from the desk, Resend from your domain, or sent for you by RTP) · the organizer allowlist and contact email · colors, fonts, illustration · languages.

Stays: the desk layout, the status flow, the five emails, anti-spam, the reflection loop.

**Smaller is fine.** Under about ten gatherings, or if you'd rather not learn a desk, build only the invitation and let applications land in a Google Sheet — choose, pay, and email from there.

## The codebase

Pizza Strip Fund's source is held at the Relational Tech Project while past participants are asked for consent to publish it. Once consented, it will be hosted and licensed as a public good and linked from here. Until then this description is the remixable unit — it is what Relational Builder reads when you press Plan this.

## Lineage

Built by With Neighbors (Rich Speeney, Tyler Heath) with Rhode Island organizers, on four years of programs: Pizza Club, Donuts in the Driveway, Friendsgiving, Long-Handled Spoons Dinners. The same machinery also ran Long-Handled Spoons Dinners (NOFA-VT) with a completely different local identity on top. The practice half is the [Microgrant Organizer Toolkit](/commons/e/microgrant-organizer-toolkit).

## Details

- **maker:** With Neighbors
- **image url:** https://relationalbuilder.org/media/commons/microgrant-program-landing.jpg
- **hosted url:** https://pizza-strips.lovable.app
- **remix idea:** Find your neighborhood's pizza strip.
- **plan stages:** story and scope, money and questions, look, payments and email
- **grant shapes:** fixed, host-picked tiers, organizer-set range
- **email options:** by hand from the desk, Resend from your domain, sent for you by RTP
- **live examples:** [object Object], [object Object]
- **related slugs:** microgrant-organizer-toolkit, microgrant-gathering, the-neighbor-gathering-microgrant
- **payout options:** by hand (Venmo/PayPal/Zelle), PayPal Payouts API, gift card or check, CSV export
- **codebase status:** held at RTP pending participant consent

---

*Contributed by With Neighbors — Rhode Island — Pizza Strip Fund (Rhode Island). Licensed [RCL-1.0](https://relationalbuilder.org/commons/license). [On the web](https://relationalbuilder.org/commons/e/pizza-strip-fund).*

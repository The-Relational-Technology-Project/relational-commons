---
title: "Community Income Sharing"
slug: "community-income-sharing"
kind: "prompt"
studio: "rt-studio"
license: "RCL-1.0"
tags: ["commons/prompt", "studio/rt-studio", "Mutual-Aid--Resource-Sharing"]
topics: ["Mutual Aid & Resource Sharing"]
attribution_source: "Relational Tech Studio library"
parent: "../tool/community-income-sharing.md"
web: "https://relationalbuilder.org/commons/e/community-income-sharing"
created: "2026-06-11"
updated: "2026-08-18"
rtp_id: "180eb412-4b86-4650-939d-1b4078deee8d"
---
# Community Income Sharing

Build a community income sharing app modeled on the Community Guaranteed Income Club, started in Baltimore in spring 2025 — concept by Alex Zhu, platform co-created by Alex Zhu, Tyler Heath, Deborah Tien, and Josh Nesbit, and stewarded by the Relational Tech Project. It's the home base for a small club of neighbors (a few dozen to ~150 people) who each contribute a percentage of their monthly income and redistribute it equally — directly, person to person. There's no pooled fund, no middleman, no means testing, and no money moving through the app itself: it does the math, makes the introductions, and keeps the record. It should feel warm, human, and trustworthy — closer to a neighborhood potluck than a fintech product. Money is the glue, not the point.

Core Features

A Welcoming Front Door
- A public landing page that explains the model in plain words: every member contributes a set percentage of post-tax income (Baltimore's pilot used 7%); on the 1st of each month a steward runs the calculation; payments travel neighbor to neighbor by Venmo or Zelle.
- An interactive calculator — "What would your month look like?" — where a visitor enters their income and sees whether they'd send or receive, and roughly how much.
- Honest numbers from the club's track record. Baltimore's pilot: 50+ members, $23k+ moved, monthly gatherings, 100% payment completion.
- Honor the lineage: income-sharing circles exist across many cultures — susu, tanda, hui, kye, tanomoshi — "we're carrying it forward."

Joining
- Simple signup (email sign-in link or password) with a short profile: name, neighborhood, what you do, a bio, a favorite "third space" (café, park, corner), payment handles, and monthly income — asked for gently, with a clear note about who can see it.
- New members wait to be welcomed in by a steward, who gets an email whenever someone applies.

The Monthly Cycle (the heart of the app)
- On the 1st, the steward presses one button. The app calculates each member's contribution, adds it all up on paper, divides it equally, and pairs senders with receivers so every dollar travels directly between two people.
- Each sender's home screen shows "Your connection this month": one neighbor's name and photo, the amount, their favorite third space, and a box for a short note — "a small victory, a question about their favorite spot, anything human." A "Send via Venmo" button opens Venmo pre-filled; then one tap: "I've sent this." ✓
- Receivers see care, not a transaction: "[Name] showed up for you with $200. Maybe say thanks at the next gathering."

Beyond the Money
- A roster of members with photos, bios, and favorite spots — the club should feel like people, not rows in a table.
- Gatherings: anyone can post a potluck, skill share, or Sunday coffee. "RSVP so the host knows to make enough food."
- An offers & needs board with three kinds of post: offer ("spare crib, free"), need ("looking for a dentist"), lead ("freelance gig open").
- A membership card with a referral code: "share it with neighbors you'd vouch for."

Steward Tools
- A plain dashboard: welcome new members, see the monthly math laid out transparently (who sends, who receives, who breaks even), run the calculation with a confirmation step, watch payment confirmations come in, and edit the site's FAQs and welcome emails.

Trust & Privacy
- Income is visible only to the member and the steward — never on the roster.
- The app never touches the money; it arranges and records direct payments between neighbors.
- Accountability is relational, not contractual: confirmations in the app, names and faces everywhere, gatherings every month.

UI / UX Guidelines
- Style: warm and bold — cream background, a sunny yellow hero, green for receiving, orange for sending and for needs; rounded corners, friendly cards, real faces.
- Typography: a confident geometric display font for headings (e.g., Space Grotesk), a clean readable sans for body.
- Tone: intimate and plain. "Hey, [first name]." "Not a charity. Not an app. A circle of neighbors who quietly carry each other through." A touchstone quote: "All flourishing is mutual." (Robin Wall Kimmerer)
- Interaction language: "Join the Club," not "Sign up." "I've sent this," not "Confirm transaction."
- Mobile-first with bottom-tab navigation: a member should finish their monthly send from their phone in under a minute.

Example User Stories
- A curious neighbor plays with the calculator, learns she'd send about $90 a month, reads how it works, and applies.
- On the 3rd, a member sees he's sending $140 to Marcus, writes "heard you love Café Neon — coffee soon?", taps through to Venmo, and confirms with one tap.
- A member between jobs receives $210 with a kind note and thanks the sender in person at the potluck listed on the events page.
- The steward runs the monthly math in five minutes and watches confirmations roll in over the week.
- Someone posts "need a bike for my commute" on the board; a neighbor has a spare.

## Related in the commons

- Grew from [Community Income Sharing](../tool/community-income-sharing.md)
- Mentions: [GitHub](../tool/github.md)

---

*Contributed by Relational Tech Studio library. Licensed [RCL-1.0](https://relationalbuilder.org/commons/license). [On the web](https://relationalbuilder.org/commons/e/community-income-sharing).*

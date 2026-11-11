---
title: "Build: A Host Map for a Day of Gatherings"
slug: "build-host-map-day-of-gatherings"
kind: "prompt"
studio: "local-civic-tech"
license: "MIT"
tags: ["commons/prompt", "studio/local-civic-tech", "local-civic-tech", "civic-tech-prompt", "starter", "microgrants", "gatherings", "block-parties", "mapping"]
topics: ["local-civic-tech", "civic-tech-prompt", "starter", "microgrants", "gatherings", "block-parties", "mapping"]
author: "Sunset Social Club"
neighborhood: "The Sunset, San Francisco"
attribution_source: "The Sunset Wave, thesunsetwave.org"
source_repo: "The-Relational-Technology-Project/sunset-wave-host-map"
source_url: "https://github.com/The-Relational-Technology-Project/sunset-wave-host-map"
web: "https://relationalbuilder.org/commons/e/build-host-map-day-of-gatherings"
created: "2026-11-10"
updated: "2026-11-10"
rtp_id: "85e9e499-0f29-4285-9bc4-679a54e73397"
---
# Build: A Host Map for a Day of Gatherings

> A starter build: one day when neighbors host gatherings on their own blocks, and a map that shows which blocks have a host and which are waiting. Plan mode asks about your place's edges, the day, your stewards, your languages and what hosts get before anything is built.

![](https://relationalbuilder.org/media/commons/sunset-wave-map.jpg)

The Sunset Wave (thesunsetwave.org) is a day when neighbors across San Francisco's Sunset District host gatherings on their own blocks, all at once. Its map shows every block: an open dot waits for a host, a waving hand means a neighbor has said yes. I want a day like that for my place, with a map like that.

Before you plan anything, ask me these, a few at a time, and wait for my answers:

1. **The place and its edges.** Which streets are in, where does it stop, and what is one "spot" on the map: a block, a stretch of road, a building, a cul-de-sac? Roughly how many spots is that?
2. **The day.** The date, the hours you suggest, why this day, and what happens if the weather turns.
3. **Who is behind it.** The group neighbors will recognize, and the two or three stewards who will read notes and place tricky locations. Where should a host's reply go?
4. **Languages.** Which languages do my neighbors read? The page should be whole in each one.
5. **What hosts get.** A party for hosts beforehand, a group thread, planning help, flyers, supplies on the day? Is there any money, and where does it come from?
6. **The name and the mark.** What is the day called, and what small symbol marks a claimed spot? (The Sunset's is a waving hand.)
7. **After the day.** What do you hope the hosts go on to do together?

If I do not have a list of streets yet, offer to start with a small hand-written list of spots so I can see it work first.

Then build this, and keep these rules:

- **One page with the map in the middle.** The name and the date, a short invitation in a neighbor's words, the map, a few tiny examples of what hosting can look like (coffee and donuts, a potluck out front, cards in the garage), what hosts get, and the questions people really ask (What do I have to do? Do I need a permit? Someone is already hosting on my block, now what? What if it rains? Who is behind this?).
- **Two kinds of spots.** Open, and claimed. Tapping an open spot offers to host there. Tapping a claimed one offers to send the host a note. More than one host on a spot is fine.
- **Offering to host takes under a minute.** Name, email or phone, and the stretch, filled in from the spot they tapped and editable. Optional: co-hosts, "the place where I'll host is sheltered from rain", and one checkbox, "my block could use some funds to help cover expenses". No application, no essay. Do not call it a grant on anything a neighbor sees.
- **A way in for places that are not on the map.** A courtyard, a corner, a street just outside the edges: they describe it in their own words, it is saved, and a steward places it. Say so on the form.
- **A note to a host goes through a steward.** The neighbor writes a short note and leaves their email or phone. A steward reads it, then forwards the note and the neighbor's contact to that spot's host, who gets in touch directly. Tell the neighbor this before they send.
- **Privacy is the design.** Host names and contact details never appear on the public page. The public page can only learn which spots are claimed, never who claimed them. Visitors can add an offer or a note but cannot read any.
- **One count, shown late.** Show how many neighbors have raised a hand, and only once the number is encouraging (the Sunset waited for 20). No counts in the map legend.
- **A steward desk behind a sign-in.** Host signups with an export, notes waiting for review with a forward button, locations waiting to be placed, and the questions section editable in each language. Every action on the desk checks the sign-in again.
- **A thank-you that asks for one more.** After someone offers to host: "You're on the map!", what happens next, and an invitation to share the page with a neighbor who might host the next block.
- **Every word in one place per language**, so no language is left half done.
- **Spot ids never change** once people have claimed them, so the map can grow without losing anyone.

Names and phone numbers need a real backend with private tables. Before the form takes real signups, tell me plainly what has to be connected and what is not safe yet, and never pretend to save.

Also write a short page for the stewards in plain language: how to review a note, how to place a location, what to say when two neighbors want the same spot, and how hosts meet each other before the day. The map fills because hosts invite hosts, so the practice matters as much as the page.

Credit the lineage in one line: remixed from The Sunset Wave by the Sunset Social Club, through Relational Builder.

## Details

- **location:** {"lat":37.7535418,"lng":-122.4952495,"basis":"attribution","label":"Sunset District, San Francisco, California","precision":"neighborhood"}
- **builds on:** the-sunset-wave
- **image url:** https://relationalbuilder.org/media/commons/sunset-wave-map.jpg
- **guardrails:** host names and contact details never show on the map, a steward reads every note before a host sees it, money is one checkbox, never an application, the count shows only once it is encouraging
- **hosted url:** https://thesunsetwave.org
- **practice kind:** prompt

---

*Contributed by Sunset Social Club — The Sunset, San Francisco — The Sunset Wave, thesunsetwave.org. [Source](https://github.com/The-Relational-Technology-Project/sunset-wave-host-map) Licensed MIT. [On the web](https://relationalbuilder.org/commons/e/build-host-map-day-of-gatherings).*

---
title: "Build: A Knowy for Your Place"
slug: "build-knowy-for-your-place"
kind: "prompt"
studio: "local-civic-tech"
license: "MIT"
tags: ["commons/prompt", "studio/local-civic-tech", "local-civic-tech", "civic-tech-prompt", "starter", "neighborhood-agent", "stewardship", "place-based-ai"]
topics: ["local-civic-tech", "civic-tech-prompt", "starter", "neighborhood-agent", "stewardship", "place-based-ai"]
author: "Relational Technology Project with Outer Sunset neighbors"
neighborhood: "Outer Sunset, San Francisco"
attribution_source: "Knowy Plover, knowy.org"
source_repo: "The-Relational-Technology-Project/neighborhood-agent"
source_url: "https://github.com/The-Relational-Technology-Project/neighborhood-agent"
web: "https://relationalbuilder.org/commons/e/build-knowy-for-your-place"
created: "2026-11-09"
updated: "2026-11-09"
rtp_id: "cae58819-6722-4cd6-b74f-092d7e43064d"
---
# Build: A Knowy for Your Place

> A starter build: an AI agent that belongs to your place, at any scale from a house to a neighborhood. Plan mode asks about your place's edges, stewards, sources, more-than-human neighbors and voice before anything is built.

![](https://relationalbuilder.org/media/commons/knowy-home.jpg)

A Knowy is an AI agent that acts on behalf of a place, not a person. The first one is Knowy Plover, for the Outer Sunset in San Francisco (knowy.org). I want one for my place. It could be a house, a block, a co-op, a co-living community or a neighborhood.

Before you plan anything, ask me these, a few at a time, and wait for my answers:

1. **The place and its edges.** What is this place, where does it start and stop, and how many people does it hold?
2. **The first stewards.** Which two or three people will look after it, and how do they decide together? Only name people who have said yes.
3. **What it may read.** Which sources can it draw on: notes we write ourselves, a shared calendar, public feeds, other sites? At the scale of a house the answer may be only what we write down.
4. **More-than-human neighbors.** Who else lives here (a creek, a garden, street trees, birds, a dog), and which people speak up for them?
5. **Its name and voice.** What is it called and how should it sound?
6. **Who can see it.** Public like a neighborhood page, or only for the people who live here? For a household, assume private until I say otherwise.

If I am not ready with real answers, offer to start with a fictional place so I can see it work first.

Then build this, and keep these rules:

- **The place's memory is plain files** a steward can read and edit without code, in the shape the original uses: `place.md` (what the place is, its name and voice), `STEWARDS.md` (who the stewards are, how they decide, their review checklist), `sources.yml` (everything it may read), `people.yml` (people it may point to, each with the date they said yes), `constituents/` (one file per more-than-human neighbor and its advocates), plus `events/`, `corrections/` and `proposals/`. Write first drafts from my answers and mark anything you guessed.
- **A page anyone in the place can ask.** It answers only from those files and the listed sources. Every factual claim shows its source and date. When the notes do not cover it, it says "I don't know" in those words and points to a person or a source. A correction beats anything fetched. Unknown hours stay unknown.
- **Good friction on changes.** When someone asks to add or change something, it drafts the exact file, shows it to them, and only after their yes sends it to the stewards to review. It never changes its own memory, and it never says a change is done before a steward has accepted it.
- **Nothing kept about people.** No accounts for asking, no memory of conversations. It declines questions about private individuals and offers the public way to reach someone instead. Nobody is listed without their yes.
- **More-than-human neighbors have standing.** It brings their interests into answers when a plan touches them and names their advocates. It never speaks as them.
- **Plain pages beside the chat:** what this is and who stewards it, what it reads, open proposals, and how to correct it.
- **AI runs only when a person asks something.** Never on page load or in loops.

Also write `STEWARDING.md` in plain language for the stewards: how to review a draft, how to ask for consent before listing someone, how to correct the agent, and what it never does.

Say plainly what this version does not do yet compared with the original (live tool use, pull requests opened by the agent, adapters for outside sources), so I can decide later whether to run the full agent on the same notes.

## Details

- **location:** {"lat":37.7541496,"lng":-122.5061507,"basis":"attribution","label":"Sunset District, San Francisco, California","precision":"neighborhood"}
- **builds on:** knowy
- **image url:** https://relationalbuilder.org/media/commons/knowy-home.jpg
- **guardrails:** it drafts, a neighbor says yes, a steward decides, nobody is listed without their yes, it says "I don't know" in those words, it never speaks as its more-than-human neighbors
- **hosted url:** https://knowy.org
- **practice kind:** prompt

---

*Contributed by Relational Technology Project with Outer Sunset neighbors — Outer Sunset, San Francisco — Knowy Plover, knowy.org. [Source](https://github.com/The-Relational-Technology-Project/neighborhood-agent) Licensed MIT. [On the web](https://relationalbuilder.org/commons/e/build-knowy-for-your-place).*

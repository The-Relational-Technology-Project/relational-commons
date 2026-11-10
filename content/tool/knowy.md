---
title: "Knowy: An AI Agent for a Place"
slug: "knowy"
kind: "tool"
studio: "local-civic-tech"
license: "MIT"
tags: ["commons/tool", "studio/local-civic-tech", "local-civic-tech", "civic-tech-tool", "neighborhood-agent", "stewardship", "place-based-ai", "open-source"]
topics: ["local-civic-tech", "civic-tech-tool", "neighborhood-agent", "stewardship", "place-based-ai", "open-source"]
author: "Relational Technology Project with Outer Sunset neighbors"
neighborhood: "Outer Sunset, San Francisco"
attribution_source: "knowy.org"
source_repo: "The-Relational-Technology-Project/neighborhood-agent"
source_url: "https://github.com/The-Relational-Technology-Project/neighborhood-agent"
web: "https://relationalbuilder.org/commons/e/knowy"
created: "2026-11-09"
updated: "2026-11-09"
rtp_id: "0f354411-6e5d-4ee2-bea3-f5cdfacfb145"
---
# Knowy: An AI Agent for a Place

> AI that belongs to a place, not a person. Neighbors ask it anything, it answers from public neighborhood notes with sources, and every change it drafts waits for a steward. First home: the Outer Sunset, San Francisco.

![](https://relationalbuilder.org/media/commons/knowy-home.jpg)

![](https://relationalbuilder.org/media/commons/knowy-mobile.jpg)

![](https://relationalbuilder.org/media/commons/knowy-about.jpg)

![](https://relationalbuilder.org/media/commons/knowy-sources.jpg)

[Knowy Plover](https://knowy.org) is the neighborhood agent for the Outer Sunset in San Francisco: AI for a place, stewarded by neighbors. A personal AI agent gets better the more it knows about you. This one belongs to a neighborhood instead, and everything it knows is public and shared.

Any neighbor can message it on a public page. It answers from the neighborhood's own notes and listed public sources, with the source and the time it was read. It says "I don't know" in those words when it doesn't, and it points to a person more often than it hands over a paragraph. Ask it to change something ("add my event", "that closes at 6 now", "can we start a tool library?") and it does not just do it. It writes the change up, shows the neighbor the exact file, and a steward decides.

**The rules it is built around**

- **The place is its stewards.** A small group of neighbors governs the agent through plain files: its voice (`place.md`), who the stewards are and how they review (`STEWARDS.md`), what it may read (`sources.yml`), who it may point to (`people.yml`), and its corrections.
- **Public data only, and nothing kept.** It reads the listed sources and nothing else. No accounts, no memory of conversations.
- **Good friction.** It never writes to the neighborhood directly. It drafts, the neighbor says yes, a steward merges.
- **Humility is structural.** Every factual claim carries its source and when it was fetched. A steward's correction beats fetched data. Unknown hours are unknown.
- **More-than-human neighbors have standing.** The ocean, the dunes, the plovers, the coyotes: it reports their vital signs, brings their interests into answers when a plan touches them, and names their human advocates. It never speaks as them.

**The practice is part of the tool.** The code is the small half. What makes a Knowy trustworthy is the stewarding: a few named neighbors, a review checklist, a yes from every person it lists, and a question log the stewards read together.

**One shape, many scales.** The same shape serves a house, a block, a co-op, a co-living community or a neighborhood. Smaller places change three things: fewer public sources (the memory is mostly what the household writes down), more consent questions (everyone it knows about lives there), and a private home for the notes may be right.

**Two ways to make your own**

1. *In Relational Builder.* Start from the prompt "Build: A Knowy for Your Place" on this shelf. Plan mode asks what a new place has to answer (its edges, its first stewards, its sources, its more-than-human neighbors, its name and voice) and builds a lighter Knowy: the place's notes as plain files, a page neighbors can ask, drafts that wait for a steward.
2. *The full agent.* The original code is open (MIT) and takes a place's notes as config, so another place can run the same code on its own data. It adds live tool use, pull requests opened through a GitHub App, per-source adapters (calendars, open data, other sites), and a place pack other tools can read. A fictional place in the repo (`fixtures/elsewhere/`) shows a complete set of notes. The notes you write in Relational Builder follow the same shape, so they carry over.

Code: MIT. The Outer Sunset's notes: CC BY 4.0, at github.com/The-Relational-Technology-Project/outer-sunset.

**See it running**

Try the original at [knowy.org](https://knowy.org): ask it how the ocean is today, or what is happening this weekend.

![Knowy Plover on a phone: the day's vital signs, then one box to ask the neighborhood](https://relationalbuilder.org/media/commons/knowy-mobile.jpg)

![The About page: what it reads, how it cites, how it checks before it adds, and what it keeps](https://relationalbuilder.org/media/commons/knowy-about.jpg)

![The Sources page: everything it reads, and a form to suggest something new for a steward to review](https://relationalbuilder.org/media/commons/knowy-sources.jpg)

## Details

- **maker:** Relational Technology Project with Outer Sunset neighbors
- **hosted:** self-hostable (Vercel, Fly, any container host); a lighter version builds in Relational Builder
- **license:** MIT (code); CC BY 4.0 (Outer Sunset notes)
- **location:** {"lat":37.7541496,"lng":-122.5061507,"basis":"attribution","label":"Sunset District, San Francisco, California","precision":"neighborhood"}
- **repo url:** https://github.com/The-Relational-Technology-Project/neighborhood-agent
- **image url:** https://relationalbuilder.org/media/commons/knowy-home.jpg
- **hosted url:** https://knowy.org
- **remix idea:** A Knowy for your own place, at any scale from a house to a neighborhood, with your own stewards, sources and more-than-human neighbors.
- **data repo url:** https://github.com/The-Relational-Technology-Project/outer-sunset
- **practice kind:** tool
- **starter prompt:** build-knowy-for-your-place

---

*Contributed by Relational Technology Project with Outer Sunset neighbors — Outer Sunset, San Francisco — knowy.org. [Source](https://github.com/The-Relational-Technology-Project/neighborhood-agent) Licensed MIT. [On the web](https://relationalbuilder.org/commons/e/knowy).*

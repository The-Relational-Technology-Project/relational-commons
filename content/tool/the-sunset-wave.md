---
title: "The Sunset Wave: A Host Map for a Day of Gatherings"
slug: "the-sunset-wave"
kind: "tool"
studio: "local-civic-tech"
license: "MIT"
tags: ["commons/tool", "studio/local-civic-tech", "local-civic-tech", "civic-tech-tool", "microgrants", "gatherings", "block-parties", "mapping", "host-network", "open-source"]
topics: ["local-civic-tech", "civic-tech-tool", "microgrants", "gatherings", "block-parties", "mapping", "host-network", "open-source"]
author: "Sunset Social Club"
neighborhood: "The Sunset, San Francisco"
attribution_source: "thesunsetwave.org"
source_repo: "The-Relational-Technology-Project/sunset-wave-host-map"
source_url: "https://github.com/The-Relational-Technology-Project/sunset-wave-host-map"
web: "https://relationalbuilder.org/commons/e/the-sunset-wave"
created: "2026-11-10"
updated: "2026-11-10"
rtp_id: "4f8eb218-5eac-4129-9e2b-f6e023649b89"
---
# The Sunset Wave: A Host Map for a Day of Gatherings

> 400 neighbor gatherings on one day, across San Francisco's Sunset District. A map shows every block: an open dot waits for a host, a waving hand means a neighbor has said yes. New hosts claim their stretch in under a minute, neighbors send a note to the host on their block, and hosts who need a little money tick one box.

![](https://relationalbuilder.org/media/commons/sunset-wave-map.jpg)

![](https://relationalbuilder.org/media/commons/sunset-wave-home.jpg)

![](https://relationalbuilder.org/media/commons/sunset-wave-host-form.jpg)

![](https://relationalbuilder.org/media/commons/sunset-wave-note.jpg)

![](https://relationalbuilder.org/media/commons/sunset-wave-support.jpg)

[The Sunset Wave](https://thesunsetwave.org) is a day when neighbors across San Francisco's Sunset District host gatherings on their own blocks, all at once: Saturday, March 20, 2027, the spring equinox. The goal is 400 hosts, about one for every block west of 19th Avenue from Lincoln to south of Sloat. A gathering can be coffee and donuts in a driveway, a potluck out front, card games in the garage, tea on the steps, or a kids' bike parade. The host decides.

It is organized by the [Sunset Social Club](https://sunsetsocialclub.org), a free neighborhood club started by two Sunset neighbors, Josh Nesbit and Sandi Lam Harder. The Sunset has spent four years in a fight over the Great Highway. The Wave is a new story to stand next to that one: neighbors who look and believe differently, hanging out on the same sidewalk. As Josh told The San Francisco Standard, "it's easier to create culture than change it." [Read the story](https://sfstandard.com/2026/11/01/the-sunset-wave-is-coming-this-spring/).

**The map is the invitation**

Every block is a dot on a real street map. An open dot is waiting for someone. A waving hand means a neighbor has raised their hand there. People look for their own block first, and what they find decides what they do next:

- **Their block is open.** They tap it and offer to host in under a minute: name, email or phone, and their stretch, already filled in from the dot. They can add co-hosts, say the spot is sheltered from rain, and tick one box if their block could use some funds.
- **Someone is already hosting.** They send the host a note ("I live on this block and could bring chairs"). A steward reads the note first, then passes it and the sender's contact on to the host, who gets in touch directly.
- **Their spot is not a dot.** A courtyard, a parklet, a corner, a street off the grid: they describe the stretch in their own words and a steward places it on the map.

More than one host on a block is welcome.

**What stays private**

Host names and contact details never appear on the map. The public page can only ask which blocks are claimed. A neighbor's note goes to a steward, not straight to the host, and the host's contact is never given out. The one number shown is how many neighbors have raised a hand, and the site waited until that number was encouraging before showing it.

**More than money**

The Wave counts as a microgrant program: sponsors and neighbors fund it, and hosts who say they need a little money get it. But the money is one checkbox on the host form, not an application. What a host really gets is company:

- a party for hosts before the day, to meet each other
- a host network, with experienced block party hosts nearby
- planning help when they ask
- flyers by local artists
- a little money if they need it
- support on the day

**Where it is going**

The day is step one. The idea is that 400 block hosts get to know one another, find out they can host, and then go on to do many neighborhood projects together with their neighbors. In Josh's words: "I want our kids to grow up in a place where they know someone on every block."

**How it is built**

- One page in English, Mandarin, Cantonese and Spanish, with all the words in one dictionary per language so no language falls behind.
- Block dots generated from the city's public street centerlines, drawn with Leaflet on OpenStreetMap tiles. Block ids never change, so a host stays attached to their block as the map grows.
- A steward desk behind a sign-in: host signups and exports, the notes waiting for review, locations that need a person to place them, and the questions page, editable per language.
- A thank-you page and email that ask each new host to share the Wave with a neighbor.
- Built by neighbors with Lovable. The code is open (MIT).

By November 10, 2026, 88 neighbors had raised a hand.

**Make your own**

1. *In Relational Builder.* Start from the prompt "Build: A Host Map for a Day of Gatherings" on this shelf. Plan mode asks about your place and its edges, the day, your stewards, your languages and what hosts get, then builds the map, the host form, the note to a host and the steward desk.
2. *From the code.* Fork [the repo](https://github.com/The-Relational-Technology-Project/sunset-wave-host-map). The Sunset's streets live in one generated file, so another neighborhood swaps in its own.

**See it running**

Find a block at [thesunsetwave.org](https://thesunsetwave.org).

![The front page: the name with its waving hand, the date, and how many neighbors have raised a hand](https://relationalbuilder.org/media/commons/sunset-wave-home.jpg)

![Offering to host: the stretch is filled in from the dot, with a small map to confirm it](https://relationalbuilder.org/media/commons/sunset-wave-host-form.jpg)

![A note to the host of a claimed block: a steward reviews it before passing it on](https://relationalbuilder.org/media/commons/sunset-wave-note.jpg)

![What hosts get, and how businesses and neighbors can support the day](https://relationalbuilder.org/media/commons/sunset-wave-support.jpg)

## Details

- **maker:** Sunset Social Club
- **place:** The Sunset, San Francisco, CA
- **hosted:** built with Lovable (TanStack Start, Leaflet, a Postgres backend); a lighter version builds in Relational Builder
- **license:** MIT
- **location:** {"lat":37.7535418,"lng":-122.4952495,"basis":"attribution","label":"Sunset District, San Francisco, California","precision":"neighborhood"}
- **repo url:** https://github.com/The-Relational-Technology-Project/sunset-wave-host-map
- **image url:** https://relationalbuilder.org/media/commons/sunset-wave-map.jpg
- **story url:** https://sfstandard.com/2026/11/01/the-sunset-wave-is-coming-this-spring/
- **hosted url:** https://thesunsetwave.org
- **remix idea:** A day of gatherings for your own neighborhood, with a map where neighbors claim their block and reach the host next door.
- **grant shape:** one checkbox on the host form, for hosts who say they need it
- **local object:** a waving hand: a wave from the ocean and a hello across the street
- **practice kind:** tool
- **starter prompt:** build-host-map-day-of-gatherings

---

*Contributed by Sunset Social Club — The Sunset, San Francisco — thesunsetwave.org. [Source](https://github.com/The-Relational-Technology-Project/sunset-wave-host-map) Licensed MIT. [On the web](https://relationalbuilder.org/commons/e/the-sunset-wave).*

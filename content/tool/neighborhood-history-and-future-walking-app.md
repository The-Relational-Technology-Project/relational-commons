---
title: "Neighborhood History (and Future) Walking App"
slug: "neighborhood-history-and-future-walking-app"
kind: "tool"
studio: "rt-studio"
license: "RCL-1.0"
tags: ["commons/tool", "studio/rt-studio", "tools-for-crafting"]
topics: ["tools-for-crafting"]
attribution_source: "Relational Tech Studio library"
source_url: "https://outersunset.place/"
web: "https://relationalbuilder.org/commons/e/neighborhood-history-and-future-walking-app"
created: "2026-06-10"
updated: "2026-08-13"
rtp_id: "0d6983b7-b0ef-4705-886b-803e57e64f8d"
---
# Neighborhood History (and Future) Walking App

> A mobile-first neighborhood walking companion that layers local history, present-day life, and community dreams onto a quiet, field-guide-style interface — built by a neighbor for the Outer Sunset, San Francisco.

![](https://studio.relationaltechproject.org/images/gallery/outer_sunset_field_guide.png)

Outer Sunset Field Guide

Build a mobile-first neighborhood walking companion for the Outer Sunset district of San Francisco, centered around 48th Avenue and Irving Street. It should feel like a calm, quiet field notebook — not a flashy app. Think of it as an adult field trip led by a knowledgeable neighbor.

Visual design:

- Maximum width of 430px, centered on larger screens, like a phone screen
- Off-white paper background with warm, muted earth tones — faded terra cotta accents, warm grays, charcoal text
- Two fonts: Lora (serif) for headings and labels, Inter (sans-serif) for body text
- Minimum 16px body text for outdoor sunlight readability
- Subtle, slow animations — gentle slides and fades, nothing flashy
- Overall aesthetic: understated, literary, like a printed field guide

Data model:

Each place in the guide has: a name, street address, latitude/longitude coordinates, a thumbnail image, an optional secondary drawing/illustration with artist credit, a prose description, a photo credit, optional audio (with label and duration), optional external links, and one or more "time layers" — past, present, or future. All place data is stored in a database and fetched on load.

Time layers:

Every place belongs to one or more of three time layers: Past (historical sites, old photos), Present (current businesses and gathering spaces), and Future (community dreams and planned projects). These are shown as three small dots — filled if active, outlined if not — next to each place entry throughout the app.

Navigation:

A fixed bottom tab bar with three tabs: Explore, Tour, and About.

Explore tab (default):

The Explore tab has three sub-views, toggled by text links in the header reading "Nearby · Map · All":

1. Nearby (default): A single large card showing one place at a time. The card has a wide thumbnail image (16:10 ratio), the place name in large serif text, the street address, walking distance and time from the user's current location (e.g. "Walk → 3 min · 0.2 mi"), and the time layer dots. Users swipe left/right or tap Back/Next buttons to move between places. Pagination dots show position. Places are sorted by distance from the user. Adjacent thumbnails are prefetched for instant transitions. If the user is within about 150 meters of a place, the card gets a subtle accent background and says "You're here." Tapping a card opens the detail view.

2. Map: A Leaflet map showing all places as colored pins — brown for past, dark charcoal for present, slate blue for future, gray for mixed. Past-only pins are outlined, future-only are dashed, present/mixed are solid. The map is grayscale-filtered. A legend explains the pin styles. Tapping a pin opens the detail view. The user's location is shown as a small blue dot.

3. All: A compact list of every place sorted by distance, showing a small thumbnail, name, address, walking time, and time layer dots. Tapping opens the detail view.

Place detail view:

Opens as a bottom sheet sliding up over the current view, scrollable, max height 92% of the screen. Contains:

- Full-width hero image (4:3 ratio) with a small expand button for a fullscreen lightbox, plus photo credit
- Optional secondary illustration below the hero, also expandable, with artist credit
- Place name, address, time layer dots, walking distance or "You're here"
- Full prose description
- Optional audio player section with play/pause button, label, and duration
- Optional external links section
- Embedded OpenStreetMap showing the location, with a "Get directions" button that opens Apple Maps on iOS or Google Maps on Android

Tour tab:

A list of four predefined walking tours: Past, Present, Future, and "Very local" (nearest 6 places). Each shows a name, description, and estimated walking time. Tapping a tour filters the Explore Nearby cards to just those places and labels the active tour in the header with a "Back to explore" link.

About tab:

A scrollable page with:

- "About this guide" section explaining what it is
- "The time layers" section with a visual key showing the three dot patterns and their meanings
- "Community credits" section
- Three collapsible form sections (each with a chevron toggle):
  - "Suggest a site" — time layer selector, details textarea, optional name and email fields
  - "Get in touch" — name, email, message fields
  - "Request a neighborhood tour" — name, email, message fields
  - All forms validate inputs and submit to the database, showing success messages after submission
- A "More neighborhood tools" section styled as a cork bulletin board with pinned cards linking to sibling neighborhood websites
- A bottom disclaimer noting it's an early prototype

Geolocation:

The app requests the user's location on load. It uses the Permissions API to distinguish between "not yet asked," "granted," and "blocked" states. If location is denied, a subtle notice appears. Walking distances and times are calculated using the Haversine formula.

Content:

The guide includes roughly 25-30 places spanning all three time layers — local cafes, surf spots, historical sites, libraries, community art spaces, planned housing projects, neighbor dreams, and historical homes of notable artists.

## Remix this tool

- Live site: https://outersunset.place/
- Fork the code: https://github.com/The-Relational-Technology-Project/sunset-walking-guide
- Studio library page: https://studio.relationaltechproject.org/library?item=062b3b52-a60f-4be7-acb9-6fea4c7e99cf

## Related in the commons

- Mentions: [GitHub](../tool/github.md)
- Mentions: [Outer Sunset Field Guide](../story/outer-sunset-field-guide.md)

## Details

- **github url:** https://github.com/The-Relational-Technology-Project/sunset-walking-guide
- **is joinable:** false
- **tool category:** tools_for_crafting

---

*Contributed by Relational Tech Studio library. [Source](https://outersunset.place/) Licensed [RCL-1.0](https://relationalbuilder.org/commons/license). [On the web](https://relationalbuilder.org/commons/e/neighborhood-history-and-future-walking-app).*

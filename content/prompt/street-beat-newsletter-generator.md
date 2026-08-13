---
title: "Street Beat Newsletter Generator"
slug: "street-beat-newsletter-generator"
kind: "prompt"
studio: "rt-studio"
license: "RCL-1.0"
tags: ["commons/prompt", "studio/rt-studio", "Communication"]
topics: ["Communication"]
attribution_source: "Relational Tech Studio library"
web: "https://relationalbuilder.org/commons/e/street-beat-newsletter-generator"
created: "2026-06-10"
updated: "2026-08-12"
rtp_id: "b2fd07f8-28ed-47d9-9bf4-e51bf3117693"
---
# Street Beat Newsletter Generator

> Contributed by Grant from Inner Richmond, SF. A tool for a neighborhood curator to turn photos of street posters and neighbor observations ('stoop talk') into a curated weekly email newsletter. It prioritizes 'street data' and human curation over algorithmic feeds.

App Title: Street Beat Newsletter Tool

Context:
Build a mobile-first web app for a neighborhood curator (human-in-the-loop). The goal is to walk around a neighborhood, capture information from physical posters AND text notes, and export it all into a single, formatted HTML email newsletter at the end of the week.

Core Features:

1. THE CAPTURE INTERFACE (Home Screen)
Create two distinct 'Input' buttons at the top:
A. 'Scan Poster' (Camera Action)
- Opens camera.
- Captures photo.
- Uses AI Vision (e.g. GPT-4o) to extract Title, Date, Time, Location, Description.
- Saves the cropped image of the poster.

B. 'Stoop Talk' (Text Note Action)
- A simple text field for quick observations (e.g., 'The cherry blossoms on 6th Ave are popping', or 'Street cleaning is canceled tomorrow').
- A 'Category' dropdown (General, Alert, Appreciation, Lost & Found).
- No image required.

2. THE REVIEW DASHBOARD (The Editor)
A list view of all items captured this week.
- Allow me to edit the text for both Posters and Notes.
- Allow me to delete/archive items that are spam or duplicates.
- Allow dragging and dropping to reorder.

3. THE NEWSLETTER GENERATOR (Export)
A button that says 'Copy Email HTML.' It should generate code compatible with standard email clients (Gmail/Substack).

Layout Structure:
- Header: 'This Week in [Neighborhood Name]'
- Section 1: 'Stoop Talk' (The Text Notes)
-- Display these as a clean, bulleted list or small text cards.
-- Use a light background color to separate them from events.
- Section 2: 'On The Board' (The Posters)
-- Display each event with the full-width image of the poster.
-- Below the image, put the Title, Date, and Location in clear, bold text.
- Footer: 'Curated by a human neighbor.'

STYLE GUIDE:
- Aesthetic: High contrast, utilitarian, 'Street smart.'
- Typography: Clean sans-serif (Inter or Roboto).
- Accent Color: Neon Yellow or Safety Orange.

TECHNICAL STACK:
- React / Next.js
- Supabase for database (preserves drafts efficiently).
- OpenAI API (or similar) for the Vision/OCR tasks.
- Tailwind CSS for styling.

## Related in the commons

- Mentioned in: [Neighborhood Newsletter (civic media format)](../reference/format-neighborhood-newsletter.md)
- Mentions: [Supabase](../tool/supabase.md)

---

*Contributed by Relational Tech Studio library. Licensed [RCL-1.0](https://relationalbuilder.org/commons/license). [On the web](https://relationalbuilder.org/commons/e/street-beat-newsletter-generator).*

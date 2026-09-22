---
title: "Build: A Today's News Section for a Neighborhood Site"
slug: "build-todays-news-section"
kind: "prompt"
studio: "civic-media"
tags: ["commons/prompt", "studio/civic-media", "civic-media", "build-prompt", "software", "starter", "local-news", "news-curation", "hierarchy-of-needs", "rss", "ai-curation", "scheduled-function"]
topics: ["civic-media", "build-prompt", "software", "starter", "local-news", "news-curation", "hierarchy-of-needs", "rss", "ai-curation", "scheduled-function"]
author: "Josh Nesbit, Outer Sunset Today"
neighborhood: "Outer Sunset, San Francisco"
attribution_source: "Civic Media shelf starter prompt"
source_url: "https://github.com/The-Relational-Technology-Project/outer-sunset-today"
web: "https://relationalbuilder.org/commons/e/build-todays-news-section"
created: "2026-09-21"
updated: "2026-09-21"
rtp_id: "ba8c1a54-60f2-4e17-8ad4-49edf548452c"
---
# Build: A Today's News Section for a Neighborhood Site

> Starter build: a scheduled function pulls a few local RSS feeds, fetches full articles, has an LLM curate 1 to 4 stories by the Hierarchy of Information Needs with structured output, and a compact component shows them. Includes the schema, the curator prompt template, and the never-blank rule.

Add a calm "Today's News" section to a neighborhood site: a few local RSS feeds, filtered and rewritten by the News Futures Hierarchy of Information Needs, showing 1 to 4 stories that matter to neighbors' daily lives. Follow the recipe "Today's News: Local News Filtered by What Neighbors Need" on this shelf. Build it in four steps, and ask for the local details in step 3 before generating the curator prompt.

**1. Storage.** A `news_items` table (Supabase, or a Community Cloud collection) with: `id`, `title` (original), `display_title` (rewritten), `source_name`, `source_url`, `article_hash` (unique), `summary`, `category`, `relevance_score` (numeric), `is_actionable` (boolean), `published_at`, `helpful_count` and `not_helpful_count` (default 0), `created_at`. Index `created_at` and `relevance_score`. Public read; writes only from the function. An `increment_news_feedback(item_id, feedback_type)` RPC or equivalent for the two buttons.

**2. Ingestion, on a schedule.** A server-side function `check-news` that runs twice a day. In Relational Builder that is an `api/check-news.ts` serverless function with a `{"crons": [...]}` entry in `vercel.json` (runs once published to Vercel), or the builder's own Supabase edge function scheduled with pg_cron. It takes a list of `{ name, url }` RSS sources; parses items from the past 96 hours; hashes `name + link` with SHA-256 and drops anything already in `news_items`; fetches each remaining article's full HTML in parallel with a 10-second timeout; strips `<script>`, `<style>`, and tags, collapses whitespace, and caps each body at 6,000 characters. The LLM key lives in a secret env var and is only ever read server-side.

**3. Curation with structured output.** Send the candidates (index, title, outlet, URL, body) to an LLM with a forced tool call `submit_curated_news` returning `articles: [{ index, display_title, relevance_score (0 to 1), category, is_actionable, summary }]`, where category is one of housing, transit, business, community, government, education, environment, safety, health, culture. The system prompt, with the builder's local details filled in:

> You are a neighborhood bulletin-board curator for [NEIGHBORHOOD] in [CITY]. This is not a news site; the tone is calm, helpful, neighborly. Choose 1 to 4 stories that genuinely matter to neighbors; one great story beats four mediocre ones. Force-rank by the Hierarchy of Information Needs. TIER 1, basic needs and safety: housing and rent policy, transit disruptions on [LINES], food access, school enrollment and closures, healthcare, active safety alerts. TIER 2, civic participation: votes, hearings, ballot measures, comment periods, community meetings. TIER 3, community connection: events, neighbor initiatives, business openings and closings, parks. TIER 4, general interest, only with a clear [NEIGHBORHOOD] angle. A Tier 1 story always outranks a Tier 3 story. CITYWIDE COUNTS: [CITY]-wide stories about [SCHOOL DISTRICT], [TRANSIT AGENCY], housing policy, ballot measures, and [LANDMARKS] are relevant even when the neighborhood is not named. DEDUPLICATE: one story per underlying event, the most useful version. CRIME: include only an active, ongoing safety concern where neighbors need to take precautions right now; exclude arrests, arraignments, charges, court proceedings, sentencing, investigations, and anything where the danger has passed. When in doubt, leave it out. HEADLINES: rewrite each, under 80 characters, plain language, what happened and what it means for neighbors, no alarm words or question-bait, as if telling a neighbor over coffee. SUMMARY: one or two sentences based only on the article body; never invent details, quotes, or calls to action. Get local geography right: [DISTRICT NOTES]. SCORING: Tier 1 starts at 0.7, Tier 4 caps at 0.5, target 0.55 or above. Always return your single best candidate with an honest score even on a slow day; return an empty list only if nothing is relevant to [CITY] residents.

After the call, keep `relevance_score >= 0.55`; if none pass, keep the single highest-scoring candidate. Upsert into `news_items` on `article_hash`. Log what was rejected and why so the builder can tune the sources.

**4. Display.** A `useNewsItems` hook that reads items created in the last 7 days, ordered by `created_at` then `relevance_score` descending, limit 4. A compact `TodaysNews` component: each story is the `display_title` linking out to `source_url` with an external-link icon, the first sentence of `summary`, `source_name` in muted text, and a small helpful / not helpful pair. Skeletons while loading, and a neighborly empty state ("Quiet week. Nothing new that needs your attention.") if the table is empty.

Before generating, ask the builder for: their neighborhood and city, 2 to 5 RSS feeds that cover it, the transit lines and landmarks the curator should know, and who will glance at the section once a week. Credit the recipe and Outer Sunset Today in the plan.

## Details

- **category:** Neighborhood Sites
- **builds on:** todays-news-local-news-by-need, hierarchy-of-needs
- **guardrails:** ask for the local nouns before writing the curator prompt, never summarize from RSS snippets alone, never leave the section blank, crime only when neighbors must act now
- **stack notes:** scheduled function: api/check-news.ts + vercel.json crons (Vercel publish), or the builder's own Supabase edge function with pg_cron, LLM key stays in a secret env var, server-side only, storage: Supabase news_items or a Community Cloud collection
- **practice kind:** prompt
- **software note:** The curator policy is the recipe; this prompt is the software shape of it. A human editor with a Sunday hour can run the same policy without any of this.
- **parent format id:** f-neighborhood-newsletter

---

*Contributed by Josh Nesbit, Outer Sunset Today — Outer Sunset, San Francisco — Civic Media shelf starter prompt. [Source](https://github.com/The-Relational-Technology-Project/outer-sunset-today) [On the web](https://relationalbuilder.org/commons/e/build-todays-news-section).*

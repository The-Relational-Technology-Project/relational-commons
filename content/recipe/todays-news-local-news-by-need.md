---
title: "Today's News: Local News Filtered by What Neighbors Need"
slug: "todays-news-local-news-by-need"
kind: "recipe"
studio: "civic-media"
tags: ["commons/recipe", "studio/civic-media", "civic-media", "civic-media-recipe", "local-news", "news-curation", "hierarchy-of-needs", "rss", "neighborhood-site", "ai-curation", "needwellbeingsafety", "needbelongingcontext", "needagencycivic_expression", "participationcollective_sensemaking", "timecommunity_rhythm", "ingredienttrust", "sizesnack", "patterncreating_shared_understanding", "charterhierarchy_of_needs", "charternews_as_care", "charterinformation_equity"]
topics: ["civic-media", "civic-media-recipe", "local-news", "news-curation", "hierarchy-of-needs", "rss", "neighborhood-site", "ai-curation", "need:wellbeing.safety", "need:belonging.context", "need:agency.civic_expression", "participation:collective_sensemaking", "time:community_rhythm", "ingredient:trust", "size:snack", "pattern:creating_shared_understanding", "charter:hierarchy_of_needs", "charter:news_as_care", "charter:information_equity"]
author: "Josh Nesbit, Outer Sunset Today"
neighborhood: "Outer Sunset, San Francisco"
attribution_source: "Relational Technology Project"
source_repo: "https://github.com/The-Relational-Technology-Project/outer-sunset-today"
source_url: "https://github.com/The-Relational-Technology-Project/outer-sunset-today"
web: "https://relationalbuilder.org/commons/e/todays-news-local-news-by-need"
created: "2026-09-21"
updated: "2026-09-21"
rtp_id: "094be4bc-c77c-4148-ba2c-2a44b8e209f1"
---
# Today's News: Local News Filtered by What Neighbors Need

> A calm, 1 to 4 story local news section for a neighborhood site: a few local RSS feeds, full articles fetched, then a curator (AI or human) that force-ranks by the Hierarchy of Information Needs, keeps out past-tense crime, rewrites headlines neighbor-to-neighbor, and never leaves the section blank. Built and tuned on Outer Sunset Today.

A neighborhood site is not a news site. It is a bulletin board that helps neighbors stay informed about what matters in daily life. This recipe turns a few local RSS feeds into 1 to 4 calm, useful stories a day, filtered by need rather than by outrage. It was built and tuned on Outer Sunset Today, a neighborhood calendar in San Francisco.

**The editorial policy** (hand this to your curator, whether a neighbor or an AI):

1. **Force-rank by the Hierarchy of Information Needs.** Tier 1, basic needs and safety: housing and rent policy, disruptions on the transit lines neighbors ride, food access, school enrollment and closures, healthcare, active safety alerts. Tier 2, civic participation: votes, hearings, ballot measures, comment periods, community meetings. Tier 3, community connection: events, neighbor initiatives, business openings and closings, parks. Tier 4, general interest, only with a clear local angle. A Tier 1 story always outranks a Tier 3 story.
2. **Citywide counts.** A school district policy or a regional transit change affects the neighborhood even when the neighborhood is never named. Do not reject those for lacking the name.
3. **Crime: only what is happening right now.** Include a crime story only if neighbors need to take a precaution today (a suspect at large, a hazard, an advisory to avoid an area). Exclude arrests, arraignments, charges, trials, sentencing, investigations, and anything where the danger has passed. When in doubt, leave it out.
4. **One story per event.** When several outlets cover the same thing, keep the version most useful to neighbors.
5. **Rewrite the headline.** Under 80 characters, plain language, what happened and what it means here. No alarm words, no question-bait. Written the way you would tell a neighbor over coffee.
6. **Summarize only from the article body.** One or two sentences. No invented details or quotes, and no generic calls to action ("neighbors should attend") unless the article itself says so.
7. **Quality over quantity, but never blank.** Pick 1 to 4 stories; one great story beats four mediocre ones. Score relevance from 0 to 1 and aim for 0.55 and up. If nothing clears the bar, keep the single best candidate so the section never goes dark.

**The pipeline** (what runs, twice a day):

1. Pull RSS from a short list of local outlets, looking back 96 hours. Hyperlocal outlets publish a few times a week, so a 48-hour window sees only the big-city feed.
2. Hash `source name + link` (SHA-256) and skip anything already evaluated. Nothing goes to the curator twice.
3. Fetch each new article's full page in parallel, strip scripts, styles, and tags, collapse whitespace, cap at 6,000 characters. RSS snippets are one-paragraph teasers, and summarizing a teaser is how an AI invents quotes and outcomes. The full body ends that.
4. Send the candidates to an LLM with the editorial policy as its system prompt and a structured tool for the answer: `articles: [{ index, display_title, relevance_score, category, is_actionable, summary }]`.
5. Keep stories at 0.55 and up, or the single best if none pass. Upsert into `news_items` keyed on the hash.
6. The page shows up to 4 stories from the last 7 days, newest first: rewritten headline linking to the source, first sentence of the summary, outlet name in muted text, and a helpful / not helpful pair so neighbors can tune it.

**What took iteration to learn:**

- Snippets hallucinate, full bodies do not. This was the single biggest quality jump.
- The crime rule has to be explicit and past-tense aware. "Local news" feeds are dense with court stories that make a block feel less safe without giving anyone anything to do.
- Citywide relevance has to be stated, or the curator rejects the school board story for not naming the neighborhood.
- Slow days are normal. The never-blank fallback plus a 7-day display window keeps the section alive without lowering the bar on busy days.
- Headlines are the tone. Rewriting them is what makes the section feel like a neighbor and not a feed.

**To adapt it for your place:** list 2 to 5 outlets that actually cover your neighborhood and city; name the transit lines, districts, schools, and landmarks the curator should recognize; state your own citywide-counts rule; and decide who skims the section once a week and adjusts the sources. The software is the smaller part. The policy above is the recipe, and it works just as well for a human editor with a Sunday hour.

Companion build prompt: "Build: A Today's News Section for a Neighborhood Site" on this shelf, with the schema, the scheduled function, the curator prompt template, and the display component.

## Details

- **rules:** force-rank by tier; Tier 1 always outranks Tier 3, citywide decisions count even when the neighborhood is not named, crime only when neighbors must act right now; no arrests, trials, or past incidents, one story per event, headline rewritten under 80 characters, calm, neighbor-to-neighbor, summary grounded only in the article body, 1 to 4 stories; relevance 0.55 and up; keep the single best if none pass
- **tiers:** {"1":"basic needs and safety: housing, transit disruptions, food access, schools, healthcare, active safety alerts","2":"civic participation: votes, hearings, ballot measures, comment periods, community meetings","3":"community connection: events, neighbor initiatives, business openings and closings, parks","4":"general interest, only with a clear local angle"}
- **example:** {"url":"https://github.com/The-Relational-Technology-Project/outer-sunset-today","name":"Outer Sunset Today","function":"supabase/functions/check-news/index.ts"}
- **lessons:** full article bodies end summary hallucination, the crime rule must be explicit and past-tense aware, citywide relevance must be stated, never-blank fallback plus a 7-day window keeps slow days alive, headline rewriting sets the tone
- **pipeline:** {"dedupe":"sha256(source_name + link)","schedule":"twice daily","threshold":0.55,"display_max":4,"window_hours":96,"body_cap_chars":6000,"display_window_days":7}
- **builds on:** hierarchy-of-needs, news-futures-charter, format-neighborhood-newsletter
- **practice kind:** recipe
- **companion prompt:** build-todays-news-section
- **charter alignment:** hierarchy_of_needs, news_as_care, information_equity

---

*Contributed by Josh Nesbit, Outer Sunset Today — Outer Sunset, San Francisco — Relational Technology Project. [Source](https://github.com/The-Relational-Technology-Project/outer-sunset-today) [On the web](https://relationalbuilder.org/commons/e/todays-news-local-news-by-need).*

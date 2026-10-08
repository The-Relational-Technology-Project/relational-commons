---
title: "Results are commons: export flatfiles so processes hand off"
slug: "results-as-flatfiles-interop"
kind: "methodology"
studio: "deliberation"
tags: ["commons/methodology", "studio/deliberation", "deliberation", "interop", "export", "methodology", "metagov"]
topics: ["deliberation", "interop", "export", "methodology", "metagov"]
author: "Metagov, Interoperable Deliberative Tools project"
attribution_source: "github.com/metagov/interop"
source_url: "https://github.com/metagov/interop"
web: "https://relationalbuilder.org/commons/e/results-as-flatfiles-interop"
created: "2026-10-08"
updated: "2026-10-08"
rtp_id: "691e1b57-1a6f-4943-858a-7b1c73e4ccee"
---
# Results are commons: export flatfiles so processes hand off

> Metagov's interop practice: every deliberative tool publishes its results as open flatfiles (JSON or CSV) so the next stage, or the next tool, can pick them up. A visible "Export results" affordance on anything built here.

The Interoperable Deliberative Tools project asks every tool to publish results in open flatfiles so processes can hand off to each other: a poll's statements and votes feed a report generator; a report feeds an assembly's briefing; an assembly's recommendations feed the decision record.

In practice for a neighborhood build:

- Expose "Export results" where results appear, writing JSON (and CSV where tabular).
- Keep the shape plain and documented in the app: participants (and who was not heard), statements, votes or agreement by group, themes with quotes, decisions.
- Import the same shape, so a tool can start from another tool's export.
- Say in the UI when the shape is a placeholder pending a partner's real schema.

What this neighborhood learns should be able to travel.

## Details

- **license:** MIT (interop repo)

---

*Contributed by Metagov, Interoperable Deliberative Tools project — github.com/metagov/interop. [Source](https://github.com/metagov/interop) [On the web](https://relationalbuilder.org/commons/e/results-as-flatfiles-interop).*

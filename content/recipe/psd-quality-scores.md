---
title: "Quality Scores"
slug: "psd-quality-scores"
kind: "recipe"
studio: "prosocial-design"
license: "CC BY-SA 4.0"
tags: ["commons/recipe", "studio/prosocial-design", "prosocial-design", "design-pattern", "pdn-ratingtentative", "wheninteractive", "civic-signalconnect", "build-bridges-between-groups"]
topics: ["prosocial-design", "design pattern", "pdn-rating:tentative", "when:interactive", "civic-signal:connect", "build bridges between groups"]
author: "Prosocial Design Network"
attribution_source: "prosocialdesign.org"
source_url: "https://www.prosocialdesign.org/library/quality-scores"
web: "https://relationalbuilder.org/commons/e/psd-quality-scores"
created: "2026-10-12"
updated: "2026-10-12"
rtp_id: "1a5c688e-e956-4a2d-b779-b7f8545e0e2a"
---
# Quality Scores

> A “quality” score displayed on posts and comments alongside popularity cues (e.g., likes, reshare counts).

![](https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/69d63dfc6db0d0b6429c878c_Quality%20Score.png)

**Goal:** Increase engagement with high quality content  
**Evidence rating (PDN):** Tentative  
**Civic signal:** Connect — Build bridges between groups  
**When to use:** Interactive

## What it is

A “quality” score displayed on posts and comments alongside popularity cues (e.g., likes, reshare counts).

## Intended impact

Because platforms almost always display popularity cues (e.g., like/share counts), which can amplify morally charged and conflict-oriented content, adding a quality score can incentivize users to engage with higher quality content, mitigating the negative effects associated with reliance on popularity cues alone.

## Evidence that it works

Wu et al. (2025) ran a survey experiment to investigate whether the presence of a quality score next to popularity cues can nudge social media users to engage with higher-quality content than they would in the presence of a popularity signal alone, which is standard on most social media platforms. (Note: While in the study displayed the term “Expert Score”, participants were previously told that score “assessed the substantive quality of the content”, with no further details, which is why we use the more general term “quality score”.)

The study used a re-posting intention task (i.e., participants were asked to select a comment they would most like to post themselves) and an experimental design that randomly placed participants into one of four conditions: (1) no feedback scores, (2) popularity scores only, (3) quality score only, (4) dual feedback scores (popularity + quality.) Participants were shown 4 comments on political topics sampled from Reddit and were asked which of them they would most like to re-post.

The popularity score used in the study was based on the number of upvotes and downvotes the comment had received in the original Reddit thread it was posted in. The quality score was created by asking an LLM to rate comments on how much they communicated individual well-being, signs of positive social media use, or indications of virtuous character traits.

The findings from the study suggest the intervention is effective: in the dual feedback condition (quality + popularity scores), users selected to share the higher-quality content 68.5% of the time, significantly higher than the 51% in the popularity-only condition (Note: all effects we include are statistically significant, unless otherwise stated.)

Though the comparison between the dual-feedback condition and the popularity-only condition makes theoretical sense since the presence of a popularity cue is the norm in most platforms, it is important to note that there was no significant improvement in content-selection when comparing the dual-feedback condition to the control, no-feedback condition. This suggests the design pattern works better as a way of reducing the negative consequences of popularity-conformity, rather than increasing baseline judgment capabilities for users.

While the results from this initial study are promising, evidence from studies that more closely replicate real-world use conditions, such as a field experiment, is needed to understand the impact of deploying a similar intervention in social media platforms.

## Why it matters

Research suggests that popularity cues and algorithms that prioritize engagement maximization lead to a greater supply of extreme, conflict-oriented, and morally laden content. By emphasizing other qualities that platforms would like to prioritize, a normative score like the one proposed here could mitigate the negative consequences derived from highlighting popularity alone.

## Special considerations

Because of the ambiguity in the study of how the quality scores were calculated and by whom, we might see variable results in real world settings depending on users’ trust in the criteria and methods used to construct quality scores.

## Citations

- *Beyond Likes: How Normative Feedback Complements Engagement Signals on Social Media.* — Wu, Y., Zhao, M., & Canny, J. (arXiv, May 14, 2025)

---

From the Prosocial Design Network's Digital Intervention Library (https://www.prosocialdesign.org/library/quality-scores), licensed CC BY-SA 4.0. Reformatted for the RT Commons; text otherwise as published. Library citation: Prosocial Design Network (2024), Digital Intervention Library, https://doi.org/10.17605/OSF.IO/Q4RMB. Anything built from this pattern should credit the Prosocial Design Network and the researchers cited above.

## Details

- **goal:** Increase engagement with high quality content
- **citations:** [object Object]
- **image url:** https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/69d63dfc6db0d0b6429c878c_Quality%20Score.png
- **pdn rating:** Tentative
- **when to use:** Interactive
- **civic signal:** Connect
- **pdn library doi:** 10.17605/OSF.IO/Q4RMB
- **civic signal goal:** Build bridges between groups

---

*Contributed by Prosocial Design Network — prosocialdesign.org. [Source](https://www.prosocialdesign.org/library/quality-scores) Licensed CC BY-SA 4.0. [On the web](https://relationalbuilder.org/commons/e/psd-quality-scores).*

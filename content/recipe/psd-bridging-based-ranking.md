---
title: "Bridging-based ranking"
slug: "psd-bridging-based-ranking"
kind: "recipe"
studio: "prosocial-design"
license: "CC BY-SA 4.0"
tags: ["commons/recipe", "studio/prosocial-design", "prosocial-design", "design-pattern", "pdn-ratingtentative", "whenproactive", "civic-signalconnect", "build-bridges-between-groups"]
topics: ["prosocial-design", "design pattern", "pdn-rating:tentative", "when:proactive", "civic-signal:connect", "build bridges between groups"]
author: "Prosocial Design Network"
attribution_source: "prosocialdesign.org"
source_url: "https://www.prosocialdesign.org/library/bridging-based-ranking"
web: "https://relationalbuilder.org/commons/e/psd-bridging-based-ranking"
created: "2026-10-12"
updated: "2026-10-22"
rtp_id: "8a925ac4-cf7b-44eb-8f5d-bc0af840f8e5"
---
# Bridging-based ranking

> A bridging algorithm is a feed-ranker that identifies and promotes content valued by people from opposing social groups, as opposed to, for example, content that generates the most engagement overall.

![](https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/6a58d5c268b32db30f88f947_Bridging-based%20ranking.png)

**Goal:** Reduce partisan animosity  
**Evidence rating (PDN):** Tentative  
**Civic signal:** Connect — Build bridges between groups  
**When to use:** Proactive

## What it is

A bridging algorithm is a feed-ranker that identifies and promotes content valued by people from opposing social groups, as opposed to, for example, content that generates the most engagement overall.

## Intended impact

To decrease partisan animosity by reducing the reach and amplification of polarizing content (e.g., posts blaming the outgroup for social problems).

## Evidence that it works

The evidence on bridging-based ranking comes from two studies: a controlled experiment in a simulated social media feed, and a large field experiment that tested an algorithm applying a similar bridging-style upranking score.

Brady et al. (2025) conducted an experiment in a simulated social media environment (YourFeed) to test whether a bridging algorithm can reduce the tendency to post group-polarizing content (called “IME content” in the paper, meaning ingroup-aligned, moral, and emotional content).

Researchers constructed a bridging algorithm that ranks posts higher when they receive engagement from both Democrats and Republicans, while down-ranking posts that only attract engagement from one side. Participants were then assigned to view one of four feeds: a control feed (posts randomly selected from a baseline pool), a feed ranked by passive engagement (dwell time), a feed ranked by active engagement (likes and shares), or a feed ranked by the bridging algorithm. (Dwell time and engagement, including bridging engagement, were estimated in a previous study.) After scrolling through their feeds, participants were asked how likely they would post content either blaming the outgroup (i.e., opposing partisans) or praising the ingroup.

The bridging algorithm reduced participants’ intentions to post outgroup blame and ingroup praise content compared to passive engagement feeds (d = 0.22 for blame, and d = 0.20 for praise) and active engagement feeds (d = 0.27 for blame, and d = 0.29 for praise). (Note: All effects included are statistically significant, unless otherwise noted. We report effect sizes using the metrics in the authors’ paper.)

In a field setting, Stray et al. (2026) tested a related, bridging-style algorithm (which they called “diverse approval”) as one arm of a large independent field experiment conducted on Facebook, X, and Reddit using a browser extension. Rather than ranking by cross-group engagement, this intervention used a Large Language Model (GPT 4o) to predict which posts both Democrats and Republicans would find valuable and engaging, and inserted that content into users’ feeds. The results indicated no significant reduction in affective polarization, and it significantly lowered average engagement with the platforms.

The results provide initial evidence that a bridging algorithm can be a healthy alternative to engagement-based ranking (the current standard for most platforms). Some limitations need to be overcome by future research, however, before we can be certain of what to expect if a similar algorithm were to be deployed. The statistically significant evidence we have comes from a simulated environment study, and the algorithms operationalize the idea of cross-partisan approval in slightly different ways (one via behavioural profiling, and the other by using LLM classifiers), so future studies should adjudicate how effective these alternatives are in relation to each other, as well as to the current platform defaults.

## Why it matters

A growing body of evidence (Brady et al., 2023; Robertson, Rosario, Van Bavel, 2024) suggests that engagement-based algorithms amplify politically extreme and morally charged content, contributing to distorted perceptions of political reality and fueling polarization. Because social media is a major source of political information for many, these algorithmic effects can have broad implications for the quality of political discourse. Brady et al. (2025) provide experimental evidence that bridging algorithms, an easy to implement and scale solution, have the potential to meaningfully reduce these distortions and contribute to less polarized digital information environments. The null results from Stray et al.’s (2026) field study, however, indicate further testing is needed to evaluate whether effectiveness in live settings hinges on specific operationalization decisions or if the bridging-based feed ranking really doesn’t translate to more prosocial outcomes like reduced affective polarization.

## Special considerations

Compared to the control condition, participants in the Brady et al. (2025) bridging condition estimated that group-polarizing content was less common (effect sizes d = 0.15 to d = 0.52) and perceived the network as less polarized (d = 0.43) and less politically extreme (d = 0.40). The authors describe this as an “underperception” of IME content posting norms, framing it as a distortion in the opposite direction from the one produced by engagement-based feeds.

It is worth noting, however, that this interpretation rests on the assumption that participants should have accurately inferred the true underlying distribution of content in the network, even though they were only exposed to a bridging-ranked feed that showed them less polarizing content. Platform designers should keep this framing in mind when weighing the underperception finding: in a live context, a bridging algorithm that reduces both the supply and demand for polarizing content may produce perceptions that are not so much inaccurate as reflective of a genuinely changed information environment.

Additional analysis in Brady et al. (2025) suggests the mechanism involves social norm perceptions: engagement-based feeds inflated beliefs about how common and socially acceptable polarizing content was, in turn increasing willingness to post it; these perceptions were also shifted in the bridging algorithm condition.

## Citations

- *Engagement-based Algorithms Disrupt Human Social Norm Learning* — Brady, William J, Joshua C Jackson, Meriel Doyle, and Silvan Baier. (OSF Preprint)
- *Algorithm-mediated social learning in online social networks.*
- *Inside the funhouse mirror factory: How social media distorts perceptions of norms.* (Current Opinion in Psychology)
- *The prosocial ranking challenge: reducing polarization on social media without sacrificing engagement.* — Stray, Jonathan, Ian Baker, George Beknazar-Yuzbashev, Ceren Budak, Julia Kamin, Kylan Rutherford, Mateusz Stalinski (ArXiV, March 20, 2026)

---

From the Prosocial Design Network's Digital Intervention Library (https://www.prosocialdesign.org/library/bridging-based-ranking), licensed CC BY-SA 4.0. Reformatted for the RT Commons; text otherwise as published. Library citation: Prosocial Design Network (2024), Digital Intervention Library, https://doi.org/10.17605/OSF.IO/Q4RMB. Anything built from this pattern should credit the Prosocial Design Network and the researchers cited above.

## Details

- **goal:** Reduce partisan animosity
- **citations:** [object Object], [object Object], [object Object], [object Object]
- **image url:** https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/6a58d5c268b32db30f88f947_Bridging-based%20ranking.png
- **pdn rating:** Tentative
- **when to use:** Proactive
- **civic signal:** Connect
- **pdn library doi:** 10.17605/OSF.IO/Q4RMB
- **civic signal goal:** Build bridges between groups

---

*Contributed by Prosocial Design Network — prosocialdesign.org. [Source](https://www.prosocialdesign.org/library/bridging-based-ranking) Licensed CC BY-SA 4.0. [On the web](https://relationalbuilder.org/commons/e/psd-bridging-based-ranking).*

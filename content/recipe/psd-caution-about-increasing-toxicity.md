---
title: "Caution About Increasing Toxicity"
slug: "psd-caution-about-increasing-toxicity"
kind: "recipe"
studio: "prosocial-design"
license: "CC BY-SA 4.0"
tags: ["commons/recipe", "studio/prosocial-design", "prosocial-design", "design-pattern", "pdn-ratingtentative", "wheninteractive", "civic-signalwelcome", "ensure-user-safety"]
topics: ["prosocial-design", "design pattern", "pdn-rating:tentative", "when:interactive", "civic-signal:welcome", "ensure user safety"]
author: "Prosocial Design Network"
attribution_source: "prosocialdesign.org"
source_url: "https://www.prosocialdesign.org/library/caution-about-increasing-toxicity"
web: "https://relationalbuilder.org/commons/e/psd-caution-about-increasing-toxicity"
created: "2026-10-12"
updated: "2026-10-12"
rtp_id: "b387391c-c6fc-4157-96d6-cb2590a2baaa"
---
# Caution About Increasing Toxicity

> Using a classifier trained on a forum's conversations, alert users when a thread they are about to reply to is likely to become tense or toxic and give them real feedback on whether their reply will reduce or add to the tension.

![](https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/647f696dc653a97c26f42b14_keeper-2.png)

**Goal:** De-escalate tense threads and reduce toxicity  
**Evidence rating (PDN):** Tentative  
**Civic signal:** Welcome — Ensure user safety  
**When to use:** Interactive

## What it is

Using a classifier trained on a forum's conversations, alert users when a thread they are about to reply to is likely to become tense or toxic and give them real feedback on whether their reply will reduce or add to the tension.

## Intended impact

By making well-intentioned users aware of rising tensions in a thread and giving them feedback on the likely impact of their reply, users can tailor and adjust their comments to de-escalate tensions.

## Evidence that it works

Chang et al. (2022) developed and tested a browser extension tool, "ConvoWizard", that alerts Reddit users if a thread they are about to reply to is "getting tense" (or not) and then gives those users real-time feedback on whether their reply will likely increase or decrease tension. The tool's predictive model was trained specifically on threads in a given subReddit using moderator labels. The researchers tested the tool with 14 volunteer participants, using a within-subjects design that randomly assigned when ConvoWizard would "pop-up." Matching participants' replies on similar threads, researchers observed that participants took more time to craft their reply on tense threads when ConvoWizard popped up as opposed to when it didn't. Participants also tended to revise their replies to be more likely to de-escalate conversations. (Note: all effects we include are statistically significant, unless otherwise stated.)

While these initial results are promising, given the small sample size and within-subject design further testing is needed to confirm that ConvoWizard is broadly effective.

## Why it matters

Given the nature of online communication, conversations can frequently escalate into toxic exchanges, even among well-meaning users. A tool that makes those users aware of the risk of escalating toxicity can help well-intentioned users not be inadvertent contributors to toxic exchanges.

## Special considerations

There are two considerations and a risk for tools that use ConvoWizard's approach. First, ConvoWizard's effectiveness may be due to its predictive model which uses discussions in a specific subReddit, so it may be less effective in mass-forums (Twitter, Facebook) where models could be less precise. Secondly, the existing tool and tests assume that a forum's participants voluntarily use the tool; there is no evidence that a ConvoWizard tool would be effective for users who did not choose to use it. Moreover, as the authors note, there is a risk that ill-intentioned users could misuse the tool to escalate tensions and toxicity.

## Citations

- *Thread with Caution: Proactively Helping Users Assess and Deescalate Tension in Their Online Discussions.* — Chang, J. P., Schluger, C., & Danescu-Niculescu-Mizil, C. (Proceedings of the ACM on Human-Computer Interaction, November 12, 2022). https://doi.org/10.1145/3555603

---

From the Prosocial Design Network's Digital Intervention Library (https://www.prosocialdesign.org/library/caution-about-increasing-toxicity), licensed CC BY-SA 4.0. Reformatted for the RT Commons; text otherwise as published. Library citation: Prosocial Design Network (2024), Digital Intervention Library, https://doi.org/10.17605/OSF.IO/Q4RMB. Anything built from this pattern should credit the Prosocial Design Network and the researchers cited above.

## Details

- **goal:** De-escalate tense threads and reduce toxicity
- **citations:** [object Object]
- **image alt:** An example of a prompt that says "Your Comment Is Likely To Be Harmful To Overs" which invites the user to edit their message or post it anyway.
- **image url:** https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/647f696dc653a97c26f42b14_keeper-2.png
- **pdn rating:** Tentative
- **when to use:** Interactive
- **civic signal:** Welcome
- **pdn library doi:** 10.17605/OSF.IO/Q4RMB
- **civic signal goal:** Ensure user safety

---

*Contributed by Prosocial Design Network — prosocialdesign.org. [Source](https://www.prosocialdesign.org/library/caution-about-increasing-toxicity) Licensed CC BY-SA 4.0. [On the web](https://relationalbuilder.org/commons/e/psd-caution-about-increasing-toxicity).*

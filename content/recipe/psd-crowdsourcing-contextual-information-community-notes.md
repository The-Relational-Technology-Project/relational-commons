---
title: "Crowdsourcing Contextual Information (Community Notes)"
slug: "psd-crowdsourcing-contextual-information-community-notes"
kind: "recipe"
studio: "prosocial-design"
license: "CC BY-SA 4.0"
tags: ["commons/recipe", "studio/prosocial-design", "prosocial-design", "design-pattern", "pdn-ratingconvincing", "wheninteractive", "civic-signalunderstand", "show-reliable-information"]
topics: ["prosocial-design", "design pattern", "pdn-rating:convincing", "when:interactive", "civic-signal:understand", "show reliable information"]
author: "Prosocial Design Network"
attribution_source: "prosocialdesign.org"
source_url: "https://www.prosocialdesign.org/library/crowdsourcing-contextual-information-community-notes"
web: "https://relationalbuilder.org/commons/e/psd-crowdsourcing-contextual-information-community-notes"
created: "2026-10-12"
updated: "2026-10-22"
rtp_id: "9a88e70e-b940-4c63-a905-d2881cdaf6c2"
---
# Crowdsourcing Contextual Information (Community Notes)

> Attaching contextual information ('Community Notes') to misleading content. Notes are crowdsourced and shown alongside a post when the Note has been rated "helpful" by users with diverse views.

![](https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/66510410a33641fa873b3845_Community%20Notes%403x.webp)

**Goal:** Reduce the spread of misinformation  
**Evidence rating (PDN):** Convincing  
**Civic signal:** Understand — Show reliable information  
**When to use:** Interactive

## What it is

Attaching contextual information ('Community Notes') to misleading content. Notes are crowdsourced and shown alongside a post when the Note has been rated "helpful" by users with diverse views.

## Intended impact

By providing relevant information to misleading posts, users may become less willing to see those posts as credible and to reshare them.

## Evidence that it works

Four studies investigate whether Community Notes ("Notes") are effective in reducing retweets of false or misleading posts on Twitter/X; one field experiment conducted by Twitter, and three studies that use public Twitter data to analyze the impact of community notes using quasi-experimental methods. Overall, the studies suggest that adding community notes may significantly reduce the likelihood of a post being reshared (25-60%), but since there is a substantial time delay from when a tweet is made and then receives a note (an average ~ 15 hours, or after 80% of retweets have been made) and only a subset of posts with misinformation posts ever receive a note, Community Notes overall may have a small impact in reducing misinformation, unless innovations allow them to be significantly scaled.

Twitter's study (Wojcik et al., 2022) reports a 25-34% decrease in the number of retweets when a Note is attached to a misleading tweet. Given that the study is a field experiment, i.e. it presumably randomly assigns some tweets to display a community note while not showing notes on other similar tweets, we would normally give its findings substantial weight. In this case, however, the study's write up (a single paragraph) does not provide enough detail - e.g., design, data, statistical method - for us to make an assessment of the strength of its findings.

The three other studies, however, are fully reported. They each make use of a public database from Twitter, but use different quasi-experimental methods to detect the effect of a tweet receiving a community note.

Chaui et al. (2023) take advantage of the fact that Community Notes were rolled out in three stages: a pilot stage where Notes were hidden to all except a small subset of users; an initial rollout when all US users could see tweets with Notes and then a final rollout to global users. The authors looked at two sets of false or misleading tweets before and after the US rollout; tweets with Notes that were marked as "helpful" (as rated by a threshold of enough diverse users) and tweets whose Notes had not reached a "helpful" threshold. Critically, Notes are only shown to users when they reach the "helpful" threshold. This allowed the authors to see what happened when 'helpful' notes became visible to all US users and compare them to notes that continued to be hidden because they hadn't reached the helpful bar. In this first analysis, the authors observed a positive effect: after the rollout, there was a drop in the number of shares of tweets with displayed Notes, but not a drop in among tweets with still-hidden Notes. This promising finding aside, the authors did not see a similar effect for the Global rollout. They also failed to see effects when looking at additional analyses, for example, comparing tweets with notes just below and above the "helpful" threshold. The authors conclude with skepticism that Community Notes have any impact.

Renault et al. (2024) and Chuai et al. (2024) use the same dataset but take a different approach to modeling a quasi-experiment. They instead use the fact that misleading tweets with helpful Notes will have a period where their notes have not yet reached the "helpful" threshold (of 0.4) and so are still hidden. Renault et al. (2024) examines what happens when individual Notes become visible (and are just above the threshold, from 0.4-0.43) to see if there's a dropoff in retweets. Importantly, because there is a natural decline in retweets over time, they match those tweets with similar tweets with notes that remain just below the helpful threshold (0.37-0.4), and so remain invisible, as a comparison "control" group. After a Note becomes visible, they observe a 50% decrease in retweets compared to matched "control" tweets, a finding they observe in a second analysis of the data. Chuai et al. (2024) uses a similar approach but instead of matching tweets with tweets that have notes just below the 0.4 threshold, they instead create a control set of tweets matched on user and tweet characteristics (including, crucially, retweeting patterns). In their analysis they see a 60% decrease in retweets once a note is displayed.

While Chuai (2023) comes to a different conclusion than Renault (2024) and Chuai (2024), their findings are not as far off as may seem. Although Chuai (2023) takes considerable steps to control for differences between their "treatment" and "control" tweets, their design necessarily leaves room for other "confounding" factors playing a role (e.g. what kind of tweets were getting notes before and after the rollouts).

Renault (2024) and Chuai (2024) point out another key difference - and what ultimately points to a limitation of Notes: their seemingly large observed effects occur after a Note becomes public which is, on average, after 80% of retweets usually have been made. In other words, any effect of a Note will usually occur at the tail end of a tweets' engagement. Taking into consideration the delay in Notes being displayed, Chuai (2024) estimates that a community note will reduce the number of a tweet's overall reshares by 11%.

In sum, although there are mixed findings of the effectiveness of Community Notes, overall we see convincing evidence that Notes reduce re-sharing of false and misleading posts. Yet their ability to have a meaningful effect is limited by the lag time between when a false tweet is posted and receives a Note and the fact that they are - currently - only ever displayed on a subset of posts. To have a meaningful impact on reducing misinformation Community Notes would need innovations to be substantially scaled, for example, this recent proposal to leverage LLMs.

## Why it matters

Misinformation that is spread on social media poses potential threats to individual well-being and can lead to toxic division and mistrust. Other interventions that aim to reduce the spread of misinformation have limited effect in part because of mistrust of platforms and professional fact-checkers. Community Notes is a promising intervention because of its potential to identify more trustworthy checks on misinformation, by virtue of being crowdsourced across ideologically diverse users.

## Special considerations

Because Community Notes' effectiveness in reducing misinformation depends on its set of volunteers being diverse (ideologically, politically, etc.), if that full set is limited to, for example, only left-leaning or only right-leaning volunteers, then Community Notes will be less able to identify and reduce the spread of misleading content.

## Citations

- *Birdwatch: Crowd wisdom and bridging algorithms can inform understanding and reduce the spread of misinformation* — Stefan Wojcik, Sophie Hilgard, Nick Judd, Delia Mocanu, Stephen Ragain, M. B. Hunzaker, Keith Coleman, and Jay Baxter (arXiv, October 27, 2022)
- *The Roll-Out of Community Notes Did Not Reduce Engagement With Misinformation on Twitter* — Yuwei Chuai, Haoye Tian, Nicolas Pröllochs, and Gabriele Lenzini (arXiv, July 16, 2023)
- *Collaboratively adding context to social media posts reduces the sharing of false news* — Thomas Renault, David Restrepo Amariles, and Aurore Troussel (ArXiV, March 3, 2024)
- *Community notes reduce the spread of misleading posts on X* — Chuai, Yuwei, Moritz Pilarski, Gabriele Lenzini, and Nicolas Pröllochs. (ArXiV, April 26, 2024)

---

From the Prosocial Design Network's Digital Intervention Library (https://www.prosocialdesign.org/library/crowdsourcing-contextual-information-community-notes), licensed CC BY-SA 4.0. Reformatted for the RT Commons; text otherwise as published. Library citation: Prosocial Design Network (2024), Digital Intervention Library, https://doi.org/10.17605/OSF.IO/Q4RMB. Anything built from this pattern should credit the Prosocial Design Network and the researchers cited above.

## Details

- **goal:** Reduce the spread of misinformation
- **citations:** [object Object], [object Object], [object Object], [object Object]
- **image alt:** A minimalist line drawing of a user interface element showing a document or content card with horizontal lines representing text. Below it is a smaller box labeled 'Readers added context' with more horizontal lines, suggesting additional information or commentary.
- **image url:** https://cdn.prod.website-files.com/647f696dc653a97c26f42a0b/66510410a33641fa873b3845_Community%20Notes%403x.webp
- **pdn rating:** Convincing
- **when to use:** Interactive
- **civic signal:** Understand
- **pdn library doi:** 10.17605/OSF.IO/Q4RMB
- **civic signal goal:** Show reliable information

---

*Contributed by Prosocial Design Network — prosocialdesign.org. [Source](https://www.prosocialdesign.org/library/crowdsourcing-contextual-information-community-notes) Licensed CC BY-SA 4.0. [On the web](https://relationalbuilder.org/commons/e/psd-crowdsourcing-contextual-information-community-notes).*

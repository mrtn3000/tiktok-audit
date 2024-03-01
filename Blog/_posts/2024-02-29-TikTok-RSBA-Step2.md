---
layout: post
title: "🧵 Auditing TikTok: Defining Scenarios for TikTok Audits"
date: 2024-02-29 09:00:00
description: "Insights from RSBA Step 2"
tags: methodology, process, step2
categories: rsba
featured: true
related_posts: true
author: Kathy Meßmer
---

*By [Kathy Meßmer](https://www.stiftung-nv.de/en/person/dr-anna-katharina-messmer).*

As described in our [previous blog post](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/), we want to share our methodological reflections, decisions we made and insights we gathered during our [Risk-Scenario-Based Audit (RSBA) process](https://www.stiftung-nv.de/de/publication/auditing-recommender-systems#step1-planning). So, here is Step 2!

Step 2 is all about the *risk scenarios* of the RSBA. A scenario breaks down abstract systemic risks, as mentioned in article 34 DSA, into concrete testable hypotheses. Utilizing these scenarios is valuable because they help to dissect complex systemic risks outlined in the DSA, such as "negative effects on civic discourse and electoral processes", into tangible components that can be examined and assessed.

To standardize the way scenarios are described, we recommended to follow our scheme and to start with deductively defining:

1. Who is **the affected party?**
2. What **characterizes** this party?
3. What **harm** does this actor, person or group experience?
4. How is **the platform** involved in this experience?
5. What are the **macro impacts** that go beyond the individual?

Answering these questions should allow for a thorough description of the risk scenario.

Putting these components together, a generic risk scenario would look like the following:

{% include figure.html path="/assets/img/2024-02_rsba_scenario_generic.jpg" caption="Generic risk scenario description." alt="Screenshot of generic risk scenario" class="img-fluid rounded z-depth-1" zoomable=true width="100%" %} 

# Which risks did we choose?

The DSA outlines several systemic risks. In order to define concrete scenarios, it was, therefore, crucial to decide on specific risks to focus on. We started our exploration phase by looking at the risk to mental well-being, as mentioned in article 34 DSA, but shortly, two other risks caught our eye. Firstly, we realized [how much promotional content is spread on TikTok’s For You feed](https://tiktok-audit.com/blog/2024/ads_ads_ads/). Secondly, the “you may like”-section on the search page attracted our interest and we started to take a closer look at those [search suggestions.](https://tiktok-audit.com/blog/2023/Israel-Hamas-War-Suggestions/) While being under the radar of public attention for quite some time, this feature recently received much attention in [public](https://www.washingtonpost.com/technology/2024/02/08/tiktok-search-suggestions-inaccurate/) and [media](https://www.businessinsider.com/tiktok-recommendations-searches-videos-creators-sensational-comments-engagement-video-posts-2024-1?r=US&IR=T) discourse. 

We spent August/September 2023 exploring potential scenarios. In October, we discussed our scenarios in a workshop with [pollytix](https://pollytix.eu/) and [AI Forensics](https://aiforensics.org/work), the two organizations we have been working with on the RSBA. In November 2023, pollytix conducted focus group discussions with TikTok users which helped us to decide on three systemic risks and the respective scenarios:

- 💸 Risks to **consumer protection** (DSA Art. 34[1][b])
- 🧠 Risks to **mental well-being** (DSA Art. 34[1][d]).
- 🗨️ Risks to **civic discourse** (DSA Art. 34[1][c])

In the following sections, we will elaborate on the concrete scenarios we decided on.

## Scenario 1: Risks to consumer protection

Like all online platforms that offer service free of charge, TikTok makes money from advertising. TikTok is often associated with the rise of shopping platforms like [Temu](https://tiktok-audit.com/blog/2024/temu-tiktok/) and Shein, as well as numerous other shops that sell low-quality products. Besides that, TikTok is [increasingly](https://nymag.com/intelligencer/2024/01/what-i-learned-selling-a-used-pencil-on-tiktok-shop.html) [integrating online shopping into the app](https://newsroom.tiktok.com/en-us/introducing-tiktok-shop) and aiming to become a [relevant player in the global online shopping market](https://www.businessinsider.com/tiktok-shop-sellers-early-hiccups-big-discounts-and-new-sales-2023-4). However, the recently introduced [TikTok Shop](https://shop.tiktok.com/) is not yet available in Germany.

All of that could challenge high consumer protection standards, a core value of the European Union ([Art. 38](https://fra.europa.eu/en/eu-charter/article/38-consumer-protection?page=1) of the EU Charta of Fundamental Rights) and explicitly mentioned in the DSA: Article 1 of the DSA states that the DSA aims to set out “harmonized rules for a safe, predictable and trusted online environment that facilitates innovation and in which fundamental rights enshrined in the Charter, including the principle of consumer protection, are effectively protected”.

Both, shops and [products](https://ec.europa.eu/safety-gate/#/screen/home), tend to neglect consumer protection standards in the EU. TikTok itself is also under [scrutiny by consumer protection authorities](https://www.beuc.eu/press-releases/investigation-tiktok-closed-important-questions-unresolved-consumers-left-dark) for [several intransparent practices](https://ec.europa.eu/commission/presscorner/detail/en/ip_24_708).

Therefore, our first risk scenario concerns the (systemic) risk to consumer protection.

### Scenario Definition

1. Who is the <span class="rsba-scenario-affected">affected party</span>?

TikTok’s target group is young people, and we assumed that all TikTok users have experienced consumer protection-related issues on TikTok at some point. Every TikTok user is shown products and/or ads and, therefore, is also a potential customer for purchases through TikTok. That is why we decided to focus on <span class="rsba-scenario-affected">young TikTok users</span> as the <span class="rsba-scenario-affected">affected party.</span>

1. What <span class="rsba-scenario-characteristics">characterizes</span> this party?

As further <span class="rsba-scenario-characteristics">characteristics,</span> we specified the <span class="rsba-scenario-characteristics">age group of young adults between 18 and 25.</span> We excluded minors from this sample as they partially fall under different legal frameworks, have restricted accessibility (f.e. credit cards) and experience different harms. To be able to (language- and context-wise) understand the content these users might see, we further specified the affected user group as located <span class="rsba-scenario-characteristics">in Germany.</span>

1. What <span class="rsba-scenario-harm">harm does this individual, group or institution experience?

As to the <span class="rsba-scenario-harm">harm</span> this affected party experiences by using TikTok, we defined <span class="rsba-scenario-harm">overspending and hidden costs.</span> The harm is always related to the (systemic) risk under investigation. In this scenario, we wanted to research risks to consumer protection, specifically anything related to unforeseen (monetary) costs that may arise from purchases through TikTok. 

1. How is the <span class="rsba-scenario-platform">platform involved</span> in this experience?

Several elements of a platform can be involved in heightening a specific risk or harm. Although TikTok’s ad strategy is constantly changing, ads and promotional content are still mainly distributed via the For You feed, the main feature of TikTok. That is why we defined the <span class="rsba-scenario-platform">platform involvement</span> as <span class="rsba-scenario-platform">exposure to (malicious and/or misleading) ads via the For You feed.</span>

1. What are the <span class="rsba-scenario-macro">macro impacts</span> that go beyond the individual?

Many of the systemic risks mentioned in the DSA are abstract. When applied to the risk scenarios, this means that risks have a negative impact on individuals and groups, as well as on society as a whole. To differentiate between those levels, every risk scenario not only defines a specific harm but also has to define the <span class="rsba-scenario-macro">macro impact</span> this harm can have on society: In our case, <span class="rsba-scenario-macro">a low trust in consumer protection. </span>


Putting all components together, this is the scenario definition:

>  <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">end up overspending or with hidden costs</span> after being <span class="rsba-scenario-platform">exposed to (malicious and/or misleading) ads when swiping through the For You feed</span> and this will lead to a <span class="rsba-scenario-macro">low trust in consumer protection</span>.

## Scenario 2: Selfoptimization and risks to (mental) health

Our engagement with the topic of well-being is a good example of how iterative work can improve the auditing process. Having started our RSBA process by focusing on exploring risks to mental health, we decided not to pursue the topic further. However, during our stakeholder engagement phase, the topic came back on the agenda. To understand the user journey better, we conducted focus groups with TikTok users between 18 and 25. These discussions taught us about the risks that TikTok users themselves perceive on the platform. We learned that young adults are concerned about how content and advertisements on TikTok negatively influence the users’ self-image and that they pose a risk to the (mental or physical) health of its users. This convinced us to reintegrate the risk into our process by developing a risk scenario on that specific topic.

### Scenario definition

1. Who is the <span class="rsba-scenario-affected">affected party</span> and 2. What <span class="rsba-scenario-characteristics">characterizes</span> this party?

A [wide range of research](https://docs.google.com/document/d/1w-HOfseF2wF9YIpXwUUtP65-olnkPyWcgF5BiAtBEy0/edit) shows a rise in mental health disorders, such as anxiety, depression or self-harm, among the younger generations that might be linked to Social Media use. The discussions with our focus groups motivated us to take a closer look at risk factors on TikTok that might negatively influence mental health. Therefore, we decided to focus on the same <span class="rsba-scenario-affected">affected party</span> and its <span class="rsba-scenario-characteristics">characteristics</span> as in Scenario 1.

1. What <span class="rsba-scenario-harm">harm</span> does this individual, group or institution experience?

Regarding the <span class="rsba-scenario-harm">harm</span> this affected party experiences by using TikTok, we followed the concerns of our focus group respondents, defining the <span class="rsba-scenario-harm">harm</span> as <span class="rsba-scenario-harm">experiencing (mental or physical) health risks.</span>

1. How is the <span class="rsba-scenario-platform">platform involved</span> in this experience?

Once again, we had our eye on the For You feed, defining the <span class="rsba-scenario-platform">platform involvement</span> as <span class="rsba-scenario-platform">repeatedly exposing users to ads for dieting/beauty products/cosmetic surgery when swiping through the For You feed.</span>

1. What are the <span class="rsba-scenario-macro">macro impacts</span> that go beyond the individual?

Last but not least as <span class="rsba-scenario-macro">macro impact</span> this will <span class="rsba-scenario-macro">reduce overall health in Germany.</span>

Here is the final scenario definition:

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience (mental or physical) health risks</span> after being <span class="rsba-scenario-platform">repeatedly exposed to ads for dieting/beauty products/cosmetic surgery when swiping through the For You feed</span> and this will lead to <span class="rsba-scenario-macro">reduced overall health in Germany</span>.

## Scenario 3: Public Discourse

The third scenario of our RSBA focuses on a different functionality of TikTok: The “you may like” section and its list of suggested searches. Those can be found under the general search, where users are able to search for specific content or usernames. As we mentioned in our [former blog post](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/), some [reports](https://archive.ph/NzzG6) have described that Gen Z increasingly uses TikTok as a search engine. The search suggestions are of specific interest because TikTok can utilize them to direct users to view content on specific topics. [Our analysis of this functionality illustrates how far this can go, as we have shown that after October 7th, it suggested war-related content for several days](https://tiktok-audit.com/blog/2023/Israel-Hamas-War-Suggestions/). Furthermore, these suggestions may drive engagement by encouraging creators to record videos picking up on these topics and thus assume a potential agenda-setting function. We found out that sometimes these trending topics spread misinformation (e.g., that a person has died); sometimes, they seem to copy recent headlines, but when clicking on it, that does not lead to any actual news about the topic. This then prompts spammers or attention grabbers to post related videos, effectively acting as clickbait. Overall, the spread of misinformation, disinformation and negative (clickbaity) news makes the [world seem worse than it is](https://www.theguardian.com/commentisfree/2018/feb/17/steven-pinker-media-negative-news). We see these dynamics as very striking, which is why our third scenario focuses on the risk to public discourse. 

### Scenario definition

1. Who is the <span class="rsba-scenario-affected">affected party</span> and 2. What <span class="rsba-scenario-characteristics">characterizes</span> this party?

For practical research reasons, we decided to focus on the same group as in Scenario 1 and 2 regarding the <span class="rsba-scenario-affected">affected party</span> and its <span class="rsba-scenario-characteristics">characteristics.</span>

1. What <span class="rsba-scenario-harm">harm</span> does this actor, person or group experience?

We defined the <span class="rsba-scenario-harm">harm</span> this affected party experiences by using TikTok as the <span class="rsba-scenario-harm">experience of a distorted version of reality.</span>

1. How is the <span class="rsba-scenario-platform">platform involved</span> in this experience?

The platform involvement is <span class="rsba-scenario-platform">the suggested search terms in the “you may like”-section.</span>

1. What are the <span class="rsba-scenario-macro">macro impacts</span> that go beyond the individual?

Suggested searches might negatively affect <span class="rsba-scenario-macro">the public discourse.</span> 

Scenario 3 is defined as follows:

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience a distorted version of reality</span> <span class="rsba-scenario-platform">viewing the suggested search terms</span>, which <span class="rsba-scenario-macro">negatively impacts the public discourse.</span>


# Learnings

Here is what we learned about Step 2 throughout the process:

### Definitions

Scenario definitions are more abstract than we thought they would be. While some questions for the scenario definition were quite easy to answer, for others, it was the better decision to narrow it down as part of the data analysis. Otherwise, we would have restricted our findings. It is neither possible to form scenarios purely deductively nor is a purely inductive approach possible. Rather, both approaches must be dovetailed with each other. 

### Prioritization

While, in theory, the prioritization of scenarios and measurements should have been separated, we realized that they must go hand in hand - at least for third-party CSO researchers with resource restrictions. For every possible scenario, we had to check whether the relevant data was accessible and if it lay within our capabilities and area of expertise to collect it. For example, we decided not to do research on minors, although it might have had a higher priority due to the higher vulnerability of that age group. However, surveys with minors would have made our data collection way more expensive and complex. 

The same is true for assessments of the macro impact part of our scenarios. While it might be a crucial part of DSA-related risk assessments, it was just impossible for us to collect data on this as it would require further large-scale studies and psychological methodologies that cannot be applied in the context of independent research by a civil society organisation. 

For more reflections on our data collection and measurements, stay posted.
---
layout: post
title: "🧵 Auditing TikTok: Our methodology and dataset"
date: 2024-03-01 06:00:00
description: "Insights into step 3 of our RSBA process"
tags: methodology, process, step3
categories: rsba
featured: true
related_posts: true
author: Martin Degeling
---

*By [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling)*

As described [before](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/), we want to share our methodological reflections, decisions we made, and insights we had when we went through our [Risk-Scenario-Based Audit (RSBA) process](https://www.stiftung-nv.de/de/publication/auditing-recommender-systems). So, here is [Step 3: methodology, dataset, and measurements](https://www.stiftung-nv.de/de/publication/auditing-recommender-systems#step3-measurements).

As part of our RSBA, we have [examined different types of audits](https://www.stiftung-nv.de/de/publication/auditing-recommender-systems#step3-measurements) and provided some technical examples of how you can use them on TikTok in the [data knowledge hub](https://www.data-knowledge-hub.com/docs/data-collection/data-collection-intro/). We conducted almost all types of audits we initially listed in our RSBA paper, at least to some extent, during the exploration phase of the first step of the RSBA process. Before going into detail about the methods we used for testing [our scenarios](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step2/), here is a quick overview of what we learned about TikTok using different techniques for exploration:

{% include figure.html path="/assets/img/2024-03_rsba_audit_types.svg" caption="Types of audits we have identified as potentially relevant for the RSBA" alt="List of audit types: Code audit, Crowd-sourced audit, Document audit, Architecture audit, Automated audit, User survey" class="img-fluid rounded" zoomable=true width="20%" %} 

- **Code audit:** We used [MobFS](https://github.com/MobSF/Mobile-Security-Framework-MobSF) and Network Traffic Analysis with [mitmproxy](https://mitmproxy.org/) to understand the TikTok Android app. We learned that the app retrieves nearly all information from the server when it starts. Therefore, we focused on the network traffic. Here, we learned that the following video recommendations come in batches of around ten videos, that videos have a unique "aweme_id," which identifies each video individually, and that the app reports the view time of each video in milliseconds back to the server.
- **Crowd-sourced audit:** We collaborated with [AlgorithmWatch on their data donation campaign](https://algorithmwatch.org/en/what-tiktok-knows-about-you-data-donations/) and were able to access their data. We learned about the complexity of such campaigns regarding recruitment and the problems with data from a diverse set of users and use cases that might not match the study design.
- **Document audit:** As external researchers, we cannot access internal documentation on TikTok. Instead, we rely on [leaked information and news reports](https://www.data-knowledge-hub.com/docs/data-collection/data-collection-intro/) to better understand what is happening behind closed doors.
- **Architecture audit:** We did not conduct an architecture audit, as the internal structure of TikTok systems is unavailable for us to assess. Instead, we relied on information gathered through the code and document audit to understand relevant, user-facing elements of the platform.
- **Automated audit:** Early on, we did automated tests of the TikTok platform, starting with scraping the web version of TikTok (resulting in this [hashtag analysis](https://hashtags.tiktok-audit.com/)). As the project continued, we decided that focusing on the Android app version was warranted if we wanted to understand better how the platform behaves for most users.
- **User survey:** We reviewed academic research on TikTok and discussed the possibility of conducting a survey early on. You can find a syllabus of audits using different methods on multiple platforms [here](https://www.stiftung-nv.de/en/publication/auditing-recommender-systems-overview-existing-audits-risk-assessments-and-studies).

Over time, as we learned about the benefits and drawbacks of each approach, explored our data access possibilities, and assessed our capabilities, **we concluded that a semi-automated audit and a user survey are the most suitable methods for our RSBA on TikTok's recommender systems and the specific scenarios at hand.**

## Prioritization

As described in this [previous post](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step2/), our scenarios focus on systemic risks related to consumer protection, health, and public discourse. For each scenario, we discussed and prioritized different methods to better assess the severity of the risk.

{% include figure.html path="/assets/img/2024-03_rsba_measurement_priorization.svg" caption="TSchema for prioritizing measurements" alt="Schema for prioritizing measurements focusing Difficulty and Detectabilty" class="img-fluid rounded" zoomable=true width="100%" %} 

Two out of three scenarios target the recommender system of TikTok's For You feed and, therefore, require the perspectives of actual users and an understanding of the app's behavior when running, which can not be conducted on the document-, architecture- or code-level. Semi-automated here means that the data collection started with a manual training phase where researchers of our group manually trained accounts, impersonating different personas and sharing the data afterward, similar to a crowd-sourced approach. The automated data collection phase then follows this.

## Scenarios 1 & 2: Consumer Protection

The scenario definitions for the first two scenarios are:

>  <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">end up overspending or with hidden costs</span> after being <span class="rsba-scenario-platform">exposed to (malicious and/or misleading) ads when swiping through the For You feed</span> and this will lead to a <span class="rsba-scenario-macro">low trust in consumer protection</span>.

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience (mental or physical) health risks</span> after being <span class="rsba-scenario-platform">repeatedly exposed to ads for dieting/beauty products/cosmetic surgery when swiping through the For You feed</span> and this will lead to <span class="rsba-scenario-macro">reduced overall health in Germany</span>.

**How difficult will it be to execute these measurements?**

*Implementation* c*osts*: Developing a scraper was within our field of expertise, but we spent six months working on the technical setup. Overall, in the last six months, we had costs for internal staff (3 full-time employees and two student assistants), fees for servers, equipment, and data plans (~2,000€), conducting focus groups, pre-test a survey and running it on a representative sample of young adults (~ 40,000 €), as well as additional help developing personas and training 38 accounts (~35,000€).

*Replicability*: While any IT engineer can replicate the technical setup, the actual data collected is unique to the setting. We increased the replicability by following a research protocol during the training phase of the accounts and storing as much data as possible during the automated collection. We also had two researchers work on each user persona to measure inter-researcher reliability. A survey has the same timing issue regarding replicability, but as long as survey questions and details are documented, it can be repeatedly used by someone with an appropriate background.

*Representativeness*: We aimed for a representative survey of young adults. To achieve representativeness in scraping is more complex; we took measures to avoid biases in account training, but the overall number of accounts that researchers could train was limited. We focused on creating accounts within a specific age group (18-25) and location (Germany) and with a set of given interests.

**How can a scenario be effectively detected with this measurement?**

*Individual harm*: To understand the individual harms (" hidden costs" and "mental or physical health risks"), we conducted focus groups and asked young TikTok users to explain how they experienced these harms. From the examples and additional research, we derived a list of specific events (e.g., "ending up with debt after spending too much on TikTok Shopping" or "feeling down because of lifestyles presented on TikTok"). We included questions about those in our survey.

*Platform influence:* Attributing any harm to TikTok's For You feed recommender is difficult. People spend time with things other than TikTok. Therefore, their actions and feelings result from more than just TikTok consumption. Further, cause and effect are hard to distinguish. If someone feels down after using TikTok, this might have already been the case before using the app and, therefore, might influence the content they sought. Still, we think TikTok is not just a "tool" with no agency; it contributes by enabling or fostering certain behaviors and selecting what content to show. To better understand the role of TikTok, we relied on users' self-assessment in the survey. We designed our data collection study with comparable personas to be able to measure different effects.

*Macro effects*: Wider effects of the scenarios are often not observable within a few months. The methods we chose only partially allow us to measure macro effects, e.g., by assessing the extent of a problem through our representative user study.

## Scenario 3: Public Discourse and Search Suggestions

Scenario 3 is defined as folllows:

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience a distorted version of reality</span> <span class="rsba-scenario-platform">viewing the suggested search terms</span>, which <span class="rsba-scenario-macro">negatively impacts the public discourse.</span>

**How difficult will it be to execute this measurement?**

*Implementation* c*osts*: The costs for scraping and storing the suggested searches are negligible for the generic terms available through a hidden API. Getting comparable personalized search suggestions is more complicated and requires a simulation of users, similar to the approach chosen for studying the For You feed. Similarly, understanding the effects of search suggestions on actual users produces costs for a survey.

*Replicability*: Again, the problem with replicability lies in the fact that search suggestions change frequently and depend on whether or not personalization is activated. Therefore, a replication of our analysis at a later time will result in different search suggestions being provided by the platform. Still, the collected data can be made available to allow others to replicate the analysis.

*Representativeness*: We aimed for a representative survey of young adults in Germany and created accounts with similar demographics. We also decided to collect data on generic search suggestions in Germany and other European countries.

**How can a scenario be effectively detected with this measurement?**

*Individual harm*: Attributing the particular harm of experiencing a distorted version of reality is difficult, as we do not have the means to directly test the effects of a search suggestion that would imply something that did not happen. However, the search suggestions might affect users even when they did not click on them. We included a question in the survey to understand better to what extent participants remember search suggestions even if they did not click on them.

*Platform influence*: We need to determine the process TikTok uses to generate search suggestions and to what extent human oversight or explicit algorithmic design choices contribute to the suggestions. From our experiments, we hypothesized that while current trending topics drive some parts, other suggestions are personalized to recently viewed videos. To better understand this, we gathered personalized and non-personalized search suggestions.

*Macro effects*: Measuring the impact of search suggestions on the public discourse is out of the scope of the two measurements. However, we observed several instances where topics mentioned in search suggestions spilled into a public debate.

# User Survey

We developed the survey with [pollytix](https://pollytix.de/), an agency specializing in surveys and political marketing research. After framing observations from our exploration phase (Step 1) into questions, they conducted focus groups with 14 participants in November 2023 to assess whether our raised topics resonated with young users. This was part of the iterative process of [involving stakeholders](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/) and [developing scenarios](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/). We wanted to understand what risks young adults encounter and how those who grow up with the platform feel about the issues we have identified from a researcher's distance.

The survey was then qualitatively pre-tested and ran in December 2023. Overall, 1,634 young adults (18-25 years old) in Germany responded to the questionnaire, which took around 15 minutes to complete. Besides demographic questions, the survey 80covered the social media usage of participants with a focus on TikTok, evaluated how users perceive ads and shopping related to TikTok, and how they assess the influence of TikTok on their health and self-image.

# (Semi-)Automated Audit

We also wanted to collect personalized data from the platform to understand how the recommender system serves content and to gather data for a quantitative analysis regarding our scenarios. We discussed various approaches to collecting data, from data donation to fully automated accounts, but opted for a hybrid approach combining manual training of accounts based on personas and continued automated data collection on these accounts. In any case we only collected public data that is also available through the website.

## Manual Training

We developed 19 Personas that covered topics related to consumer protection and health (covering scenarios 1 and 2). We devided the personas between six researchers from SNV and AIF, with whom we collaborated, to create two accounts per persona by different researchers. This setup allowed us to limit potential researcher-related biases. The researchers created 38 accounts and trained them between 17 minutes and 4 and a half hours with a median (average) time 92 minutes. In terms of watched videos the median was 850 videos.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-03_manual_training_watchtime.svg"  class="img-fluid rounded" zoomable=true width="50%" %} 
        <div class="caption">Watchtime of 34 users for which this data was available</div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-03_manual_training_watchlist.svg" class="img-fluid rounded" zoomable=true width="50%" %} 
<div class="caption">Number of videos seen by accounts (n=38)</div>
    </div>
</div>

Researchers used a template with guidelines on how to use the accounts. They tried to find videos on specific topics and "train" TikTok's recommender system to show videos that the persona would find interesting. The guidelines were developed in multiple trial runs before the experiment started. While we focused on using the For You feed, researchers could use the search function to look for specific topics. During the RSBA, we learned that searching for a particular topic and watching several videos on that topic will be reflected on the For You feed - if not immediately, then after a short break and with a new session.

## Automated data collection

Once the researcher considered an account “trained”, which we defined as “staying on the predefined topic for 15 minutes”, the training ended. Afterward, the accounts were transferred to separate phones and a data export was triggered to preserve the list of videos viewed during the manual training phase. Then, the account usage continued - this time automated. For this phase, we set up an process that rates each video a “user” gets recommended and decides whether the account should continue watching the video based on what types of videos were watched in the training phase. The purpose was to keep the accounts in line with their training and continue to gather data on videos and ads.

<div class="row justify-content-sm-center"><div class="col-sm-12 mt-12 mt-md-12">
{% include video.html path="/assets/video/2024-03_TikTok-Automated.webm" %} 
<div class="caption">Video shows 4 ohones automatically swiping through TikTok</div>
</div></div>

For the automated data collection, the phones were set up to intercept the traffic between the TikTok app and servers and store relevant information like video and account metadata in a database.

To contextualize the video data, we separately collected data on:

- ads that were shown and the content the ads linked to
- authors/creators publishing videos, including the public links posted on their profile pages
- the first 25 comments on each video
- advertisements listed on library.tiktok.com
- suggested search terms for different sessions

The following graphic gives a high-level overview of the process.

{% include figure.html path="/assets/img/2024-03_data_collection_flow.svg" caption="Types of audits we have identified as potentially relevant for the RSBA" alt="List of audit types: Code audit, Crowd-sourced audit, Document audit, Architecture audit, Automated audit, User survey" class="img-fluid rounded" zoomable=true width="100%" %} 

As of today, we have collected metadata on roughly half a million videos from the app, 2 million comments, 20 Million ads from the ad library, information on 1000,000 creators, and followed the links in 4,000 ads.

We hope that combining the data from the user survey and semi-automated means can help us conduct an informed risk assessment of TikTok.

## Learnings

- Developing a survey and setting up the scraping costs time and resources. Each method has its set of (serious) limitations. It is, therefore, necessary to combine methods, but developing both in parallel is also challenging as they might have different implications and setup timelines.
- Automated data collection comes in different flavors, from easy (hidden API) to difficult (scraping on mobile).
- Unforeseeable and sudden platform changes make automated analysis challenging, it means that the data collection has to be adapted continuously and might result in a number of different formats that must be consolidated for the analysis.
- Although TikTok seemingly has endless engineering resources, some implementation is surprisingly low-key.
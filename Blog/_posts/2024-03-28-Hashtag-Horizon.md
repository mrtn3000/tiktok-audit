---
layout: post
title: "#️⃣ Hashtags Horizons: What we see and what not "
date: 2024-03-28 08:00:00
description: "An analysis of the prevalence of hashtags on TikTok"
tags: hashtags, analysis
categories: research
featured: true
related_posts: true
author: Greta Hess, Alexander Hohlfeld, Martin Degeling
---

*By [Greta Hess](https://www.stiftung-nv.de/de/person/greta-hess), [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling) and [Alexander Hohlfeld](https://www.stiftung-nv.de/en/person/alexander-hohlfeld)*

<div class="alert alert-secondary" role="alert">
  <h4>💡 TL;DR</h4>
 <ul>
 <li>Hashtags are not as prominent as perceived, with 28% of videos we've seen containing no hashtags.</li>
 <li>TikTok's recommendation system, while influenced by hashtags, also considers various other factors like time, region, and soundtrack.</li>
 <li>Despite assumptions about hashtag importance, their absence in a significant portion of videos suggests a need for more transparency in TikTok's algorithm.</b>
 <li>TikTok needs to provide additional means to researchers and users alike for content exploration and filtering, as reliance solely on hashtags may overlook substantial content within the platform.</li>
</li>
</ul>
</div>


With over 34 million videos uploaded on TikTok daily, the recommendation system is, at its core, a sorting mechanism that navigates the sheer amount of content and tailors it to individual users. As an integrated infrastructure within this system, hashtags influence this recommendation system while enabling users to search for specific labels, categorize media, connect cultures, and fuel trends on the platform.

For this reason, hashtags are often used in research and marketing to provide insights into platform logic and user behavior. [TikTok also provides an analytics tool](https://ads.tiktok.com/business/creativecenter/inspiration/popular/hashtag/pc/en), where very basic statistics of hashtag usage (f.e. related audience and top countries) can be seen. How these hashtags can be analyzed differs depending on the research objective and platform affordances. The Center for Countering Digital Hate (CCDH) has used the same tool in multiple studies, including [fact-checking TikToks own claims regarding the spread of Antisemitism on the platform](https://counterhate.com/blog/fact-checking-tiktoks-claims-on-antisemitism/). Weeks after the latest study, the CCDH drew attention to how TikTok has turned off a function allowing researchers to get insight on the total number of video views related to selected hashtags [(see more details here)](https://counterhate.com/research/tiktok-removes-views-from-hashtags/). In the analytics tool information is now limited to the most-viral hashtag. 

The importance of hashtags for the discovery of content for researchers is also highlighted by the fact that they are one of (the few) filters that can be used in the [research API](https://developers.tiktok.com/products/research-api/). Together with the option to search for keywords in the video description they are a critical entry point for the text-based search. 

# Are hashtags really that important?

From a reputational standpoint, hashtags are seen as a crucial parameter for driving the reach and popularity of video content. According to a 2021 study by [Klug et al.,](https://dl.acm.org/doi/10.1145/3447535.3462512) TikTok users assume that "hashtags are the main feature the algorithm picks up on to push videos to the trending section and a 'for you' page."

> "I don’t know if this is how the algorithm works or not
but it seems like the more hashtags you have the more TikTok puts
you on other people’s screens." (Klug et al., 2021)
> 

This quote explains why users often tend to pile up hashtags, no matter whether these are related to the video's content, or even try to increase their chances of becoming viral by adding hashtags like #foryou or #fyp, which target the features of TikTok directly. The same study also found that following the strategy of using popular hashtags ultimately does not increase the chances of a video being recommended. 

Our analysis supports this insight as we found only a very small correlation between play counts and hashtag amounts. For example, [this cute cat video](https://www.tiktok.com/@titi20252025/video/7317651211962879265) lists a total of 223 hashtags (including duplicates) and has more than 1.5 million views, [this video on weightloss pills](https://www.tiktok.com/@mumshealth0/video/7315547844763520288) makes use of 218 unique hashtags but received only a few hundred views.

This does, of course, not mean that hashtags do not influence TikTok's For You Feed. TikTok itself claims that hashtags are a crucial feature for content recommendation on the For You Feed and actively advertise the usage hashtags such as in their ["trend discovery"](https://ads.tiktok.com/business/creativecenter/inspiration/popular/hashtag/).

Acknowledging the importance of hashtags for users as well as researchers to explore content on TikTok we explored our data set to understand the actual relevance of hashtags within the platform.

# 28% of videos have no hashtags

We first looked at hashtags' overall presence in our video [data set](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step3/). Our analysis showed that in the time from 01/12/23 - to 31/01/24, around **28%** of the **244,255** videos **did not contain any hashtags**. TikTok hashtags are part of the description of videos, but the absence of hashtags does not necessarily mean that videos lack any textual description.

{% include plotly.html data="/assets/plotly/2024-03_hashtags_chart.js" id="57791e31-70e6-4c5c-a251-1814182cfed3" caption="Percentage of videos without hashtags and/or description in our set of 244,255 videos." %} 

As we explored the presence of hashtags in our database, we noticed that it’s often not just hashtags that are missing. We found that **10.9%** of all videos in the data set do not have any description whatsoever, while still being recommended to users. 

Here are two examples:

- This [video](https://www.tiktok.com/@melyclain/video/7316134458426477857) from an account that has only posted 9 videos overall barely uses textual descriptions and still received 1.5M views on one of them.
- A [video](https://www.tiktok.com/@thebrainkash/video/7317355134231629089) was posted by an account that has zero followers (because they are intentionally deleted by the creator) and, on average, has only a few hundred views per video managed to gather more than 135.000 views on this one without providing any description.

## **User-based Analysis: Share of videos with hashtags**

To better understand the experience of individual users with hashtags on the platform we hypothesized that hashtags might become less relevant the more data the recommender system has about a user's behavior. We did so by analyzing the watch history of the accounts we had created. By looking at the individual user experience, we can learn more about the personalizing behavior of the recommendation system. 

We first looked at each user's watch history to assess the overall share of videos with at least one hashtag. We know this as the data structure of our gathered data lists hashtags separately from the content description. TikTok further indicates the existence of any hashtags in a separate field called 'isHashtag'.

{% include plotly.html data="/assets/plotly/2024-03_hashtag_percentage_user.js" id="fffebea9-b9e8-4d22-85ab-fd0c6cbab18e" caption="Boxplot of the distribution of hashtag prevelance over all users" width="50%" %}

Our analysis showed that throughout the watch history of all accounts hashtags the prevelance of hashtags was always between 66% and 90% with a median (average) of 81%.

## Does hashtag relevance decrease over time?

During our training session, we experienced that as we spent more time on the app, content became less “viral”, such as videos with low view counts without any description or hashtags. 

Our hypothesis was that **the number of hashtags will decrease with increasing watch time.**

We, therefore, decided to look into how the prevalence of videos with hashtags changed over time by analysing the data [from our study](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step3/) where researchers engaged with the TikTok algorithm through our user accounts at different times. In order to account for these different sessions, we decided to split up the scraped watch history of our different users accordingly. Each session is characterized by the consecutive time spent on the application. Technically this means that we sorted the videos by timestamps and ended the sorting once two consecutive videos were watched with over 30 min apart. Within these sessions we then formed batches of 20 videos and calculated the average hashtag use within each batch. This was conducted for each user individually, giving insights into their distinct user journey. The plot below shows a regression line for each user derived from the percentage of hashtags throughout all different sessions.

{% include plotly.html data="/assets/plotly/2024-03_hashtag_exposure.js" id="8f8c5e6d-2035-4a08-9d48-51766407798f" caption="Hashtag prevelance within user sessions over time" %}

As illustrated in the Figure above, some users are initially exposed to up to 45% of videos without hashtags in individual sessions. However, the overall hypothesis does not hold up, and users do not necessarily see fewer hashtags the more time they spend on the platform. There are users for whom the number increases as well as those for whom it decreases. The average converges around 70 to 80%, and the percentage of videos with hashtag does not fall below 60%.

# Fewer hashtags = less transparency and control

While hashtags are not as omnipresent as often thought and therefore might not be as relevant to the recommender system, they are still important on other levels. They play a crucial role in content navigation for both users and researchers exploring certain topics. However, the absence of textual descriptions can make it challenging for users to understand why they're recommended a certain video or to search for related content. This limitation also restricts user agency, as TikTok's tool for managing their [For You Feed](https://support.tiktok.com/en/using-tiktok/exploring-videos/how-tiktok-recommends-content), e.g. to block certain content, heavily depends on filtering videos using keywords or hashtags.

Tiktok also provides users the option to give feedback on specific recommendations, which could be practical in the case of a video without any text description. Nonetheless, it remains unclear how this information is used in practice or how TikTok is classifying videos without descriptions accordingly. Recent research by the [Panoptykon Foundation](https://en.panoptykon.org/algorithms-of-trauma-2-anxious-about-health) or [Mozilla Foundation](https://foundation.mozilla.org/en/blog/mozilla-investigation-youtubes-dislike-button-other-user-controls-largely-fail-to-stop-unwanted-recommendations/) has highlighted that such user agency mechanisms often pretend to have an influence that they actually do not have in practice and are thus highly misleading. 

For researchers the lack of hashtags and descriptions on videos means that they need to find other ways to explore topics and find related videos, e.g. by looking at other videos posted by the same creator, the use of the same sound or by features like [stitches](https://support.tiktok.com/en/using-tiktok/creating-videos/stitch) and [duets](https://support.tiktok.com/en/using-tiktok/creating-videos/duets) that relate videos to another. At it’s current state the [research api](https://developers.tiktok.com/doc/about-research-api/) TikTok offers is not equipped for this. It is focused on exploring videos by keywords (in the description) and hashtags or by exploring the network between users through following and commenting. Additional meta data like overlay text shown in videos, relations through stitches or duets, or content classification as it is offered on the [explore](https://www.tiktok.com/explore) page are be necessary to explore content beyond it’s textual descriptions.

If TikTok does not offer users and researcher more meaningful ways to filter and search, harmful content without any description and hashtags can then bypass filters, making it challenging to grasp the entirety of the digital space and content comprehensively.

## What about the DSA?

Article 27 of the DSA on “Recommender System Transparency” states that:

> 1. Providers of online platforms that use recommender systems shall set out in their terms and conditions, in plain and intelligible language, the main parameters used in their recommender systems, as well as any options for the recipients of the service to modify or influence those main parameters.
> 
> 2. The main parameters referred to in paragraph 1 shall explain why certain information is suggested to the recipient of the service. They shall include, at least:
> 
> (a) the criteria which are most significant in determining the information suggested to the recipient of the service;
> 
> (b) the reasons for the relative importance of those parameters.
> 

The DSA mandates transparency in how online platforms utilize recommender systems, insisting that the main parameters guiding these systems be clearly outlined in terms users can easily understand. Specifically, it requires an explanation of the criteria most significant in determining suggested content, alongside the rationale for the importance of these parameters. 

TikTok provides such a [list of factors](https://www.tiktok.com/transparency/en-us/recommendation-system/), which includes hashtags, but it does not provide the relative importance of those parameters.

Given the gap between perceived importance of hashtags by creators and their widespread absence in our data set, we would argue that TikTok's claim about the importance of hashtags potentially obscures the actual mechanics of content recommendation.

# Summary

TikTok personalizes the For You Feed based on various factors to [predict the likelihood that a user engages with the recommended piece of content](https://github.com/snv-berlin/tiktok-audit/blob/main/TikTok%20Algo%20101%20EN.md). While TikTok mentions that the algorithm takes into account various signals such as the time, the region, the soundtrack, or the hashtags of the video, the latter is often assumed to be more relevant. We have shown that for regular users, 28% of videos are not labeled with hashtags and 11% lack any textual description. Therefore, we think the platform needs to provide more information to users as well as researchers, including:

We think the platform should provide more information to users as well as researchers, including

- The relative importance of the parameters as well as the reasons behind such a weighting as described in Art. 27 of the DSA.
- Researchers studying TikTok should be able to access (e.g. through the API) additional meta or textual data like the text used within videos and the content classification performed by TikTok.
- To be able to explore videos on certain topics, the API should provide recommendations, e.g. “similar” videos that the algorithm would also recommend to users.
- Control mechanisms for users should be expanded beyond text-based filters.

In conclusion, we can say that hashtags and content descriptions are important, but less prevelant than one might think. With this post, we want to highlight that those relying on hashtags to draw conclusions about the prevalence of certain content might miss a significant part of the ecosystem in their analysis.
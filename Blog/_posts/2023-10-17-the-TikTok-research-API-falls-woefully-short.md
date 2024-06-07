---
layout: post
title: "🤦‍♀️ The Research API falls woefully short"
date: 2023-10-16 10:00:00
description: We look into the Research API and its shortcomings.
tags: analysis
categories: research API
featured: false
related_posts: true
---
*By: [Santiago Sordo Ruz](https://www.stiftung-nv.de/en/person/santiago-sordo-ruz), [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling) and [Kathy Meßmer](https://www.stiftung-nv.de/en/person/dr-anna-katharina-messmer)

TikTok's reach is measured in the billions. According to different [sources](https://www.usesignhouse.com/blog/tiktok-stats), in 2022 it had 1.7 billion users, 1 billion daily views and 1.12 billion monthly active users. This is why we need a systematic way of accessing data about the platform to conduct thorough research about it - may it be for exploring the platform's affordances or conducting a full-blown audit. 

One way TikTok provides access to some of its data is the Research API. It makes getting some insights into the platform's inner workings possible, but it is far from satisfactory. Especially because the provided data is very limited compared to which data is publicly available via scraping. So, let’s have a closer look at that.

<div class="row justify-content-sm-center"><div class="col-sm-8 mt-4 mt-md-0">
{% include figure.html path="/assets/img/2023-10_tt-apis.png" class="img-fluid rounded z-depth-1" zoomable=true %} 
</div></div>
*Image: The number of variables available on TikTok through different means of data acccess.*

## TikTok's Research API

TikTok offers an application programming interface (API) where vetted academic researchers can obtain information about the content published by TikTok’s users. An API is —in short— a way to request and obtain information from a system. [TikTok's Research API](https://developers.tiktok.com/products/research-api/) provides access to what is essentially a carefully curated database of the videos the platform hosts.

The API provides data and metadata about comments, users and videos. The number of variables available for each of these categories is as follows:

| Object | Variables |
| --- | --- |
| Comments | 6 |
| Users | 8 |
| Videos | 9 |

These variables contain information about different aspects of the objects in question. For example, this is what is available in the case of comments:

1. **Create Time:** This is the time when the comment was posted on a video.
2. **ID:** This is the unique comment ID for a comment posted on a video.
3. **Like Count:** The total number of likes for a comment under a video created by users by clicking the “Heart” icon.
4. **Parent Comment ID:** This is the unique ID of the parent comment when the user responds to another user's comment. If the comment was directly entered for a video, this ID is the same as the Video ID.
5. **Text:** This is the actual text of the comment entered on a video. To protect the privacy of users, other information is removed.
6. **Video_ID:** This is the video ID for which the comment was entered.

The API's [official](https://developers.tiktok.com/doc/research-api-codebook) codebook provides a detailed description of all available variables. While these may shed light on *some* research questions, especially related to the analysis of content posted on the platform, they are extremely limited in number and scope.

## Getting more useful data is hard

Since civil society organisations like the SNV can’t use the Research API, we decided to explore the platform on our own. We have done this using what is known as content *scraping*, which is the automated collection of data from online sources. We have collected data from two of TikTok’s clients: the Android app and the web app. 

Scraping data from the web is quite common and poses a relatively low technical barrier. However, scraping data from a smartphone app such as TikTok's Android client is quite challenging; we speak from experience. At the same time, scraping TikTok content from the Android app has proven invaluable. Its smartphone apps are the most natural way to use the platform —providing data closer to what users actually encounter— and **the amount and variety of the information we have collected is incomparable to what is available through the Research API.**

## The Research API falls woefully short

Scraping TikTok directly from the source has allowed us to collect information on various platform aspects. We have gained more and better perspectives on comments, users and videos, and also into officially undocumented features like the app's automated search suggestions. 

To illustrate this, let's have a look at the data and compare the number of variables on which we have collected information through scraping with those offered by the Research API:

| Source | Variables | Date collected |
| --- | --- | --- |
| [Research API](https://github.com/snv-berlin/tiktok-audit/blob/main/Data%20Access/tiktok_researchapi_annotated_metadata_list.csv) | 32 | July 6, 2023 |
| [Web](https://github.com/snv-berlin/tiktok-audit/blob/main/Data%20Access/tiktok_web_annotated_metadata_list.csv) | 186 | July 6, 2023 |
| [Android App](https://github.com/snv-berlin/tiktok-audit/blob/main/Data%20Access/tiktok_app_annotated_metadata_list.csv) | 845 | July 6, 2023 |

You can have a look at each source's codebook by clicking on the links in the table; note the trove of insights that scraping affords. Note as well that our codebooks are —and will remain— works in progress.

**As you can see, the Research API falls woefully short.** Furthermore, keep in mind that documenting scraped data constitutes a technical challenge, meaning these numbers are conservative estimates.

## Why this matters

[According to the company](https://developers.tiktok.com/products/research-api/), the Research API serves the following purpose:

> TikTok supports independent research about our platform. Through our Research API, academic researchers from non-profit universities in the U.S. and Europe can apply to study public data about TikTok content and accounts.
> 

Put into perspective, what TikTok offers is such a weak attempt at supporting independent research that one has to ask whether the company is simply [claiming credit without doing the work](https://www.gmfus.org/news/ai-audit-washing-and-accountability). To make things worse, as mentioned above, access is so restricted that our very own researchers at Stiftung Neue Verantwortung do not qualify for the API. Put simply, if we want to be able to scrutinise a platform like TikTok and thus assess the potential harms and impacts that its widespread usage entails, the Research API is grossly inadequate as a window into it.

Ultimately, with some technical expertise, much more data is already publicly available and accessible anyway. It shouldn't take an in-house computer scientist with a PhD to obtain valuable insights into a social media platform billions of people use. While it is reasonable for the platform to want to keep its inner workings secret, its potential impacts warrant profoundly wider and deeper access to the data generated by its users and about its users. That’s why the data we have obtained should not remain hidden behind a formidable technical wall. On the contrary, it should be made readily available to researchers, including those working within civil society organisations. 

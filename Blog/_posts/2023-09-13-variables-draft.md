---
layout: post
title: The research APIs is not enough (draft)
date: 2023-09-13 15:09:00
description: 
tags:
categories: 
featured: true
---
**Introduction**

TikTok´s reach is to be measured in the billions. According to different [sources](https://www.usesignhouse.com/blog/tiktok-stats), in 2022 it had 1.7 billion users, 1 billion daily views and 1.12 billion monthly active users. These numbers reveal the sheer scale of this platform but also the potential impact it can have on its users, including the risk of harm. This is why it doesn't matter if you are exploring the platform's affordances or conducting a full-blown audit, you need a systematic way of accessing data about the plafform in order to conduct any thorough research about it.

Wether in response to stakeholder pressure, legal requirements or even voluntarily, some platforms provide systematic acces to data. In the case of TikTok, this is offered through their *research API*. In [the company's own words](https://developers.tiktok.com/products/research-api/):

>*TikTok supports independent research about our platform. Through our Research API, academic researchers from non-profit universities in the U.S. And Europe can apply to study public data about TikTok content and accounts.*

But what exactly is TikTok offering? 

**TikTok's research API**

TikTok offers an application programming interface (API) where vetted users can obtain information about the content published by its users. An API is -in short- a way to request and obtain information from a system. TikTok's research API allows us to access what is essentially a database curated by the company containing information about its content.

TikTok's research API provides data and metadata about comments, users and videos. The number of variables available for each of these categories is as follows:

<!--<div align="center">-->
|Object|Variables| 
|:-:|:-:|:-:|
| Comments | 6 | 
| Users | 8 |
| Videos | 9 |
<!--</div>-->

These variables contain information about different aspects of the objects in question. For example, this is what is available in the case of comments:
>
1. **Create Time:** This is the time when the comment was posted on a video.
2. **ID:** This is the unique comment ID for a comment posted on a video.
3. **Like Count:** The total number of likes for a comment under a video, created by users by clicking the “Heart” icon.
4. **Parent Comment ID:** This is the unique ID of the parent comment when the user responds to another user's comment. If the comment was directly entered for a video, this ID is the same as the Video ID.
5. **Text:** This is the actual text of the comment entered on a video. To protect the privacy of our users, other information is removed.
6. **Video_ID:** This is the video ID for which the comment was entered.

A detailed description of all available variables can be found in the API's [official codebook](https://developers.tiktok.com/doc/research-api-codebook).

While these variables may shed light into some research questions, especially given the fact that we have the platform's official descriptions for what they contain, they are extremely limited in number and scope. 

**Getting more and more useful data**

We have collected data from two of the platform's : its Android and web apps.


**Documenting your data**

So you've set up some scrapers to gather data from the platform and are now swimming in it. But what exactly are you collecting? One of the few advantages of the research API is that you have the database's codebook, which means you know exactly what every variable is supposed to contain.

There is simply no way around this and it is a manual, artisanal and -if you are doing a good- a lenthy process. However, there are ways of producing at least a skeleton in an automated way. If you are interested in learning how, we've put together a Python notebook, where we explore a strategy to create a codebook template to make the process of documenting your data easier. 

**To be continued...**
Questions unanswered: to whom it is offering it

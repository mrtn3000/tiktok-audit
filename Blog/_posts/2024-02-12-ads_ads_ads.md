---
layout: post
title: "🛒 Ads, Ads, Ads"
date: 2024-02-12 10:00:00
description: How the for you feed is clogged with ads.
tags: ads, marketing, fyp
categories: ad-library
featured: false
related_posts: true
author: Anna Semenova, Martin Degeling and Kathy Meßmer
---

*By [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova), [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling) and [Kathy Meßmer](https://www.stiftung-nv.de/en/person/dr-anna-katharina-messmer).*

Like other social media platforms, TikTok relies heavily on advertisements to sustain its operations. Marketing experts assessed that advertisers spent more than 3.8 billion US Dollar on TikTok in 2021, and [forecasts expect these numbers to rise to 23 Billion in 2024](https://www.insiderintelligence.com/content/tiktok-surpasses-snapchat-favorite-app-of-teens). The reasons for TikTok's success are its young user base and the fact that advertising on the platform is as easy as posting a video. At the same time, many marketing techniques are available, including targeting users based on socio-demographic categories and interests.

As part of our [Risk Scenario-Based Audit](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/) (RSBA) of TikTok, we have looked into TikTok's advertising ecosystem. We discovered that up to one in three videos a user sees in their “For You”-feed contains paid advertising or direct brand mention. We also found that TikTok removes approximately 2.5% of the ads for violating their guidelines. Still, these removals are intransparent and can happen after thousands of users have already seen the ad.

Advertisers on TikTok have a [plethora of options](https://insense.pro/blog/tiktok-ads) to get their message on the users’ display. The most common ones are “in-feed ads”, which are the main topic of this post. These video ads are seamlessly integrated into TikTok’s main feature, the video feed, allowing users to engage with them as they scroll through the "For You Page."

TikTok's advertising system leads to several challenges in consumer and youth protection. A report by the [European Consumer Organisation (BEUC)](https://www.beuc.eu/sites/default/files/publications/beuc-x-2021-012_tiktok_without_filters.pdf) highlights instances where undisclosed or unlabeled content blurs the line between genuine engagement and commercial promotion. Moreover, we have previously shown that TikTok [fails to implement its own guidelines on political advertising](https://tiktok-audit.com/blog/2023/We-found-100-political-ads-on-TikTok-Germany/) correctly, even within labeled ads.

<style>
    video{max-height:500px}
</style>
<div class="row justify-content-sm-center"><div class="col-sm-6 mt-6 mt-md-6">
{% include video.html path="/assets/video/2024-02_TikTok-AdCount.webm" class="img-fluid rounded z-depth-1" zoomable=true width="50%" %} 
</div></div>

## Definitions

To facilitate our analysis, we classify TikTok advertising into two categories:

1. **Paid promotion:** Content published and paid for, e.g., by a brand or company, via official TikTok advertising tools. It is discernible as an advertisement on TikTok. Paid content is also where TikTok takes its share. Paid content can appear in the For You feed as well as on other features like search results.
2. **"Organic"/Influencer marketing**: Content that targets an audience through the viral effects of the platform rather than relying on paid promotion. This marketing approach is closely linked with influencer marketing, wherein users receive compensation to promote a product or service, leveraging the authenticity of these influencers for the benefit of the brand. When publishing their content, creators are asked to disclose if the video promotes something. If they choose to disclose this, the video will also be labeled as “Anzeige” (“Paid Partnership” in English). 
    1. *Cooperation:* Influencers with large audiences often rely on agencies to manage brand partnerships. However, TikTok also provides its [“Creator Marketplace”](https://creatormarketplace.tiktok.com/) (a service for which it takes a share) to facilitate cooperation. Creators can label these videos as ads during the publishing process and may include “Ad” in the video description.
    2. *Self-Marketing:* Users can also advertise their own products or services. TikTok is known for being a place where [products go viral](https://www.nytimes.com/2021/10/02/style/tiktok-shopping-viral-products.html), and people try their luck with dropshipping online shops or affiliate marketing. When advertising their products, they are also asked to disclose this advertisement to be labeled as ads.
    3. *Unpaid Consumer to Consumer Marketing***:** The last category of "organic" marketing involves consumers advertising products to other consumers. Often, these videos are variations of the Haul, in which users disclose product details, prices, and sources without receiving payment from the brands they review.

The boundaries between different types of advertising are blurry. For instance, a video that has been created through cooperation between an influencer and a brand may also be promoted via paid promotion to reach a larger audience (with the hope of “going viral” after the initial forced push). Additionally, as we have described in the case of [Temu](https://www.notion.so/2024-01-10-Shop-Till-You-Drop-How-Temu-s-exploitation-of-TikTok-affordances-creates-an-abyss-of--2243d97825cc423fae6aa350e30b2fe9?pvs=21), companies try to nudge users into creating videos that end up being unpaid consumer to consumer marketing when users are offered a discount on their *next* purchase.

{% include figure.html path="/assets/img/2024-02_tt_ad_label_example.png" caption="Example of an advertising label on TikTok in Germany. 'Anzeige' is German for 'Advertising'. On the English app version, the videos are labeled as 'Sponsored.'" class="img-fluid rounded z-depth-1" zoomable=true width="100%" %} 

Formally, only the first one (”paid promotion”) falls under the definition of advertisement according to the Digital Services Act (DSA): “*‘advertisement’ means information designed to promote the message of a legal or natural person, irrespective of whether to achieve commercial or non-commercial purposes and presented by an online platform on its online interface against remuneration specifically for promoting that information*” (DSA, Art. 3 (r)). Thus, TikTok as a platform has to be involved in the monetary flow.

Moreover, this type of advertising should be accessible on the TikTok [Ad Library](https://library.tiktok.com/), a repository mandated by the DSA for very large online platforms platforms. The DSA specifies that VLOPs must ensure public access to repositories of advertisements presented on their online interfaces, facilitating supervision and research into emerging risks associated with online advertising (Recital 95).

## Methodology

For our analysis, we concentrated on the in-feed ads, particularly emphasizing paid promotions. To gather quantitative data for a more comprehensive analysis, we conducted a (semi-)automated audit of 39 accounts based on different personas (for which we had defined, e.g., age, gender and interests like “fashion” or “finance”). After we had manually trained these accounts and collected the training data, they were automated to continue the data collection. The automated data collection involved swiping through the For You feed for about 20 minutes a day while intercepting network traffic and storing metadata on videos, comments, ads, and more. In the coming weeks, we will publish a more in-depth description of our methodology. All tests were conducted using IP addresses implying that the user resides in Germany.

## Every fifth video in the For You feed is paid promotion

Our dataset sheds light on a significant prevalence of advertisements on TikTok. Of the 94,854 videos in our database (as of Jan 27th, 2024), 14,523, or 15.3%, were shown as paid promotions in our users’ feeds. However, this is just a comparison at the level of unique videos. While regular videos are mostly shown once, ads can target multiple users in a target group multiple times. For example, this [ad for Disney+](https://library.tiktok.com/ads/detail/?ad_id=1784736476404737) was shown to 9 million users in Germany. In our sample, the ad appeared on 13 of 39 accounts and 5 accounts even saw it twice. At the same time, only a handful of non-ad videos came across the For You feeds of different accounts in our sample. 

The plot below shows the share of ads per day during our automated data collection phase. Looking at the total share of ads per user, the average in January was around 19.9% - that is 1 in 5 videos.

{% include plotly.html data="/assets/plotly/2024-02_ad_share.js" id="9971be77-cf72-4de2-a3d7-fd10bbb72ad1" caption="Each line represents a user from our training sample. The share of ads is characterized by variability, with noticeable fluctuations for individual users from one day to the next. The black dashed line represents the average per day." %} 

Importantly, this figure exclusively pertains to the count of paid promotion content. However, learning more about the "organic" marketing part of the platform is much more complicated. As explained above, creators are asked when uploading videos whether the content is advertising something. But only 0.8% of videos in our dataset were labeled as “Promotional Content” or “Paid Partnership” by the creators. If you have ever used TikTok, you might have noticed that this is a surprisingly low number in itself. But interestingly enough, that also means that even videos that are uploaded for paid promotion via TikTok are not labeled as “Promotional Content” by the uploading creators.

For us, as third-party auditors, researching TikTok from the outside, it is hard to tell if a video creator received money from a company. We found a small number of 179 videos, which is 0.1% of our sample, that used a specific hashtag like #ad (or #anzeige in German) or clearly named the fact of being paid in the description of the video, while at the same time, they were not visibly labeled as “paid partnership”.

## Some brands rely on unpaid advertisements on TikTok

However, "organic" marketing drives the ad ratio higher than 20%. To give you an example: We trained four accounts on fashion interests. Of the 8964 videos those four accounts saw, 11% mentioned specific brands. The short list of fashion brands we noticed included Action, Primark, Shein, Sheglam, Temu and Zara. Of those, all but Zara completely rely on "organic" unpaid advertisements. Only [Zara](https://library.tiktok.com/ads?region=DE&start_time=1701385200000&end_time=1706569200000&adv_name=ZARA%20ESPA%C3%91A%20SA&adv_biz_ids=6952877848373756673&query_type=2&sort_type=last_shown_date,desc) can easily be found in the ad library, with a handful of ads during the test period. We recently highlighted the problems with this form of advertising using the example of [Temu](https://tiktok-audit.com/blog/2024/temu-tiktok/).

**Combined with the paid promotions, for the accounts trained in fashion, roughly one of three videos is an ad.** 

This analysis has some significant limitations as it is based on hashtags, which were only available for around 70% of the videos in this dataset.

## Most paid promotion ads target small audiences

{% include plotly.html data="/assets/plotly/2024-02_ad_cummulative.js" id="ceba7163-8f49-4dcc-9e4f-c44ef053c008" caption="The chart illustrates the cumulative distribution of advertisements based on the share of users they are exposed to. The x-axis, 'Share of Users,' indicates the proportion of users to whom an ad is shown, while the y-axis, 'Cumulative Frequency (%),' represents the cumulative percentage of ads falling within or below each share-of-users category." %} 

The chart above shows that a significant portion of videos, accounting for over 60% of all ads, is exclusively shown to a single user within our group of test accounts. Approximately 80% of ads are presented to a maximum of two users, implying that **only around 20% of ads extend their reach to more than two users in our test group**. The distribution shows that the Disney+ ad mentioned above is an outlier. This is likely an effect of limited ad spending on the majority of campaigns that limit their reach to a small audience. This leads to a high number of ads, but a limited number of ad campaigns reaching a large audience on TikTok.

# Insights from the ad library

TikTok's [ad library](https://library.tiktok.com/) should give simple access and allow the exploration of ads. The repository provides insights into the general statistics on “paid promotion” ads. For example, during our data analysis period, which spanned from November 28, 2023, to January 27, 2024, **1,861,925 ads targeting Germany were recorded in the repository**.

## 1.8 million ads in the last two months

However, besides these general statistics, the ad library could be more usable as the search is more or less dysfunctional, and it is often impossible to find information about an ad you saw in your feed.

Therefore, we developed our own means of access to be able to match the paid content shown to our sock puppets with the ads in the library. We found that over 1.8 million ads targeted users in Germany over the last two months; on average, each ad campaign had a duration of just 2 days, calculated as the difference between the first and last display date. During that time, the typical ad garnered around 1000 impressions, as indicated by the median value. This means that more than half of the ads received 1000 impressions or fewer; see figure below.

{% include plotly.html data="/assets/plotly/2024-02_ad_impressions.js" id="f3eb34b3-2692-41cf-ae05-cc856ec5a81b" caption="The plot shows the number of <b>published</b> (upper chart) <b>removed</b> (lower chart) ads listed by the number of impressions in Germany confirming the outlier position of the Disney+ ad, which falls in the highest category of 10-20 million impressions." %} 

## Removing ads is slow and usually happens after ads have reached their audience

While the ad library has some volatility, making it hard to get exact numbers, we found 50,279 (2.7%) ads being removed in Germany during our two month test period, citing reasons such as the expiration of authorization or violations of the terms of service. Interestingly, the average campaign duration of removed ads was also two days, meaning those ads still reached their audience before removal. 129 ads even reached more than 1 million users before they were removed. **Unfortunately, TikTok deletes any identifying information from ads when they are removed from the ad library**, so it is impossible to know what these ads had shown.

However, even if an ad is removed, the video can still be available on TikTok as non-ad content - it is just not promoted as ad anymore. In our dataset, we caught 20 ads that were removed after they had been viewed by our accounts, and since the videos were still available, we were able to review which ads were deleted. Here are a two examples:

- [This entirely AI-generated video](https://www.tiktok.com/@FocusUp/video/7325217813247921409) promoting Ashwagandha tea is still online as content but was [removed](https://library.tiktok.com/ads/detail/?ad_id=1788382923589681) as ad after running for five days and being shown to 3000 users. TikTok gives the following reasons for removing it as an ad: "The product/service promoted on the ad/landing page belongs to a prohibited industry of the targeted location(s)[…]"
- This [ad](https://www.tiktok.com/@credimaxx/video/7252671337053850885), removed for making an "exaggerated financial claim" (it says that "even with a negative credit rating you would have *an excellent chance* to get a credit between 500 and 35.000€), was [had 281.000 impressions](https://library.tiktok.com/ads/detail/?ad_id=1770675512982530) over six(!) months before it was removed as an ad.

Finding these examples took effort, and TikTok is not making it easy to understand which ads are removed and why. The ad library is mostly a transparency theatre, and we'll publish more on that in one of the next posts.

## Limitations

As noted above, our methodology has some limitations: 

- We gathered data on the For You feed in Germany and for specific personas. This does not reflect the general audience. Therefore, we additionally collected data in a user survey that we will publish later. We also cross checked our data with other sources, and our observation of roughly 20% paid promotional content was confirmed in this [reddit thread](https://www.reddit.com/r/tiktokgossip/comments/14cyhqz/im_seriously_getting_an_ad_every_4_vids_on_tiktok/).
- There was an issue with our data collection over the Christmas holidays, making it impossible to assign videos watched to the persona between the end of manual training and December 27th. This affected 22 accounts. We, therefore, limited the analysis relying on the persona to data collected after December 27th.
- As mentioned above, finding ads in the “grey area” where the creator is seeking financial gain from reviewing or showcasing a product is difficult. We, therefore, chose very specific criteria (using the hashtag #ad or #anzeige or mentioning the brand) to get a lower bound for this type of consumer-to-consumer marketing. Future research should try to narrow down features to identify this type of marketing, similar to TikTok trying to leverage this by [automatically identifying products and advertising their own shop](https://gizmodo.com/tiktok-testing-users-will-put-up-every-video-being-ad-1851207082).
- We also noted that the ad library is rather volatile and changes are made after ads have been published. We continuously scraped the library from November 2023 on for new ads published at least 48 hours ago, but also going back to September 2023. We only checked again for ads we encountered with our automated accounts to fill gaps in our dataset; we do not have a complete mirror of it.

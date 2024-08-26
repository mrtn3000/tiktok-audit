---
layout: post
title: "📰 Understanding TikTok's For You Feed"
date: 2024-08-26 10:00:00
description: "An analysis of the user journey"
tags: analysis, step4, FYP,
categories: research, rsba
featured: true
related_posts: true
author: Anna Semenova, Martin Degeling, Greta Hess
---

*By [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova), [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling), [Greta Hess](https://www.stiftung-nv.de/de/person/greta-hess).*


{% include figure.html path="/assets/img/2024-08_interest_overview.png" class="img-fluid rounded z-depth-1" zoomable=true %}


TikTok is full of videos that try to sell something. In a survey young users in Germany report that up to 50% of the videos they see in their For You feed have a commercial interest. As part of our risk assessment on consumer protection we set out to verify this number with automated accounts. On the way we also learned something about the personalization in the For You feed.

This blog post continues our series of detailed examinations of findings from scenario testing, as outlined in our post ["TikTok's Impact on Consumer Rights: A Closer Look!"](https://www.tiktok-audit.com/blog/2024/Consumer-Protection-on-TikTok/) Each post focuses on one step of the theoretical framework for risk assessments, developed in our risk-scenario-based audit process (RSBA). For our methodological reflections, see our posts on the [methodology](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/).

Here, we'll examine the aspect of platform involvement as outlined in the RSBA, focusing on TikTok's For You feed and its advertising content. We've chosen this focus because the For You feed is the primary way users encounter content on the platform.

In summary we find:

- **Personalization**: The For You feed becomes increasingly personalized over time, with up to 80% of videos matching predefined user interests after about an hour of scrolling. In the other side the highest amount of shared videos among users occurs within the first 15 minutes of using the app, decreasing later as content becomes more personalized.
- **Commercial Content:** On average, 21% of videos in users' watchlists were from accounts indicating commercial interest, without being labeled as official ads. This is in addition to the 20% of videos that are official ads, that we have [previously measured](https://tiktok-audit.com/blog/2024/ads_ads_ads/).
- **User Perception:** In our survey, users estimated that every second post on TikTok is an advertisement or product recommendation, closely matching our findings on the prevelance of commercial content.

These findings highlight the complex interplay between personalization, advertising, and user experience on TikTok's For You feed, raising important questions about transparency and consumer protection.

## Platform Involvement: For You Feed

Understanding a platform’s technical and organizational structure is crucial in an audit process because it allows auditors to pinpoint specific elements that contribute to systemic risks posed by the recommender system. In [our scenario,](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step2/) we hypothesized that TikTok's strategy to maximize user engagement through its "For You" feed may expose its younger audience to harmful content. By examining factors like user experience, interface design, algorithmic logic, and moderation practices, auditors can effectively evaluate and mitigate these risks.

The For You feed is the most important feature of TikTok, and the recommender system behind it - designed to capture attention by tailoring content to individual interests - is often described as TikTok’s “[secret sauce](https://www.eugenewei.com/blog/2020/8/3/tiktok-and-the-sorting-hat)”. This blog begins by exploring user journeys and how TikTok’s algorithm personalizes the For You feed.

In this personalized environment, TikTok also introduces various forms of commercial content, including in-feed ads, branded hashtag challenges, live streams, and many more. The [variety of ad formats](https://tiktok-audit.com/blog/2024/ads_ads_ads/) blurs the line between organic and paid content, complicating the platform’s involvement and making it difficult to assess their full impact on users.

The variety of advertising formats enhances user engagement by integrating ads into the user experience in a way that feels less intrusive. This approach keeps users interacting with the content longer, as they’re less likely to recognize or skip ads that are seamlessly woven into their feed. Many forms of promotional content fall into a "grey zone," where they are not clearly labeled as ads but are nonetheless driven by commercial interests. We have already [written](https://tiktok-audit.com/blog/2024/ads_ads_ads/) extensively on the various types of advertisements on TikTok, focusing primarily on paid promotions. This blog extends that analysis by highlighting the complexities of grey zone advertising.

With our research we aimed to understand how TikTok’s For You feed operates and how it helps drive grey zone advertising. Unlike user-initiated actions (like viewing a video shared by someone), the For You feed continuously serves content based on individual behavior and inferred preferences. This personalized stream makes it easy for commercial content to blend seamlessly with original posts, often without clear labels. By focusing on the For You feed, we can see how TikTok’s algorithm subtly integrates unlabeled advertising.

## TikToks Recommender System and "Interests"

Understanding how TikTok’s recommender system adjusts to user input is a complex task. To begin with, we needed to classify videos in order to differentiate between video material and thematic shifts in the recommended content. TikTok uses multiple classification schemes for videos and users. External researchers often rely on hashtags to understand content types, as TikTok uses hashtags to structure their data. However, the use of hashtags is not as relevant on TikTok as on some other social media platforms. As we have already [shown](https://tiktok-audit.com/blog/2024/Hashtag-Horizon/) in one of our previous blog posts, up to 28% of all videos in our data collection lacked any hashtags.

A recurring classification method we observed involves the “interests” that TikTok assigns to both users and videos. Users can have multiple interests in various topics (that can be reviewed in the app’s settings menu under Ads -> Manage Inferences). TikTok publicly shows interests related to specific hashtags are listed on its [Trend Monitoring](https://ads.tiktok.com/business/creativecenter/hashtag/cashstuffing/pc/en?countryCode=DE&period=7) site. During our investigation we found that each video is also assigned an interest, enabling us to compare the content each account views with the interest categories assigned to the user prior to [the account training process](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step3/). 

TikTok’s interest taxonomy is organized in a tree-structure with 13 high-level categories like “Entertainment” or “Lifestyle” and a varying level of detailed subcategories, for example: Lifestyle > Food & Drink > Mukbangs & Tasting. The following chart shows the prevelance of interests assigned to the videos in our dataset.

{% include plotly.html data="/assets/plotly/2024-08-interest_tree.js" id="656631a2-c906-450b-bdcb-04044012ec29" caption=""  style="display:none" width="100%" %}

One limitation of this evaluation is the interest classification itself. Reducing the content of a video to just one of 73 interests often oversimplifies its nuances. This classification is likely only one of many factors TikTok uses in its recommendation system. For this study, we relied on interests assigned by a fasttext classifier we developed, which was trained on observed interests from 688,000 videos and achieved a precision of 95%.

## Analysis of the User Journey

Comparing user journeys on TikTok is challenging due to the varying duration of scrolling sessions. Therefore, we compare users within the same For You feed scrolling duration intervals from the start of the scrolling, such as after the first 15 minutes or within the 45 to 60 minute-interval for each account.

The chart below shows the share of videos labeled with specific interests within each 15-minute interval of [the data collection process](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step3/) for each user profile.


<div id="fig-mobile-no">

{% include plotly.html data="/assets/plotly/2024-08-interests_slider.js" id="38752460-1e95-4b6c-b399-14da1643c644" style="display:none" width="100%" %}

</div>

<div id="fig-mobile-yes">

{% include figure.html path="/assets/img/2024-08_interests_slider_static.png" class="img-fluid rounded z-depth-1" zoomable=true %}

</div>

<style>

@media only screen and (max-width: 1200px) {
#fig-mobile-no{
        display: none !important;
      }
}

@media only screen and (min-width: 1200px) {

      #fig-mobile-no{
        display: block;
        margin-left: -13em;
      }

      #fig-mobile-yes{
        display: none;

        }

    }
</style>

In the first 15-minute interval, we observe a strong focus on a few categories like “Entertainment” or “Movies” across all accounts.

Moving the slider shows how the interests change in the later stages, such as the 45-60 minute interval, accounts seem to get more personalized as the share of "Entertainment" videos is reduced. There is no longer a shared focus on one category among all accounts. Categories that match the profile become more prevalent, such as “Outfit” for fashion accounts or “Lifestyle” for home organization accounts.

However, sometimes during the later stages, the focus returns to a few initial categories. We hypothesize that TikTok’s recommender system introduces content from diverse interests periodically to keep users engaged and help them discover new topics.

## How personalized is the For You feed?

To examine when personalization starts and when TikTok picks up on content engaging for the user, we looked into individual curves for each user. For every user, we identified if each watched video is relevant to them based on the video interests and the user profile assigned before the start of the data collection process. For example, for a user with the profile “Home Decoration” the relevant videos would be those labeled with one of the interests from the list: "Home & Garden", "DIY & Handcrafts", "Lifestyle", "Daily Life".

The following chart visualizes the share of videos deemed relevant to a user over time, broken down into 15-minute intervals. Each curve represents the experience of a different user, showing how the proportion of relevant content evolves as they continue to scroll through the For You feed. For many accounts, the peak is reached within the first hour of scrolling the For You feed.

{% include plotly.html data="/assets/plotly/2024-08-relevant_videos.js" id="11d6987a-f55d-48e6-b4a7-c37a3ab8f4cd" width="100%" %}

Similar to the previous chart, this chart shows that the share of relevant videos typically peaks within the first hour of scrolling the For You feed. Afterward, the proportion of relevant content tends to fluctuate, suggesting that TikTok periodically introduces new interests to maintain user engagement. This cyclical pattern hints at the platform’s strategy to continuously explore user preferences. On the one hand, this can help to “escape” rabbit holes, and on the other hand, means that users always cycle back to the main categories of entertaining content.

We also examined how shared video experiences evolve among users over time. The next chart shows the number of unique videos seen by more than one user in each 15-minute interval. The highest amount of shared videos is within the very first 15 minutes spent on the For You feed, decreasing later, indicating that accounts tend to become more personalized after just 15 minutes of using the app (see the figure below).

{% include plotly.html data="/assets/plotly/2024-08-videos_multiple_users.js" id="347949ab-9c31-43d4-9bfe-ef7f936167a2" width="100%" %}

As TikTok’s recommender system fine-tunes content to user preferences, it also introduces commercial content in ways that are not always transparent. While some ads are clearly marked, much of the promotional content on the platform exists in a grey zone, where it is not formally recognized as advertising but still serves commercial purposes. This raises important questions about consumer protection and the platform’s responsibility in clearly distinguishing between organic content and ads. One example of such an account is shown in the screenshots below. It is an account that continuously advertises home decoration products and promotes their shop, but has not labeled any of their videos as commercial.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-08_example_account_1.png" class="img-fluid rounded z-depth-1" zoomable=true   caption="Screenshot of the account overview advertising their linktree." %}       
    </div>
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-08_example_account_2.png" class="img-fluid rounded z-depth-1" zoomable=true  caption="Screenshot of an individual video advertising their own reseller shop."  %}
    </div>
</div>

In our earlier analysis, we explored the various advertising formats TikTok employs. Now, we will examine the complexities of this grey area, where the lines between content and commerce blur, affecting both the user experience and transparency on the platform.

## Grey Zone Advertising on For You Feed

In our blog post on advertising we have outlined the extent and range of possible advertising functionalities on TikTok. The platform offers a range of options of showcasing and promoting products, while only Paid Promotion formally falls under the definition of advertisement according to the Digital Services Act (DSA). In our previous report, we found about 20% of the videos on the For You Feed to be paid promotions. This number is much lower than what users described in our survey, where they report on average 48% (so, roughly half) of the content they see is advertising or recommending some product or service (see the following figure with survey results).

{% include plotly.html data="/assets/plotly/2024-08-percentage_ads.js" id="ba091737-4f69-44f3-8ead-330db1554112" width="100%" %}

The extent of promotional content that falls in a type of grey zone (in marketing terms: “organic advertisement”), which is not regulated by the DSA, raises concerns regarding user protection. This particularly includes content which can be described as “organic” and “influencer marketing”, as it utilizes the dynamic and viral effects of the platform in a targeted manner to drive creator or brand objectives. It leverages the authenticity of these influencers for the benefit of the brand **or/and** a product or service. 

To get a better idea of the extent of grey zone ads, we identified two simple proxies for commercial interest of creators. The following analysis focuses on:

- Bio links in the user profiles that we automatically followed and classified to understand whether or not creators try turn their online fame into money through the linking of shops or personal discount codes.
- The commercial content library to cross reference whether creators had already published a video they had labeled as commercial in the past

During our manual training phase, our researchers viewed 60,000 videos from roughly 16,000 different creators. Out of those 16,000, about 6,581 (40.95%) had added a link in their Bio page.

We first used a manual classification that helped us identify 1,520 of the domains as clear-cut cases of automated classification with 433 links pointing to hosted shops. We classified the remaining sites that fell in the category of “Other” or “Link-Pages” using OpenAIs GPT API. We ended up with the following distribution:

{% include plotly.html data="/assets/plotly/2024-08-biolink_types.js" id="04273642-b18d-46f8-88f2-c6b1ce4305d7" width="100%" %}

To verify, we cross-checked a random assortment of 50 accounts, 25 with the commercial indicator of having a shop link in the bio and 25 with at least on video marked as commercial content. Of the accounts with shop links in their bio, around 76% indicated commercial interest or self-promotional interests in their videos. For the accounts which have had at least one commercial content, the analysis showed a higher rate at 84%. This shows that these two simple indicators can be used as proxies to help estimate the amount of commercial content people see.

We then checked how high the distribution of videos of such accounts was in our users watchlist. Our results showed that on average 26% of all videos in our personas’ watchlists were from accounts which indicated a commercial interest, without being labeled as official ads. The beauty profiles showed an above-average rate of 31.6%. This amount of advertising is what users see in addition to the 20% official ads. It is no surprise that our survey showed that, on average, users estimate that **every second post** on TikTok is an advertisement or a product recommendation.

## Conclusion

In this blog post, we've outlined our investigations into the inner workings of the For You feed algorithm and its use of interests as a measure of personalization. We've compared the personalization effects between different profiles we created for our risk scenario-based audit and found that the personalization provides up to 80% of videos matching our predefined interests.

In a second step, we tried to shed light on "grey zone" advertising or "organic marketing" to assess how much of the For You feed consists of videos attempting to promote goods or services to users. Our simple metrics for classifying commercial intent closely match the user assessment in our survey, where people report that half the videos in their feed try to sell something.

Our results contribute to our analysis of the [systemic risk to consumer protection](https://tiktok-audit.com/blog/2024/Consumer-Protection-on-TikTok/) but also have implications for the debate on platform transparency and regulation. As mentioned, it wasn't easy to clearly assess which creators pursue commercial interests, and this should be considered when examining consumer protection. The fact that we were able to identify videos with commercial intent on a larger scale than what is actually labeled as such shows that the platform's labeling of individual videos is inefficient.

Our study also demonstrates the benefits of studying the effects of personalization, which means analyzing not just specific videos but how and in what order they are shown to users. This analysis was only possible with our own study setup and is not feasible with the research API TikTok is currently offering.


<script type="text/javascript">window.PlotlyConfig = {MathJaxConfig: 'local'};</script>
<script src="{{ '/assets/js/plotly.js' | relative_url }}" type="text/javascript"></script>
<script type="text/javascript">
var plotDataArray = "{{ plot_data }}".split("|");
// create script tag for each element in plotDataArray with the data as src
for (var i = 0; i < plotDataArray.length; i++) {
  var script = document.createElement('script');
  script.src = plotDataArray[i];
  script.type = 'text/javascript';
  script.async = true;
  document.head.appendChild(script);
}
</script>

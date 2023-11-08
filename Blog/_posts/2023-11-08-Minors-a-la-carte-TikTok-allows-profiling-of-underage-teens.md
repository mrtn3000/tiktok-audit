---
layout: post
title: "🍽️ Minors à la carte: TikTok allows profiling of underage teens "
date: 2023-11-07 10:00:00
description: We look into the Research API and its shortcomings.
tags: ads, analysis
categories: ad-libary
featured: true
related_posts: true
---
*By: [Santiago Sordo Ruz](https://www.stiftung-nv.de/en/person/santiago-sordo-ruz), [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova) and [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling).

In [a previous post](https://tiktok-audit.com/blog/2023/ads-targeting-minors/), we shared that TikTok is still allowing advertisers to target minors -aged between 13 and 17- despite announcing that it would stop this practice starting 11 July. Today we dive a little deeper into this topic to discuss the subtleties of the role that profiling plays in advertising to this particularly vulnerable age group and the platform’s compliance with its own announcement and the DSA. After an explanation of what profiling means in the context of the DSA, we show that despite some recent changes regarding this practice, TikTok is neither completely adhering to their own standards, nor to the DSA.

## Profiling in targeted advertising

To maximise the impact of their campaigns, advertisers seek to serve content that is as close to tailor-made to their target audiences as possible. User **profiling** enables by estimating the interests of individual user and is standard practice in the online marketing industry. However, abiding by the DSA’s online protection of minors provisions, which will be applicable across the EU from 17 February 2024, entails refraining from targeting advertisements to minors by profiling them. Article 28(2) reads:

> Providers of online platform [***sic***] shall not present advertisements on their interface **based on** **profiling** as defined [[in the GDPR](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32016R0679&qid=1697727163779#d1e1489-1-1)] using personal data of the recipient of the service when they are aware with reasonable certainty that the recipient of the service is a minor.
> 

The [definition](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32016R0679&qid=1697727163779#d1e1489-1-1) in the GDPR is the following:

> ‘profiling’ means any form of automated processing of personal data consisting of the use of personal data to evaluate certain personal aspects relating to a natural person, in particular to analyse or predict aspects concerning that natural person's performance at work, economic situation, health, personal preferences, interests, reliability, behaviour, location or movements;
> 

So, with these definitions in mind, is TikTok enabling profiling to target minors with ads?

## The profiling menu

To answer this question, let’s first look more closely into [TikTok’s Ad Library](https://library.tiktok.com/ads). The data we have gathered from it includes an interesting set of variables that is literally prefixed with the `targeting` keyword. While we can’t know this for certain, we have every reason to believe these variables describe some of the characteristics that the DSA is trying to protect: personal preferences, interests and behaviour.

To investigate our question, we looked at the data we have collected for Germany and filtered for ads presented to minors which also used at least one of these variables: `targeting.audience`, `targeting.interest`, `targeting.video_interactions` and `targeting.creator_interactions`. If you hover over the ⓘ symbol beside a variable on any ad in the library, the following descriptions pop-up:

| Variable | Description |
| --- | --- |
| audience | Whether the ad was shown to users who belong to or share similar characteristics to a specific audience list. These lists are based on the users' on and off-TikTok activity as specified by the advertiser. |
| interest | Whether the ad was shown to users in these interest categories. |
| video_interactions | This ad was shown to users who engaged with videos in these categories. |
| creator_interactions | This ad was shown to users who followed or viewed creators in these categories. |

It would be very interesting to have a closer look into the `audience` variable to see how those audience lists look like and -especially- to figure out what kind of off-TikTok activity it considers, but we won’t do it here. Let’s illustrate what the other three variables describe and how they enable profiling. Consider the following table, which ranks the most popular targeting categories in our data:

| Rank | interest | creator_interactions | video_interactions |
| --- | --- | --- | --- |
| 1 | Beauty & personal care | Fashion & beauty | Beauty & style |
| 2 | Apparel & accessories | Game | Entertainments |
| 3 | Games | Relationship | Lifestyle |
| 4 | News & entertainment | Talent | Sports & outdoors |
| 5 | Life services | Fashion & beauty, random shoot | Lifestyle, beauty & style |

This is a snapshot of the most widely used categories used within the profiling menu that advertisers are offered by the platform to create segments matching their target audiences. If minors are part of this menu, then the company is not only not complying with its own deadline, but also not using profiling to target them **precisely** in the way described in the DSA.

## Our findings and some conclusions

The figure below shows how the frequency of ads that target minors *and* use profiling has evolved in the last months; the red vertical line marks 11 July. As you can see, the platform has been allowing this practice and has continued to do so well past its self-imposed deadline. However, it is also clear that the practice is being discontinued, with some days even exhibiting zero ads. This could mean TikTok is enforcing its decision gradually or that advertisers are aware of the new rules and simply to do attempt to target minors to the same extent.



<div class="row justify-content-sm-center"><div class="col-sm-8 mt-4 mt-md-0">
{% include figure.html path="/assets/img/2023-11_tt-ads-targeting-minors.png" class="img-fluid rounded z-depth-1" zoomable=true %} 
</div></div>
*Image: The number of variables available on TikTok through different means of data acccess.*


While the real test with respect to the DSA comes on 17 February 2024 when targeting of minors using profiling becomes mandatory we can -for now- qualify our previous finding: TikTok has and is still targeting minors *******************and it has and is still allowing the use of profiling to do so*******************. Even if we see a drop in the numbers, the platform still allows around one 700 ads violating it’s policies and the DSA in September 2023.

What is already clear is that societal oversight -be it on behalf of the government or civil society- is crucial in assuring that the systemic risks associated with Tiktok, other VLOPs and online services in general are mitigated. The technologies and strategies these companies employ are in constant evolution, and we can’t afford to stay behind. 

One fundamental ingredient of this oversight is transparency on behalf of platforms. Regulations such as the DSA already constitute important progress in this direction. Tools like Tiktok’s Ad Library and its Research API are important steps towards achieving it. However, we have already seen that such efforts currently [fall woefully short](https://tiktok-audit.com/blog/2023/the-TikTok-research-API-falls-woefully-short/). Be it protecting minors or mitigating any other potential harms, if we want to provide society and governments with tools that actually match the challenge, we must demand broader, deeper and less restricted access to the kind of data that made this post possible.

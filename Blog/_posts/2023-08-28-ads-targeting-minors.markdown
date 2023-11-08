---
layout: post
title: "🔞 Ad-Targeting for minors still exists but it shouldn't"
date: 2023-08-28 18:00:00
description: An data analysis of ads targeting minors on a set of 7.000.000 ads shows that, altough TikTok claimed it ended the practice, still exists
tags: ads, analysis
categories: ad-libary
featured: false
related_posts: false
---
*By: [Martin Degeling](https://www.stiftung-nv.de/de/person/dr-martin-degeling) & [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova)*


Owner: Martin

On June 28th, TikTok [announced](https://www.tiktok.com/business/en/blog/privacy-updates-improved-data-control-transparency-tools) that “Starting today […] people in the United States aged 13 to 15 will no longer see personalized ads on TikTok based on their activities off TikTok. From Tuesday, July 11, people in the European Economic Area, United Kingdom, and Switzerland aged 13 to 17 will no longer see personalized ads on TikTok based on their activities on or off TikTok”. 

The changes in the EEA are related to the Digital Services Act coming into force - Article 28 (2) on “Online protection of minors” prohibits profiled advertisements for minors.

Now that TikTok has made its ads library publicly available, we wanted to test whether TikTok actually followed through on these announcements. And they do not. There are still ads targeted specifically to minors, and there is no barrier for advertisers to place these ads.

Here is how we come to that conclusion:

More than 7.000.000 ads in the ad library have been targeted at a German audience since October 2022. Most ads are not targeted at any specific age group, which means all age groups except 13-17 are listed. But over 3000 have been targeted only at minors (ages 13-17). And out of those, only 22 have been removed. 

This is not surprising, in general. TikTok only announced an ending to this practice in July. Therefore, we expected to see a drop in the number of ads targeted at minors after July 11th. But this is not the case. The following histogram shows the number of ads targeted at minors per day over the whole time span. There is no indication that targeting minors has stopped or even declined since July 11th.  

{% include figure.html path="/assets/img/tt_adtargeting_minors_histogram.svg" class="img-fluid rounded z-depth-1" zoomable=true %} 
*Histogram of the number of ads targeting only users 13-17 years old*

While targeting only minors is not super common in Germany, the fact that it is still happening, although TikTok claimed to have disabled it, is surprising. See, for example, this [Warner Brothers ad](https://library.tiktok.com/ads/detail/?ad_id=1773031834457089) for the movie Meg2. It is targeted at male users between 13-17 and the “audience” feature is set to “yes”. Enabling this feature means that ads are “**based on the users' on and off-TikTok activity as specified by the advertiser.”** Activity-based targeting is explicitly mentioned in the TikTok press release as being deactivated by July 11th.

Out of curiosity, we wanted to see what changes TikTok had implemented to prevent this type of targeting on the platform. We used a business TikTok account to get quotes for promoting a video.

The screenshot below shows that TikTok implemented at least some kind of measure. When selecting 13-17 as your audience, the interface says *“Metrics cannot be displayed due to data security requirements for minors”.*

<div class="row justify-content-sm-center"><div class="col-sm-4 mt-3 mt-md-0">
{% include figure.html path="/assets/img/tt_targeting_13-17_estimate.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div></div>
*Screenshot from the TikTok App not-showing estimates for the audience size for 13-17 yo*

However, this limited data disclosure has only been implemented for the estimated audience. After specifying the targeting criteria for an ad, we are asked to specify the budget and duration of the ad placement. In that process (as seen in the screenshot below) TikTok discloses our ads' “Estimated video views”. While TikTok does not disclose the exact audience size of 13-17-year-olds in Germany who are interested in Education, we now see a lower bound for the same target group and learn that about 266.519 to 709.520 users in that audience are expected to be online within a day.

<div class="row justify-content-sm-center"><div class="col-sm-4 mt-3 mt-md-0">
{% include figure.html path="/assets/img/tt_targeting_13-17_education_estimate.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div></div>
*Screenshot from the TikTok App showing estimated views from the target group*

The fact that targeting minors with ads targeting not only their age, but also gender and interests, which TikTok infers from user behaviour, is not only in violation with TikTok's own announcement but also the Digital Services Act that prohibits this type of advertising.

PS: Here is a list of the advertisers that target minors most often:

```
Warner Bros. Entertainment GmbH                          283
Non-trivial                                               93
eBay Kleinanzeigen GmbH                                   63
Bayerischer Jugendring                                    62
Scoolio GmbH                                              60
GHIS School                                               59
www.bpods.de                                              53
ethno IQ GmbH                                             52
EF Educational Foundation for Foreign Study AG            45
Ministerium der Justiz des Landes Nordrhein-Westfalen     45
FRØSLEV AFTERSCHOOL                                       39
LEONINE Distribution GmbH                                 36
Handelsverband Deutschland - HDE e.V.                     35
Pikoya Ltd.                                               34
HuLab GmbH                                                31
Scopely, Inc.                                             30
epods1                                                    29
neo venture GmbH                                          29
lukas.pain                                                28
Party Club Berlin Freizeitkultugestaltung e.V.            28
```

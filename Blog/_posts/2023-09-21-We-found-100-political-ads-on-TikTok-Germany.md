---
layout: post
title: "🔭 We found 100 political ads on TikTok Germany"
date: 2023-09-25 10:00:00
description: An update on political ads in Germany + Dataset
tags: ads, analysis, political-ads
categories: ad-libary
featured: true
related_posts: true
---
*By: [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova) and [Alexander Hohlfeld](https://www.stiftung-nv.de/de/person/alexander-hohlfeld)*

In our blog post [Diving into TikTok's Ad Library: Surfacing with Missing Data and Unenforced Guidelines](https://tiktok-audit.com/blog/2023/tiktok_political_ads/) we found, that contrary to [TikTok´s guidelines](https://www.tiktok.com/creators/creator-portal/en-us/community-guidelines-and-safety/tiktoks-stance-on-political-ads/) political advertising exists on the platform. Even though we argued that a systematic analysis is currently not possible, due to a lack of information provided by the ad library, we took a closer look at it and developed methods to assess the prevalence more in-depth. We matched names of politicians and political parties with the names of accounts that posted ads or those who paid for an ad.

But this is a very limited analysis and therefore our general criticism persists: TikTok needs to provide more features and data for the ad library to serve it’s purpose. For example, the videos are missing textual descriptions like hashtags the users would see. TikTok could also provide subtitles, that would allow researchers to automatically analyse what is said.

In the meantime, our limited approach offers a glimpse at the prevalence of political ads in specific contexts. But there is a major limitation: comparing politicians names with the available data only brings up those ads that are provided or paid for directly by political parties and candidates themselves. It is possible that political ads that are provided by third parties (e.g., lobby groups) could be even more prevalent, as they could be used to intentionally circumvent TikToks ban as well als political regulation on political ads.

Our analysis is based on the data of over **7.5 million advertisements that included Germany as a target country over the period from 01.10.2022 to 31.08.2023**.

As described above we queried our dataset with the names of politicians. We compiled a list of names of 1.) members of the the German parliament (MdBs), 2.) members of the German federal parliaments (MdLs) as well as 3.) all members of the European parliament (MEPs), searching for the personal names in the usernames and the ad sponsors. Additionally, we also looked for the party names in those data fields.

In total, we found 105 ads.

{% include figure.html path="/assets/img/2023-09_tt_political_ads_by_accounts.png" class="img-fluid rounded z-depth-1" zoomable=true %} 

While the SPD posted the most ads in total, the majority is related to one campaign. If we look at the number of different accounts that used ads we can see that members of the AfD made the most attempts of posting political ads:

{% include figure.html path="/assets/img/2023-09_tt_political_ads_by_party.png" class="img-fluid rounded z-depth-1" zoomable=true %} 

While most ads were not targeted at a specific audience, we also found that some political ads include particular targeting criteria. This is relevant to the current debate as microtargeting in political advertising has been scrutinised for a while and is part of an [ongoing debate in the European Union](https://oeil.secure.europarl.europa.eu/oeil/popups/ficheprocedure.do?reference=2021/0381(COD)&l=en), with the European Data Protection Supervisor [arguing for tighter](http://arguing/%20for%20tighter/) regulations. Specifically, we found, for example, that “News & Information” was the main interest category targeted by political ads. Still, we also found ads targeting specific topics like the Bavarian FDP politician whose [talk show monologue on early childhood education](https://library.tiktok.com/ads/detail/?ad_id=1765779799994426) was shown as an ad to 3000 German users interested in “Kids & Maternity”; or AFD’s Frank Rinck [4-minute ad of a speech in the Bundestag arguing for agricultural self-sufficiency](https://library.tiktok.com/ads/detail/?ad_id=1755552014103605) was shown to about 5000 users interested in “Appliances, Vehicles & Transportation, Tech & Electronics”.

{% include figure.html path="/assets/img/2023-09_tt_political_ads_by_targeting.png" class="img-fluid rounded z-depth-1" zoomable=true %} 


The whole set of political ads we found in the TikTok ad-library can be [downloaded as csv](/assets/data/2023-09_political_ads.csv).
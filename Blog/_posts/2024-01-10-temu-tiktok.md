---
layout: post
title: "🛍️ Shop Till You Drop...: How Temu exploits TikTok's affordances"
date: 2024-01-10 12:00:00
description: A short analysis of political ads and TikToks new advertisement library
tags: analysis, temu, fyp, tiktokmademebuyit
categories: rsba
featured: true
related_posts: true
---

<div class="row justify-content-sm-center"><div class="col-sm-6 mt-6 mt-md-6">
{% include figure.html path="/assets/img/2024-01_tt-temu.png" class="img-fluid rounded z-depth-1" zoomable=true width="100%" alt="generated with DALL·E 3" %} 
</div></div>

*By [Alexander Hohlfeld](https://www.stiftung-nv.de/en/person/alexander-hohlfeld) and [Kathy Meßmer](https://www.stiftung-nv.de/en/person/dr-anna-katharina-messmer)*

With over 50 million active users and more than 3 million downloads [in the weeks before Christmas](https://www.data.ai/de/apps/ios/app/temu-team-up-price-down/?MEANINGFUL_INTERACTION_COUNT=3&mps_date_filter=30-days), the app “Temu” is dominating both the Google Play and the App Store charts.

Temu was founded in July 2022 as a subsidiary of the Chinese company “PDD Holdings”, only a few months after PDD Holdings´ shopping app [“Pinduoduo” was suspended from Google’s Play store](https://www.reuters.com/technology/google-suspends-chinas-pinduoduo-app-due-malware-issues-2023-03-21/) due to security concerns and malware issues. The app faced [drastic accusations from researchers](https://edition.cnn.com/2023/04/02/tech/china-pinduoduo-malware-cybersecurity-analysis-intl-hnk/index.html). It might continuously run in the background, preventing itself from being uninstalled and thereby pushing its monthly user base. It might have the ability to spy on tracking activities of competing shopping apps or even the social network accounts of users. 

The rebranding as “Temu” for Western countries and the [relocation of its office](https://www.dw.com/en/temu-app-downloads-soar-as-western-shoppers-look-for-cheap-chinese-goods-and-sales/a-66683429) for the European market to Dublin can be interpreted as attempts to distract from the scandals of its mother company. However, this should not obscure the fact that Temu is also struggling with serious consumer protection problems.

First of all, [similar data privacy concerns](https://www.politico.eu/article/booming-chinese-shopping-app-temu-faces-western-scrutiny-over-data-security-2/) have already been expressed about the Temu app as with the earlier Pinduoduo app.

Second, Temu considers itself not an online shop but rather an “online marketplace”, even though that is barely visible to the user. In a [previous version of its Terms of Use from August 29th](https://web.archive.org/web/20231004112508/https:/www.temu.com/de/terms-of-use.html), Temu used that position to distance itself from the products it sold and denied any liability:

> “We do not have control over and do not guarantee the existence, quality, safety, suitability, or legality of the Products or the truthfulness, accuracy or legality of any information contained in the Product listings or other information provided by Sellers or other users”.
> 

In the [latest version of the Terms of Use](https://www.temu.com/de/terms-of-use.html) from December 29th, this has been updated and Temu admits its liability “**for slight negligent breach of essential obligations**”. What this means in practice still needs to be investigated. 

Third, products on Temu are extremely cheap and it can be assumed that this goes hand in hand with low quality and a lack of consumer protection standards. Many products offered on Temu have astonishing optical similarities with products of famous brands, thus moving on the border being considered as counterfeit products.

Finally, Temu is working with highly deceptive design practices. There are indications that some of these could be considered as misleading practices under European competition law. According to the [EU Directive on Unfair Commercial Practices](https://eur-lex.europa.eu/legal-content/EN/TXT/?qid=1410437777196&uri=CELEX:32005L0029) a practice shall be regarded as misleading if the practice is “like to receive the average consumer” and is “likely to cause [..] a transactional decision that he [the customer] would not have taken otherwise”. This includes, for example ["phony 'free' offers", "dark design patterns", such as "fake countdowns", "false offers of prizes, gifts" or "false use of limited offers"](https://europa.eu/youreurope/citizens/consumers/unfair-treatment/unfair-commercial-practices/index_en.htm).

<div class="row justify-content-sm-center"><div class="col-sm-6 mt-6 mt-md-6">
{% include figure.html path="/assets/img/2024-01_temu_pricewheel.png" class="img-fluid rounded z-depth-1" zoomable=true width="50%" %} 
</div></div>
*Screenshot of a price wheel on temu*


Temu is promoting price wheels all throughout the app, which usually offer supposedly “free” products. At first glance, it is not obvious to the user that the products advertised as “free” are in fact not free at all. The user needs to order a certain amount of other products to be able to proceed with the order. The “price wheels” also do not seem to work randomly, but in fact propose that the user would get the “Jackpot” almost all the time. A constant flood of notifications on allegedly free products or prizes is pressuring the user and creating “FOMO” (fear of missing out). Until recently, a countdown in the upper left corner offered “Free Shipping”  and restarted as soon as the countdown ended. But this might just be one example of fake limited offers on Temu. Opening the website or the app reveals an avalanche of countdowns and supposedly time-limited offers. While a more detailed legal investigation would be desirable, it seems obvious that these practices can have deceptive effects.  

As a reader of our blog – that is about auditing TikTok – you might wonder: ***What does this have to do with TikTok*?** We argue that the success of Temu is, to a large extent, built on the platform affordances of TikTok. No app or product has ever exploited the platforms' logic this systematically before.

{% include figure.html path="/assets/img/2024-01_tt_temu_hashtag_use.png" class="img-fluid rounded z-depth-1" zoomable=true %} 

*The screenshot above is from [TikToks Trend Analysis site for marketers](https://ads.tiktok.com/business/creativecenter/hashtag/temu?period=365&countryCode=DE) and shows that the #temu hashtag was used more than 53.000 times last year in Germany alone. For comparison, the hashtag #amazon was used 50.000 times in that time.*

Temu is extremely present on TikTok. Videos with the hashtag “**temu**” generated a total of **9.9B** **views**, **#temuhaul** a total of **3.4B** **views** and **#temufinds** **2.5B views** (09.01.2024). What makes Temu so successful on TikTok is that they perfectly understood the platform and developed strategies to exploit its platform logic. Their strategy builds on three main pillars:

1. Influencer Program
2. Affiliate Program
3. Gamification efforts

**The Influencer Program:** Temu is trying to [recruit influencers](https://www.temu.com/influencer-collaboration.html) with a mix of free products and monthly “influencer cash”. The key to its strategy is not to focus on specific or famous influencers. Instead, everyone with more than 300 followers can register for their program. That strategy makes it possible to **flood TikTok with the content of so-called “Nano-influencers”**. Temu proudly claims that “10,000+ influencers have already collaborated with Temu”. At the same time, the influencer program uses gamification strategies. Influencers are encouraged to “join campaigns”, “post and share” and thereby earn “benefits” (mainly Temu vouchers).

**The Affiliate Program:** The so-called “[Affiliate Program](https://www.temu.com/affiliate_account_activity.html)” takes this strategy to another level. To join, a user does not even need to have 300 followers. Everyone can create affiliate codes which are then shared on **TikTok** to receive a commission. This leads to a flood of spam content and comments from people promoting their affiliate codes. The registration is quite simple; all it takes is a Temu and a social media account (Instagram, TikTok or YouTube). With notifications like “xx earned 2.817,59€”, a starting balance of “3€” and statistics that are framed as games (such as “Ranking Race” or “Referral Race”), the users are encouraged to share their codes and referral links. Temu specifically encourages users to share them “in your bio”, “in your post” or “Send to your friends”. The promises of quick money (2€ reward for each download through the referral link) and large sums (e.g., 5,000€ bonus) are especially tempting for young people, leading them to spam social media network sites such as TikTok with their affiliate codes.

<div class="row justify-content-sm-center"><div class="col-sm-6 mt-6 mt-md-6">
{% include figure.html path="/assets/img/2024-01_temu_affiliate_program.png" class="img-fluid rounded z-depth-1" zoomable=true width="50%" %} 
</div></div>
*Screenshot of the affiliate program screen in the Temu app*

Although Temu (hidden under “more details”) points out that, "[u]nauthorized commission obtained through false advertising or posting referral codes as irrelevant comments on any videos or app stores is prohibited”, we were able to find a large number of such comments on **TikTok**. 

**Gamification Efforts:** Temu is also offering different gambling-like [mini games](https://www.temu.com/de/games.html), creating group pressure, to which young people are particularly susceptible:

- “Temu Fishland Game is an underwater adventure that allows players to catch fish and earn money based on the size and rarity of their catch.”
- “Temu Farmland is a farming simulation game where players can grow crops, raise animals, and sell their produce for a profit.”
- “Temu Redeem Cash is a game that offers users the chance to win real money by redeeming coins earned through other Temu games.”
- “Temu Lucky Flip is a game of chance where players can win big by flipping a coin and guessing the outcome correctly.”
- “Temu Free Gift is a daily bonus game that rewards users with free coins and prizes just for logging in.”

While constantly pushing the user to new price wheels for allegedly “free products”, encouraging users to share codes and links as well as strong gamification efforts, the combination of Temu with social media platforms like TikTok might cause consumer protection harms that need further investigation. We are currently investigating these harms, that result from the exploitation of TikTok´s affordances by e-commerce platforms like Temu or “fast fashion” apps like “Shein”. Follow our blog to not miss our next articles.


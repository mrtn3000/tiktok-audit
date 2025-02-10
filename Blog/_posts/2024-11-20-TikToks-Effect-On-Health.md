---
layout: post
title: "💊 TikToks Effect on Health"
date: 2024-08-26 10:00:00
description: ""
tags: analysis, step4, FYP,
categories: research, rsba
featured: true
related_posts: true
author: Anna Semenova, Martin Degeling, Greta Hess
---

*By [Anna Semenova](https://www.stiftung-nv.de/de/person/anna-semenova), [Martin Degeling](https://www.stiftung-nv.de/en/person/dr-martin-degeling), [Greta Hess](https://www.stiftung-nv.de/de/person/greta-hess).*


{% include figure.html path="/assets/img/2024-08_interest_overview.png" class="img-fluid rounded z-depth-1" zoomable=true %}


TikTok’s impact on the mental and physical well-being of its users, especially young adults, has raised significant concerns. While the platform has been criticized for influencing public discourse, consumer protection, and the spread of misinformation, there is also concern about how TikTok’s content may affect users' (mental) health and self-perception. TikTok’s algorithm-driven features, such as the For You feed and search function, are designed to maximize engagement but can sometimes surface content with unintended consequences for its audience.

Our research findinga from both the survey and scraped data highlight several concerns about the presentation of health-related content on TikTok. Our survey results indicate that TikTok use is correlated with a heightened desire to change one’s appearance, especially among women. On average, 58% of respondents reported social media influencing their desire to alter their appearance, with a gender gap showing 68% of women and 49% of men agreeing. TikTok users were more likely to report body discomfort and a desire for change than non-users. Content like #WhatIEatInADay and frequent ads for diet products or cosmetic services further try to monetize and reinforce this desire, despite many finding such content unrealistic.

Our research is the last part of a detailed series of examinations that build on the findings from our scenario testing of TikTok. These studies are grounded in our [risk-scenario-based audit process](https://www.interface-eu.org/publications/auditing-recommender-systems) (RSBA); for more on our methodology, you can read our [methodology blog post](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/).

In our previous scenarios, we explored how TikTok impacts [consumer protection](https://tiktok-audit.com/blog/2024/Consumer-Protection-on-TikTok/), particularly through various types of ads, and how its [search suggestions](https://tiktok-audit.com/blog/2024/Search-Suggestions/) can influence public discourse. In this scenario, we focus on potential health risks that arise when young TikTok users in Germany are exposed to content promoting dieting, cosmetic surgery, and body modification, and similar themes. The scenario is as follows:

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience (mental or physical) health risks</span> after beeing <span class="rsba-scenario-platform">exposed to ads for dieting/cosmetic surgery when swiping through the For You fee</span> and this will lead to <span class="rsba-scenario-macro">reduced overall health in the European Union.</span>

The potential impact of this content is not just a matter of individual concern but a broader public health issue, particularly within the European Union. Health is recognized as a systemic risk in the EU’s Digital Services Act (DSA). We wanted to understand the risks posed by TikTok’s promotion of health-related content and how this exposure can negatively affect users’ mental and physical well-being.

We’ve also dedicated separate blog posts to exploring key elements of our risk scenarios in more detail. For those interested in the platform involvement component of this scenario, we recommend reading our post on [The For You Feed](https://tiktok-audit.com/blog/2024/For-You-Feed/). Additionally, for a comprehensive analysis of the affected party - demographics of the 18-25 age group and their TikTok usage patterns, see our post on [How Young Adults Use TikTok](https://tiktok-audit.com/blog/2024/How-Young-Adults-Use-TikTok/).

In this post, we’ll build on that foundation and focus on the distinct harms that arise from the health content young adults are exposed to on TikTok. Specifically, we analyzed TikTok content related to promoting weight loss, cosmetic surgery, dietary supplements, protein powders, and teeth whitening. Our findings highlight correlations between exposure to this content and users' desire to change their appearance or body. We also found that TikTok users are slightly more likely than non-users to feel dissatisfied with their body image, and frequent exposure to ads for diet and beauty products further amplifies this effect. Additionally, we observed concerns regarding the spread of misleading medical content through influencers operating in grey zones.

## A Note Upfront: Correlation is not Causation

Mental and phsysical health are important but also complex issues that involve any societal and governemntal questions like costs and accessbility of care or support with communities and families. The impact of social media on the mental and physical health of young users has long been debated in both popular and scientific media. There are [examples](https://harvardpublichealth.org/tech-innovation/tiktok-mental-health-videos-do-they-actually-help/) of TikTok having a positive influence on mental health topics. However, there are also documented cases where it contributes to negative body image and related issues.

It is important to clarify that our study does not seek to pinpoint the exact causes of mental or physical health problems among young users in Germany. Instead, our focus is on understanding the correlation between exposure to content and behavioral changes. Establishing a direct causal link between social media use and mental or physical health issues is challenging because it involves ruling out counterfactuals and controlling for numerous confounding variables. Specifically, it requires comparing what actually happens with what would have occurred without social media use, while also accounting for other factors influencing health. 

Regardless of the intricacy of cause and effect we think TikTok has a responsibility to reduce the systemic risks and mitigate negative developments. For instance, TikTok could enhance its recommender system to diversify content and suggest more supportive material to mitigate these risks.

## Desire for appearance changes is higher among TikTok users, with notable gender disparity

Our survey explored various aspects of self-perception and the influence of social media. Respondents were asked to indicate their level of agreement with several statements related to their self-esteem and social media impact. 

{% include plotly.html data="/assets/plotly/2024-11-statements-by-gender.js" id="97961684-a4ad-449b-976d-3f8355275379" style="display:none" width="100%" caption="Share of Respondents Who Strongly or Somewhat Agree with the Statements" %}

The plot shows a bar chart comparing the responses of (self-identified) women and men to various statements about self-perception and the influence of social media. Each bar represents the percentage of respondents who agreed with the statements, with two bars for each question: one for women and one for men. Colors are used to indicate statistical significance based on p-values, with darker shades representing significant differences (p-value < 0.05) between the genders.

The survey results shows, for example, a notable difference between genders regarding the statement: **“Social media content and people sometimes make me want to change aspects of my appearance or body.” While 68% of women agreed with this sentiment, only 49% of men did.** On average, 58% of respondents expressed a desire to change aspects of their appearance or body due to social media. This highlights how people think social media impacts their self-perceptions and their lives, shaping desires and societal norms.

When focusing specifically on TikTok, and comparing the replies of TikTok users to those not using TikTok to the same questions, we observed a statistically significant difference as well, although it is smaller than the gender difference.

{% include plotly.html data="/assets/plotly/2024-11-statements-by-tiktok-use.js" id="0e15524c-9ef5-43ad-9026-589481e46117" style="display:none" width="100%" %}

**Among TikTok users, 60% expressed a desire to change their appearance or body after viewing social media content, compared to 55% of non-users.**

Similarly, there is a statistically significant difference between TikTok users and non-users regarding their answers to statements like “I feel comfortable in my body” - 62% (TikTok users) vs 68% (non users) "agree" or "tend to agree", or “I have a positive attitude towards my body” - 61% vs 67%, or “Content and people on social media sometimes make me want to change something in my life and everyday routine” - 73% vs 68%.

**This shows that TikTok users feel less comfortable with their body and abilities than those that do not use TikTok.** It is important to reiterate that these findings indicate a **correlation rather than causation**. This is due, in part, to the fact that TikTok usage is associated with the use of other social media platforms, among other potential contributing factors. We also want to note that, while there are differences between the groups of TikTok users and non-users, dissatisfaction with body image is common in the general population as well. In [2018](https://www.notion.so/Drafts-and-Ideas-10e56afb84ee4855ab895fb118c16bdc?pvs=21), 31% of respondents in Germany said they were somewhat dissatisfied, and 8% were very dissatisfied with their body. [Another survey](https://www.notion.so/Drafts-and-Ideas-10e56afb84ee4855ab895fb118c16bdc?pvs=21) found that 27% of respondents disagreed with the statement, "Overall, I am satisfied with myself" .

## Viewing eating or exercise content is correlated with the desire to change one’s appearance

{% include plotly.html data="/assets/plotly/2024-11-whatieatinaday.js" id="bedf0220-c9b4-4509-b476-41d8791a665f" style="display:none" width="100%" %}

Respondents were also asked about their reactions to TikTok content featuring daily routines, eating, and exercise behaviors—such as those shared under hashtags like #WhatIEatInADay or #GymRoutine. 53% reported that such content makes them want to change their appearance or body, and 66% felt the content was unrealistic, portraying a distorted view of everyday life. Notably, 37% of those who believe the content is unrealistic still felt the urge to change their appearance, highlighting the concerning psychological impact even on those with media literacy.

{% include plotly.html data="/assets/plotly/2024-11-exposure-self-assessment.js" id="06d87e27-38e5-4a04-b10e-f115de58f992" style="display:none" width="100%" %}

Focusing on consumer protection, we also asked respondents whether they had seen ads or recommendations for specific products—such as diet pills, weight loss injections, cosmetic surgery, dietary supplements, protein powders, and teeth whitening/bleaching—within the last three weeks. In total, 74% reported encountering at least one of these ads either very or rather frequently. Note that we did not further specify ads, so this includes grey zone advertising, promotional videos that where not labeld as ads.

{% include plotly.html data="/assets/plotly/2024-11-statements-adviewers.js" id="06d87e27-38e5-4a04-b10e-f115de58f992" style="display:none" width="100%" %}

TikTok users who reported seeing ads for diet and related products more frequently in the past three weeks were more likely to want to change their body or lifestyle and reported feeling less attractive than users who saw fewer or no ads. Again, it's important to emphasize that correlation does not imply causation; the link between ad exposure and user perceptions may reflect TikTok’s ability to target individuals already interested in such products.

There are also statistically significant gender differences: 52% of women report that those or similar ads on TikTok have influenced their desire to change something about their body or appearance, compared to 38% of men.


## Grey Zone Health Ads and Medfluencers

In our previous post, “[Understanding TikTok’s For You Feed](https://tiktok-audit.com/blog/2024/For-You-Feed/),” we identified proxies to assess our scraped data for so-called “Grey Zones”: bio links in user profiles that we automatically followed and classified and the commercial content library to cross-reference whether creators had previously published commercially labeled content.

Building on this, our current investigation focuses on health- and medical-related content. We wondered what role these grey zones play in the proliferation of content that shares advice and recommendations regarding users' health. The algorithmic promotion of such content, which may not always be reliable or scientifically sound, poses potential risks for young users.

Several recent studies have examined the spread of health and medical advice on TikTok, highlighting the potential risks and influence of misinformation on the platform. One study, *The Investigation of Health-Related Topics on TikTok*, analyzed how public health behaviors are influenced by TikTok's user-generated content. This study found that health advice is often packaged in highly engaging formats, making it difficult for users to distinguish between credible information and misleading advice ([MDPI](https://www.mdpi.com/2673-6470/3/1/7)). Another study, *Emergence of MedTok*, explored the characteristics of TikTok videos about common health conditions, noting that videos created by non-professional influencers often spread misinformation, particularly about conditions affecting younger individuals ([Oxford Academic](https://academic.oup.com/pmj/advance-article-abstract/doi/10.1093/postmj/qgae021/7611052)).

Research published in the *Journal of Medical Internet Research* examined attitudes and misinformation regarding Cognitive Behavioral Therapy (CBT) on TikTok. It found that a significant portion of videos contained misleading information, which can influence users' decisions about seeking professional treatment ([JMIR](https://www.jmir.org/2023/1/e45571)). Similarly, a 2024 review of sinusitis-related videos showed that 44% of videos contained non-factual information, with many "nonmedical influencers" promoting unverified and sometimes harmful home remedies ([Med Xpress](https://medicalxpress.com/news/2024-04-health-tiktok-trends.html)).

These studies underscore the potential risk that underlies this specific content group, particularly in the context of medical influencers or "medfluencers." These content creators post blends personal experience, product promotion, and medical advice, creating a grey zone that skirts the boundaries of both advertising and medical guidance. Medfluencers may not explicitly disclose commercial affiliations or the commercial nature of their advice, leaving users vulnerable to misinterpreting personal anecdotes as reliable health recommendations. This poses significant public health risks, particularly as medical misinformation can spread rapidly through platforms optimized for virality.

By analyzing 519 videos featuring terms like "Doktor," "Arzt," "Chirurg," and similar medical themes, we found key trends highlighting the unregulated spread of health advice on TikTok.

Firstly, the our data reveals a **wide range of medical professionals** active on TikTok. This diverse group includes students, general practitioners, specialists (e.g., cardiologists, urologists), and dentists. Some influencers use their medical background to promote products like period underwear through their bio links, while others focus on medical content but also participate in media appearances.

In terms of **engagement levels**, there is significant variation. Some influencers boast large follower counts (e.g., 503.3 thousand followers) and actively promote their services or businesses via bio links. Conversely, others, despite holding reputable medical positions, have relatively small followings (e.g., 756 followers).

{% include figure.html path="/assets/img/2024-11-medfluencer_1.png" class="img-fluid rounded z-depth-1" zoomable=true %}

A particularly concerning trend is the presence of **grey zone medfluencers**. Among the scraped accounts, only 60% of influencers were verified as having legitimate medical credentials. The remaining 40% operated in a grey zone, with insufficient evidence of qualifications, making it challenging for viewers to trust the advice being shared. Some accounts include disclaimers like "No medical advice," but many do not, raising concerns about the unchecked dissemination of medical content. Without platform-enforced regulations, the presentation of medical content remains inconsistent, which is concerning when the platform’s algorithm can promote unverified advice alongside legitimate medical recommendations, increasing risks for unsuspecting viewers.

This aligns with survey data about general ad perception among our respondents: two third of TikTok users (62%) say boundaries between ads and entertainment on TikTok are blurring, 58% of TikTok users report often seeing dubious and untrustworthy ads, while 41% say they have encountered dangerous ads or product placements

{% include figure.html path="/assets/img/2024-11-medfluencer_2.png" class="img-fluid rounded z-depth-1" zoomable=true %}

Furthermore, many of these influencers engage in commercial promotion, often without clearly distinguishing between medical advice and product promotion. For instance, some offer hypertension courses through their bio links or promote their medical books. This blending of advice and commerce blurs the lines for consumers, making it difficult to discern objective health guidance from promotional content.

{% include figure.html path="/assets/img/2024-11-medfluencer_3.png" class="img-fluid rounded z-depth-1" zoomable=true %}

{% include figure.html path="/assets/img/2024-11-medfluencer_4.png" class="img-fluid rounded z-depth-1" zoomable=true %}

Another significant issue is the promotion of unverified alternative health advice. Some accounts endorse treatments or remedies lacking scientific backing. This mirrors findings from studies such as The Investigation of Health-Related Topics on TikTok, where engaging but misleading content often gains more traction than credible health advice. Influencers sometimes use AI-generated visuals to explain medical conditions, which can give an appearance of credibility while spreading unverified advice. This dynamic of viral but unverified content reflects broader trends observed in studies like The Investigation of Health-Related Topics on TikTok and Emergence of MedTok, which show that engaging yet misleading content often gains more traction than verified advice.


{% include figure.html path="/assets/img/2024-11-medfluencer_5.png" class="img-fluid rounded z-depth-1" zoomable=true %}

The scraped data emphasizes the critical need for regulation and transparency in how medical advice is shared on platforms like TikTok, where grey zone medfluencers continue to blur the lines between health guidance and commercial promotion.

Examining TikTok's ad library for removed ads from August 2023 to October 2024 provides additional insight:

- **36,719 ads** were removed for featuring restricted or prohibited claims/content related to healthcare and pharmaceutical products and services. This includes images of certain health conditions, medical claims without proof, suggestions that discourage healthy habits, or content that could be seen as irresponsible behavior.
- **22,441 ads** were removed because the promoted product or service required a country's approved medical license or certification.
- **722 ads** featured prohibited products/services related to the healthcare and pharmaceutical industry, including prohibited medical institutions, pharmacies, medicines, treatments, or cosmetic clinics/services.
- **51 ads** were rejected because the ad creative or landing page may feature or promote medical misinformation.

These numbers illustrate the ongoing challenges in monitoring and regulating health-related content and advertisements on TikTok, highlighting the need for more stringent enforcement to protect users from misleading and potentially harmful information.

## Conclusion

Scraped data reveals that many TikTok accounts, including both legitimate medical professionals and unqualified individuals, blur the lines between personal experience, product promotion, and medical guidance, creating a grey zone where commercial affiliations and the credibility of advice are often unclear. Studies have shown that engaging yet potentially misleading health advice can spread rapidly on the platform, posing risks to young users who may struggle to distinguish between credible information and misinformation. The analysis of TikTok’s ad library further underscores the challenges in regulating this content, with a substantial number of health-related ads being removed for featuring unverified claims or promoting prohibited products and services. 

The DSA does not provide specific guidelines for medical content but enforces broad transparency measures aimed at addressing health-related misinformation. It mandates that platforms explain moderation decisions and allow vetted researchers access to data to study the spread of misinformation. Additionally, VLOPs must conduct systemic risk assessments to identify potential public health risks, particularly relevant for platforms like TikTok, where misleading health advice can rapidly gain traction from influencers lacking medical credentials. While the DSA aims to mitigate harmful content, a significant grey area remains in how medical advice is presented. Our scraped data shows a proliferation of self-regulatory approach by some influencers, who include disclaimers like "No medical advice" in their bios.

In Germany, the legal framework around medical and health advice is primarily governed by the Heilmittelwerbegesetz (HWG) (Law on Advertising in the Health Sector), which regulates how medical services and products can be advertised. The HWG places strict limitations on the claims that can be made in health-related promotions, ensuring that they are backed by scientific evidence and that there are no deceptive or misleading statements. This regulatory framework is particularly relevant given our findings that a significant number of TikTok users report being impacted by unrealistic health content and advertising. Together, these insights underscore the urgent need for clearer regulations to protect users from misleading health information and to promote a healthier digital environment on platforms like TikTok.

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

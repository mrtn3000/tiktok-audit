---
layout: post
title: "🗳️ Other search for … the opposition party"
date: 2024-07-16 12:00:00
description: "TikToks Search Suggestion in Germany before the EU elections"
tags: analysis, step4, survey, search suggestions, public discourse
categories: research, rsba
featured: true
related_posts: true
author: Miazia Schüler, Martin Degeling, Salvatore Romano and Kathy Meßmer
---

By [Miazia Schüler](https://aiforensics.org/about), [Martin Degeling](https://www.interface-eu.org/persons/dr-martin-degeling), [Salvatore Romano](v) and [Kathy Meßmer](https://www.interface-eu.org/persons/dr-anna-katharina-messmer)

{% include figure.html path="assets/img/2024-07_search_suggestions_header.jpeg" alt="A stylized TikTok logo, in the background posts from political parties" caption="A stylized TikTok logo, in the background posts from political parties. Image credit: Denis Constant, Ittai Studio" class="img-fluid rounded" zoomable=true width="50%" %}

TikTok aims to create an [entertainment-focused and politically diverse environment](https://newsroom.tiktok.com/de-de/wie-wir-uns-auf-die-europawahl-2024-vorbereiten) for its users. The social media platform hosts a significant amount of global active political content. TikTok is also known for its recommender system algorithms that significantly influence what content users see and engage with, which warrants an analysis of whether or not the algorithms work towards their claimed aim. Previous work has indicated that TikTok’s various algorithms prioritize [sensational and misleading content](https://www.futurity.org/tiktok-algorithm-3211962/), exacerbating the spread of misinformation and contributing to social and political polarization.

For this study [interface’s](https://www.interface-eu.org/) TikTok Audit Team partnered with the civil society organization [AI Forensics](https://aiforensics.org/) on a study of the “Others Searched For” feature to understand if it exhibits similar tendencies. As we issued with [der SPIEGEL](https://www.spiegel.de/netzwelt/web/tiktok-warum-macht-die-app-so-seltsame-suchvorschlaege-a-cd4e4798-c078-4737-bf42-b0c887ed4263?giftToken=006ff40a-4ac2-495c-85a8-dccd0d9e6675), TikTok provides highly questionable search suggestions beyond false celebrity death rumors or other random search terms. The platform also suggests oddly specific and partially misleading search ideas that can lead users to believe questionable information or send them down contentious political rabbit holes. Specifically in the context of electoral processes, the risk is heightened when “Others Searched For” suggestions provide distinct political information, possible rumors, factual disinformation, or even dog whistles for conspiratorial content.

The year 2024 is a pivotal global election year, signified by key elections in countries such as the European Union, the United States, India, and many more countries. Therefore, interface and AI Forensics set out to investigate the extent to which social media platforms like TikTok and its “Others Searched For” feature push harmful or false narratives in a political context. Our research is part of a series of detailed examinations dedicated to elaborating on the findings from our scenario testing of TikTok. We have conducted studies based on our framework for risk assessments: the risk-scenario-based audit process (RSBA; read about our [methodology](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step1/) here). In this post, we focus on the risk scenario for public discourse that we have [previously](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step2/) defined as:

> <span class="rsba-scenario-affected">Young TikTok users</span> <span class="rsba-scenario-characteristics">in Germany between 18 and 25 years old</span> <span class="rsba-scenario-harm">experience a distorted version of reality</span> <span class="rsba-scenario-platform">viewing the suggested search terms</span>, which <span class="rsba-scenario-macro">negatively impacts the public discourse.</span>

Specifically, we examine how the search suggestions might create a distorted view of reality that can potentially negatively impact public political discourse, especially amongst young users who increasingly rely on TikTok's search feature. By investigating the effects on the 18-25 age group in Germany, we aim to highlight the potential spread of misinformation and politically polarizing content, contributing to a more informed and balanced media environment during this pivotal election year, in which many are first-time voters.

## Users Remember Search Suggestions

In December 2023, we [surveyed](https://tiktok-audit.com/blog/2024/TikTok-RSBA-Step3/) [1,643 young adults (18-25 years old, of which 59% use TikTok)](https://tiktok-audit.com/blog/2024/How-Young-Adults-Use-TikTok/) in Germany. When asked about their use of different platform features, 67% reported using the search “frequently” or “somewhat frequently,” with only 3% claiming never to use it or not even knowing about it. The data confirms [reports on the TikTok search feature becoming more relevant for younger users](https://www.nytimes.com/2022/09/16/technology/gen-z-tiktok-search-engine.html). In the youngest age range included in our survey (ages 18-19), the regular or frequent use of the search feature was considerably higher at 74% than for the oldest age group (24-25 years at 62%). Notably, there were no measurable gender differences.

In the next step, we showed participants a list of search suggestions we manually compiled from what we had seen on the platform. All participants saw the same ten suggestions in a randomized order, without any kind of personalization. Three-quarters of the participants could imagine clicking on one of the search suggestions, with the same three-quarters being interested in the suggestive headline “Olaf Scholz caught in a club”. While we had seen this suggestion regularly throughout the study, we found no relation to a factual incident, nor did we find any videos on the platform mentioning anything comparable.

{% include plotly.html data="/assets/plotly/2024-07-search-suggestions-clicks.js" id="b612f88e-48fa-4884-b238-d6e92cca10bf" caption="Basis: All TikTok users. Missing values: I don't know. Deviations due to rounding. " width="100%" %}

Later in the survey, we returned to the search suggestions user had seen had seen earlier and asked participants which specific suggestions they were able to recall. We also gave several additional suggestions we had collected from the app which we had not included in the first steps of the survey.

As the graph below shows, the participants overwhelmingly correctly identified the search suggestions they had previously seen, even with accuracy on the level of the exact wording, although they had not planned to click on them.

{% include plotly.html data="/assets/plotly/2024-07-search-suggestions-recall.js" id="a245abbe-2a2e-468f-99e6-607909e3021e" caption="Basis: All TikTok users. Missing values: I don't know. Deviations due to rounding." width="100%" %}

### **Search Suggestions Are Deeply Integrated**

Over the last few years, TikTok has expanded its search suggestion features to different elements of the mobile app. We found them integrated in four parts of the user interface:

1. Search suggestions appear below the search bar, when users click the search icon on the top right of the For You Page (FYP). These search suggestions are a mixture of trending topics and personalized entries based on the recently watched videos and long-term interests of the user. (We have analyzed these [search suggestions in the past](https://tiktok-audit.com/blog/2023/Israel-Hamas-War-Suggestions/) outside of this study. We recommend  [Zear.ch](http://zear.ch/) which collects and visualizes these search suggestions in Germany frequently.)
2. Occasionally, a similar list of suggestions is embedded into the FYP as a separate slide users see between videos. Similar to the suggestions on the search bar feature, they combine personalized and trending suggestions.
3. Video-specific search terms are sometimes suggested at the bottom of the screen below the video itself, or above the comments in the comment section. Previous [news reports](https://www.washingtonpost.com/technology/2024/02/08/tiktok-search-suggestions-inaccurate/) have highlighted how [suggestive search terms](https://chaos.social/@mrtn3000/111940386591964823) in the videos below can negatively impact the creators of those videos.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-07_searchsuggestions_video_1_h.png"  class="img-fluid rounded z-depth-1" zoomable=true width="50%" %}
        <div class="caption">Screenshot of a video on TiKTok with a single search suggestion at the bottom of the page.</div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
{% include figure.html path="/assets/img/2024-07_searchsuggestions_video_2_h.png" class="img-fluid rounded z-depth-1" zoomable=true width="50%" %}
<div class="caption">Screenshot of the TikTok app with a single search suggestions at the top of the comment section.</div>
    </div>
</div>

4. Search suggestions are also embedded in the display of search results. As Figure 3 shows,  we find eight so-called “Others searched for” search suggestions below the first two videos (of TikTok’s mobile app) that match the search query. Specifically, the “Others searched for” suggestions are the focus of this study. 

{% include figure.html path="assets/img/2024-07_searchsuggestions_greens.png" alt="Screenshot from TikTok showing search suggestion for 'The Greens' in July 2023. Suggestions include 'putin wars turkish people in Germany', 'cdu' and 'habeck wife left'" class="img-fluid rounded" zoomable=true width="50%" %}

Amongst researchers and experts, it is still unclear how these search suggestions are generated. TikTok claims they are based on [user-generated searches](https://www.spiegel.de/netzwelt/web/tiktok-warum-macht-die-app-so-seltsame-suchvorschlaege-a-cd4e4798-c078-4737-bf42-b0c887ed4263). This, however, does not explain the order of the suggested searches, their moderation, or the lack thereof. In a first exploratory analysis in Fall 2023, we tried to understand the extent of embedded personalization and found that the search suggestions on the search page are indeed highly personalized. The suggestions continuously vary across TikTok sessions, as they adapt to recently viewed videos. Still, we found that the most common search suggestions, which we measured by scraping the search suggestions from non-logged-in users, also often appeared in the list of search suggestions for logged-in users at the beginning of their sessions (e.g. when they opened a search feature for the first time that day).

# Case Study on Search Suggestions Before the EU Elections

To collect TikTok’s “Others Searched For” suggestions, we compiled a list of queries of German political parties and politicians who were active candidates for the 2024 European Parliament elections. This query list consists of 9 parties and 51 politicians, evenly distributed among the parties. When applicable, we included the full name of parties as well as their commonly used abbreviations (e.g., “Sozialdemokratische Partei Deutschland” and “<abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr>”). Based on these queries, we collected the “Others Searched For” suggestions data two times a day throughout one month before the parliamentary elections in June 2024 using a server with a German IP address. This study focuses on the 20 most common suggestions per party or candidate, to limit the scope to relevant search suggestions. In total, we collected 89780 search suggestions, of which 3740 are unique. The combination of the 20 most common suggestions for parties and candidates resulted in 531 suggestions, of which 208 were shown for parties and coded.

We then developed a coding scheme to specifically address the questions of what the “Others Searched For” suggestions look like and the extent to which they push false or potentially harmful narratives in political contexts. In the context of election-related searches, we identified 8 main suggestion type categories, or type labels: `No Suggestions`, `Unrelated`, `Diversion`, `Insights`, `Clickbait`, `Suspicious`, `Dog Whistle`, `Other` (see Table below). We applied these categories to the “Others Searched For” suggestions as multiple choice labels, meaning that these type labels are not mutually exclusive to one another since there are considerable thematic overlaps amongst the suggestions. The coding is always specific to and contextualized with the respective query, meaning that a search recommendation shown for different political queries might not be coded the same way if its respective political implications differ. Certain suggestions appear multiple times across different parties or candidates but have different implications for the query itself based on the respective political context.

The data was collaboratively coded by two researchers from AI Forensics and Interface. This collaborative approach was taken to ensure a high level of reliability and validity of the data and following analysis, as well as for consistency purposes of the coding process.


| Type Label | Label Description | Example 1  | Example 2 |
| --- | --- | --- | --- |
| No Suggestion | The are no search recommendations for the initial search query.  | Query: <abbr title="Alternative für Deutschland">AfD</abbr> Suggestion: “-” | Query: Christlich Soziale Union Suggestion: “-” |
| Unrelated  | The search recommendation does not directly refer to or is related to the initial search query, nor does it carry potentially harmful implications. This label cannot be used with another. | Query: <abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr> Suggestion: “Michaela Schaffrath” | Query: Freie Wähler Suggestion: “tiktok deutschland” (engl. ‘tiktok germany’) |
| Diversion | The search recommendation redirects the reference and does not refer to initial search query itself, but refers to another party or politician.  | Query: Die PARTEI Suggestion: “bsw partei” (engl. ‘bsw party’) | Query: Bündnis Sahra Wagenknecht Suggestion: “annalena baerbock”  |
| Insights | The search recommendation relates to harmless, factually oriented information about the queried party or politician. The search recommendation is related to the politician or party directly in relation to current news, facts, interviews, interactions with other politicians, etc. | Query: <abbr title="Christlich Demokratische Union">CDU</abbr> Suggestion: “cdu politiker jung” (engl. ‘cdu politician young’) | Query: Die Grünen Suggestion: “grüne jugend” (engl. ‘green youth’) |
| Clickbait | The search recommendation refers to distinct attention-attracting headlines such as news, but can also imply a spread of rumors, gossip, and/or potential misinformation, that reflect unverified (or false) claims about the politician or party.  | Query: Sozialdemokratische Partei Deutschland Suggestion: “wahlen deutschland 2024” (engl. ‘elections germany 2024’) | Query: Alternative für Deutschland Suggestion: “erdbeben deutschland heute 2024” (engl. ‘earthquake germany today 2024’) |
| Suspicious | The search recommendation may or may not directly refer to or relate to the initial search query, but it contains content that could potentially have politically-motivated, sexual, nationalist, or slanderous implications. | Query: Alternative für Deutschland Suggestion: “ganz deutschland weint” (engl. ‘all of germany cries’) | Query: Freie Wähler Suggestion: “venus unzensiert” (engl. ‘camel toe uncensored’) |
| Dog Whistle | The search recommendation ishttps://en.wikipedia.org/wiki/Dog_whistle_(politics), disinformation, slander, or unfounded conspiratorially-leaning theories that suggest secretive and harmful activities or mindsets. This could also describe a direct campaign against a party or politician. | Query: Sozialdemokratische Partei Deutschland Suggestion: “deutschland muss deutsch bleiben” (engl. ‘germany musst stay german’) | Query: Alternative für Deutschland Suggestion: “warnung deutschland 2024” (engl. ‘warning germany 2024’) |
| Other: | The search suggestion does not fall into any of the categories above.  | Query: Die Linke Suggestion: “opas gegen links” (engl. ‘grandpas against the left’) | Query: Freie Demokratische Partei Suggestion: “welche partei wählen” (engl. ‘vote for which party’) |

## Others did *not* search for…

Throughout the “Others Searched For” data of party and candidate queries, we surprisingly found that many queries did not return any search suggestions. From 60 query terms, the search suggestions for 21 consistently returned no results, as seen in the Table below. This indicates that the platform intervened to specifically disable the search suggestion for these search terms, e.g., through a blocklist. The `No Suggestions` label was applied to queries “<abbr title="Alternative für Deutschland">AfD</abbr>”, “<abbr title="Bündnis Sahra Wagenknecht">BSW</abbr>”, “<abbr title="Freie Demokratische Partei">FDP</abbr>” and “Christlich-Soziale Union” and various political candidates too. Across party affiliation, the <abbr title="Alternative für Deutschland">AfD</abbr> and the <abbr title="Christlich-Soziale Union">CSU</abbr> seem to have the most no-result queries, closely followed by Die Grüne. 

Interestingly, most no-result party queries like “<abbr title="Alternative für Deutschland">AfD</abbr>”, “<abbr title="Bündnis Sahra Wagenknecht">BSW</abbr>”, and “<abbr title="Freie Demokratische Partei">FDP</abbr>” are party abbreviations that are quite frequently used. However, the non-abbreviated “Christlich-Soziale Union” as well as abbreviations such as “<abbr title="Christlich Demokratische Union">CDU</abbr>”, “<abbr title="Christlich-Soziale Union">CSU</abbr>”, or “<abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr>,” which do return search suggestion results, show that no-result queries are not consistent across specific abbreviations. Among the list of candidate names that yield no results are Maximilian Krah and Petr Bystron from the <abbr title="Alternative für Deutschland">AfD</abbr>. Both are known to be [“scandal-plagued”](https://www.politico.eu/article/far-right-AfD-group-alternative-for-germany-expel-maximilian-krah-scandal/) politicians who have been publicly and controversially discussed across mainstream media. However, most other no-result candidates seem somewhat scandal-free. Most of them are also not top contenders for their party and might be less known within the TikTok space. The lack of clear theme inconsistencies across no-result party queries raises questions about how and why specific queries are blocked or moderated by the platform.

| Blocked Query | Party Affiliation | Query Type |
| --- | --- | --- |
| <abbr title="Alternative für Deutschland">AfD</abbr> | <abbr title="Alternative für Deutschland">AfD</abbr> | party |
| Maximilian Krah | <abbr title="Alternative für Deutschland">AfD</abbr> | politician |
| Petr Bystron | <abbr title="Alternative für Deutschland">AfD</abbr> | politician |
| René Aust | <abbr title="Alternative für Deutschland">AfD</abbr> | politician |
| <abbr title="Bündnis Sahra Wagenknecht">BSW</abbr> | <abbr title="Bündnis Sahra Wagenknecht">BSW</abbr> | party |
| Jan-Peter Warnke | <abbr title="Bündnis Sahra Wagenknecht">BSW</abbr> | politician |
| Andrea Wechsler | <abbr title="Christlich Demokratische Union">CDU</abbr> | politician |
| Norbert Lins | <abbr title="Christlich Demokratische Union">CDU</abbr> | politician |
| Christlich-Soziale Union | <abbr title="Christlich-Soziale Union">CSU</abbr> | party |
| Angelika Niebler | <abbr title="Christlich-Soziale Union">CSU</abbr> | politician |
| Monika Hohlmeier | <abbr title="Christlich-Soziale Union">CSU</abbr> | politician |
| Markus Ferber | <abbr title="Christlich-Soziale Union">CSU</abbr> | politician |
| <abbr title="Freie Demokratische Partei">FDP</abbr> | <abbr title="Freie Demokratische Partei">FDP</abbr> | party |
| Andrea Menke | Freie Wähler | politician |
| Gregor Voht | Freie Wähler | politician |
| Terry Reintke | Die Grüne | politician |
| Anna Cavazzini | Die Grüne | politician |
| Michael Bloss | Die Grüne | politician |
| Martin Schirdewan | LINKE | politician |
| Özlem Alev Demirel-Böhlke | LINKE | politician |
| Maria Noichl | <abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr> | politician |

## From Diversion to Dog Whistles: Coding Suggestions for Political Parties

In the following, we provide an overview of common themes we identified in the coded data based on party queries, specifically. The graph below shows the distribution of type labels used to code the party data. As previously mentioned, each search suggestion could have been coded with multiple labels, whilst some are mutually exclusive and others simply matched one type label.

{% include plotly.html data="/assets/plotly/2024-07-search-suggestions-coding.js" id="0c4177cf-215e-473d-930b-2ea5fa23ceca" caption="Representation of all label percentages" width="100%" %}

Our findings show that 31% of the suggestions were entirely unrelated to the queried German political party. The Unrelated label is the only label that was not paired with any other label (with one exception: query ”<abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr>” and suggestion “vomex”). Among the remaining 69% we identified as related, suggestions could have been either in direct relation to the queried party, or diverted to another. In total, we found Diversion across 26% of all search suggestions, as seen in the query for “<abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr>” suggesting “<abbr title="Alternative für Deutschland">AfD</abbr> aktuell” or the query for “Bündnis Sahra Wagenknecht” for “alice weidel”. The interactive Alluvial graph below displays not only the proportions but also the immediate redirection of one party to another. This graph shows that the <abbr title="Alternative für Deutschland">AfD</abbr>, Germany’s far-right party, was disproportionally mentioned in the search suggestions of other parties. We see this as a crucial ill-equilibrated misrepresentation of German parties and what they stand for. The <abbr title="Alternative für Deutschland">AfD</abbr> is likely the most active party on TikTok, which is a possible explanation of their overrepresentation. However, the disproportionate leveraging of its visibility within the search suggestion feature clearly perpetuates this imbalance. This is a distinct indication of TikTok prioritizing engagement and virality over quality, messaging, or proportional representation of political parties on their platform. 

{% include plotly.html data="/assets/plotly/2024-07-search-suggestions-diversions.js" id="ddb5573e-11ca-4816-8845-808c816cafdd" caption="Interactive Graph of Diversions based on search suggestions for a party that we labeled as diversion (left) and the party referenced in the search suggestion (right)" width="100%" %}

Roughly 31% of all suggestions were labeled as `Insight`, representing informational inquiries in relation to political parties or candidates, eg. query “Die Grünen”, suggestion “habeck right now” (habeck aktuell). While thematically similar to `Insight`, `Clickbait` refers to 12% of all suggestions, which directly imply intentions of gossip, rumors, clickbait headlines, or disinformation as seen in the query “Die Grünen” with the following suggestion of “habeck frau weg”. This specific suggestion, which translates to *‘Habeck’s wife leaves’* insinuates a gossip-like curiosity based on a spread of false information on Green politician Robert Habeck for the sake of a seemingly news-worthy headline that has little political implications. Furthermore, the `Suspicious` label was applied to 13% of the suggestions, as seen for the query “<abbr title="Sozialdemokratische Partei Deutschland">SPD</abbr>” and sexualized suggestions “bisexual princess” or for the query “Alternative für Deutschland” which suggests *‘all of Germany cries’* (“ganz deutschland weint”), which subtly insinuates nationalist motives. 

More explicitly, `Dog Whistle` was applied to 8% of all suggestions. This label category includes suggestions such as *‘Putin warns Turkish people in Germany’* (“putin warnt türken in deutschland”) for queries such as “Die Grünen” or “Sozialdemokratische Partei Deutschland”, or  *‘Christian Lindner [the German minister of finance and head of <abbr title="Freie Demokratische Partei">FDP</abbr>] threatens Germany’* (“christian lindner droht deutschland”), indicating contentious campaigns and fear-mongering messaging. We have observed a correlation between what we categorized as `Dog Whistle` and how the queries and suggestions are formulated. While most `Dog Whistle` suggestions contain the word “**deutschland**” (*’Germany’*), so do the party queries such as “Sozialdemokratische Partei **Deutschland**” or “Alternative für **Deutschland**” in which we have come across what we would attribute to this label. While this may explain the presence of what we interpret as highly nationalist content in the “Others Searched For” suggestions, the easily-made conspiratorial associations are yet equally present and, nonetheless, pose an extreme threat to how we consume political information concerning party-specific contexts. 

For the parties specifically, we have found connections of term-based overlaps (often homonyms) in 33% of all party queries and resulting suggestions. This can be seen with the query “Christlich-Soziale **Union**” and suggestions “1 fc **union** berlin” (a German soccer team) or query “**Alternative** für Deutschland” and suggestion “**alternative** girls”. However, this observation extends beyond party queries and is represented in 13% of the dataset that includes candidates specifically. We have found this in examples such as the query “**Andreas** Schwaab” and “psycho **andreas**” (a reality TV personality), query “Joachim **Streit**” and suggestion “freund **streit**” (translates to ‘friend fight’, ’Streit’ being the politician’s last name but also meaning ‘fight’ or ‘argument’). This implies that “Others Searched For” suggestions are curated by the association of single terms that can be found in both the query and the respective search suggestion itself, even if there is no political (or thematic) correlation between the two outside of the terminology they share.

Moreover, while this was not the focus of our research, we found strong anecdotical evidence for gendered stereotypes and hypersexualization amongst our selection of politicians, which warrants crucial further investigations.

# Discussion

Search suggestions are an integral part of the TikTok use experience. The feature is rolled out in different elements of the platform and is generally becoming increasingly important for young users. While search suggestions are highly personalized, they also contain a recurring theme of “trending” searches around specific topics that users recall, even without checking their validity. Our study highlights crucial issues of search suggestions within an electoral context. We found that they perpetuate an imbalance in the representation of parties, highlight clickbait over informative facts, and even include various dog whistles or conspiracies. This aligns with [previous research by Crossover, a Finnish civil society organization, which studied search suggestions for Finnish accounts.](https://crossover.social/wp-content/uploads/2024/07/TheTiktokEffect.pdf)

We have multiple hypotheses about the reasons for this behavior. Oftentimes there is no apparent relation between a search suggestion and the quality of the results it will bring up, indicating that their appearance and order are driven by measured engagement with the search suggestions themselves (in the form of clicks) instead of a more qualitative measure like whether or not the results where helpful to the user. While this can be frustrating for users (who do not find what they are looking for), engagement-driven behavior can perpetuate even false narratives about individuals and parties.

Another hypothesis about the origin of odd search suggestions is the issue of [data voids](https://datasociety.net/library/data-voids/). Search algorithms return results regardless of the quality of their results. On sparse data, this can lead to fringe or unrelated results which, especially in the context of the search feature, lead to word lists with no apparent connection, for which the human mind and curiosity, however, create strong associations nonetheless. As described above, many contentious search suggestions are based on homonyms (eg. for politician Joachim Streit, who is not active on TikTok but whose last name is also a common German noun).

Although we are still left to speculate on how TikTok curates its search suggestions, we see two better solutions for improvement: disabling the feature or adding consistent content moderation. TikTok seems to already apply this but does so inconsistently and in a highly non-transparent way. We have continuously studied search suggestions since 2023 and have observed some improvements for the search suggestions below the search bar (meaning fewer bad suggestions). However, these improvements do not translate to the “Others Searched For” feature. Moreover, the simplest solution of enabling these search suggestions is applied only to some queries (one-third of our set). Unlike what our findings have shown, disabling the feature for political parties and candidates should be done so in a consistent manner.

## Search Suggestions Are a Systemic Risk for Public Discourse

The starting point of our analysis was our scenario on the systemic risks of search suggestions for the public discourse. We think the combination of our results from our user and case study shows that this feature poses a systemic risk. Young adults who actively rely on TikTok’s search feature to get information on the European parliament elections in Germany will have experienced a distorted version of reality, likely of an overemphasis on specific parties or the presence of clickbait suggestions.

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

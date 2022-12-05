# Recommender goals
The ultimate goal of the app recommendation is to improve DAU *(MD: daily active users)*.

Retention and DAU are positively correlated in most cases: when retention rises, the DAU will generally rise, and when retention declines, the DAU will generally fall.
As an indicator, retention has many advantages over DAU. We currently mainly optimize the retention indicator. App usage time is also a very important indicator.
App usage time is also a very important indicator.It is generally believed that the length of time the app is used can reflect the user's satisfaction with the app that day.Retention is an indicator that can only be observed after one or more days, and the noise is often relatively large.
The use time is faster than the retention feedback, and it is easier to test the experimental benefits, and most of the changes in experiments to increase the length of use time have improved retention, so the use time is considered to be an approximate indicator of retention.

## Recommender Sorting Model

The purpose of the recommendation of the recommendation model is to rate the candidate videos according to a formula, and return the videos with the highest scores to the user.

The form of the sorting formula is this: 

(IMG TITLE )What content recommendation does is to rate the candidate videos according to a formula, and return the videos with the highest scores to the user:


	  P_like × v_like + P_comment × v_comment + E_playtime × U_playtime + P_play × v_play

So what is the specific meaning of this formula?

Users can make various interactions with the video they see, and these interactions reflect the user's preference for this video.

For example, it is better for users to like than not to like, it is better to finish reading than not to finish reading, and it is better to dislike than dislike.(??)

In other words, every interaction a user has with the video they watch has positive or negative value.

The app's recommendation sorting model assumes that the value obtained by users watching a video is equal to the sum of the value of all interactions that occur on the video.

The goal of the recommendation system is to push the most valuable videos to users.

[Page2]
In order to calculate the value of video playback, we introduced a value model (v) to measure the value of the interactions that occur.

If a video is liked by the user after it has been viewed, and no other interaction has occurred, then the actual value of this video viewing is added.


	 v_like + v_play

caption: If a video is liked by the user after it has been viewed, and no other interaction has occurred, then the actual value of this video viewing is added.


When the recommendation service selects the video to be pushed to the user, the user has not seen the video, and the interaction that will occur is unknown, so the precise value of the video playback cannot be calculated.

In order to complete the scoring without knowing the actual interaction of the user, we need to use the prediction model (p) to predict the probability of each interaction, and replace the actual value in the above formula with the expected value of the value created by this video playback.

The formula we get at this time is the beginning of the above exhibition
The form of display: the value of actual occurrence.

The formula we get at this time is the form shown at the beginning above.:

	 P_like × v_like + P_comment x v_comment + E_playtime × v_playtime + P_play × v_play

This is the formula for recommending services to sort videos (the meaning of play here is to play, and a video will be played as long as it is launched, so p_play is always equal to 1, which is written to be consistent with other forms of interaction).

What the recommendation service actually does is to use this value formula to rate all videos, and return the videos with the highest scores (that is, the videos with the highest value creation) to the user.

For brevity, this doc uses an extremely simplified formula.The sorting formula actually used online is much more complicated than the one above, but the logic behind it is the same.

## Predictive model

[Page3]
A predictive model is a model that predicts the probability of various interactions (or more broadly, all unknown things at the time of sorting) happening.Predictive models are generally machine learning models. They use video and user-related data as input to output the probability of something happening.

Common predictive models include: like model, comment model and other models that predict whether interaction will occur.

A model that predicts a specific value such as playback time, personal page stay time, etc.

A model for classifying content such as likes, fake comments, etc.

The input characteristics of the prediction model can be divided into such parts:

1. User-related information, such as user id, user region, user historical interaction statistics, list of video ids that users have recently watched, etc.

2. Video-related information, such as video id, video duration, what stickers are used in the video, video interaction statistics, video content, and so on.

3. Author-related information, such as author id, author's number of fans, author's historical statistics, etc.

4. There is also a lot of other information, including the experimental group where the user is.

The prediction model is personalized. A model often gives different estimates for the same video, on different viewers, or in different environments of the same viewer.

For example, the like model predicts the probability that the current user will like the current video when they see the current video in the current scene.

For a star's video, the probability of his fans and non-fans liking it may be different, this is clear.


## Value model

A value model is a model that gives value to interaction.

The value of interaction is mainly divided into these types:

1. User value.The value created for the users to whom the current video is pushed.Mainly for current users. Duration, retention, and satisfaction.

[Page4]
2. Author value.The value created for the author of the video, including the traffic, interaction, income, etc. obtained by the author.

3. Platform value.The value created for the platform.Including brand effect, content security, platform revenue, etc.

4. Indirect value.The value generated indirectly by the playback of this video (the user who is not in this playback, the author above, and the platform is not directly generated), such as the notification received by other users after commenting, may increase the retention of other users (the user value of other users), the impact on the content ecology (the author value of other authors) and so on.


Every interaction of a user may have one or more of the above values. For example, a value formula for likes is:

> v_like=1+u_like_cnt×0.01-same_tag_today×0.5+is_vv_lower_than_100×10-is_like_bait*100

			User value   -    User value (Long-term) +   Author value + Platform value

The user likes a video, indicating that the user likes the video, so the likes should be positive.

User value (1 in the formula above).The more likes users have clicked on the same type of content today (same_tag_today), the more it is available for use. User likes
Increased the number of likes of this video, which has an motivating effect on the author (especially in low likes)
(Pointer to is_vv_lower_than_100)), so there is no place.

If the video is a fraudulent like frequency, giving them too many likes may affect the overall ecology, so the likes on the fraudulent like video (is_like_bait) may have (negative) platform value.

The value model is our understanding of what videos should be recommended to users. It needs to be adjusted and speculated repeatedly in order to achieve the best results.

In most cases, our optimization of the value model is to better decompose the value of each interaction clearly, and write the decomposed value formula into the fusion formula to maximize the benefits of video recommendations.
The following is a breakdown of the value model of the main feed:

[Page5]

According to this decomposition, we will optimize the user's likes, comments, completion, author's contribution rate, retention, revenue, live broadcast, social, poi and other functions penetration rate and other goals.

## Limitations and solutions of the above model

The sorting model described above can be used to solve most of our problems, but there are also many problems that need to be solved in other ways, such as:

**Some value is created through the combination of multiple videos.**
Continuous exposure of the same follower may change the user's perception of the follower (for example, seeing an author's video continuously may change the user's perception of the follower).
Let users have a deeper impression of the author, so that they are more willing to continue watching his videos, and even take the initiative to search /browse whether the author has posted new videos, etc.
As another example, some authors' videos may have some stems. Only by watching more of this author's videos can we better get the author's points).
Therefore, the total value of these videos watched by this user is greater than the sum of the values of each individual video watched.
For example, a user likes certain types of videos, but if he keeps pushing such videos to him, he may quickly become bored and close the app.
The total value of this user watching these videos of the same type is less than the sum of the value of watching each individual video, because the homogenization of these videos leads to the more users watch, the easier it is to get tired.
There are two solutions to this kind of problem: make some assumptions and split the value into the value formula. For example, for the continuous exposure problem of followers mentioned above, it can be approximated by adding a value of "same_author_seen", and the problem of similar video boredom can also be solved by adding a negative value of "same_tag_today".
Such problems can also be solved by methods other than the value formula, such as forced insertion, breaking up, and internal strategies.
For example, the problem of boredom with similar videos can be solved by breaking up.

**Problems caused by inconsistencies between the pre-stage of the value model and the value model.**
As will be mentioned below, the recommendation architecture is divided into multiple stages, and the value model is applied in the last stage.
If the goals of the value model are inconsistent with the goals of the pre-stage, it may be necessary to solve the problems of the pre-stage.
Give an example: when trying to make a social direction, you may need to return more friend videos to the user, but if the videos of these friends are not recalled in the recall stage, then adjusting the value model will not work. .
The problems in the recall stage need to be solved first in order to better achieve the goal.

The model does not optimize the ultimate indicator (WIP = Work in Progress)

## Model Optimization

[Page6]
## Vision

We hope to transform the problem into a problem within the above framework (value model + predictive model) as much as possible to solve it.

The main reason for this is:

1. This framework is a good abstraction of the video recommendation problem, and most of the problems can be solved well with this framework.
2. Because of long-term accumulation, within this framework, our development costs are the lowest and our testing and analysis tools are the most complete.
3. Most of the previous experiments are based on this framework, and the accumulated experience can help us better complete new attempts.

## Methodology

To make a strategy, you need:

1.** Clear goals**.
Think clearly about what the ultimate goal of this strategy is (user value, author value, revenue, etc.).
The ultimate goal must be one of the three values of user value, author value, and platform value. Projects that have no value to these three must have no value.

2. **Decompose the problem**.Goals can be divided into multiple dimensions: the ultimate goal refers to the value to be created, including author value, user value, and platform value.
Indirect goals refer to indicators that may be improved by the strategy and have a certain causality with the ultimate goal, such as content diversity, user like rate, etc.
The direct goal refers to the indicators of the direct optimization of the strategy. For example, the direct goal of optimizing the like model is the prediction effect (logloss) of the like model.
The decomposition problem refers to the decomposition of the things to be done to complete these layers of goals.Let's look at a few examples of target decomposition:

The target decomposition of the cheat praise model is:

First of all, the suppression of fraudulent videos is ultimately to improve user retention and combat opportunistic actions.
To give normal authors better incentives, this is the ultimate goal of the project.Reducing the submission and vv of fraudulent videos may be helpful to the ultimate goal, because it will enhance users' impression of the platform and reduce the traffic that opportunistic authors get on the platform.

[Page7]
![[Pasted image 20221130173121.png]]


In order to reduce the distribution of fraudulent like videos, we need a fraudulent like model to label the videos with fraudulent likes. So what we have to do in the end is to make a good enough cheating model.

The goal decomposition of the differentiated quantity preservation project is:

![[Pasted image 20221130173617.png]]

The causal relationship between the two adjacent targets in the target decomposition chain needs to be reliable enough to ensure the correctness of the entire target decomposition chain.
The criterion for "reliability" is either that there is a sufficiently clear causal relationship logically, or that there is sufficient data verification.
Starting from the effectiveness of the entire link, there are two principles for the decomposition of the target:
The higher the reliability of each layer of causality, the better, and the shorter the chain, the better.
In the process of goal decomposition, one of the easier mistakes to make is to confuse these layers of goals, or [Page8] to ignore the changes in one layer.

For example, optimizing the like model only depends on whether the likes have risen, ignoring whether the effect of the like model has improved, generally ignoring the direct goal, or equating the direct goal with the indirect goal.

1. **Develop strategies.** Develop relevant strategies and test them based on goals and directions that we think may be profitable.In the recommended scenario, the optimization of the strategy can be divided into several types:

2. **Optimize the indicators corresponding to a certain goal on the chain**, such as improving the AUC(_area under the curve_) of the cheating model, and the benefits of the direct goal are passed to the final goal through the problem decomposition chain, and the benefits of the final goal are obtained.

3. **Better break down goals.** What the goal of better decomposition is to do is to replace the current causal chain with a better causal relationship (mentioned above, the higher the reliability of each layer of causal relationship, the better, and the shorter the chain, the better) chain. For example, in the differentiated quantity preservation project, we currently use to predict whether a video will catch fire to judge how much the video should be preserved, the more likely it is. The more fire protection, the more problems this indicator actually has. If this indicator can be replaced with a better indicator, the optimization effect will be better later. For example, if you change it to how much vv is guaranteed, the subsequent user-side distribution effect (such as how much vv is obtained) can exclude videos that can be distributed well even without cold start support, saving traffic for videos that are not so easy to distribute and require a cold start.

4. **Design experiments.** The design experiment is mainly to clarify such elements: the way the experiment is opened, and the reality. The core indicators and expected returns of the experiment and observation, the intermediate indicators and direct indicators in the target decomposition chain, and the expected changes in these indicators.The core indicators are used to determine whether the experiment has achieved its purpose (the benefits in Step 1), such as supporting certain types of authors, it should be seen whether the retention of contributions by such authors has improved. Intermediate indicators are used to determine whether the experiment is turned on correctly. Generally speaking, **the indicators to be observed in the experiment are the summaries of the indicators to be observed at each layer in the target decomposition diagram.** After clarifying the indicators that need to be observed, according to the indicators that need to be observed, determine the way to start the experiment, including: whether to watch the consumer side or the author side in the experiment, the flow rate of the experiment, the parameters of the experiment, the time the experiment needs to be observed, etc. These elements are clear and very important when starting the experiment. Think clearly about these elements in advance so that the experiment can be carried out correctly, and it can also avoid the problem of subjectively interpreting the experiment based on the results, shooting arrows first and then drawing a handle.

5. 5. **Check the experimental results.** Check whether the experimental results meet expectations, and if they meet expectations, determine whether it needs to be online. If it does not meet expectations, it is necessary to analyze the experiment, make changes to the program based on the analysis or abandon the attempt.The experiment meeting expectations means: **The income of the core indicators meets expectations, so 

[THERE PAGES MISSING HERE]
[Page9]

3. A more reasonable split of the value of each interaction goal.This is the most common optimization method. Optimization often corresponds to a deeper understanding of the product, such as:
4. Long videos are distributed directly, why has the number of click challenges dropped by 80%?
5. Some users have a like rate of 50%+, and some users never like them. What is the difference between the value of likes between these two types of users?
6. Is the value of a like for a video with a 10% like rate the same as a like for a video with a 1% like rate?
7. Some users will use the collection function, and some users will use the like function as a collection function. How to consider the significance of these two interactions?
8. Should clicking to follow include following after clicking into the personal homepage?
9. Should it be considered an action to click on the avatar to enter the personal homepage, and click on the name to enter the personal homepage?

# Recommendation architecture

This part gives a brief description of the recommendation architecture, understands the common concepts of the recommendation architecture, and helps to communicate better with the recommended colleagues.

## Recommended process

When a user swipes the app, the appapp will request a recommendation service to return the video to the user to watch.
The process of recommending services is roughly divided into these steps:
![[Pasted image 20221130182314.png]]

1. Filter video
[THERE PAGES MISSING HERE]
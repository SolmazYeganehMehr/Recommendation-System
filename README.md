# Recommendation-System
* Spyder is a package we use to build the Recommender System.
From Anaconda, install and launch Spyder environment, There you can run the code.


## Introduction and how they work

The data for a recommender system comes from different sources. To recommend things that we might like, a platform (such as Netflix or Amazon) with a recommendation system needs data about us, our tastes and interests, as an individual user, and merge it with the collective behavior of everyone else like us.  

##### But where does that data about our unique interests or interest of our costumers come from? 

One way to understand our users or customers is through explicit feedback. For example, asking users to rate a content or product, \ on a scale of one to five stars or rating if they like or dislike, gives a thumbs up or a thumbs down and, we use that data to build up a profile of that user's interests. The problem with explicit ratings or feedback is that requires extra work from our users/costumers. It they do not participate we will have a very sparse data that leads to low quality recommendations. 

Another way to gather data about our users/costumers tastes is through implicit behavior. This is looking at the things they do anyhow and interpreting them as indications of interest or disinterest. For example clicking on a link, a product, or an ad.

Click data is great because, there is so much of it so we do not have problems with data sparsity. But clicks are not always a reliable indication of interest. People often click on things by accident. Purchase data is a much better indication of interest because actually opening up your wallet and spending our hard earned money is a sure sign that we are interested in something, well unless it's a gift but that's its own problem. 

Another implicit source of interest is consumptions data. For example, how many minutes’ users spend watching a video is an indication of how much they like it.

When we design a recommender system, it is important to think about what sources of data we have about our user's interests and start from there because even the best recommender system cannot produce good results unless it has good data to work with and lots of it.

##### The purpose of a recommender system
Note that the job of a recommender system is not to predict what would be a user’s rating for everything that they have not rated already, BUT, to produce a top-N list of the best things to present to a given user. Our recommender systems are successful if we are able to find the best top recommendations for our users/costumers.


## How to measure if our Recommendation System acts properly?

Normally we calculate Accuracy of our models by RMSE or MAE. These are to measure how well the model predict the future act. But, they are not suitable for Recommendation System, because as we said with the Recommendation System models we do not want to predict which movies people are likely to watch, but we would like to know how the people react to the Top N list of movies that we recommend to them.



#### Metrics to measure the effectiveness of the Recommendation System
The different ways to measure the effectiveness of top n recommender’s offline in the Recommendation System are:

- Hit rate
- Live-one-out- cross validation
- Average reciprocal hit rate (ARHR)
- Cumulative Hit rate
- Rating Hit rate (rHR)

#### Coverage: 
the percentage of possible recommendations that your system is able to provide

####  Diversity:
a measure of how broad a variety of items your recommenders system is putting in front of people.. If we look at the similarity scores of every possible pair in a list of top n recommendations, we can average them to get a measure of how similar the recommended items in the list are to each other. Diversity is opposite of similarity. We subtract Similarity from 1 to get a number associated with diversity. High diversity is not always a good thing, because by just recommending very random items you can achieve a high diversity. You need to look at diversity alongside metrics that measure the quality of the recommendations as well.

#### Novelty: 
Your recommendation system should recommend at list few popular items; there is a reason why those items are popular. If the users have not heard of any of items you are recommending, they may think you do not know them o your recommendation system is not good. Your recommendation system should be a balanced mix of the familiar items to build trust with the users and the new items that the users can discover and they might love.

#### Churn:
how often do the recommendations for a user change? The recommendation system should change by the new behaviour of the users. If we recommend the same items repeatedly to the users and they do not click on the item, we do not have a good Recommendation System. 
 
#### Responsiveness:
How quickly does new user behaviour influence your recommendations? It is good that your system be responsive, but instant responsiveness make your system too complicated. This is determined by the business and you need to keep a balance between responsiveness and simplicity.

#### A/B testing (the most important test)
All these metrics should be looked at together and we need to understand the trade offs between them. But the real test of the Recommendation System is achieved by A/B testing.

We use AB testing to tune our recommender system using the real customers and measuring how they react to the recommendations. We put recommendations from different algorithms in front of different sets of users and measure if they actually buy, watch, or otherwise indicate interest in the recommendations we have presented. By always testing changes to our recommender system using controlled online experiments, we can see if they actually cause people to discover and purchase more new things than they would have otherwise. None of the metrics matter more than how the real customers react to the recommendations we produce in the real world	



# DSI_Project_3

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification

---
### Problem Statement

I work as an IT consultant who has a project with Reddit. The problem that Reddit found is the similar movies named 9-1-1 and NCIS have subreddit, but some users do not know the name of the subreddit that make them cannot post the new post or create the post in the wrong subreddit. Therefore, Reddit wants to try a model to collect the post from the user and select the subreddit for the user and increase more efficiency to manage the wrong post in subreddits.

---
### Executive Summary

Reddit is a big online community that has many subreddit, but this website does not have the feature to recommend the user about the relevant subreddit with their post. The model classification is introduced to increase the convenience when the user want to post but they do not know which subreddit that they should select and the model also decreases the wrong post in the subreddit. 9-1-1 and NCIS is the action drama which have many similar points so Reddit wants the model to separate the post before sending the post to the subreddit. The model in this work has accuracy at 87.5% and the word classification shows the user usually talk about 'Buck' which is the main character in 9-1-1. After using the model, Reddit will get a more clean subreddit (lower number of wrong posts) and improve the quality of the website.

---
### Conclusions and Recommendations

**Model and Word Evaluation**


The best model in this work is the model by Naive Bayes with TF-IDF Transformation. This model has the highest efficiency at 87.5% on unseen data. This model has a misclassification of about 12.5%. Therefore, I improved the model by common word removal but the accuracy does not be improved and it decreases to 86.4%. For this reason, I selected the model without the common word removal and analyse the important word for prediction.

In this work, I assumed '911FOX' as 1 and 'NCIS' as 0 and the result of the coefficient shows the influence of each word on 911FOX prediction. The result of the important word with the coefficient is shown in the following table 1. The top 10 words have 3 character names (buck, maddie, eddie) and 2 words the name of season (lone, star) and 1 word of movie website (hulu). The top words show the popular characters are 'Buck', 'Maddie' and 'Eddie' and the popular season is 911: Lone Star, and the popular platform the user post on 911FOX Reddit is the Hulu website. 

Table 1: The top 10 words that will help to increase the correct prediction on 9-1-1.

|No.|Subreddit|Word|Coefficient|
|---|---|---|---|
|1.|**911FOX**|*buck*|-5.1725|
|2.|**911FOX**|*like*|-5.6173|
|3.|**911FOX**|*one*|-5.8541|
|4.|**911FOX**|*star*|-5.8801|
|5.|**911FOX**|*lone*|-5.8884|
|6.|**911FOX**|*maddie*|-5.8998|
|7.|**911FOX**|*eddie*|-5.9597|
|8.|**911FOX**|*watch*|-6.0233|
|9.|**911FOX**|*hulu*|-6.0553|
|10.|**911FOX**|*anyone*|-6.0826|


**Business Recommendation**

- The model can help to increase the accuracy of the post in 911FOX and NCIS subreddits, and encourage Reddit to create a new searching system. When we have the model to predict the subreddit for each post, Reddit can improve the searching system to receive the input from the user as the specific word and recommend the relevant subreddit. This will make the user post easier because some users do not know the name of the subreddit.
- The subreddit with the most accuracy of the post checking and show only the relevant post will increase the satisfaction of the user.
- When Reddit has more accuracy of the post in each subreddit, they can make the business deal with another website. In this case, we know the 911FOX has the post about Hulu and the Hulu is the top 10 words which have high coefficient so Reddit can make a deal with the Hulu website to increase the value of Reddit and the number of users.


**Next step of the future work**
- The model from this work can improve the classification between r/911fox and r/ncis but it has some misclassification. So, Reddit should have the word recommendation when the user post on Reddit to prevent misspelling and increase the quality of data when the text from the user inputs to the model. 
- Since the common word removal cannot develop the model, so the next step should be the setting the hyperparameter for all regression model (logistic regression, Naive Bays and RandonForest Classifier) to get the best parameter.

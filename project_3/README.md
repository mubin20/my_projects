# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

## Executive Summary
---

## Goals:  

1. Using Pushshift.io API, collect posts from two subreddits(r/Crypto_com and r/bodyweightfitness).
2. Use NLP to train a classifier model on which subreddit a given post came from.
3. Stretch goal: Use sentiment analysis to understand which subreddit tends to gain higher positive sentiments.

## Problem Statement:

Can we leverage on machine learning to create a classifier that can accurately predict the origins of reddit posts?

## Process:  

- Data collection: Reddit and pushshift.io APIs
- Data cleaning and EDA
- Preprocessing and Modeling
- Evaluation
- Conclusions

## Data Collection:  

#### 1) Subreddit: r/Crypto_com
- a) https://api.pushshift.io/reddit/search/submission/?subreddit=Crypto_com (Submission)
- b) https://api.pushshift.io/reddit/search/comment/?subreddit=Crypto_com (Comments)

#### 2) Subreddit: r/bodyweightfitness
- a) https://api.pushshift.io/reddit/search/submission/?subreddit=bodyweightfitness (Submission)
- b) https://api.pushshift.io/reddit/search/comment/?subreddit=bodyweightfitness (Comments)

Pushshift was used for data collection. Data collected from pushshift was 19,898 comments (10,000 for r/Crypto_com and 9898 for r/bodyweighfitness).
<br>Upon analysing the posts for respective subreddits, there were mostly images for r/Crypto_com submissions and text for r/bodyweighfitness submissions.Therefore, I decided to analyzed the comments for two subreddits as they will be more comparable.

## Data Cleaning and EDA

The following were removed from the comments: html, hyperlinks, punctuation, words with 2 or fewer letters, whitespace including line returns, non-standard characters. Duplicate messages were dropped. After cleaning, there were approximately 18,255 records total, still split approximately in half by crypto and bodyweightfitness classes. Words in the comments were lemmatized and stop words were removed. Out of top 50 frequently used words about 33% were commonly used in both subreddits but the rest were unique.


## Data Modelling

Data Modelling table shows the score for each models along with hyperparameter. Logistic Regression model performed the best.

<p align="center">
  <img src="https://github.com/mubin20/my_projects/blob/master/project_3/images/Data_Modelling.PNG" />
</p>

## Bonus: Sentiment Analysis

Sentiment analysis using TextBlob, below are the mean and median sentiment for respective subreddit's.

**Crypto mean sentiment: 0.10844257144167661**
**Crypto median sentiment: 0.014245129870129863**

**Fitness mean sentiment: 0.13875229678706325**
**Fitness median sentiment: 0.10833333333333332**

Bodyweightfitness subreddit tends to have slighltly higher mean positive sentiment.
Between both subreddit's r/Crypto_com and r/bodyweightfitness they share similar positive sentiments between 10-15%.

## Conclusions

Logistic regression model achieved the best accuracy scores (train / test scores: 0.9044 / 0.9129).

Potential improvements for future: collect more training data, do more data cleaning and preprocessing (remove more stop words i.e. numbers, stem/lemmatize i.e. -ing verbs), more intensive gridsearching to optimize models, include n-gram parameter in gridsearch, try more models (boosting, SVM)

Sentimental Analysis between both subreddit's r/Crypto_com and r/bodyweightfitness share similar positive sentiments of only between 10-15%. In my opinion, this could be because of the volatitily in crypto trading, thus the negative sentiments outweigh the positive ones. Similarly for bodyweight fitness, since it is not routined or structured, it is left up to the individuals to decide their pace and structure thus impacting on the overall intended progress and outcome. This might then resulted to them not achieving their planned goals, hence the negative sentiments. 
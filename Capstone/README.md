# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone Project: IPL Score Predictor
![GIF](resources/ipl_teams.jpg)

## Executive Summary
---

## Goals: 

1. Gather dataset for IPL matches.
2. Perform data analysis on the collected data to look for trends and select important variables.
3. Use Linear Regression models to predict the score of IPL match for batting team.
4. Use flask to create web framework.

## Problem Statement:

1. Business Problem: Coaches and Captain of batting team needs to stratergize the game plan based on current score statistics to increase winning chances.Therefore,predicting score would help them optimise the performance of their team.
2. Data Science Problem: Predict the IPL score for the batting team. 

## Process:  

- Data collection: Kaggle dataset from year 2008-2020
- Data cleaning and EDA
- Preprocessing and Modeling
- Evaluation
- Conclusions

## Data Collection
1) IPL matches dataset (overview of each match played between 2008 to 2020.
2) IPL ball-by-ball dataset (granular dataset of each match i.e ball by ball details)

## Data Source
- [Kaggle Dataset 2008-2020](https://www.kaggle.com/patrickb1912/ipl-complete-dataset-20082020)

## Overview
- EDA on ball-by-ball data was performed to identify trends and patterns of different variables.
- Feature engineered columns (last_5_over_wickets,last_5_over_runs,final_score(total score of the batting team),etc.)
- 8 most consistent teams were selected.
- Train test split on the featured engineered dataset with 70% train data and 30% test data ratio.
- Models used:
   	i. Linear Regression
	ii. Ridge
	iii. Lasso
	iv. Decision Tree
	v. Random Forest
	vi. Ada Boost
	vi. Gradient Boost

- Hyperparameter tunning on various model was performed, which resulted in best model selection as **Random Forest**.
- Data Modelling table shows the score for each models.

<p align="center">
  <img src="https://github.com/mubin20/my_projects/blob/master/..../..../model.PNG" />
</p> 

## Conclusion
- Difference of train dataset MAE and test dataset MAE is **5.127921** for Gradient Boost.
- Difference of train dataset MAE and test dataset MAE is **0.679447** for Random Forest.
- Train score (accuracy or **r2_score**) of Gradient Boost algorithm is higher than Random Forest but Random Forest's **MAE** difference between train and test dataset is lower than Gradient Boost.
- Reason for selecting random forest over gradient boost being high difference in **MAE** for gradient boost which can result into **overfitting**.


## Demo
- I have deployed this on Heroku platform
Link: [https://ipl-jaysoftic.herokuapp.com/](https://ipl-jaysoftic.herokuapp.com/)

![GIF](resources/predict.gif)

## How to use
- Select venue, batting team, bowling tean and fill the inputs with proper information then click on predict button you will get predicted score of batting team.





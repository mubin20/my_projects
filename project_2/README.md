# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement

1) Business Problem : As a Ames Real Estate Agency we been relied highly on the opinions and expertise of our relators to manually evaluate the price of the homes listed on our agency website. In order to keep up with the market of automation these days we will be hiring a team of data scientist expert to help us with the estimation of the property prices based on data from year 2006 to 2010.
2) Data Science Problem: As a member of Data Science team, we will be exploring property features of data available from 2006 to 2010 to predict sale price of different property types using Linear regression model.

---

### Contents:

**DATA Cleaning**
- Background
- Import Train/Test Data
- Data Dictionary
- Clean Train/Test Data
- Summary Statistics
- Export Clean Data

**EDA**
- Numerical Variables
- Heatmap
- Scatter plots
- Discrete Variables
- Continuous Variables
- Log Transformation
- Boxplots
- Categorical Variables
- Cardinality Values
- Histogram to compare categorical features and saleprice

**Feature Engineering, Modelling and Conclusion**
- Feature Engineering
- Model Preparation
- Modeling
- Model Selection
- Calculate Root Mean Squared Error
- Conclusions and Recommendations
- References
- Kaggle Submission Screenshot

---

### Data Dictionary

**As the data dictionary content of over 80 features, please refer to [link](https://www.kaggle.com/c/dsi-us-12-project-2-regression-challenge/data) to access the data dictionary.**

**Some of the added features after featured engineering are listed below**

|Feature|Type|Description|
|---|---|---|---|
|total_baths|float|Combination of 4 features as follows (full_bath,half_bath,bsmt_full_bath,bsmt_half_bath)|
|total_livable_sf|float|Combination of 3 features as follows (bsmtfin_sf_1,bsmtfin_sf_2,gr_liv_area)| 
|neighborhoods_1|int|Consist of neighbourhoods (StoneBr,NridgeHt,Veenker,NoRidge,GrnHill)|
|neighborhoods_2|int|Consist of neighbourhoods (SawyerW,CollgCr,Somerst,Gilbert,Crawfor,NAmes,ClearCr,Blmngtn,Greens)|
|subclass20|int|Only value of Subclass20 was taken into consideration from ms_sublass column| 
|subclass60|int|Only value of Subclass60 was taken into consideration from ms_sublass column|
|subclass120|int|Only value of Subclass120 was taken into consideration from ms_sublass column|
|garage|float|Combination of 2 features as follows (garage_area,garage_cars)|
|near_offsite|int|Property close to off-site feature(PosN Near positive, PosA Adjacent to postive off-site feature)|
|near_busy_st|int|Property near busy street (Artery Adjacent to arterial street,Feedr Adjacent to feeder street) |
|stone_veneer|int|Only value of stone veneer was taken into consideration from mas_vnr_type column|
|new_home|int|Only value of new homes was taken into consideration from sale_type column|
|estate|int|Only value of COD Court Officer Deed/Estate was taken into consideration from sale_type column|
|good_basement|int|Only value of basement with good living quarters was taken into consideration from bsmtfin_type_1 column|
|kitchen_cond|int|Only value of kitchen with excellent rating was taken into consideration from kitchen_qual column|
|top_3_zones|int|Only value of top three zones(RL,FV,RH) was taken into consideration from ms_zoning column|

---

### Sources:

- [Ames Population](https://datausa.io/profile/geo/ames-ia/#about)
- [City of Ames](https://www.cityofames.org/about-ames/about-ames)
- [Real Estate ML](https://unionstreetmedia.com/the-rise-of-machine-learning-in-real-estate/#:~:text=Personalized%20Marketing%20Automation%20%E2%80%93%20machine%20learning,neighborhood%20and%20property%20is%20best)
- [Lasso Regression](https://chrisalbon.com/code/machine_learning/linear_regression/effect_of_alpha_on_lasso_regression/)
- [Krish Naik youtube channel](https://www.youtube.com/channel/UCNU_lfiiWBdtULKOw6X0Dig)
- [Towards Data Science](https://towardsdatascience.com/wrangling-through-dataland-modeling-house-prices-in-ames-iowa-75b9b4086c96)
- [medium.com](https://medium.com/@kamskijohnm2m/ames-housing-price-prediction-complete-ml-project-with-python-2af595a749d6)

### Conclusions and Recommendations

## Conclusions: 

### 1) Linear Regression model tends to account for approx 88.34% of the variation in sale price of a property.
### 2) It was able to predict sale price within 22,800.19.
### 3) Upon plotting actual price vs predicted price scatter plot we could see that the model could only predict the price in range of 85k to just over 210k but at both extremes it was lagging in preicting the sale price.
### 4) Having below top 5 features in the house will result in property price increase.
![](../images/lr_Top5.png)
### 5) Having below bottom 5 features in the house will result in property price decrease.
![](../images/lr_bottom5.png)
### 6) Properties located in Stone Brooke, Northridge Heights,Veenker and Green Hill  results in 6.8% increae in price.
![](../images/neighborhood_1.png)
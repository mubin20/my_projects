# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis


### Problem Statement

Analyze trends using SAT/ACT 2018 and 2019 data to develop a hypothesis to recommend strategies to improve SAT performance.

---

### Contents:

- Background
- Datasets used for this project:
- Data Import & Cleaning
- Data Import and cleaning for year 2018
- Data Import and cleaning for year 2019
- Combined data for SAT and ACT 2018 and 2019
- Data Dictionary
- Exploratory Data Analysis
- Summary Statistics
- Investigate trends in the data
- Data Visualization
- Heatmap using seaborn
- Histogram
- Boxplots
- Scatter plots
- Additional plots
- Choromap
- Conclusions and Recommendations

---

### Data Dictionary

**Dictionary for Dataset of SAT and ACT for the year 2018-19.**

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT/SAT|name of states in USA|
|participation_sat_2018|float|SAT 2018|percent participation in decimal| 
|ebrw_sat_2018|int|SAT 2018|average SAT Evidence-Based Reading and Writing test score| 
|math_sat_2018|int|SAT 2018|average math test score| 
|total_sat_2018|int|SAT 2018|average SAT total score|
|participation_act_2018|float|ACT 2018|percent participation in decimal|
|composite_act_2018|float|ACT 2018|average ACT composite score|
|participation_sat_2019|float|SAT 2019|percent participation in decimal| 
|ebrw_sat_2019|int|SAT 2019|average SAT Evidence-Based Reading and Writing test score| 
|math_sat_2019|int|SAT 2019|average math test score| 
|total_sat_2019|int|SAT 2019|average SAT total score|
|participation_act_2019|float|ACT 2019|percent participation in decimal|
|composite_act_2019|float|ACT 2019|average ACT composite score|

---

### Sources:

- https://www.collegeraptor.com/getting-in/articles/act-sat/4-reasons-why-its-still-worthwhile-to-take-the-act-sat/
- https://www.collegeraptor.com/getting-in/articles/act-sat/states-act-sat-given-free/
- https://blog.collegeboard.org/what-is-the-average-sat-score
- https://uk.usembassy.gov/states-of-the-union-states-of-the-u-s/
- https://www.number2.com/average-sat-score/
- https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows
- https://www.collegeraptor.com/getting-in/articles/act-sat/states-act-sat-given-free/
- https://plotly.com/python/map-configuration/#named-map-scopes-and-country-subunits
- https://www.studypoint.com/ed/sat-and-act-test/

### Conclusions and Recommendations

## Conclusions: 
### 1) According to the data, where SAT are offered free to students, participation rate is higher,however this does not translate into higher scores.**

- **Average Participation rate SAT 2018 (96.54%)**
- **Average total score SAT 2018 (1022)**
---
- **Average Participation rate SAT 2019 (97%)**
- **Average total score SAT 2019 (1015)**

### 2) It can be observed from the data that states without free SAT tend to perform better than average.

- **Average total score SAT 2018 (1146)**
- **Average total score SAT 2019 (1139)**

### 3) The reason for the higher commitment could be that they invested some money into taking the test, so they are more driven to achieve a higher score. 

## Recommendation:
### It is worthwhile to charge a nominal fee for SAT to ensure better performance of the results from the participants.
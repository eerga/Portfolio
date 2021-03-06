# Data Science Portfolio
By Erika Ergart

---
# Google Cloud Platform (GCP) Projects

## [Project 1: Market Share Decrease Analysis of the NYC Yellow Cab](https://github.com/eerga/nyc_yellow_cab)

### Project Scope
Our Data Analytics team utilized GCP and Data Studio to conduct exploratory analysis (EDA) along with utilizing machine learning algorithms to identify areas of improvement for the Yellow Cab company and come up with suggestions that would increase its market share.

### ML Models
The two main machine learning models used were **Boosted Classifier Tree** and **Linear Regression**

### One of the key exploratory findings
![alt text](images/NYCTaxi.png)
Not only is it posisble to see that the highest activity of NYC Yellow Cab is in the Manhattan neighborhood but also that credit cards was the most utilized payment option.

### Summary of the project 
• Supervised statistical analysis on market share decrease of NYC Yellow Cab Company in Google Cloud Platform over 225 million records by running linear regression and boosted tree classifier models and visualizing in Data Studio <br />
• Recommended business strategies such as introducing a yellow cab app with more transparent fare calculations, flexible payment options and optimized route to lower driving costs

## [Project 2: Twitter & Plane Landing Correlation Assessment](https://github.com/eerga/twitter_flights)
### Project Scope
Google Cloud Platform (GCP) has real-time Twitter and flights datasets available. We decided to explore the possibility of correlation between the number of successfully landed commercial flights and overall Twitter activity. Assuming this hypothesis is proven, our team would have recommended Twitter to make a joint program with airlines using the hashtag #landedsafelywith[name_of_the_airline_company] to promote flights for specific airlines. As a result, this would create a mutually beneficial relationship between Twitter and the associated airline companies. Twitter would gain user traffic while airline companies are given free marketing material.

### Tools Used
The analysis was performed using **SQL** and **Python**. Since Twitter information is highly nested, this made defining schemas significantly more difficult on GCP. The Python script was used to extract the most relevant Twitter information. 

### ML Models
The main machine learning models used were Linear and Logistic Regressions

### One of the key exploratory findings
![alt text](images/twitter_activity.png)</br>
Even though we did observe activity spikes for both flights and Twitter, the activity spikes did not overlay, which means that other variable(s) may better explain Twitter activity increase. 

### Summary of the project 
The analysis suggests that our hypothesis should be rejected as this marketing strategy is not supported by available data. 

---
# R Projects
## [Project 1: Time Series Analysis of Minimum Temperatures in Melbourne, Australia](https://github.com/eerga/globalwarm)

### Project Scope
In this data, we have daily readings of minimum temperatures from Melbourne, Australia for 10 years (1981-1990). I was curious to see if any global warming trends would be visible on the 10-year scale. The reason for choosing minimum temperatures might not seem obvious, but I decided to play with those in order to observe extreme case of global warming. If minimum temperatures directly indicate presence of glabal warming, then we may need to do something before it is too late. I was also curious to see which of the models commonly used in time series forecasting would perform the best. The source code can be viewed in 3 formats: *.ipynb*, *.PDF*, and *.HTML*.

### Models Used
- Seasonal Naive </br>
- Time Series Model with Seasonality </br>
- Holt-Winter </br>

### Key Exploratory Figure
![alt text](images/Summary.png)</br>
We normally use RMSE to evaluate model accuracy. Even though I expected for Holt Winter’s model to have the best performance, it turns out that a simpler time series linear model has the best performance. Seasonal naive was used as a base model. It is used for highly seasonal data and the forecasting accuracy might’ve not been as good as time series’ because the model uses the most recently observed value.

### Conclusions
Even though we learned a lot about the models, it wasn’t possible to conclude anything globalwarming tendencies. There are 2 possible reasons for this: 1). The range of data is not large enough. It might be more reasonable to obtain at least 50 years of minimum temperature readings and take a look at the data trend to make more appropriate conclusions; 2). While only Melbourne, Austria, was considered in the this analysis, it might be more effective to consider at lear 3 various locations to draw out a better conclusion.

## [Project 2: Survival Analysis of Patients with Diabetic Retinopathy](https://github.com/eerga/Survival_Analysis)

### Project Scope
In our study, we are interested in finding out which parameters contribute to the patient blindness and which do not. We used three methods to identify those parameters:
- **Kaplan-Meier Curve** (univariate analysis)
- **Log-rank test** (univariate analysis)
- **Cox Proportional-hazards model** (uni- and multivariate analysis)

### Key Exploratory Findings
![alt text](images/summary_table.png)</br>
- It was discovered that whether or not a patient received treatment was significant. Those who received treatment were 57% less likely to lose vision as those who did not receive treatment
- Those patients who were in the high risk category were 106% more likely to lose vision as those who are in the medium group.

### Suggestion
The age category group was not balanced as minors constituted 64% of the group and adults consituted the remaining 36%. The implementation of *ntile* would evenly distribute patients into two categories, which potentially can lead to different statistically significant results (i.e., age category might end up being significant). 

---
# Python Projects
## Project 1: Understanding and Predicting Project Payment Latency in the Covid-19 Era

### Abstract
This study develops an order-to-cash process map predictive solution to better understand home remodeling projects' pre- and post-COVID-19 payment latency. In remodeling projects, the day a project is sold (and past rescission) to the time payment is received or installment is first accepted is defined as “order-to-cash.” The risks of delayed processes and delay customer payments can hurt the company’s solvency and financial stability. Especially in the economic condition caused by the pandemic. The motivation for the current study is to optimize the prediction model of the order-to-cash during the pandemic.

### Methodology
![alt text](images/Methodology.png)

### ML Models and Techniques Used
- CatBoost
- Random Survival Forest
- LightGBM
- XGBoost
- Stacked Ensemble
- Target Encoding
- Weighing Data Based on Its Recency

### Results
 - Improved client’s base machine learning model by implementing target encoding feature engineering technique and weighing data, attaining 3% OpEx decrease or $800,000 potential savings
- [1st place](http://meetings2.informs.org/wordpress/analytics2021/poster-sessions/) in the Student Poster Competition at INFORM Business Analytics Conference

### Suggestions
Each project has [task dependency](https://www.prince2.com/usa/blog/project-dependencies). For example, you have to first cook the dinner in order to eat it. Similarly, here we had to get the product delivered in order to install it. The task durations present are in cumulative days. Further study would benefit from finding individual task durations, identifying the longest average/median task durations and then finding ways of shortening those. 

Another item includes possible incorporation of time series analysis techniques to accurately predict order-to-cash estimates.

## [Project 2: The Popularity Secret Behind Pokémon Card Resale Market](https://github.com/eerga/da_project)

### Goal
Our Data Analytics team assessed the influence of Pokémon YouTubers on Pokémon card resale. Our **hypothesis** was: the higher the YouYube views are, the higher the resale rate of Pokémon cards is. We web scraped historical data of Pokémon card prices and top 10 Pokémon YouTubers’ views, using Wayback Machine and Python </br>

### What we used
The packages we used are *Chromedrive* and *BeautifulSoup*.

### Project Conclusion
After conductig statistical analysis and building a descriptive model, we concluded that YouTube views solely cannot explain an increased popularity in Pokémon card resale and other features should be incorporated into the study.

The two main metrics used to derive the conclusion were p-value and R^2 score as demonstrated in the picture below
![alt text](images/statistical_analysis.png)

---
# Tableau Project
## [Dive Into World Suicide Data](https://public.tableau.com/app/profile/erika.ergart/viz/WorldSuicideStudy/Story1)

### Project Motivation
As someone who absolutely loves life, I wanted to explore what were some of the main driving mechanisms behind suicide and what can be done with the data

### Project Source
[WHO Suicide Statistics](https://www.kaggle.com/szamil/who-suicide-statistics)

### Key Findings
- Even though some of the highest suicide numbers reported are in Russia, United States, and Japan, the suicide % rate per capita is the highest for Lithuania, Hungary, and Russia as can be seen in the following figure:</br></br>
![alt text](images/Suicide_Rate_Percent_per_Capita.png)</br></br> The study would have been more comprehensive if data from China and India were included.

- Men have higher suicide % rate per capita across all age categories. Even though it is suspected that this comes from social stigma associated with utilizing mental health facilities. However, to prove this hypothesis, mental health therapy data should be included in this study.

- The data suggests that the overall suicide rate has been declining. To have a more comprehensive study, it would be interesting to explore how COVID-19 has affected the suicide rate in the world.

---
# SQL Project
## [College Review Website](https://github.com/eerga/Universities)

### Project Overview
Our data analytics team is consulting for Niche.com.  While Niche is a reputable resource in the American market, the website is limited to the US market. Our firm has been brought in to expand upon their current data set by introducing more distinguishing fields as well as to establish data on universities from abroad in order to grow their user base internationally. 

### Data Used

- [World University Rankings](https://www.kaggle.com/mylesoneill/world-university-rankings?select=cwurData.csv)
- [Salaries by College Type](https://www.kaggle.com/wsj/college-salaries?select=salaries-by-college-type.csv)
- [Recent College Grads Can Expect to Make the Highest Salaries in Germany and US](https://www.kornferry.com/about-us/press/Recent-College-Grads-Can-Expect-to-Make-the-Highest-Salaries-in-Germany-and-U.S)
- [Cost of Living](https://www.expatistan.com/cost-of-living/country/ranking)


### Question Asked and Sample Query

Is having a higher rate of international students and smaller student to staff ratio related to higher Mid-Career 90th Percentile Salary?

```sql SELECT s1.SchoolName, s1.SchoolType,
s1.MidCareer90thPercentileSalary, t1.student_staff_ratio,
T1.international_students
FROM salaries_by_college_type as s1
INNER JOIN timesData as t1
on s1.SchoolName = t1.university_name
WHERE s1.MidCareer90thPercentileSalary != 'N/A' 
and s1.SchoolName != 'University of Wisconsin'
GROUP BY s1.SchoolName, s1.SchoolType
ORDER BY s1.MidCareer90thPercentileSalary desc
```

### Description of Business Problem Addressed
Lower student to staff ratio leads to more personal relationships professors develop with students, which results into:
- More questions answered
- Assisting with finding higher paying jobs

Higher international student ratio leads to:
- More diverse learning experience
- Better professional expertise
---
# SAS Project
## [Classification Algorithms to Forecast if a Firm Will Collapse](https://www.kaggle.com/c/fall2020-mgmt571lec-project/overview)

### Project Overview
Firm collapse prediction has been a subject of interests for almost a century and it still ranks high among hottest topics in economics. The aim of predicting financial distress is to develop a predictive model that combines various econometric measures and allows to foresee a financial condition of a firm. The purpose of the bankruptcy prediction is to assess the financial condition of a company and its future perspectives within the context of longterm operation on the market.

### Final Model
![alt text](images/final_model.jpg)

### Model Score
Our model accuracy achieve a score of 0.79 with the high-performance neural net

---
# Bridging the Gap Between Kafka Streaming and Real Time Data Analysis 
## [Burroughs](https://pages.github.itap.purdue.edu/Burroughs/Burroughs/)

### Project Goal
Our team made a Kafka topic behave similarly to a relational database to circumvent spending required for training analysts and data scientists to learn KSQL for real-time data analysis.

###  Tools used
- Java (Apache Calcite)
- Apache Kafka
- Docker
- ksqlDB

### [Project Link](https://pages.github.itap.purdue.edu/Burroughs/Burroughs/)

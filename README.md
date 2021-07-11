# Portfolio
Data Science Portfolio

# Google Cloud Platform (GCP) Projects

## [Project 1:Market Share Decrease Analysis of the NYC Yellow Cab](https://github.com/eerga/nyc_yellow_cab)
---
### Where to use?
This project is to be run on Google Cloud Platform (GCP). It includes running a **Pub/Sub job**.

### Which data to use?
For supervised learning algorithms, it is a common practice to split the data into training and test sets to see how well a model will perform.

For the purpose of this study, we are using 3 datasets - 2 historical datasets from Google's Marketplace in NYC TLC Trips and one newly updated one from pub/sub topic *projects/pubsub-public-data/topics/taxirides-realtime*. 

### What's the table schema (necessary for proper data loading)? 
The following code was used to create table schema for data transfer: <br /> 
`bq mk --time_partitioning_field timestamp --schema ride_id:string,point_idx:integer,latitude:float,longitude:float,timestamp:timestamp,meter_reading:float,meter_increment:float,ride_status:string,passenger_count:integer -t taxirides.realtime`

### Train / test data
Tlc_yellow_trips_2015 was used as a training set
In cases when it was possible (i.e., appropriate prediction values were present in the test set), realtime table was used as a test set. Otherwise, tlc_yellow_trips_2016 was used as a test set instead.

### ML Models
The two main machine learning models used were Boosted Classifier Tree and Linear Regression 

### Summary of the project scope
• Supervised statistical analysis on market share decrease of NYC yellow cab company in Google Cloud Platform over 225 million records by running linear regression and boosted tree classifier models and visualizing in Data Studio <br />
• Recommended business strategies such as introducing a yellow cab app with more transparent fare calculations, flexible payment options and optimized route to lower driving costs

# Python Projects
## [Project 1: The popularity secret behind Pokémon card resale market](https://github.com/eerga/da_project)

### Goal
Our Data Analytics team assessed the influence of Pokémon YouTubers on Pokémon card resale. Our **hypothesis** was: the higher the YouYube views are, the higher the resale rate of Pokémon cards is. We web scraped historical data of Pokémon card prices and top 10 Pokémon YouTubers’ views, using Wayback Machine and Python </br>

### Notebook description
 Initial part of the project has been performed by my collegue Dawson and consists of scraping the number of YouYube views for top 10 most popular Pokémon YouTubers from [SocialBlade](socialblade.com) (*socialbladescrape.ipynb*). The packages we used are *Chromedrive* and *BeautifulSoup*.
 
 Second part of the project consists of 3 notebooks, i.e. *pokemon_scraping.ipynb*, *analysis_prep.ipynb*, and *analysis.ipynb*.

1. *pokemon_scraping.ipynb* **scrapes** historical data for **top 100 pokemon cards** sold from [here](https://pokemonprices.com/top_100) for 2019 and 2020. Items obtained are card names and card rarity numbers. Those two variables are accompanied by dates collected and prices of pokemon cards on those dates. 

2. analysis_prep.ipynb is where additional data cleaning is performed. Moreover, Pokémon data was modified to obtain average prices for each Pokémon card (grouped by name and unique_id, i.e. rarity number) and is joined with YouTube views to later obtain insight on how YouTube views might affect the Pokémon cards prices. 

3. In analysis.ipynb, statistical analysis is performed and appropriate conclusions are made.

### Project Conclusion
After conductig statistical analysis and building a descriptive model, we concluded that YouTube views solely cannot explain an increased popularity in Pokémon card resale and other features should be incorporated into the study.

The two main metrics used to derive the conclusion were p-value and R^2 score as demonstrated in the picture below
![alt text](images/statistical_analysis.png)

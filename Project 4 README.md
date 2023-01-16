# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Group 1 - Dengue Cases

## Introduction

1. Dengue is a disease transmitted to humans through the bite of infected Aedes aegypti mosquitoes. There are 4 different types based on the virus (DENV1-4)
2. Infected individuals may develop symptoms in 2 weeks as the incubation period is about 1 week
3. There are several symptoms of dengue fever such as fever, persistent headache, nause, and skin rash where in severe case it can lead to bleeding and persistent vomiting which can eventually lead to death
4. Individual effort to reduce potential mosquito breeding locations is highly encouraged, however, NEA takes prevention seriously through scheduled fogging and Project Wolbachia (releasing male Wolbachia-Aedes mosquitoes to breed with female mosquitoes and their egg won’t hatch)

## Problem Statement
As part of NEA planning team, we are going to try to forecast Dengue case in Singapore to ensure our fogging schedule 

## Dataset and APIs

We used data from the following sites
1. http://www.weather.gov.sg/climate-historical-daily/
2. https://data.gov.sg/dataset/weekly-number-of-dengue-and-dengue-haemorrhagic-fever-cases (Currently has weekly number of cases from 2014 to 2018)
3. https://outbreak.sgcharts.com/data 

We also used data from the following APIs and Python Libraries
1. googlemaps
2. matplotlib.image
3. geopy
4. geolocator


#### Allocation of Tasks

This project was executed as a group. Here are the work done by each member. Their work can be seen in the respective folders in the GitHub page.

1. Natasha
    a. Scraping of weather data points from "http://www.weather.gov.sg/climate-historical-daily/" using BeautifulSoup
    b. Scraping of dengue data points from "https://outbreak.sgcharts.com/data" using Beautiful Soup
    c. Generating the Latitude and Longitude for each address data point in the Dengue Outbreak dataframe using the googlemaps API.

2. Steven
    a. Merging all dataframes together into one holistic dataframe using Pandas.
    b. Time Series Analysis of Weather Data using Seasonal Decompose and SARIMA Modelling.
    c. Investigated causality of data using Granger Causality Test.
    d. Additional analysis using Augmented Dickey-Fuller Test and VarARIMA

3. Joel
    a. Generated Spatial Analysis Heatmap plots of dengue outbreaks by their specific addresses using Latitude and Longitude data and the respective intensities using matplotlib.image and googlemaps API.
    b. Generated Rainfall Heatmap using googlemaps API
    c. Consolidated the respective address data into Suburb and County groups using the geolocator library in Python. 

**GitHub Repo**

1. Create a GitHub repository for the group. Each member should be added as a contributor.
2. Retrieve the dataset and upload it into a directory named `assets`.
3. Generate a .py or .ipynb file that imports the available data.

**EDA Binary Classification- Dataset Check**
1. High collinearity 
2. A lot of missing data in weather data based on Station
3. Preprocessing: rainfall imputed with 0 and temperature with average temperature. Limitation: might skew our data
4. Data used: based on county (weather, trend, cases)

**Modeling**

![alt text](https://github.com/joel-quek/project4-predict-dengue/blob/main/Spatial%20Analysis%202019.png)

---

.
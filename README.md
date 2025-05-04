# AirBNB DATA CLEANING
## Project overview
##### This analysis focuses on preparing and cleaning the Airbnb NYC 2019 dataset, with the primary goal of building a reliable foundation for future exploratory data analysis (EDA), modeling, and actionable business insights. This process emphasizes data integrity, consistency, and accuracy, which are essential to ensure meaningful insights.
## Introduction
##### The rise of short-term rentals has transformed urban travel, with platforms like Airbnb offering flexible, localized lodging experiences. To understand trends in pricing, availability, and user engagement, the Airbnb NYC 2019 dataset provides a detailed snapshot of listings across New York City’s five boroughs.

However, raw data is rarely ready for direct analysis. Before drawing insights or building predictive models, the dataset must undergo a rigorous cleaning process. This report documents the systematic steps taken to clean and standardize the data, with a focus on handling missing values, detecting and removing outliers, and preparing features for reliable analysis.

The objective is not just technical — it's analytical: to create a trustworthy dataset that reflects real-world behavior, reduces bias, and unlocks actionable insights for hosts, analysts, and urban planners.
## Key Goals
#####      •	Identify and handle missing values
           •	Standardize and format text for numerical features
           •	Detect and remove outliers that could bias results
           •	Ensure the dataset is clean and ready for exploratory analysis and modeling

## Tools and Techniques used
##### The cleaning process was conducted in Python, using the following libraries:
#####      Tool	                Purpose
          pandas	                Data handling, missing value imputation
          seaborn & matplotlib	     Visualizing outliers via boxplots
          numpy	                Statistical calculations
          datetime	                Handling and converting date fields
          The Interquartile Range (IQR) method was used to detect and remove outliers.
          

## Loading the dataset
![import data](https://github.com/omodara12/oibsip_task-No-2/blob/main/images/task2-1.png)
![dataset](https://github.com/omodara12/oibsip_task-No-2/blob/main/task%202-2.png)
## Data cleaning
##### Checking for missing values
![missing values](https://github.com/omodara12/oibsip_task-No-2/blob/main/task%202-4.png)
![missing values](https://github.com/omodara12/oibsip_task-No-2/blob/main/task2_3.png)
## Handling missing values
![Handling missing values](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task2-5.png)
![Handling missing values](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task2-6.png)
## Standardize and format text for numerical features
![Standardize](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task2-10.png)
## Visual for the key numerical features
![key numerical values](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task%202-11.png)




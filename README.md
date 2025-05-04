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
## Data cleaning Summary
##### •	last_review (10,052 missing): Converted to datetime and kept missing entries as NaT
##### •	reviews_per_month: Missing values filled with 0.0 to represent listings with no monthly reviews
##### •	host_name and name: Minimal missing values dropped, as they were not critical for numerical analysis
##### •	
## •	Standardization
##### •	Text fields like neighbourhood_group, room_type, and host_name were cleaned for casing and spacing
##### •	Ensured uniform formatting for categorical variables to prevent grouping inconsistencies


## Visual for the key numerical features
![key numerical values](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task%202-11.png)
## Detecting Outliers(IQR)
![outliers detection](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task2-13.png)
## Removing Outliers(IQR)
![Removing outliers](https://github.com/omodara12/oibsip_task-No-2/blob/main/Task2-18.png)
## Outlieir Detection interpretation
##### I focused on the following key numerical fields:
## Column	Outliers Removed and reason for Concern
##### price:	            High-priced listings (> $1,000) skewed averages and models	
##### • minimum_nights :	            Unrealistically long stays (e.g., > 30 nights) disrupted guest behavior insights	
##### • number_of_reviews :	 Listings with 400+ reviews distorted demand metrics	
##### • reviews_per_month :	 Spikes in review rates suggested automated or rare behavior	
##### • availability_365 :	 Listings always available (365 days) could mask seasonal trends	
## By visualizing boxplots before and after IQR-based filtering, I confirmed significant improvement in scale and distribution.
## Insights and Interpretations
##### •	Extreme prices and long minimum stays were the most influential outliers — removing them improved the representativeness of the data.
##### •	Review metrics required careful handling; instead of deletion, we applied log scaling and kept moderate outliers for richer patterns.
##### •	Availability values of exactly 365 are worth flagging — they likely represent commercial listings and might require segmentation in future analysis.
## Conclusion
##### This report has documented the essential process of transforming the Airbnb NYC 2019 dataset from its raw form into a structured and analysis-ready format. Through a systematic approach to data cleaning — including handling missing values, standardizing text entries, and detecting outliers — the dataset has been refined to more accurately represent the real dynamics of Airbnb listings across New York City.Outliers in key variables such as price, minimum_nights, and number_of_reviews were identified using the IQR method and carefully removed to avoid skewed insights. The process revealed how a relatively small number of extreme values could disproportionately impact average metrics and modeling accuracy.Throughout this project, I relied on powerful tools such as Pandas, NumPy, Matplotlib, and Seaborn to not only clean the data but also to visualize and validate each step. Each decision made during cleaning was grounded in a goal: to ensure consistency, accuracy, and analytical value.The resulting dataset is now a strong foundation for further exploration — whether through visualization, trend analysis, or machine learning. By investing time in this crucial preparatory phase, I’ve ensured that future findings will be based on high-quality, meaningful data. This project has not only improved the dataset but also deepened my practical understanding of data cleaning as a vital skill in the data science lifecycle.









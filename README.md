# Global Employee Layoffs

## Repository Contents
Postgresql Notebook containing the code and step-by-step EDA process

README : This document summarizes the Data Wrangling Process, analysis observation, and insights.

Dashboard: This visualizes the data, revealing patterns and trends interactively. 
https://public.tableau.com/views/2020-2023Companylayoffs/Dashboard?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link

## Project Objective
This project aims to analyze layoffs experienced between 2020 and 2023 at the company, industry, country, and Period (Date) levels, to uncover patterns, reveal the most impacted industry, and provide insight. The exploratory analysis is done using PostgreSQL and it is visualized using Tableau.

## Data Overview
The dataset used is data from Kaggle. It includes information on the Company name, Location (City), Industry, Total laid off, Percentage laid off, date, Company Stage, Country, and Funds raised.

## Data Wrangling(cleaning) Process:

•	The dataset was downloaded in Excel format and cleaned using PostgreSQL. The Steps are:

•	Created a staging table layoffs_copy, to preserve the raw data.

•	Identified and removed duplicate entries using ROW_NUMBER() OVER() function.

•	Standardized the data by fixing the whitespaces on the 'company' column and updating the table

•	standardized the 'industry' column by updating inconsistent entries. i.e. "Crypto Currency" to "Crypto"

•	Standardized and updated the 'country' column by removing trailing "full stops": "United States." to "United States"

•	Handle Null values, update similar records with missing values, and remove any rows not useful for the analysis

## Exploratory Data Analysis & Insights
In the phase I explored to understand the patterns and trends within the dataset to derive meaningful insights, I focused on various aspects such as:

•	Companies with 100% laid off, signifying closure. Drilled down by Country to analyze if any company experienced total closure in Nigeria.
•	Companies with the biggest single Layoff in a day, and then drilled down by Country to Nigeria.
•	Companies' overall total Layoffs.
•	Geographical Distribution of layoffs
•	Most impacted industry
•	Most impacted country
•	Total laid off by year and month
•	Rolling total of laid-offs, showing month-by-month progression
 
Observations
•	The analysis reveals that January and towards the end of the year consistently experience the highest number of layoffs.
•	The consumer industry emerges as the sector with the highest number of layoffs, followed by the retail and transportation industries. 
•	The majority of the companies with layoffs are in the post-IPO stage. 
•	The United States emerges as the country with the highest number of laid-offs. India follows as the second-highest country. 


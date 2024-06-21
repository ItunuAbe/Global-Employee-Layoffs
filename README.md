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

![Screenshot (81)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/d658d24d-49de-4beb-83a8-33066e60a51c)
We have four companies in United States and more others, majorly in Food Industry.


![Screenshot (82)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/2da02451-c80e-46d9-9ba3-ff894e2eba99)
No company in Nigeria experienced total closure






•	Companies with the biggest single Layoff in a day, and then drilled down by Country to Nigeria.

![Screenshot (83)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/0e473106-4df2-426a-a6aa-c7ba9a4339ca)
Google, Meta, Microsoft and Amazon topping the charts.


![Screenshot (84)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/f875927c-2578-4458-a9ef-6dccc9683f91)
Jumia came first with 900 layoffs in a day.





•	Companies' overall total Layoffs.

![Screenshot (85)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/ae0aee9e-4aba-4f1b-91a2-9e038af816bf)


![Screenshot (86)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/8db40068-36ef-4704-bde5-801502c7d83b)





•	Geographical Distribution of layoffs

![Screenshot (87)](https://github.com/ItunuAbe/Global-Employee-
Layoffs/assets/110028869/778b04d5-7563-4231-98fd-b1ac1b4b7cc1)
SF Bay Area, Seattle and New York City all in United States experienced the highest number of layoff


![Screenshot (88)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/9badc69c-9406-487f-bc1c-735e9f3037b0)
In Nigeria , we have 1482 layoffs in Lagos and 400 layoffs in Ibadan.





•	Most impacted industry

![Screenshot (89)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/c7b4561b-37a6-437f-ae64-6287679e14d8)
Consumer, Retail and Transportation sectors  experienced the highest volume of layoffs




•	Most impacted country
![Screenshot (90)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/23a730ec-44c7-4d34-83b6-07c84139ab84)
United States has the highest figure, follow by India 



•	Total laid off by year and month
![Screenshot (91)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/0592cfad-89e5-4b2d-b7f1-593afe0fee94)
In January 2023 84714 layoffs occur worldwide.



•	Rolling total of laid-offs, showing month-by-month progression
 ![Screenshot (92)](https://github.com/ItunuAbe/Global-Employee-Layoffs/assets/110028869/4ae0a864-ee26-4235-b7ca-8ab71e87f9d3)


## Observations

•	The analysis reveals that January and towards the end of the year consistently experience the highest number of layoffs.

•	The consumer industry emerges as the sector with the highest number of layoffs, followed by the retail and transportation industries. 

•	The majority of the companies with layoffs are in the post-IPO stage. 

•	The United States emerges as the country with the highest number of laid-offs. India follows as the second-highest country. 


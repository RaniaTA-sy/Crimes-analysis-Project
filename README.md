# Crimes-analysis-Project
#### Crimes analysis project from 2021 to 2023, to determine the most dangerous months of the year, most prevalent types of crimes in the study areas, and most dangerous time for crimes.

## table of contents
- [project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results-Finding](#results-finding)
- [Recommendations](#recommendations)




## Project Overview

 This project aims to create a clear crime analysis dashboard that highlights crime patterns over time, by location, and by age group. It will help us understand when and where crimes are most common, identify the most dangerous times and groups, and provide insights to support better safety measures. Ultimately, it’s about turning data into actionable information to improve community safety.
 
![Dashboard](crimes Dashboard.pdf)

 [Crimes Dashboard.pdf](https://github.com/user-attachments/files/21519161/Crimes.Dashboard.pdf)
### Data Sources

Crime Data: The primary dataset used in the analysis is a "crime_data.csv" file containing detailed information about all crimes recorded from 2021 to 2023.

### Tools

- Excel: Power Query for Data Cleansing
  -[download here](http://micrsoft.com)
- Excel: create an interactive Dashboard

  ### Data Cleaning Preparation

  We performed the following tasks:
  
  1- data loading and inception
  
  2-handling missing value
  
  3-Check the quality of the data and adjust the data type
  
  4- Data Modelling: Check the relationships between tables in the data model.
     
  5-Add a New Column called Time_group to determine the time of committing crimes within periods to clarify which periods within the day are the most dangerous.

## Exploratory Data Analysis
EDA includes exploring the crime data to answer key questions such as:

Requirements
1.	Total crimes:
 sum of all reported crimes in the dataset
2.	Crimes distribution by year and yearly changes:
Analysis of crimes categorized by year, including insights into year-over-year changes.
3.	Monthly crime trend with percentage variance.
4.	Crimes by time range
5.	Exploration of time occurrence within a definite time.
6.	 Crimes by country.
7.	Total resolved and unresolved crimes.
8.	Identification of the most dangerous time of the day.
### Data Analysis
Include the functions and steps to figure out the previous questions
-Create a measure to figure out the Total Crimes and the previous years' crimes
``` Excel function 
-	Total Crimes =COUNTROWS(Crimes_tbl)
-	PrevYearCrimes=CALCULATE([Total_Crimes],SAMEPERIODLASTYEAR(Crimes_tbl[Crime Date]))
```
-	Add a Chart between Year and total crimes (explain YOY) change.
-	Add a line chart to show the monthly change of crimes, Month over Month.
-	Make A hit map to show the weekly and monthly crime changes, add conditional formatting to the pivot table
-	Add a map chart
-	Add waterflow to explain the resolved and unresolved crimes
-	Add a column called Age group to group people by Age by applying this if-nested function.
``` Excel Function
=IF(HOUR(G3) <3,"12 AM - 3 AM",IF(HOUR(G3)<6,"3 AM - 6 AM",IF(HOUR(G3)<9,"6 AM - 9 AM",IF(HOUR(G3)<12,"9 AM - 12 PM",IF(HOUR(G3)<15,"12 PM - 3 PM",IF(HOUR(G3)<18,"3 PM - 6 PM",IF(HOUR(G3)<21,"6 PM - 9 PM","9 PM - 12 AM")))))))
```
### Results-Finding
1-The percentage of total crimes increased by 184% in 2012, and decreased by 17.8% in 2023.

2- Months with high crime numbers are( March-May-July-September-October).

3-The most dangerous time is from 9 pm to 12 pm

4-The most dangerous Hour is 11:30:00 pm

5-Max crime type is violence and sexual.

6 - Weekdays with most crimes start with Sunday, then Wednesday, and Saturday.

### Recommendations

-Increase police watches in the evening on Sundays and Wednesdays, particularly between 11:30 PM and late at night, when crimes are most likely.

-Plan safety awareness campaigns during September and October to help communities stay safe during peak periods.

-Work closely in partnership with communities to bring an end to violence and sexual crimes, working primarily where these crimes happen most often.

-Special attention must be given to the increase in crime rates in 2022, and proactive steps to keep those numbers low in the future.

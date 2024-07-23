# Crime-Data-Analysis-in-Python

## Project Overview
The purpose of this project was to analyze crimes reported for a local town in Utah named Orem. The analysis dives into the incidents reported and recorded by the Orem police department for the year 2015. Insights such as what type of incidents occur the most and at what time of day are uncovered along with several others. These insights are intended to help individuals, or the Police Department know what type of crimes occur the most and when and where. This will drive decisions on how many officers need to be on duty at what times of day and where. For citizens, it helps them determine when they are at risk for certain incidents and when they should exercise extra caution.

The CSV dataset pulled contains records of incidents in Orem Utah from 2008 till 2019. The data has columns for what type of crime occurred, the weekday, time of day, date, address, and more. 2015 held the highest count of records compared to other years so the analysis was done on the incidents for that year. This provided more accurate results and insights on the typical level of crime for an average year in the city.

Review the python notebook script *[HERE](https://github.com/msanders25/Crime-Data-Analysis-in-Python/blob/main/Crime%20Data%20Analysis.ipynb)*

The original data can be found at this link: 
 - *[opendata.utah.gov](https://opendata.utah.gov/Public-Safety/Orem-City-Police-Crime-Data/52dt-95n9/data_preview)*

## Insights
The notebook contains graphs near the end for visualizations on all the insights uncovered. See a few examples below:
- Top 5 Incident types - Community Policing, Traffic, Theft, Alarm, Family Offense
- Top 3 Incident Count by Month - March, August, September
- Highest Incident Count by Time of Day - 4 pm and 5 pm
- Highest Incident Count by Weekday - Thursday and Monday
- Highest Theft Related Incident Count by Time of Day - 3-5 pm
- Highest Assault Related Incident Count by Time of Day - 3-5 pm

A goal of the analysis was to determine specifically what times during the day is someone most at risk for theft or assault and the general answer to that question was around 3 to 5 pm.

## Project Challenges and Solutions
While this project presented various challenges, the following were particularly demanding and required additional research to achieve the desired outcomes.

### Challenge 1 - Creating Data Frames for Visualization
All the data frames created in the code that are used to prepare the visualizations were challenging to create. I could've manually typed out the resulting count of assault or theft related crimes in lists but I wanted to write code that would skip the manual part.

For a solution to this, I created nested for loops that would gather the count of certain items after being filtered for each iteration in a month, time of day, or weekday list. Each crime type considered theft or assault was counted and aggregated for each time of day or month and stored in a list. Following this process, the data frames could be created much easier for later visualization and any manual entry process could be avoided.

### Challenge 2 - Calculating Incident Count by Year
As part of the initial data review process, I wanted to get a feel of the dataset and see which years had the most reported incidents. Manipulating the datetime column proved to be tricky when trying to isolate just the year and count the number of records per year.

As a solution for this, I created a list of unique years in the datetime column using the str.slice function in python to isolate the text to just the year portion of the date. From there, I created a for loop that would count the number of occurrences for each year in the year list and store the counts in a separate list titled year_count. The two lists could then be used to create a data frame to view which years had the most incidents recorded for the dataset.

## Methods and Process
The approach I took for this analysis involved four steps:
- Review the data
- Data cleaning
- Analysis
- Prepare Visualizations

I spent time reviewing the dataset before doing any cleaning to understand what information it contained and how the data was stored. From that point I could decide best how to clean the data to answer my initial questions.

Python code used to complete this project involved using various basic functions and features such as:
- loops
- def functions
- lists
- dictionaries
- group by
- sort
- append
- isin

There were more functions used but the above provides an example list of the types of functions used.

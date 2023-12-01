# -Cyclist-Case-Study-
In this case study, as a data analyst at Cyclistic, a bike-share company, I analyze historical trip data to understand differences between annual members and casual riders. The goal is to formulate a targeted marketing strategy aimed at converting casual riders into profitable annual members, contributing to Cyclistic's future success.

# Cyclistic Bike-Share Analysis Case Study: Unveiling Insights for Marketing Strategy

## Introduction

Hello! I'm excited to present my work on the Cyclistic bike-share analysis case study. In this project, I took on the role of a data analyst within Cyclistic, a fictional bike-share company based in Chicago. The marketing team aimed to enhance the company's future success by understanding the disparities in how casual riders and annual members utilize Cyclistic bikes. My task was clear — unravel the data to provide insights that would inform a new marketing strategy focused on converting casual riders into annual members.

## Scenario

As part of the marketing analytics team at Cyclistic, I delved into the extensive dataset, encompassing over 5,800 bicycles and 600 docking stations. Cyclistic boasts a unique offering, including reclining bikes, hand tricycles, and cargo bikes, making bike-share accessible to a diverse range of users. The primary ridership leans towards leisure, with approximately 30% using bikes for daily commuting.

## About the Company

Cyclistic, established in 2016, has evolved into a prominent bike-share program in Chicago. The fleet of 5,824 geotracked bicycles spans 692 stations, allowing users the flexibility to unlock and return bikes at any station within the network. The company's marketing strategy, until now, focused on broad awareness and diverse pricing plans catering to single-ride passes, full-day passes, and annual memberships.

## The Business Task

Our director, Lily Moreno, emphasized the crucial role of annual memberships in Cyclistic's profitability. Recognizing the potential to convert casual riders into members, Moreno outlined a clear goal — design marketing strategies based on data insights. My initial task was to answer the question: How do annual members and casual riders use Cyclistic bikes differently?

## Data Cleaning Process for Ride Share Data (2023)

### Prepare

My main goal in this data cleaning process was to delete faulty data while not getting rid of anything valuable. It would have been easier to delete anything with a null value, but I wanted to utilize all the legitimate data I could.

1. **Create a View for Querying**

2. **Create a Table with All Data:**
   - The creation of Ride_Share_All_Data_2023 involved merging data from individual months into a single, comprehensive table.
   - This master table laid the foundation for subsequent analyses and provided a holistic view of the entire dataset.

3. **Isolate Date and Time Columns by Adding Columns for Exploration:**
   - Columns for start_date, end_date, start_time, and end_time were added to facilitate additional dimensions of analyses.

4. **Explore Trip Duration and Identify Issues:**
   - Some trip records show unusual durations or indicated that trips were lasting over a month.

5. **Identify and Handle Trips Lasting Longer Than 1 Day:**
   - *Issue Description:* Some trips lasted longer than one day, potentially indicating bikes not properly returned.
   - *Solution:* Identified and deleted trips with a duration of more than one day.

6. **Add a Column for Trip Duration in Minutes:**
   - *Issue Description:* The trip duration calculation I used above did not account for trips spanning over midnight.
   - *Solution:* I added a column for trip duration in minutes, updating it to handle trips over midnight.

7. **Filter Out Short Trips and Correcting Station Information:**
   - *Issue Description:* There were many short trips starting and ending at the same station. These were likely not legitimate.
   - Leveraging the latitude and longitude information provided in the dataset, I implemented a calculated approach to estimate distances between stations. Recognizing that one degree of latitude and longitude is approximately 69 miles, a rounded value of 0.0145 degrees was established as a threshold for a one-mile radius.

**Summary:**
This data cleaning process addresses data issues such as trips spanning over midnight, excessive trip durations, and short or potentially incorrect trips. These documented steps ensure a cleaner and more reliable dataset for further analysis.

## Data Exploration: Ride Trends and User Behavior

1. **Popular Start and End Stations**

![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/cd76f5eb-c288-427c-9cc9-2cf6aaf55094)






2. **Average Trip Duration by Rider Status and Ride Type:**
   - Casual riders tend to take longer trips.
   - Short trips are more common among members.

3. **Trip Popularity and Duration Analysis:**
   - Most popular trips are short point-to-point journeys.
   - Longer trips starting and ending at the same place are potentially for tourism or leisure.

4. **User Behavior Analysis for Trip Duration by Day, Month, and Hour:**
   - Member trips are consistently between 10-15 minutes throughout the year while casual usage is much longer in the temperate month and drops off as the months get colder.
   - There is a spike in longer trips for casual riders during the nicest hours of the day while members consistently stay in the 10-15 minute range.

5. **User Behavior Analysis for Amount of Trips by Day, Month, and Hour:**
   - Members ride the most during weekdays while casual riders are the opposite, taking trips the most during the weekends and dropping off during the week.
   - Most trips are taken in the warmer months while colder months see a drop in usage from casual riders.

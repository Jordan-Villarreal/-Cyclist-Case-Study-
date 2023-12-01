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
    - Casual riders tend to take round trips in high tourism and recreational areas.
    - Members tend to take short point to point trips.
![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/0fcc4867-d33e-4fac-bada-b4e35f169f71)







2. **Average Trip Duration by Rider Status:**
   - Casual riders tend to take longer trips.
   - Short trips are more common among members.
  
![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/fd6b97e4-e046-4d8f-934a-ee33cad2e08a)








3. **User Behavior Analysis for Trip Duration by Day, Month, and Hour:**
   - Member trips are consistently between 10-15 minutes throughout the year while casual usage is much longer in the temperate month and drops off as the 
     months get colder.
   - There is a spike in longer trips for casual riders during the nicest hours of the day while members consistently stay in the 10-15 minute range.

![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/9212cb33-3c76-4f4b-8497-80eb311d8e20)








![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/054e81bd-efcb-4624-9eb0-fe6f39323635)








4. **User Behavior Analysis for Amount of Trips by Day, Month, and Hour:**
   - Members ride the most during weekdays while casual riders are the opposite, taking trips the most during the weekends and dropping off during the week.
   - Most trips are taken in the warmer months while colder months see a drop in usage from casual riders.
  
![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/c1b7bd78-9864-4cc7-b395-63341c405372)







![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/660dd39c-1c5b-49ea-a25a-87b5358a6da0)



     



5. **User Behavior Analysis for Type of bicycle used:**
   - The electric and classic bikes are the most popular.
   - Docked bikes are only used among casual users
  





![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/d8112561-cdba-4e90-a3f1-be022ccda900)






![image](https://github.com/Jordan-Villarreal/-Cyclist-Case-Study-/assets/126938990/98362115-97d1-43a9-9787-af6140782354)







# Business Recommendation: Enhancing Cyclistic's Offerings for Diverse User Needs

## Key Insights:

### Divergent Usage Patterns:

- **Casual Members:**
  - Tend to take longer, recreational trips.

- **Members:**
  - Prefer shorter point-to-point journeys, potentially for daily transportation and working delivery services.

### Untapped Market Potential:

- **Recreational Riding:**
  - Casual members using bikes for leisure and tourism present an opportunity for specialized offerings.

## Recommendations:

### Targeted Marketing and Recreational Membership:

- Introduce a specialized membership tier for casual riders focusing on tourism and recreational rides.
- Provide exclusive access to curated routes, promotions for leisure rides, and potentially collaborate with local tourist attractions.

### Exercise-Focused Initiatives:

- Create specialized routes or stations for fitness enthusiasts, possibly incorporating exercise bikes in select locations.
- Implement new bicycles used for fitness and physical health.
- Attract members looking to supplement their gym routine or engage in fitness activities, expanding Cyclistic's user base.

### Lake Shore Promotions:

- Direct marketing efforts towards the lake shore, the most popular location for casual riders.
- Increase brand visibility and attract more casual members, potentially through partnerships with local businesses along the lake shore.

### Promotional Collaborations:

- Collaborate with local businesses such as aquariums and museums to offer promotions for Cyclistic annual memberships.
- Incentivize casual riders to opt for annual memberships, especially if they supplement gym memberships or align with leisure riding trends.

### Alternative Memberships:

- Implement monthly or seasonal memberships for casual riders who tend to only use the service in warmer months.
- Create specialized stations and routes that follow along scenic routes for riders that use the service for only recreation.

## Summary:

Casual members seem to use the bicycle service in a completely different way than the members. It seems to me that any casual users who use the service often, naturally choose to become members because it is the more cost-effective choice per trip. In order to convert casual users and create return customers, more effort will need to be put in for the recreational users. I would put special promotions and advertisements in all high recreation areas. I would also work with businesses in those areas to create promotions and deals that market to the consumers.

It also seems to me that although casual users tend to ride for over an hour on average, they are not doing this for exercise. If they were, they would also become members as it is more cost-effective if you take many trips per year. This seems like an untapped market to explore. I would recommend more research in this area.

Another focus is on family-oriented rides. Offering special promotions and deals for family memberships or day passes might encourage more families to convert from casual to membership.

## Expected Outcomes:

- **Diversified Memberships:**
  - Attract a broader audience by offering membership options tailored to different user preferences.

- **Increased Membership Adoption:**
  - Encourage casual riders to become annual members through targeted promotions and specialized offerings.

- **Enhanced Brand Loyalty:**
  - Establish Cyclistic as a versatile service catering to transportation, physical health, and recreational needs.

- **Revenue Growth:**
  - Tap into untapped markets, potentially increasing revenue through a variety of membership plans and increased ridership.



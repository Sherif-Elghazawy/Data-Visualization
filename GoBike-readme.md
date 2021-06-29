# Analyzing and Visualizing Ford GoBike System Data (February 2019)
## presented by Sherif Elghazawy


## Introduction:

Ford GoBike (also known as Bay Wheels system) is a regional public bicycle sharing system in California's San Francisco Bay Area and was introduced in 2013 as a pilot program for the region, with 700 bikes and 70 stations across San Francisco and San Jose. Ford GoBike consists of a fleet of specially designed, environment-friendly and durable bikes that are locked into a network of docking stations throughout the city. The bikes can be unlocked from one station and returned to any other station in the system, making them ideal for one-way trips.

People use bike share to commute to work or school, run errands, get to appointments or social engagements and more. It's a fun, convenient and affordable way to get around. The bikes are available for use 24 hours/day, 7 days/week, 365 days/year and riders have access to all bikes in the network when they become a member or purchase a pass.

In June 2017, the system was officially re-launched as Ford GoBike in a partnership with Ford Motor Company. After Motivate's acquisition by Lyft, the system was renamed to Bay Wheels in June 2019.The system is expected to expand to 7,000 bicycles around 540 stations in San Francisco, Oakland, Berkeley, Emeryville, and San Jose.

## Dataset Overview: 
The data consisted of 183,412 rows and 16 attributes for 183,412 bike rides. The attributes include the ride statistics, such as ride duration, ride start and end time, and station information and coordinates, user information, such as user type, birth day, and gender, as well as additional features such as bike id and bike share. 17,318 missing data points were imputed, rather than being removed from the analysis as these rows, including these NaN values, are used in analyzing and ploting other attributes of interest. After wrangling the dataset, the total number of columns has become 27, instead of 16, as we have extracted 11 attributes to facilitate our exploratory analysis and visualization.

## Investigation Overview:
In this investigation of the Ford GoBike System, I would like to explore the most influential customer behaviors and characteristics, such as user type, gender and age, as well as features like ride duration, timing, distance, stations, and whether the whole ride used GoBike bike or not. Finally, I will investigate how these attributes impact the usage of Bay Wheels system.

## Data wrangling process:
We have assessed data types and corrected the incorrect ones:
* start_time and end_time: From Object To Datetime.
* user_type, member_gender and bike_share_for_all_trip: From Object To Category.

We have imputed and filled up the missing values to ignore losing valuable data related to our attributes of interest:
* 'start_station_name', 'end_station_name' and 'member_gender' with 'Not Defined'.
* 'member_birth_year' with '0'.
* 'member_gender' with 'Not_Defined'.

We have also Extracted the following new attributes from the existing features:
* Duration Minute and Duration Hour.
* Start Time Hour, Start Time Day, Start Time Weekday and Start Time Month.
* End Time Hour, End Time Day, End Time Weekday and End Time Month.
* Member Age.
* Distance(km).

Accordingly, the structure of the dataset has changed and the total number of columns has become 26 as shown in the next info cell, instead of 16, as we have droped 2 attributes and extracted 12 attributes to facilitate our exploratory analysis and visualization.

## Summary of Findings
* Ford GoBike service dataset for the month of February consists of 183,412 rides and subscriber users have most of the rides at 89% of totoal rides while customers make 11% of the total rides.

* For user types and genders, customers have higher duration(minute) for all genders(20.9-34.4 minutes) than subscribers'(10.3-15.2 minutes) and they have higher duration(hour) for all genders(0.3-0.6 hour) than subscribers'(0.2-0.3 hour) and females' duration(hour)(0.22 hour) is higher than that of males(0.19 hour).

* For ride times, avg. start time(hour) for working day (12.8-1.7 PM) is earlier than that of weekend days(1.7-2.3 PM). Avg. start time hour for all genders and user types is 1PM-2PM. Avg. start time(hour) for subscriber(1.4 PM) is earlier than that of customer(1.6 PM) and avg. start time(hour) for Female gender (1.2 PM) is earlier than that of Male (1.52 PM).

* For age, avg. age for subscriber(33 years) is higher than that of customer(28 years) and avg. age for males(34 years) is higher than that of females(33 years).

* For distance, avg. distance(km) for customers (1.9km) is higher than that of subscribers(1.7km) and avg. distance(km) for females(1.77km) is higher than that of males(1.66km). Avg. distance(km) for start & end working day (1.7-1.72km) is higher than that of weekend days(1.6km)
Weekdays: average duration(minute) for working days(Monday-Friday) ranges from 11.1 to 11.9 minuts while weekend days has an average which ranges between 15 and 15.3 minuts and average duration(hour) for working days(Monday-Friday) ranges from 0.18 to 0.2 hour while weekend days has an average which between 0.25 and 0.26 hour. Average start time (hour) for working days(Monday-Friday) ranges from 12.8 PM to 1.7 PM while weekend days has an average which between 1.7 to 2.2 PM. Average distance(km) for start and end time working days(Monday-Friday) ranges from 1.67km to 1.73km while weekend days has an average of 1.6km.

* For shared/not share bikes, avg. duration(minute) for non-shared bikes during the ride(12 minutes) is higher than that of shared bikes(11 minutes). Avg. distance(km) for non-shared bikes is 1.7km and for shared bikes is 1.3km.

* For age groups, avg. duration(minute) for age group 60-70 (12.73 minutes) is higher than that other groups(10.4-12.26 minutes). The middle groups 18-60 has average of 11.5-12.27 minutes and the loweest age group is 70-140(10.4 minutes). Avg. distance(km) for age group 30-40 (1.8km) is higher than other age groups(1.3km-1.7km). The middle age groups(18-20 & 20-30 & 70-141) have an average distance of 1.5km-1.7km and the lowest age group 18-20 has an average distance of 1.3km.

* For stations, San Fransisco has 156 stations, Oakland_Berkeley have 127 stations, and San Jose has 47 stations. Avg. number of rides per station in San Fransisco is , in Oakland_Berkeley is 1,480, and in San Jose is 295. Average member age for San Fransisco 's Sations is 33 years old, for Oakland_Berkeley 's Sations is 34 years old, for San Jose 's Sations is 31 years old. Average duration (hour) for San Fransisco 's sations is 0.23 hour, for Oakland_Berkeley and San Jose's stations is 0.21 hour. Average distance(km) for San Fransisco 's sations is 1.9km, for Oakland_Berkeley and San Jose 's stations is 1.7km.


## Key Insights for Presentation

* Usage pattern of the Gobike service differs based on user type and gender. Subscribers seen to be commuters who use the service for work purposes and this fact can be confirmed by the number of subscribers, who constitutes 89% of total riders, elder age than customers and capacity of working weekdays. Most of rides occur during the working weekdays as compared to week days. Customer are younger than subscribers who may use the service for fun and sports. Additionally, subscribers' rides start time is earlier than that of customers. However, customers have higher durations than subscribers and they also have longer distance than subscribers.

* Women use the service for long durations than men and for long distance than men do.

* Although most of rides are associated with ages 23-40 years old, the avg. duration(minute) for age group 60-70 is higher than other age groups. However, avg. distance(km) for age group 30-40 (1.8km) is higher than other age groups(1.3km-1.7km).

* Finally, San Fransisco has the largest number of stations and is higher in all statistics than Oakland_Berkeley and San Jose cities. Average duration and distance is higher in San Fransisco than other cities but San Fransisco 's member age is older than other cities.

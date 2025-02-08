# Case_Study_Cyclistic

## Scenario
You are a junior data analyst working on the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

### Characters and teams
* Cyclistic: A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand
tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use the bikes to commute to work each day

* Lily Moreno: The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program.
These may include email, social media, and other channels.

* Cyclistic marketing analytics team: A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy learning about Cyclistic’s mission and business goals—as well as how you, as a junior data analyst, can help Cyclistic achieve them.

* Cyclistic executive team: The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.

### About the company
* In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

* Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

* Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs.

* Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

## Ask 

### Business Tasks: The Problems We're Trying to Solve
* How do annual members and casual riders use Cyclistic bikes differently?
* Why would casual riders buy Cyclistic annual memberships?

## Prepare

### Datasets
* The datasets used were from [link](https://divvy-tripdata.s3.amazonaws.com/index.html)
* The time-frame of the data used was from August 2020 to July 2021

### Addressing Licensing, Privacy and Security
* The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement)
* Data-privacy issues prohibit us from using riders’ personally identifiable information.
* This means that we won’t be able to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.

## Process

### Tools chosen
* Google Sheets: The data (per month) was first analyzed in Sheets to get a general understanding of the data
* R: The data (per year) was analyzed as a whole using R as the dataset was too big to utilize SQL and it offers faster data manipulation than spreadsheets
* Tableau: Tableau was utilized for the purpose of data visualization and creating the dashboard

### Changelog (Sheets)
* Added two new columns to all the months:
1. ride_length: Calculated the total lengths of each trip using the started_at and ended_at columns
2. day_of_week: Calculated the day of each trip using the started_at column

* Created pivot tables for each month, focusing on the following metrics:
1. Total Rides per Weekday: Calculated the total no. of rides per weekday for members and casuals
2. Average Ride Length: Calculated the average length per different days of the week of trips for members and casuals
3. Total Rides per Hour: Calculated the total no. of rides per the time of day by members and casuals 
4. Total Rides per Day: Calculated the total no. of rides per each day of the month for members and casuals 
5. Total Rides per Bike Type: Calculated the total no. of rides per bike type for members and casuals

## Analyze

### Documentation
* The aggregation, organization and formatting of the data was done using R, and so were the corresponding calculations
* The entire process is documented in R_Script_I.

## Share

### Data Visualization
* The changes made to the R Script for the data visualization process are documented in R_Script_II.
* The dashboard created using Tableau can be accessed using this [link](https://public.tableau.com/app/profile/arnav.shandilya/viz/Case_Study_Cyclistic_17390290136070/Dashboard1)

### Final Conclusion
* The **members** had the most rides **(56% of total rides)**.
* The **classic bike** was the most popular bike type. But for casual riders specifically **docked bikes** were the most popular bike type.
* **Weekends** were the most popular days, with **Saturday** being the most popular day for both users.
* Casual riders showed great variation in weekly bike usage, with a **standard deviation of 95623.17**, roughly **37% of the mean (260481.71)**. While members show much more constant usage, with a **standard deviation of 22714.02**, roughly **6.83% of the mean (332680.43)**.
* **Summer (June - August)** was the busiest season for both users, with the most number of bike rides in **July**.

## Act

### Next Steps: Strategy to Convert Casual Riders to Annual Members
* Personalize discounts and effectively highlight the perks of the membership program based on the riders' preferences and riding habits.
* Discounts would work best during busy times of the year, like during the summer months or on weekends.
* Have current members share their stories about how being an active part of Cyclistic changed their life and to create a sense of community for newer members to feel more welcome.

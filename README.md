# [DUFT by Schaffy](https://duftswiss.com/)
A temporary company to dive deeper into understanding data and how to make data-driven decision making.

Course certificate: [Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/account/accomplishments/verify/P67G9BM7HW47)

# Introduction
In this case study, I will perform many real-world tasks of a junior data analyst at my temporary company, [DUFT by Schaffy](https://duftswiss.com/). In order to answer the key business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

SQL Queries:
01. Data Combining
02. Data Exploration
03. Data Cleaning
04. Data Analysis

Data Visualizations: Tableau

# Background
DUFT by Schaffy is a temporary brand run by Schaffy Zainuddin, a well-known influencer with more than 170K subcribers on Youube and over 20K followers on Instagram. The company is renowned for its luxurious Swiss-inspired collection, primarily offers exquisite home perfumes, candles, and body scrubs. The Winter Collection, featuring Lavender, caters to introverts seeking solace, while the Spring Collection showcases the opulent Luxurious Rose scent, tailored for confident extroverts and elegant gatherings.

Operating in Malaysia, a muslim majority country, yet entirely managed in Switzerland, DUFT by Schaffy achieved a commendable break-even within two months, retailing 1000 products in 10 months. Employing various marketing strategies, including influencer and celebrity endorsements, the outcomes have been intriguingly unpredictable. The sales peak during December, coinciding with Christmas celebrations, while sales during Eid, the Muslim equivalent of Christmas, exhibit a downturn. Leveraging data analytics, our case study seeks to unravel the underlying factors behind these trends.


# Ask
Business Task
Devise marketing strategies to convert casual riders to members.

Analysis Questions
Three questions will guide the future marketing program:

How do annual members and casual riders use Cyclistic bikes differently?
Why would casual riders buy Cyclistic annual memberships?
How can Cyclistic use digital media to influence casual riders to become members?
Moreno has assigned me the first question to answer: How do annual members and casual riders use Cyclistic bikes differently?

# Prepare
Data Source

Data Organization
There are 12 files with naming convention of YYYYMM-divvy-tripdata and each file includes information for one month, such as the ride id, bike type, start time, end time, start station, end station, start location, end location, and whether the rider is a member or not. The corresponding column names are ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng and member_casual.

# Process
BigQuery is used to combine the various datasets into one dataset and clean it.
Reason:
A worksheet can only have 1,048,576 rows in Microsoft Excel because of its inability to manage large amounts of data. Because the Cyclistic dataset has more than 5.6 million rows, it is essential to use a platform like BigQuery that supports huge volumes of data.

Combining the Data
SQL Query: Data Combining
12 csv files are uploaded as tables in the dataset '2022_tripdata'. Another table named "combined_data" is created, containing 5,667,717 rows of data for the entire year.

Data Exploration
SQL Query: Data Exploration
Before cleaning the data, I am familiarizing myself with the data to find the inconsistencies.

Data Cleaning
SQL Query: Data Cleaning

All the rows having missing values are deleted.
3 more columns ride_length for duration of the trip, day_of_week and month are added.
Trips with duration less than a minute and longer than a day are excluded.
Total 1,375,912 rows are removed in this step.

# Analyze and Share
SQL Query: Data Analysis
Data Visualization: Tableau

# Act
After identifying the differences between casual and member riders, marketing strategies to target casual riders can be developed to persuade them to become members.
Recommendations:

Marketing campaigns might be conducted in spring and summer at tourist/recreational locations popular among casual riders.
Casual riders are most active on weekends and during the summer and spring, thus they may be offered seasonal or weekend-only memberships.
Casual riders use their bikes for longer durations than members. Offering discounts for longer rides may incentivize casual riders and entice members to ride for longer periods of time.

# [DUFT by Schaffy](https://duftswiss.com/)
A temporary company created to learn deeper into understanding how to make data-driven decision.

Course certificate: [Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/account/accomplishments/verify/P67G9BM7HW47)

# Introduction
In this case study, I am performing data analytics tasks as the Digital Marketing Manager at [DUFT by Schaffy](https://duftswiss.com/). In order to answer the key business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

Technical processes included:
01. Data Exploration (spreadsheet)
02. Data Cleaning (spreadsheet)
03. Data Combining (SQL)
04. Data Analysis (SQL)
05. Data Visualizations (Tableau)

# Background
[DUFT by Schaffy](https://duftswiss.com/) is a temporary company to sell only 1000 products run by [Schaffy Zainuddin](https://www.youtube.com/@schaffyzainuddin/), an influencer with more than 170K subcribers on YouTube and over 25K followers on [Instagram](https://www.instagram.com/schaffybuffy/). The company is renowned for its luxurious Swiss-inspired collection, primarily offers exquisite home perfumes, candles, and body scrubs. The Winter Collection, featuring Lavender, caters to introverts seeking solace, while the Spring Collection showcases the opulent Luxurious Rose scent, tailored for confident extroverts and elegant gatherings.

Operating in Malaysia, a muslim majority country, yet entirely managed remotely in Switzerland, [DUFT by Schaffy](https://duftswiss.com/) achieved a commendable break-even within two months, retailing 1000 products in a year. Employing various marketing strategies, including influencer and celebrity endorsements, the outcomes have been intriguingly unpredictable. The sales peak during December, coinciding with Christmas celebrations, while sales during Eid, the Muslim equivalent of Christmas, exhibit a downturn. Leveraging data analytics, our case study seeks to unravel the underlying factors behind these trends.


# Ask

Analysis Questions

1. Which type of marketing exposure is most succesful:
   - Endorsement: Celebrity or influencer?
   - Platform: YouTube or Instagram?
1. When is the best time of the month and year to promote luxurious products while still maintain its exclusiveness?
1. How can DUFT use digital media to influence buyers to buy more products?

# Prepare
Data Source and Organization

There are 3 files wich are 'annual_sale', 'customer_report' and 'customer_persona'. For 'annual_sale' it includes information for each month's total sale, total order, total shipping amount, total gross saleand total net sale. In 'customer_persona' includes names, order_id, number of order, date purchased, product type, region, email, address, total spend, AOV, Postcode. 'customer_persona' includes names, order_id, sex, relegion and age

# Process
Spreadsheet is used to combine the various datasets into one dataset and clean it.

Reason:
Since the number of dataset is below 100,000 it is the company's best ineterest to use spreadsheet to maintain the small number of data. It is however essential at this point to use a platform like BigQuery, so I can demonstrate my technical skills in SQL.

### 01. Data Exploration (Spreadsheet)

Before cleaning the data, I am familiarizing myself with the data to find the inconsistencies.

### 02. Data Cleaning (Spreadsheet)

- All the rows having missing values are deleted.
- 3 more columns are added 'order_id', 'sex' and 'region' (for data privacy purpose before sharing this data to the public)
-    'order_id' and 'sex' to replace customers' names
-    'region' is to replace their full address
- Unsuccessful orders that equals to $0 payment are excluded.
- Total 14 rows are removed in this step.

### 03. Combining the Data (SQL)

Three csv files are uploaded as tables in the dataset 'customer_report' and 'customer_persona'. Another table named "annual_sale" is created, containing 12 rows of data for the entire year.

# Analyze and Share

### 04. Data Analysis (SQL)

I utilized SQL to extract data from 2 different tables from the database using **JOIN** and **VIEW**.

### 05. Data Visualization

Please refer here: Tableau

# Act

Recommendations:

Marketing campaigns for luxurious products are best to be conducted in December of the year than any month. Expect a drop of sale during religious celebration for luxurious product. 

Endorsement from influencers are more effective than an A-class celebrity. Although the influencers's audience must first be analyzed to reach the targeted results during marketing campaign

Best to offer discounts is during last week of the month starting from Thursday. Saturday and Sunday is not that effective.

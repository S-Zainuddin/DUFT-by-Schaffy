# [DUFT by Schaffy](https://duftswiss.com/)
A temporary company selling only 1000 limited luxury products.

[Course certificate for Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/account/accomplishments/verify/P67G9BM7HW47)

# Introduction
In this case study, I am performing data analytics tasks as the Digital Marketing Manager at [DUFT by Schaffy](https://duftswiss.com/). In order to answer the key business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

Technical processes included:
01. Data Exploration (spreadsheet) 
    - [Shipment Report (raw but complete),](https://docs.google.com/spreadsheets/d/1GJXUTIs9mA_2KQewCUC8mBlYMuzv37Xr9gE7hwv4Xwg/edit?usp=sharing)
    - [Customer Report (raw & incomplete)](https://docs.google.com/spreadsheets/d/1DeJP3ipuAoH03-n637Y6AaxwYkdooS5uKw0ghecJFKI/edit?usp=sharing)
02. Data Merging (spreadsheet)
    - [Customer Report (processing)](https://docs.google.com/spreadsheets/d/1_GP89bI8O67QkSgPSGSjzbLZHkTQLW4-hD_GLOMgBVc/edit?usp=sharing)
03. Data Cleaning (spreadsheet)
    - [Shipment Report (merged and cleaned),](https://docs.google.com/spreadsheets/d/1wa46LmuE2DELTxfd0UK7dWhwiXqrbVkv-3jxKbVfVyo/edit?usp=sharing)
    - [Customer Report (cleaned)](https://docs.google.com/spreadsheets/d/1tsIvlwGVXkzDTGnek8y7EfeY6NKKjy36HEJ86s0_Nwk/edit?usp=sharing)
04. Data Combining (SQL)
05. Data Analysis (SQL)
06. Data Visualizations 
    - [Tableau](https://public.tableau.com/app/profile/syafafa.zainuddin/viz/Book1_16909912115190/NetSalebyMonth?publish=yes)

# Background
[DUFT by Schaffy](https://duftswiss.com/) is a temporary company to sell only 1000 products run by [Schaffy Zainuddin](https://www.youtube.com/@schaffyzainuddin/), an influencer with more than 170K subcribers on YouTube and over 25K followers on [Instagram](https://www.instagram.com/schaffybuffy/). The company is renowned for its luxurious Swiss-inspired collection, primarily offers exquisite home perfumes, candles, and body scrubs. The Winter Collection, featuring Lavender, caters to introverts seeking solace, while the Spring Collection showcases the elegant Luxurious Rose scent, tailored to invoke confidence at gatherings.

Operating in Malaysia, a muslim majority country, yet entirely managed remotely in Switzerland, [DUFT by Schaffy](https://duftswiss.com/) achieved a commendable break-even within two months, retailing 1000 products in a year. Employing various marketing strategies, including influencer and celebrity endorsements, the outcomes have been intriguingly unpredictable. The sales peak during December, coinciding with Christmas celebrations, while sales during Eid, the Muslim equivalent of Christmas, exhibit a downturn. Leveraging data analytics, our case study seeks to unravel the underlying factors behind these trends.


# Ask

Analysis Questions

1. What is the most effective month to launch a marketing campaign for a luxury product in a Muslim country? Does the occurrence of religious celebrations influence the outcomes?
1. How can DUFT use digital media to influence buyers to buy more products?

# Prepare
Data Source:

* Data are collected after every marketing campaigns. There are six marketing campaigns over the course of one year (Christmas Sale, Chinese New Year Sale, Harry Potter Sale, Eid Sale, Mother's Day Sale and Goodbye Sale)

* Endorsement from a local [influencer with 270K followers on Instagram](https://www.instagram.com/aisyahhabshee/?hl=en) is performed during Harry Potter Sale

* Endorsement from a local [celebrity with 1M followers on Instagram](https://www.instagram.com/mishaomar/?hl=en) is performed during Mother's Day Sale

* There are 3 files which are 'annual_sale', 'customer_report' and 'customer_persona'. For 'annual_sale' it includes information for each month's total sale, total order, total shipping amount, total gross saleand total net sale. In 'customer_persona' includes names, order_id, number of order, date purchased, product type, region, email, address, total spend, AOV, Postcode. 'customer_persona' includes names, order_id, sex, relegion and age

Challenges:

01. According to the spreadsheet, there is only 'name' given but no customer_id. Customer_id must be added into the coloumn as it will be used to protect data privacy before sharing this database to public.

02. With data privacy set up within woocommerce, all data about customers in customer_report from August 2022 to January 2023 are automatically deleted leaving only 'number of order' 'total spend' and 'last time updated'. The only way to retrieve some of the important data is by collecting them from other platform which is easyparcel.com, an online delivery service. According to te data, there are 363 parcels sent and delivered. However I will first investigate, then process and clean the data.

03. The two source of database must be merged together in order to create customer_id.

# Process
Spreadsheet is used to combine the various datasets into one dataset and clean it.

Reason:
Since the number of dataset is below 100,000 it is the company's best ineterest to use spreadsheet to maintain the small number of data. It is however essential at this point to use a platform like BigQuery, so I can demonstrate my technical skills in SQL.

### 01. Data Exploration (Spreadsheet)

* Before cleaning the data, I am familiarizing myself with the data to find the inconsistencies.

### 02. Data Merging (Spreadsheet)

* Database from two different platforms are merged together to create customer_id. It is done wthin a single csv file caled customer_report.

### 03. Data Cleaning (Spreadsheet)

For customer_report file:
- All the rows having missing values are deleted.
- One more column is added, 'order_id' (for data privacy purpose before sharing this data to the public)
-    'order_id' to replace customers' names
-    'region' is to replace their full address
- Unsuccessful orders that equals to $0 payment are excluded.
- Total 14 rows are removed in this step.

For customer_persona file:
- Copied from customer_report file.
- Four more columns are added,
-    Country
-    Sex
-    Religion
-    Total Spend
- Unsuccessful orders that equals to $0 payment are excluded.
- Total 14 rows are removed in this step.

### 04. Combining the Data (SQL)

* Three csv files are uploaded as tables in the dataset 'customer_report' and 'customer_persona'. Another table named "annual_sale" is created, containing 12 rows of data for the entire year.

# Analyze, Share and Act

### 05. Data Analysis (SQL)

*  I utilized SQL to extract data from 2 different tables from the database using **JOIN** for analysis.

### 06. Data Visualization

* Please refer here: [Tableau](https://public.tableau.com/app/profile/syafafa.zainuddin/viz/Book1_16909912115190/NetSalebyMonth?publish=yes)

### 07. Answering the analysis questions and recommendations:

1. What is the most effective month to launch a marketing campaign for a luxury product in a Muslim country? Does the occurrence of religious celebrations influence the outcomes?

- Even in a Muslim-majority country, it is optimal to run a high budget marketing campaigns for luxury products in December as opposed to any other month. This choice is not influenced by religious celebrations; rather, it stems from the fact that during this time, individuals tend to possess greater purchasing power due to end-of-year bonuses. It is important to anticipate a decline in sales during religious festivities such as Chinese New Year and Eid. One of the contributing factors is that people tend to allocate their spending towards the religious celebrations, prioritizing them over expenditures on high-end items.

2. How did DUFT successfuly influenced buyers to buy more luxury products?

- Enhance the perception of exclusivity.

- The strategy: During the recent marketing campaign titled "Goodbye Sale," the volume of orders surged significantly, resulting in products being out of stock within a month's time. Notably, this campaign generated the highest revenue compared to all previous marketing endeavors, even surpassing the Winter Sale held in December. This success can be attributed to the strategy employed, which aimed to create a sense of urgency by emphasizing the dwindling availability of items. The campaign's messaging conveyed that DUFT would be closing its doors in two months, enhancing the perception of exclusivity. Evidently, this approach effectively resonated with customers and yielded the intended outcomes.



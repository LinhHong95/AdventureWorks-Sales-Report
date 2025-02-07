# AdventureWorks-Sales-Report
## Introduction
This project aims to improve sales reporting by delivering an interactive dashboard with dynamic filters, enabling stakeholders to easily explore sales insights and make data-driven decisions. Key performance indicators (KPIs) will be developed to analyze sales trends, product performance, and customer purchases. Actionable insights and recommendations will be provided to support the growth and success of the sales team.
## Business Question
This project focuses on upgrading the sales report from static to interactive visuals, as requested by the Sales Manager. 
- The enhanced report will display total sales, product performance, customer purchases, and sales trends over time.
- It will also include filtering options for salespeople and products to enable deeper analysis and better decision-making.
## User Empathy
<img width="771" alt="Image" src="https://github.com/user-attachments/assets/566560d7-02a4-4713-9746-793ac9974887" />

## Tools and Techniques
- BigQuery
    - Data Preparation
    - Data Processing
- Power BI
    - Data Connection
    - Data Transformation
    - Data Modelling
    - Data Visualisation
## Data source
The AdventureWorks dataset is a publicly available business database in BigQuery, simulating sales transactions for an international bicycle and outdoor equipment company. It includes data on sales, products, customers, employees, and territories, making it ideal for sales performance analysis.

Source: Google BigQuery AdventureWorks Dataset (https://console.cloud.google.com/welcome?q=search&referrer=search&project=adventureworks2019&inv=1&invt=Abo1bw)
## Workflow
### 1. Data Preparation
This stage involves identifying key tables, selecting relevant columns, and structuring data for seamless analysis.
<img width="553" alt="Image" src="https://github.com/user-attachments/assets/cf5de890-bef2-4bab-9803-4b4425a03724" />

### 2. Data Processing
#### 2.1. Extracting data with BigQuery
I queried relevant data and performed initial cleaning such as date formatting and text joins.
- Fact_SalesOrderHeader Table
<img width="867" alt="Image" src="https://github.com/user-attachments/assets/6735c6a7-e206-4aa1-9681-590f9fb5fda3" />

- Fact_SalesOrderDetail Table
<img width="863" alt="Image" src="https://github.com/user-attachments/assets/72130fcb-b56d-44cb-ad78-41c482b250ec" />

- Dim_Product Table
<img width="863" alt="Image" src="https://github.com/user-attachments/assets/cf73fd5c-e53d-46c5-96f6-20612cad14a4" />

- Dim_Customer Table
<img width="868" alt="Image" src="https://github.com/user-attachments/assets/b10eb600-4098-4be9-ba86-2aff99215347" />

- Dim_Salesperson Table
<img width="862" alt="Image" src="https://github.com/user-attachments/assets/31ed1453-dc41-4898-89d5-a3a8baf1a9bb" />

- Dim_Location Table
<img width="866" alt="Image" src="https://github.com/user-attachments/assets/dad7bcdd-cb5e-4fbf-a7ab-a77fa5810291" />

#### 2.2. Connecting data to Power BI
Processed data is saved as CSV files and directly imported to Power BI.
#### 2.3. Transforming data
- A Dim_Date table is created to support time-based analysis, enabling filtering by year, quarter, month, and day.
- I standardised column names and formats for consistency across tables.
#### 2.4. Modelling data
<img width="1125" alt="Image" src="https://github.com/user-attachments/assets/25b8ed3f-6e00-43d7-ad17-ce8b0c733dab" />

### 3. Data Analysis
I established calculated columns and measures for KPIs based on the key formula:
- Sales performance:
  Total Sales = Number of Orders x Average Order Value (AOV)
- Product performance:
  Total Sales = Average Price per Unit x Unit Sold
- Customer purchase:
  Total Sales = Revenue per Customer x Number of Customers
Sales Trends Over Time are explored by multidimensions namely overall performance, product efficiency and customer spending. 

### 4. Data Visualisation
<img width="1024" alt="Image" src="https://github.com/user-attachments/assets/491ec4df-caa2-458f-ab39-31fe682ccda2" />
<img width="1023" alt="Image" src="https://github.com/user-attachments/assets/d8224566-bb9f-47a0-9970-30d473cd2e78" />
<img width="1024" alt="Image" src="https://github.com/user-attachments/assets/94d90ce4-2de5-41ac-8eec-7b54f9108fbc" />

### 5. Insights and Recommendations
#### 5.1. Pricing and Revenue Trends
- Sales peaked annually from March to October, suggesting a seasonal demand pattern. The Sales Team should launch targeted promotions and new product releases ahead of peak season to maximise revenue.
- Australia's sales revenue almost doubled (+99%), from $2.12M to $4.23M from 2012 to 2013. This significant increase placed Australia as the 4th highest revenue-generating country. With this remarkable growth, Australia presents a highly promising market for further expansion.
- The average price per unit declined significantly by 73.5% (from $1,259 in 2012 to $333 in 2014), primarily due to price reductions in the Bike and Components category. The decline in revenue despite steady unit sales suggests price sensitivity in the market. Lower margins on high-revenue products indicate a need for strategic pricing adjustments.
#### 5.3. Product Performance
- Accessories sales surged 459% (from 5,750 to 32,153 units), and Clothing sales increased 93% (from 19,228 to 37,180 units) from 2012 to 2013, demonstrating shifting consumer preferences. In 2014, Accessories revenue surpassed Clothing and Components, becoming the second-highest revenue-generating category.
- This shift reflects a growing consumer preference for add-on purchases, presenting a strategic opportunity to position Accessories as a market penetration product. Their broad appeal, affordability, and upselling potential make them an effective driver for expanding the customer base and increasing overall sales. The Sales Team should introduce bundled promotions, upsell with bike purchases, introduce premium and budget-friendly accessories to cater to diverse customer segments and optimise distribution channels to maximise accessibility.
- The bike category remained the highest revenue contributor, but notable shifts in consumer preferences emerged. Road bikes and touring bikes experienced a decline in unit sales from 2012 to 2013, while mountain bikes saw a significant increase in demand, driving overall category growth. This upward trend in mountain bike sales persisted despite a decrease in the average price across all bike products, suggesting that volume growth offset price reductions. The Sales team should prioritise Mountain Bike Marketing, investigate declining sales in road and touring bikes to identify potential causes.
#### 5.2. Customer Trends
- The customer base grew 262% (from 3,915 to 14,182), but spending per customer declined 64% (from $8,563 to $3,076) from 2012 to 2013. This trend was expected to continue in 2014, indicating a shift toward lower-value purchases.
- While attracting new customers has been successful, lower spending per customer suggests a need for improved customer retention and upselling strategies. Loyalty programs, personalized product recommendations, and bundled discounts should be implemented to encourage higher spending among existing customers.

## Summary
In this project, I enhanced sales reporting by developing key performance indicators (KPIs) to analyze sales trends, product performance, and customer purchases. I leveraged BigQuery for data extraction and processing, then imported and transformed the data in Power BI, where I established relationships between tables and created calculated measures for deeper analysis. Finally, I designed an interactive dashboard with dynamic filters for salespeople, products, time, and location, enabling stakeholders to explore sales insights more efficiently and make data-driven decisions.








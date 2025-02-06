# AdventureWorks-Sales-Report
## Introduction
Traditional static sales reports limit data exploration, making it difficult to spot trends, track performance, and gain actionable insights. In contrast, visual sales reports offer interactive dashboards that let users easily filter data, identify trends, and make quicker, more informed decisions. By shifting to a visual reporting system, businesses can improve efficiency, enhance decision-making, and gain a deeper understanding of sales performance, customer behaviour, and product trends.
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
I queried relevant data, performed initial cleaning such as date formatting, text join.
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
  Total Sales = Number of Order x Average Order Value (AOV)
- Product performance:
  Total Sales = Average Price per Unit x Unit Sold
- Customer purchase:
  Total Sales = Revenue per Customer x Number of Customers
Sales Trends Over Time is explored by multidimension namely overall performance, product efficiency and customer spending. 

### 4. Data Visualisation
<img width="1024" alt="Image" src="https://github.com/user-attachments/assets/491ec4df-caa2-458f-ab39-31fe682ccda2" />
<img width="1023" alt="Image" src="https://github.com/user-attachments/assets/d8224566-bb9f-47a0-9970-30d473cd2e78" />
<img width="1024" alt="Image" src="https://github.com/user-attachments/assets/94d90ce4-2de5-41ac-8eec-7b54f9108fbc" />

### 5. Insights and Recommendations

## Summary
This project enhances sales reporting with KPIs of Sales trend, Product performance and Customer Purchase. Using an interative dashboard with dynamic filters for salespeople, products, time and location allows a faster and deeper analysis of sales KPIs. 

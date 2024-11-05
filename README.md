# Retail Store Sales Analysis


### Project Outline

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)


### Project Overview

This project aim is to analyze the sales performance of a retail store using sales data to uncover key insights such as 
top-selling products, regional performance, and monthly sales trends. 
The goal is to produce an interactive Power BI dashboard that highlights deeper understanding of the company's performance.

### Data Source

The Source of the data used is LITA Capstone Project. xlsx

### Tools Used

- Excel
   - Data Cleaning
   - Data Analysis
   - Data Visualization
- SQL Server
  - Data Manipulation
- Power BI
  - Data Visualization
 
 ### Data Cleaning and Preparation

In the Initial data preparation phase, we performed the following tasks:

 1. Data Loading and Inspection
 2. Handling missing Values
 3. Data cleaning and formatting.

### Exploratory Data Analysis

This involves using sales data to answer key questions such as:

i. Total sales by product

ii. Total sales by region.

iii. Total sales by month.

iv. Average sales per product 

v. Average total revenue by region.

### Data Analysis

This includes the interesting code/features worked with

* AVERAGEIF function: This was used to get the average sale per product in excel
```
  =AVERAGEIF(C:C,C7,H:H)
```
  * SUMIF Function: This function was used to get total sales per region

```
  =SUMIF(D:D,D4,H:H)
```

*SQL QUERIES AND RESULTS

 
1.   Find below quaries used to retrieve the total sales for each product category

 ```sql

SELECT Product, Sum (Total_Sales)
FROM lita_capstone_dataset
GROUP by Product
ORDER by Product
```
![Sql_1](https://github.com/user-attachments/assets/703fd7f3-587b-4477-9e3c-6882bda5c822)

2.   Find the number of sales transactions in each region.

 ```sql
SELECT Region, sum(Quantity) as Sales_TXN
FROM lita_capstone_dataset
GROUP by Region
ORDER by Region
```
![Sql_2](https://github.com/user-attachments/assets/b07a1669-1fad-49cc-acc7-71442b95b4e1)

3.   Find the highest-selling product by total sales value

```sql
SELECT Product, Sum(Quantity*Unit_Price)as Total_Sales 
FROM lita_capstone_dataset
GROUP by product
ORDER by Total_Sales Desc;
```
![Sql_3](https://github.com/user-attachments/assets/8e11f8b0-2311-4957-801b-e38dffa10754)

4.   Calculate total revenue per product

```sql
SELECT Product, Sum(Total_Sales) as Total_Revenue 
FROM lita_capstone_dataset
GROUP by product
ORDER by product;
```
![Sql_4](https://github.com/user-attachments/assets/60db0123-e52a-47f6-979b-948f8923f8bf)

5.   Find the top 5 customers by total purchase amount

```sql
SELECT Customer_Id, Sum(Quantity*Unit_price) as Total_sales
FROM lita_capstone_dataset
GROUP by customer_Id
ORDER by Total_sales Desc
LIMIT 5;
```
![Sql_5](https://github.com/user-attachments/assets/1b5da802-d924-488b-a1af-0ae4a7e3a756)

### Data Visualization

Below are the visuals created using the dataset provided.

#### Excel Pivot Tables

![Exc_1](https://github.com/user-attachments/assets/f2d30351-c6ec-4bbf-94d2-b5770724a05c)

![Exc_2](https://github.com/user-attachments/assets/3c9a6819-0236-4681-88bb-a7e34875d55a)

![Exc_3](https://github.com/user-attachments/assets/642396f3-df85-4335-b249-dc70c4aeaae2)

![Ecx_4](https://github.com/user-attachments/assets/d6a74a56-aba0-4415-a72e-d925e05e8717)

#### Power BI Dashboard

![PBI_1](https://github.com/user-attachments/assets/79cb9d5e-6a31-4224-8dea-f25e55ff690f)

![PBI_2](https://github.com/user-attachments/assets/373aa038-c243-4268-9414-176694c7786e)



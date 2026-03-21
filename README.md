# Amos Giftware

## Contents Table
- [Introduction](#1-introduction)
  - [Overview](#2-overview)
  - [Business Questions to Answer](#3-business-questions-to-answer)
- [Dataset Overview](#4-dataset-overview)
  - [Dataset Shape](#5-dataset-shape)
  - [Key Variables](#6-key-variables)
  - [Data Types](#7-data-types)
- [Project Scope and Tools](#8-project-scope-&-tools)
  - [Scope](#9-scope)
  - [Tools & Technology](#10-tools-&-technology)
- [Missing Data](#11-missing-data)
- [Key Findings](#12-key-findings)
- [Recommendations](#13-recommendations)

## 1. Introduction

### 2. Overview
Amos Giftware is a UK-based online retail store that sells unique all-occasion gifts.
The company provides to the general public and to a large percentage of international wholesalers.

### 3. Business Questions to Answer
- What are our customer behaviour trends?
- Which are the top products sold?
- Is there a trend in sales?
- Can we identify loyal customers?
- Can we identify customers that could become churn?
- What are our best Countries for sales?

## 4. Dataset Overview
The dataset is the online_retail_II dataset sourced from [Kaggle.com](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci).
And covers the years 2009 - 2011.

### 5. Dataset Shape
**Rows**: 1067371.
**Columns**: 8.

### 6. Key Variables
The 8 Columns are: Invoice, StockCode, Quantity, Description, InvoiceDate, Price, Customer ID, Country.

### 7. Data Types
- object
- int64
- float64

## 8. Project Scope & Tools

### 9. Scope
**In Scope**: All 8 columns can be used for the analysis.

**Out of Scope**: During the EDA, I will exclude all stock codes beginning with 'C' as these are cancelled orders/transactions
and could skew the results. I will use the cancelled orders for the dashboard.

### 10. Tools & Technology
- Jupyter Notebook - This will be used for the Analysis part of the project.
- CSV file - The dataset is in a CSV format.
- Power BI - Power BI will be used to create the dashboard in the final step.

## 11. Missing Data
**Null values**:
Description - 4382 (22.77%)
Customer ID - 243007 (0.41%)

**Negative Values**:
Customer ID - this shows that orders were from guest orders or that the order was cancelled.
Quantity - There are negative values in the Quantity column, which match the Cancelled orders/transactions.

## 12. Data Cleaning
**Null Values**
- Customer ID - Changed all 0 values and null values to 0 to represent Guest checkouts.

**Empty Values**
- Quantity - All 0 values in Quantity related to Cancelled orders/transactions, these were removed as they would skew the results.
- Price - All 0 values in Price related to Cancelled orders/transactions, these were removed so they did not skew the results.

**Data Type Changes**
- InvoiceDate - Changed the InvoiceDate from an object to datetime.
- Customer ID - Changed from float to int.
- Customer ID - Changed from float64 to int64.

**New Columns Added**
- Weekday - Added a weekday column to make trend analysis easier.
- TotalSales - Makes the transactions easier to analyse in full cost.

## 13. Analysis
**Univariate**
- Top 10 Countries by Quantity.
**Findings**: The UK has the highest Quantity score.

- Top 10 Products.
**Findings**: The best Product for Quantity was the 'WW2 Glider Asstd Designs'.

**Bivariate**
- Top 10 Countries by Total Sales.
**Findings**: The UK, top Total Sales, with Eire and the Netherlands following 2nd and 3rd.

- Monthly Sales Trend.
**Findings**: In 2010 and 2011, October is the best Month for sales. This is because of the Christmas period.

- Daily Sales Trend.
**Findings**: The sales trends are even in both years. The most notable drops are in 2010 for May and August.

- Weekday Sales.
**Findings**: Saturday is the worst day, and Sunday 2nd worst. The best 2 days for sales are Thursday & Tuesday.

**RFM (Regency, Frequency, Monetary)**
- Distribution of RFM counts.
**Findings**: The scores are in 9 bins. The highest count bin is the 9th with 1200 counts. The other 8 bins are even with around 600 counts each.

- Top 15 Customers.
**Findings**: Customer ID 15380 is the top customer. Above Customer 15380 are all the Guest buyers.

## 12. Key Findings

## 13. Recommendations

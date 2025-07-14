# 🛒 Supermarket Sales Data – Cleaning and Analysis

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Results and Findings](#results-and-findings)
- [Limitations](#limitations)
  - [Data Quality Issues](#data-quality-issues)
  - [Data Tidiness Issues](#data-tidiness-issues)

---

## 🔎 Project Overview

This project focuses on analyzing supermarket sales data from the first quarter of 2019. The objective is to extract insights, discover patterns, and make data-driven recommendations to better understand the supermarket's performance and customer behavior.

---

## 📂 Data Sources

The dataset used is titled **"Capstone Data - Supermarket Sales.csv"**, which contains detailed transactional data such as invoice numbers, customer information, payment methods, product categories, and timestamps.

---

## 🛠️ Tools Used

- **Python**: For data cleaning, transformation, and analysis.  
- **Power BI**: For interactive dashboards and visual storytelling.  
  > 🔗 [Download Power BI](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

---

## 🧹 Data Cleaning and Preparation

Initial preprocessing included:

1. Importing and inspecting the dataset.
2. Handling missing, duplicated, and inconsistent values.
3. Converting columns to appropriate data types.
4. Formatting and restructuring data to prepare for analysis.

---

## 📊 Exploratory Data Analysis (EDA)

Key questions explored during analysis:

- How many invoices were issued?
- What is the total revenue?
  - Revenue by city
  - Revenue by day and city
  - Revenue by product line and gender
  - Revenue by time of day and weekday
  - Revenue by month, customer type, and payment method
- What is the average customer rating per city?
- How many customers were there by gender and type?
- What was the most commonly used payment method?

---

## 📈 Results and Findings

1. **Total Revenue**:  
   - The total revenue during Q1 2019 was approximately **$323,000**.

2. **Top Revenue City**:  
   - **Naypyitaw** recorded the highest revenue.  
     *Note: Revenues across all cities were nearly equal.*

3. **Highest Customer Rating**:  
   - Naypyitaw also had the highest average rating.

4. **Peak Sales Time**:  
   - **7:00 PM** was identified as the peak sales hour.

5. **Top Revenue Month**:  
   - **January** was the most profitable month.

6. **Lowest Revenue Month**:  
   - **February**, with a **16%** drop in revenue compared to January.

7. **Customer Type Comparison**:  
   - Normal customers generated more revenue than members.  
     *Note: Customer type had minimal impact on revenue per invoice.*

8. **Top Sales Day**:  
   - **Saturday** generated the highest revenue.

9. **Best-Selling Product Line**:  
   - **Food & Beverages** was the most purchased category.

10. **Customer Type Distribution**:  
    - More **normal** customers than **members**.

11. **Gender Distribution**:  
    - The number of **male** customers was higher than **female** customers.

12. **Most Used Payment Method**:  
    - **E-wallets** were the most commonly used, although usage across all payment types was quite similar.

---

## ⚠️ Limitations

### 🧼 Data Quality Issues

To ensure clean and reliable data, the following issues were identified and addressed:

1. Removed duplicated rows to prevent double-counting.
2. Standardized `Rating` values to fall within the 0–10 range by scaling down any values above 10.
3. Cleaned the `Unit Price` column by removing non-numeric characters and converting values to float.
4. Converted negative values in the `Quantity` column to positive.
5. Filled missing values in the `Tax 5%` column by recalculating the correct tax amounts.
6. Rounded values in the `Tax 5%` and `Total` columns to four decimal places for consistency.
7. Reformatted the `Time` column into 24-hour format (HH:MM).
8. Corrected misspelled entries such as `"Memberr"` to `"Member"`.
9. Replaced missing or undefined customer types (`"-"`) with `"Normal"`.

---

### 🧹 Data Tidiness Issues

To improve structure and clarity:

1. Created a new column `City` with values: `Yangon`, `Naypyitaw`, and `Mandalay`.
2. Dropped old one-hot encoded city columns.
3. Combined the `City` and `Branch` columns into a single column for regional identification.
4. Removed the original `City` and `Branch` columns after merging.

---

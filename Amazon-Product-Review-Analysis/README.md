# 📊 AMAZON PRODUCT REVIEW - Capstone Project

This project was created as part of my final certification for the **Digital SkillUp Africa (DSA) Incubator Program**. It demonstrates my practical expertise using **Microsoft Excel** to analyze product and customer review data from Amazon to generate insights that can guide product improvement, marketing strategies, and customer engagement.

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis & EXCEL Function Examples](#data-analysis--excel-function-examples)
- [Business Insights](#business-insights)
- [Dashboard Previews](#dashboard-previews)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

## 📌 Project Overview

This Amazon product review analytics project analyzes data scraped from Amazon product listings, including:
- Product details (name, category, actual and discounted prices, ratings)
- Customer engagement (review counts and scores)

Each row represents a unique product, and the dataset contains:
- **1,465 records**
- **16 fields**

The project aims to generate business insights for **RetailTech Insights**, a company focused on e-commerce analytics.

---

## 📂 Data Sources

- `Amazon case study.xlsx` (provided as part of the capstone task)

---

## 🛠 Tools Used

- Excel ([Download](https://apps.microsoft.com/detail/9N4JH8NGJR9B?hl=en-us&gl=NG&ocid=pdpshare))

---

## 🧹 Data Preparation

Key actions taken:
- Removed missing/null values and unnecessary columns
- Separated and capitalized joined product categories (e.g., `Computers&Accessories` → `Computers & Accessories`)
- Converted data into a structured Excel Table (`Ctrl + T`)
- Added calculated columns:
  - **Rating Score** = Rating × Review Count
  - **Price Bucket** = `<₹200`, `₹200–₹500`, `>₹500`
  - **Potential Revenue** = Actual Price × Review Count

---

## 📊 Exploratory Data Analysis (EDA)

The following 14 business questions were addressed using PivotTables and formulas:

- What is the average discount percentage by product category?
- How many products are listed under each category?
- What is the total number of reviews per category?
- Which products have the highest average ratings?
- What is the average actual price vs the discounted price by category?
- Which products have the highest number of reviews?
- How many products have a discount of 50% or more?
- What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
- What is the total potential revenue (actual_price × rating_count) by category?
- What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
- How does the rating relate to the level of discount?
- How many products have fewer than 1,000 reviews?
- Which categories have products with the highest discounts?
- Identify the top 5 products in terms of rating and number of reviews combined.

---

## 🧮 Data Analysis & DAX Expressions

**Examples of Excel formulas and tools used:**

- **Extract Product Category**:  
  `=PROPER(SUBSTITUTE(LEFT(C2, FIND("|", C2)-1), "&", " & "))`

- **Convert Formula Output to Text**:  
  Copy → Paste as Values

- **Create Table**:  
  `Ctrl + T`

- **Insert Pivot Table**:  
  `Alt + N + V`

- **Custom Format for Revenue**:  
  `#,##0.00,, "k"`

- **Calculated Columns**:
  - `Potential Revenue`: `=F2 * H2`
  - `Rating Score`: `=G2 * H2`
  - `Price Bucket`: `=IF(D2<200,"<₹200",IF(D2<=500,"₹200–₹500",">₹500"))`

- **Review and Discount Filters**:  
  `=COUNTIF(F2:F1465, ">=0.5")`  
  `=COUNTIF(H2:H1465, "<1000")`

---

## 🧠 Business Insights

- **751 products** had discounts of **50% or more**
- **327 products** had fewer than **1,000 reviews**
- **Categories with highest average discounts**:
  - Computers & Accessories: 94%
  - Electronics: 91%
  - Home & Kitchen: 90%
- **Top 5 high-performing categories** by combined ratings and reviews:
  - Computers & Accessories
  - Electronics
  - Home & Kitchen
  - Office Products
  - Home Improvement
- **Top 3 Products with highest number of reviews** 
  - Computers & Accessories
  - Home & Kitchen
  - Electronics
 
---

## 📷 Dashboard Previews
### [Amazon Product Dashboard)
<img width="1283" height="717" alt="Amazon_Dashboard_pg1" src="https://github.com/user-attachments/assets/64def7f6-ca12-4125-97b9-93cff78ad37f" />
<img width="1282" height="702" alt="Amazon_Dashboard_pg2" src="https://github.com/user-attachments/assets/f8661a42-7980-4f70-a2c0-ad401d062b10" />

[Amazon_Capstone_Project_Dashboard](https://github.com/user-attachments/assets/231ee634-cfd7-46a8-8fab-7b07a77b1737)

### [Average Discount percentage by Category]
<img width="425" height="318" alt="Average_discount%_per_category" src="https://github.com/user-attachments/assets/d3025360-79ee-4bf8-aa92-f4fff1904d1c" />

### [Product Count per Category]
<img width="413" height="311" alt="Product_count_by_category" src="https://github.com/user-attachments/assets/8f68e197-a65f-4ccd-98d1-8d026a465101" />

### [Total Review by Category]
<img width="427" height="316" alt="Total_review_per_category" src="https://github.com/user-attachments/assets/49c9fff8-146e-408f-8cd0-9ae7b0e6f8f8" />

### [Price range Bucket]
<img width="425" height="310" alt="Product_count_by_Price_bucket" src="https://github.com/user-attachments/assets/ef12e54b-424f-493f-a814-8dde419d87a6" />

### [Highest Discount by Category]
<img width="430" height="318" alt="Highest_discount_by_category" src="https://github.com/user-attachments/assets/86b9be57-d8b4-407f-b002-ceba172ec82a" />

### [Potential Revenue by Category]
<img width="415" height="283" alt="Potential_Revenue_by_category" src="https://github.com/user-attachments/assets/96e807a0-25b7-468c-b91f-0ae2a19c7dc1" />

### [Rating by Product Count]
<img width="420" height="283" alt="Rating by Product_Count" src="https://github.com/user-attachments/assets/04c5c32b-4681-4dfd-bfb6-0df968337911" />

### [Rating relating to level of Discount]
<img width="431" height="309" alt="Rating_relating_to_the_level_of_Discount" src="https://github.com/user-attachments/assets/948af6c2-3f36-42d0-ac78-553fd1e7dab1" />

### [Average Actual Price vs Average Discounted Price]
<img width="427" height="311" alt="Average_actualprice_Average_Discountedprice" src="https://github.com/user-attachments/assets/05ce4952-f4f8-47a1-84b9-fd4d8c123162" />

### [Highest Average Rating by Products]
<img width="436" height="308" alt="Highest_average_product_rating" src="https://github.com/user-attachments/assets/02c2ca2d-7f86-4963-8dba-2729191349ab" />

### [Products with highest number of Reviews]
<img width="419" height="310" alt="Product_with_highest _number_of_review" src="https://github.com/user-attachments/assets/232ddcf0-698c-4d26-a8e4-b5cb9302e942" />

### [Top 5 Products by Rating & Reviews Combined]
<img width="437" height="285" alt="Top5_Product_by_Rating_Review_Combined" src="https://github.com/user-attachments/assets/0941c356-2317-47fd-882e-16f064aa3018" />


---

## ✅ Recommendations

- Focus marketing on top-performing categories (e.g., Computers & Accessories, & Electronics)
- Re-target underperforming products with high discounts but low reviews
- Encourage more reviews for high-rating products with fewer than 1,000 ratings
- Consider adjusting pricing strategies for products in low-revenue buckets

---

## ⚠️ Limitations

- Only aggregated review data was provided; detailed review text was not analyzed
- Static Excel analysis; automation not implemented
- Regional differences in customer behavior not accounted for

---

## 📚 References

- Source: Amazon product dataset (DSA Capstone)
- Program: Digital SkillUp Africa – DSA Incubator Program

---

> Created by **Adeleke Olusegun** | Data Analytics Capstone Project | 2025

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
  - Electronics
  - Computers & Accessories
  - Home & Kitchen
 
---

## 📷 Dashboard Previews
### [Amazon Product Dashboard)
[Amazon_Capstone_Project_Dashboard](https://github.com/user-attachments/assets/231ee634-cfd7-46a8-8fab-7b07a77b1737)

### [Average Discount percentage by Category]
[Avg_Discount_percentage_by_Category](https://github.com/user-attachments/assets/9487a911-ec22-41af-8640-67525e751aef)

### [Product Count per Category]
[Product_count_by_category](https://github.com/user-attachments/assets/025a3c42-7ed8-4c15-9af7-268e909d766b)

### [Total Review by Category]
[Total_review_per_category](https://github.com/user-attachments/assets/8aea7c1f-18fc-4c1a-8058-ad01f8497187)

### [Price range Bucket]
[Product_count_by_Price_bucket](https://github.com/user-attachments/assets/4dc2ba87-99be-4ffa-9d7f-3dc158f5a5d6)

### [Highest Discount by Category]
[Highest_discount_by_category](https://github.com/user-attachments/assets/c4765a92-64d6-40a6-857c-31efb601fd92)

### [Potential Revenue by Categor]
[Potential_Revenue_by_category](https://github.com/user-attachments/assets/c822b736-2e1c-45da-b523-cbb2317acb08)

### [Rating by Product Count]
[Rating_by_product_count](https://github.com/user-attachments/assets/95d759ef-f34c-4afe-a5e0-4273972f2bf1)

### [Average Actual Price vs Average Discounted Price]
[Avg_actual_price_vsAvg_discounted_price_Category](https://github.com/user-attachments/assets/6eb0097c-b5c3-453b-aad3-b633a5f932ba)

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

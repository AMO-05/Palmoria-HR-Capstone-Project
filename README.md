# 📊 Palmoria HR Dashboard – Capstone Project

This project is part of my final certification for the **Digital SkillUp Africa (DSA) Incubator Program**, designed to demonstrate my practical expertise in using **Power BI** to analyze HR data and provide actionable business insights.

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Preparation & Modeling](#data-preparation--modeling)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis & DAX Examples](#data-analysis--dax-examples)
- [Business Insights](#business-insights)
- [Dashboard Previews](#dashboard-previews)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

## 📌 Project Overview

This HR analytics project analyzes workforce data from **Palmoria Group** across three regions. The goal is to uncover gender disparities, salary compliance issues, and bonus distribution fairness, enabling data-driven decisions for better HR policy alignment.

---

## 📂 Data Sources

- `Palmoria Group emp_data.csv` – Employee details  
- `Palmoria Group Bonus Rules.xlsx` – Bonus allocation logic

---

## 🛠 Tools Used

- Power BI Desktop ([Download](https://apps.microsoft.com/detail/9ntxr16hnw1t))
- Power Query
- DAX (Data Analysis Expressions)

---

## 🧹 Data Preparation & Modeling

Key actions taken:
- Cleaned null/missing values
- Removed obsolete employee records
- Created conditional columns: `Salary Band`, `Salary Sort`, `Below Minimum`
- Built relationships between datasets using the `Rating` field in the model view

---

## 📊 Exploratory Data Analysis (EDA)

Questions answered:
- What is the gender distribution by region and department?
- Is there a gender pay gap?
- Which employees are below the $90K minimum salary threshold?
- How are performance ratings and bonuses distributed?

---

## 📊 Exploratory Data Analysis (EDA)

Questions answered:
- What is the gender distribution by region and department?
- Is there a gender pay gap?
- Which employees are below the $90K minimum salary threshold?
- How are performance ratings and bonuses distributed?

---

## 🧮 Data Analysis & DAX Examples

```DAX
-- Employees below $90K
Employee Below Minimum Pay Count = 
CALCULATE(COUNTROWS('Cleaned Palmoria Group emp-data'), 
'Cleaned Palmoria Group emp-data'[Below Minimum]= "Below")

-- Gender Pay Gap %
Gender Pay Gap % = 
DIVIDE([Average Male Salary] - [Average Female Salary], [Average Male Salary], 0)
Bonus % was determined using LOOKUPVALUE with conditional logic on rating and department.

🧠 Business Insights
- Gender count gap: 18 employees (1.9%)

- Gender pay gap: $2.2K (2.94%)

- Salary regulation non-compliance: 654 employees below $90K

- Bonus distribution: Nearly equal (Male: 50.95%, Female: 49.05%)

- Regions with highest gaps: Kaduna (gender & pay)

- Department with highest gender gap: Legal

📷 Dashboard Previews

[Gender Distribution]
[Palmoria-HR-Dashboard_Gender_Distribution](https://github.com/user-attachments/assets/15ce0a29-b659-4157-ac68-bd106b57abef)

[Performance Rating Analysis]
[Palmoria-HR-Dashboard_Rating](https://github.com/user-attachments/assets/ad4f2957-f6a9-4e51-9211-ce35b26f151d)

[Salary Band Distribution]
[Palmoria-HR-Dashboard_Salary_Structure](https://github.com/user-attachments/assets/5ada841f-29ad-40a8-97cf-2780a7f12349)

[Compliance with $90K Regulation]
[Palmoria-HR-Dashboard_Salary_compliance](https://github.com/user-attachments/assets/1f3ecfda-d6c6-466f-8ea1-1a4ba03fb273)

[Bonus Allocation Breakdown]
[Palmoria-HR-Dashboard_Bonus_Distribution](https://github.com/user-attachments/assets/c2df70d8-39bc-4201-8f33-c0ae9c459828)

✅ Recommendations
- Focus on Kaduna and Legal department to address gender gaps.

- Adjust salary structures to align with the $90K minimum compliance benchmark.

- Continue tracking performance-based bonus fairness across departments.

⚠️ Limitations
- Salary differences may be influenced by experience, qualifications, or job level.

- Some gender gaps may reflect role-specific labor market availability.

📚 References
- Power BI Official Docs

- Digital SkillUp Africa – Incubator Program

**Created by Adeleke Olusegun | Data Analytics Capstone Project | 2025**


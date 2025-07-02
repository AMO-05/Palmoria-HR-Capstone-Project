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

## 🧮 Data Analysis & DAX Examples

```DAX
-- Employees below $90K
Employee Below Minimum Pay Count = 
CALCULATE(COUNTROWS('Cleaned Palmoria Group emp-data'), 
'Cleaned Palmoria Group emp-data'[Below Minimum]= "Below")

-- Gender Pay Gap %
Gender Pay Gap % = 
DIVIDE([Average Male Salary] - [Average Female Salary], [Average Male Salary], 0)

- Bonus % was determined using LOOKUPVALUE with conditional logic on rating and department.

🧠 Business Insights
Gender count gap: 18 employees (1.9%)

Gender pay gap: $2.2K (2.94%)

Salary regulation non-compliance: 654 employees below $90K

Bonus distribution: Nearly equal (Male: 50.95%, Female: 49.05%)

Regions with highest gaps: Kaduna (gender & pay)

Department with highest gender gap: Legal

📷 Dashboard Previews
(Add your own chart screenshots or use the Power BI report embed link here)

### [Gender Distribution]
[Palmoria-HR-Dashboard_Gender_Distribution](https://github.com/user-attachments/assets/fa195441-27d5-4fa3-af60-cab4a942ce34)

### [Performance Rating Analysis]
[Palmoria-HR-Dashboard_Rating](https://github.com/user-attachments/assets/564287b4-e956-4906-8130-b8e52cf912ae)

### [Salary Band Distribution]
[Palmoria-HR-Dashboard_Salary_Structure](https://github.com/user-attachments/assets/3f54febd-c2dc-4979-9f7d-bcce5b3df135)

### [Compliance with $90K Regulation]
[Palmoria-HR-Dashboard_Salary_compliance](https://github.com/user-attachments/assets/a4f6c453-edb3-4e57-b038-c17df74149c5)

### [Bonus Allocation Breakdown]
[Palmoria-HR-Dashboard_Bonus_Distribution](https://github.com/user-attachments/assets/1a5de18a-f8b9-4d44-8fbb-006f348f29d4)

✅ Recommendations
Focus on Kaduna and Legal department to address gender gaps.

Adjust salary structures to align with the $90K minimum compliance benchmark.

Continue tracking performance-based bonus fairness across departments.

⚠️ Limitations
Salary differences may be influenced by experience, qualifications, or job level.

Some gender gaps may reflect role-specific labor market availability.

📚 References
Power BI Official Docs

Digital SkillUp Africa – Incubator Program

**Created by Adeleke Olusegun | Data Analytics Capstone Project | 2025**


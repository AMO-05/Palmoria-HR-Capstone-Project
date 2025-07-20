# 📊 Palmoria HR Dashboard – Capstone Project

This project is part of my final certification for the **Digital SkillUp Africa (DSA) Incubator Program**, designed to demonstrate my practical expertise in using **Power BI** to analyze HR data and provide actionable business insights.

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Preparation & Modeling](#data-preparation--modeling)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis & DAX Expressions](#data-analysis--dax-expressions)
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

- Palmoria Group `emp_data.csv`
- Palmoria Group `Bonus Rules.xlsx`

---

## 🛠 Tools Used

- Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)

---

## 🧹 Data Preparation & Modeling

Key actions taken:
- Cleaned missing/null values
- Removed records with incomplete gender or salary info
- Created calculated columns: **Salary Band**, **Salary Sort**, **Below Minimum**
- Linked tables via the **Rating** field in Model View

---

## 📊 Exploratory Data Analysis (EDA)

Questions answered:
- What is the gender distribution by region and department?
- Is there a gender pay gap?
- Which employees are below the $90K minimum salary threshold?
- How are performance ratings and bonuses distributed?

---

## 🧮 Data Analysis & DAX Expressions

**Key measures used in the analysis:**

- **Employee Below Minimum Pay Count**: Counts employees earning less than $90K  
- **Below Minimum Pay %**: Measures gender gap below regulation  
- **Meets/Exceeds Minimum Pay Count**: Counts those who meet the $90K salary mark  
- **Gender Count Gap %**: `ABS(Male % - Female %)`  
- **Gender Pay Gap %**: `(Average Male Salary – Average Female Salary) / Average Male Salary`  
- **Bonus Amount**: Calculated as `Salary * Bonus %` based on Rating  
- **Bonus %**: Pulled from department-specific rules using `SWITCH(TRUE(), LOOKUPVALUE(...))`

---

## 🧠 Business Insights

- Gender count gap: **18 employees (1.9%)**
- Gender pay gap: **$2.2K (2.94%)**
- Salary regulation non-compliance: **654 employees below $90K**
- Bonus distribution: Male – 50.95%, Female – 49.05%
- Region with highest gaps: **Kaduna**
- Department with highest gender gap: **Legal**

---

## 📷 Dashboard Previews

- ###[**Gender Distribution**]

<img width="1183" height="661" alt="HR-Dashboard_Gender_Distribution" src="https://github.com/user-attachments/assets/1f52d9a8-0609-4c99-b645-1b630e6629b0" />

- ###[**Rating by Gender**]
  
<img width="1169" height="658" alt="Palmoria-HR-Dashboard_Rating" src="https://github.com/user-attachments/assets/6b0fb351-26c5-4b0d-9b67-ff230f2a749e" />

- ###[**Salary Structure & Banding**]
  
<img width="1122" height="669" alt="Palmoria-HR-Dashboard_Salary_Structure" src="https://github.com/user-attachments/assets/cd4c92fe-cfc9-460d-9955-ce70f2533af2" />

- ###[**Minimum Salary Compliance**]
  
<img width="1126" height="665" alt="Palmoria-HR-Dashboard_Salary_compliance" src="https://github.com/user-attachments/assets/a4859626-c4fe-48f3-b8fe-8aa26ab89681" />

- ###[**Bonus Allocation Insights**]
  
<img width="1130" height="668" alt="Palmoria-HR-Dashboard_Bonus_Distribution" src="https://github.com/user-attachments/assets/694ea5e7-6973-4b17-96fb-fd59b0663499" />


---

## ✅ Recommendations

- Address gender imbalance in **Kaduna** and **Legal department**
- Review compensation structure to comply with the $90K minimum
- Maintain fair and transparent bonus systems

---

## ⚠️ Limitations

- Salary differences may be influenced by factors like experience or job level
- Some department-specific gaps may reflect labor market availability

---

## 📚 References

- Power BI Official Docs  
- Digital SkillUp Africa – DSA Incubator Program

---

> Created by **Adeleke Olusegun** | Data Analytics Capstone Project | 2025

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

### [Gender Distribution]
[Palmoria-HR-Dashboard_Gender_Distribution](https://github.com/user-attachments/assets/fa195441-27d5-4fa3-af60-cab4a942ce34)

### [Rating by Gender]
[Palmoria-HR-Dashboard_Rating](https://github.com/user-attachments/assets/564287b4-e956-4906-8130-b8e52cf912ae)

### [Salary Structure & Banding]
[Palmoria-HR-Dashboard_Salary_Structure](https://github.com/user-attachments/assets/3f54febd-c2dc-4979-9f7d-bcce5b3df135)

### [Minimum Salary Compliance]
[Palmoria-HR-Dashboard_Salary_compliance](https://github.com/user-attachments/assets/a4f6c453-edb3-4e57-b038-c17df74149c5)

### [Bonus Distribution Insights]
[Palmoria-HR-Dashboard_Bonus_Distribution](https://github.com/user-attachments/assets/1a5de18a-f8b9-4d44-8fbb-006f348f29d4)

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




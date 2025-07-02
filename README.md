# PALMORIA HR DOCUMENTATION
This is one of my Data Analysis Capstone project in fulfilment of Digital Skillup Africa- DSA INCUBATOR HUB for the final certification.  

It is to demonstrate my technical indepth in using POWERBI to analyse real world situation and give explicit insights that would enhance decision making.

## PROJECT TOPIC: PALMORIA GROUP HR ANALYSIS

## PROJECT OVERVIEW

This Data Analysis project aims to generate insights that the Palmoria Group management team would be able to address the issues bordering on gender inequalities in its 3 regions.

By analysing the various parameters in the data received, we seek to identify key areas within the business in relation to workforce structure, gender balance, salary distribution, and bonus allocation across Palmoria Group.

This will enable the management team to making spontaneous decisions that would bring about gender equality across its region and beyond for future expansion.

## DATA SOURCES
Primary source of data used here is 'Palmoria Group emp_data.csv' and 'Palmoria Group Bonus Rules.xls'
[Download Here] ()

## ⚙️ TOOLS USAGE
- Power BI Desktop [Download Here](https://apps.microsoft.com/detail/9ntxr16hnw1t?launch=true&mode=full&hl=en-us&gl=ng&ocid=bingwebsearch)
   - Data Cleaning and Preparation
    In the initial phase of the cleaning and prepations, we perform the following actions:
           1. Data loading and inspection
           2. Handling missing variables:
              i. Assigning a generic gender status to those employees whose gender were not specified.
              ii. Some employees records without salaries were deleted because they are no longer with the company
              iii. Some records indicating department as “NULL” were also deleted
           3. Data cleaning and formatting
  - Data Manipulation
  - Data Munching
- DAX
- Power Query
    - Conditional columns were created to aid in generating absolute outcome during analysis.
      
## EXPLORATORY DATA ANALYSIS

EDA involved the exploring of the data to answer some questions about the data such as:

- Gender distribution and pay gap by department and region
- Salary structure vs. $90K minimum compliance
- Rating analysis by gender and region
- Bonus distribution with individual insights

## DATA ANALYSIS

This is where I include some basic lines of codes and even some of the DAX expression used during the analysis.

... Measure to count the numbers of employee below minimum pay
- Employee Below Minimum Pay Count = 
CALCULATE(COUNTROWS('Cleaned Palmoria Group emp-data'), 'Cleaned Palmoria Group emp-data'[Below Minimum]= "Below")

... Measure to get below Minimum pay percentage
- Below Minimum Pay % = ABS([Male Minimum Pay %] - [Female Minimum Pay %])

... Measure to create 
- Employee Meets/Exceeds Minimum Pay Count = 
CALCULATE(COUNTROWS('Cleaned Palmoria Group emp-data'), 'Cleaned Palmoria Group emp-data'[Below Minimum]= "Meets/Exceeds")

... Measure to get the Gender count gap percentage
- Gender Count Gap % = 
ABS([Male Percentage] - [Female Percentage])

...Measure to get the Gender pay gap percentage
- Gender Pay Gap % = 
DIVIDE([Average Male Salary] - [Average Female Salary],[Average Male Salary],0)

... Measure to get the Bonus Amount
- Bonus Amount = 'Cleaned Palmoria Group emp-data'[ Salary ] * 'Cleaned Palmoria Group emp-data'[Bonus Percent]

... Measure to get the Bonus percentage
- Bonus Percent =
  SWITCH(TRUE(),'Cleaned Palmoria Group emp-data'[Rating] = "Very Poor", LOOKUPVALUE('Bonus Rules'[Very Poor], 'Bonus Rules'[Department], 'Cleaned Palmoria Group emp-data'[Department]),'Cleaned Palmoria Group emp-data'[Rating] = "Poor", LOOKUPVALUE('Bonus Rules'[Poor], 'Bonus Rules'[Department], 'Cleaned Palmoria Group emp-data'[Department]),'Cleaned Palmoria Group emp-data'[Rating] = "Average", LOOKUPVALUE('Bonus Rules'[Average], 'Bonus Rules'[Department], 'Cleaned Palmoria Group emp-data'[Department]),'Cleaned Palmoria Group emp-data'[Rating] = "Good", LOOKUPVALUE('Bonus Rules'[Good], 'Bonus Rules'[Department], 'Cleaned Palmoria Group emp-data'[Department]),'Cleaned Palmoria Group emp-data'[Rating] = "Very Good", LOOKUPVALUE('Bonus Rules'[Very Good], 'Bonus Rules'[Department], 'Cleaned Palmoria Group emp-data'[Department]))

... Add Column
- Conditional columns were created for Salary Band, Salary Sort, 

### DATA MODELING
Linking the two tables together.  This is to ensure alignment and to making the two tables see each other to enable data-column relationship.
- In Model View, RATING FIELD as a column was used to link the two tables - as it was present in the two column tables

## 🧠 Business Insights
- Gender Count gap of 18 (1.90%)
   - Kaduna shows the highest gender gap of 17 amongst the regions
- Gender pay gap of $2.2K (2.94%)
- 654 employees below salary regulation ($90K)
- Bonus pay distribution is nearly equal (50.95% male / 49.05% female)

## ANALYSIS

### [Dashboard Preview - Gender Distribution]
[Palmoria-HR-Dashboard_Gender_Distribution](https://github.com/user-attachments/assets/fa195441-27d5-4fa3-af60-cab4a942ce34)

### [Dashboard Preview - Rating]
[Palmoria-HR-Dashboard_Rating](https://github.com/user-attachments/assets/0e04dfb9-c659-463b-be11-986d37c13897)

### [Dashboard Preview - Salary Structure]
[Palmoria-HR-Dashboard_Salary_Structure](https://github.com/user-attachments/assets/3f54febd-c2dc-4979-9f7d-bcce5b3df135)

### [Dashboard Preview - Salary Compliance]
[Palmoria-HR-Dashboard_Salary_compliance](https://github.com/user-attachments/assets/a4f6c453-edb3-4e57-b038-c17df74149c5)

### [Dashboard Preview - Bonus Distribution]
[Palmoria-HR-Dashboard_Bonus_Distribution](https://github.com/user-attachments/assets/1a5de18a-f8b9-4d44-8fbb-006f348f29d4)



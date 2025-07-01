# PALMORIA HR DOCUMENTATION
This is one of my Data Analysis Capstone project in fulfilment of Digital Skillup Africa- DSA INCUBATOR HUB for the final certification.  

It is to demonstrate my technical indepth in using POWERBI to analyse real situation and give explicit insights that would enhance decision making.

## PROJECT TOPIC: PALMORIA GROUP HR ANALYSIS

## PROJECT OVERVIEW

This Data Analysis project aims to generate insights that the Palmoria Group management team would be able to address the issues bordering on gender inequalities in its 3 regions.

By analysing the various parameters in the data received, we seek to identify key areas within the business in relation to workforce structure, gender balance, salary distribution, and bonus allocation across Palmoria Group.

This will enable the management team to making spontaneous decisions that would bring about gender equality across its region and beyond for future expansion.

## DATA SOURCES
Primary source of data used here is 'Palmoria Group emp_data.csv' and 'Palmoria Group Bonus Rules.xls'
[Download Here] ()

## TOOLS USAGE
- Power BI Desktop
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

### DATA MODELING
Linking the two tables together.  This is to ensure alignment and to making the two tables see each other to enable data-column relationship.

## 🧠 Business Insights
- Gender Count gap of 18
   - Kaduna shows the highest gender gap of 17 amongst the regions
- Gender pay gap of $2.2K (2.94%)
- 654 employees below salary regulation ($90K)
- Bonus pay distribution is nearly equal (50.95% male / 49.05% female)


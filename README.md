### Project Report



# Executive Summary

This analysis investigates the data set for insights into customer behavior, financial standing, and engagement patterns. 
Major metrics such as churn rate, customer segmentation, and behavioral trends are used to support strategic recommendations. Analysis and visualization of this data set were carried out using Jupyter, which included the importation of Libraries, Data profiling, cleaning, and data analysis

# Objectives
The objective of this analysis is to understand the demographic and financial characteristics of the bank's customers, identify trends and patterns in customer engagement, and highlight potential areas for business improvement.

# Introduction
This report gives responses to some relevant business questions as well as insights and findings into a Bank Customer data set.

The data set was profiled, cleaned, and duplicates were removed. Some Columns were renamed, others were added, while some columns were dropped. 

# Data Overview

The dataset was in CSV. format. The data set that was provided had two sheets (Customer Info and Account Info).  Data Libraries were imported. A Data Dictionary was also provided, which captures information about the data set.
The Customer Info contained 10001 rows and 8 columns (CustomerId, Surname, CreditScore, Geography, Gender, Age, Tenure	EstimatedSalary), while the Account Info contained  10002 rows and 7 columns ( CustomerId, Balance, NumOfProducts, HasCrCard, Tenure, IsActiveMember, Exited). The customer Info data set had 1 duplicate, while the Account Info data set had 2 duplicates. They were 6 null rows in the data set.

<img width="674" height="333" alt="image" src="https://github.com/user-attachments/assets/b4d869e7-cc95-4b0c-9c93-7754928797f2" />

#### Customer Info - Raw Data

<img width="631" height="336" alt="image" src="https://github.com/user-attachments/assets/5338ec91-a629-40e8-899e-f7b48accb681" />

#### Account Info - Raw Data

<img width="504" height="433" alt="image" src="https://github.com/user-attachments/assets/71c38466-7944-4315-91ad-917a280d1937" />

#### Customer Data Dictionary

# Data Processing
To start with, all duplicates in the data set were removed. This was followed by renaming some columns in both tables. Columns such as CustomerId, Numofproducts, HasCrCard, IsActiveMember, CreditScore, and EstimatedSalary.
Customer Age was rounded to a whole number using the round method [customer_info['Age'] = customer_info['Age'].round(0)].
Roles with Null Values were removed. Both Tables were merged (using the merge method). Items in roles such as Country, Surnames were corrected using the replace method.

### Data Preparation
Some columns were added to the table. This includes Customer Status, Churned, Age Distribution, and Balance Range Columns. The customer status was created using information in the Active Member column. The Churned Column was created using information in the Exited column. Age Distribution was created using the age column, and the Balance Range column was created using the Balance column. Both Exited and Active Member columns were dropped using the drop method. 

<img width="1100" height="210" alt="image" src="https://github.com/user-attachments/assets/41ef687e-f232-4f75-ac91-dfbb074eec75" />

#### Comb_df - Cleaned Data Set

## Key Performance Index (KPI)
The KPI for this analysis is shown in the table below


| KPI | Value|
| :---: | :---: |
| Total Customers | 9997 |
| Male Customers | 5456 |
| Female Customers | 4541 |
| Churned Cuatomers | 2037 |
| Churn Rate (%) | 20.38 |
| Avg Credit Score | 650.55 |
| Avg Balance | 76482.68 |
| Avg products | 1.53 |
| Avg Tenure | 5.01 |


### Churned Customers by Age Distribution
The Number of churned customers by Age Distribution is represented using the Bar plot below

<img width="1063" height="561" alt="image" src="https://github.com/user-attachments/assets/adc407eb-88ed-442e-8cd3-7fccb9af90b8" />

### Retained Customers by Age Distribution
The Retained Customer by Age Distribution was also represented using a bar plot

<img width="1088" height="576" alt="image" src="https://github.com/user-attachments/assets/adc7fa7f-55be-4630-96d2-fcad9318a069" />

### Customer Churn and Retention Rates by Gender
A Bar plot was also used to show the representation of the Churn and retention Rate by Gender

<img width="704" height="384" alt="image" src="https://github.com/user-attachments/assets/03e3a02e-09f0-471d-aa38-308f9dd032c5" />

<img width="719" height="390" alt="image" src="https://github.com/user-attachments/assets/3841d32a-d972-46ab-9478-a63bd3d95938" />

| Gender | Churned| Retained |
| :---: | :---: | :---: |                     
| Female | 0.749174 | 0.250826 |
| Male | 0.835411 | 0.164589 |

The percentage retention rate for both males and females is 83.5411% and 74.9174% respectively
The percentage churn rate for both males and females is 16.4589% and 25.0826% respectively

### Average Credit Score by Churn Status
This plot shows how credit score relates to customer churn. 

<img width="670" height="388" alt="image" src="https://github.com/user-attachments/assets/9137f418-4721-4c17-80f7-0a3fa341a860" />

### Churn Rate by Number of Bank Products Owned
This plot gave a response to the question about how owning more bank products correlates with reduced churn
<img width="1204" height="680" alt="image" src="https://github.com/user-attachments/assets/15367c51-bce5-42cc-9690-692d8cffc83b" />

### Account Balance by Churn Status
The average balance by Churn Status is represented using a bar chart 
<img width="703" height="387" alt="image" src="https://github.com/user-attachments/assets/a3069921-80d1-4833-a978-654dc1e52d55" />



# Data Analysis and Visualization



# Insights and Recommendations

# Conclusion

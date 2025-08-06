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




# Data Analysis and Visualization


# Insights and Recommendations

# Conclusion

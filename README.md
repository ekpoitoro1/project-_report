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

# # Data Analysis and Visualization

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
<img width="887" height="493" alt="image" src="https://github.com/user-attachments/assets/d8861174-0d80-44b2-834c-66fb39352189" />

### Retained Customers by Age Distribution
The Retained Customer by Age Distribution was also represented using a bar plot

<img width="847" height="488" alt="image" src="https://github.com/user-attachments/assets/77aaa26a-7b9c-4ef2-ae0f-ae621c4782cc" />

### Customer Churn and Retention Rates by Gender
A Bar plot was also used to show the representation of the Churn and retention Rate by Gender

<img width="813" height="565" alt="image" src="https://github.com/user-attachments/assets/7215a535-3713-4940-b019-ba2560b8b514" />

<img width="709" height="567" alt="image" src="https://github.com/user-attachments/assets/e5f1204e-46ec-45ae-ab05-84665d2b2d33" />

### Churn Rate by Country
The column chart of the churn rate by country shows the country with the highest Chun Rate.

<img width="950" height="483" alt="image" src="https://github.com/user-attachments/assets/d08732da-1843-4e6b-9747-716208b746f5" />


The percentage retention rate for both males and females is 83.5411% and 74.9174% respectively
The percentage churn rate for both males and females is 16.4589% and 25.0826% respectively

### Average Credit Score by Churn Status
This plot shows how credit score relates to customer churn. 

<img width="737" height="395" alt="image" src="https://github.com/user-attachments/assets/2a2a23a5-2b41-4cdc-b147-8e547980f5a2" />

<img width="670" height="388" alt="image" src="https://github.com/user-attachments/assets/9137f418-4721-4c17-80f7-0a3fa341a860" />

### Churn Rate by Number of Bank Products Owned
This plot gave a response to the question about how owning more bank products correlates with reduced churn

<img width="873" height="499" alt="image" src="https://github.com/user-attachments/assets/bd804366-8d22-4cf5-988f-d6fcab4eae96" />

<img width="1204" height="680" alt="image" src="https://github.com/user-attachments/assets/15367c51-bce5-42cc-9690-692d8cffc83b" />

### Account Balance by Churn Status
The average balance by Churn Status is represented using a bar chart 

<img width="686" height="389" alt="image" src="https://github.com/user-attachments/assets/11205e17-089f-49bf-ac57-feccadae4b70" />

<img width="703" height="387" alt="image" src="https://github.com/user-attachments/assets/a3069921-80d1-4833-a978-654dc1e52d55" />


### Churn Rate by Balance Range
The plot of churn Rate(%) by balance range shows whether or not there is a balance threshold above which customers are more likely to churn.

<img width="1118" height="584" alt="image" src="https://github.com/user-attachments/assets/a839ec51-792a-457d-adf0-9f500b57f65d" />

<img width="1080" height="585" alt="image" src="https://github.com/user-attachments/assets/28071c62-eead-4daf-a7ba-71590ea6c5d4" />

### Average Number of Products by Churn Status

![Uploading image.png…]()


<img width="701" height="468" alt="image" src="https://github.com/user-attachments/assets/0c2e613d-1d6a-483d-8522-495ddc219af7" />

### Churn Rate by Customer Tenure
How does customer tenure impact churn—are newer or long-term customers more likely to exit?"

# Insights and Recommendations

# Conclusion

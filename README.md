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

### Churn Rate by Number of Bank Products Owned
This plot gave a response to the question about how owning more bank products correlates with reduced churn

<img width="873" height="499" alt="image" src="https://github.com/user-attachments/assets/bd804366-8d22-4cf5-988f-d6fcab4eae96" />

### Account Balance by Churn Status
The average balance by Churn Status is represented using a bar chart 

<img width="686" height="389" alt="image" src="https://github.com/user-attachments/assets/11205e17-089f-49bf-ac57-feccadae4b70" />


### Churn Rate by Balance Range
The plot of churn Rate(%) by balance range shows whether or not there is a balance threshold above which customers are more likely to churn.

<img width="1118" height="584" alt="image" src="https://github.com/user-attachments/assets/a839ec51-792a-457d-adf0-9f500b57f65d" />

### Average Number of Products by Churn Status
The Average Number of Products by Churn Status was also shown using a column chart

<img width="681" height="473" alt="image" src="https://github.com/user-attachments/assets/1a97b471-fa8f-41b9-8ae5-e5bbe7d369fb" />

### Churn Rate by Customer Tenure
A column chart was used to respond to the question about whether newer or long-term customers are more likely to exit 
<img width="1039" height="605" alt="image" src="https://github.com/user-attachments/assets/25446a1d-b275-4032-a6cb-40de4d3bb6fb" />

### Churn Rate Distribution Activity Status
A column chart was used to show if active members are significantly less likely to churn than inactive ones
<img width="645" height="416" alt="image" src="https://github.com/user-attachments/assets/e883c41f-3457-42f2-bb20-196339548ff9" />

### Balance Variability by Customer Tenure
The stability of financial behavior (e.g., consistent balances) of customers in relation to longer account history was shown using a column chart.
<img width="1130" height="593" alt="image" src="https://github.com/user-attachments/assets/5ee7f225-b4e7-46d1-8d97-5c36b7514da3" />

# Is there a relationship between the number of products used and tenure length?
The relationship between the number of products used by customers and customer tenure length is represented using a column chart
<img width="1074" height="594" alt="image" src="https://github.com/user-attachments/assets/9f2cf958-09ff-4e38-9596-71f619cda161" />


### Average Customer Balance by Tenure
The Average Customer Balance by Tenure was represented by a column plot

<img width="1081" height="598" alt="image" src="https://github.com/user-attachments/assets/e883c9ec-828f-4f56-b839-6e6f7ee3a4f3" />


# Insights and Recommendations
The analysis of this data set showed that a significant portion of customers have churned, highlighting a concern for customer retention. There were a significant number of male and female customers, although there were more males than female customers. 

There was also a noticeable churn rate of Female customers compared to male customers. This might be related to the fact that offerings (such as products or services) are more aligned with male financial behavior or interests. There is also a possibility that most of these products, although valuable, may be underutilized by female customers, thereby leading to low engagement.
Retention rates between male and female customers are relatively similar, showing no significant gender bias in churn behavior. Gender-targeted churn strategies may not be necessary — focus should shift to behavioral and financial indicators.
There is a gradual increase in the average number of products as tenure increases.

Recommendation
Marketing or retention campaigns might be inadvertently male-oriented, not addressing the specific needs or goals of female customers. Long-term customers tend to adopt more products, suggesting cross-selling efforts may be more successful with loyal customers.


Inactive customers(65.3%) churn at glaringly higher rates than active customers(34.7%). A proactive approach to monitor and re-engage inactive customers can drastically reduce churn. This confirms that customer status is a strong predictor of customer retention.  A proactive approach to monitor and re-engage inactive customers can drastically reduce churn.



# Conclusion

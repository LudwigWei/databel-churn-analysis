# Data Dictionary: Databel Churn Dataset

This dictionary defines the fields used in the Databel Churn analysis project.

## 1. Fact_Churn
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| Customer ID | String | Unique identifier for each customer. |
| Churn Label | String | 1 for Churned, 0 for Retained (Used for calculations). |
| Churn Category | String | High-level reason for churn (e.g., Competitor, Attitude). |
| Churn Reason | String | Specific root cause of churn. |
| Monthly Charges | Decimal | Average of all Monthly Charges to the customer. |
| Total Charges | Decimal | Cumulative charges over customer tenure. |
| Extra Data Charges | Decimal | Contains the extra charges for data downloads for customers who are not on an unlimited plan. |
| Customer Service Calls | Integer | Number of calls made to support. |

## 2. Dim_Customer
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| Customer ID | String | Unique identifier (Foreign Key to Fact_Churn). |
| Gender | String | Male or Female. |
| Age | Integer | Customer age. |
| Age Group | String | Categorized age (Under 30, Adult, Senior). |
| Group | String | Indicates if the customer is part of a group contract. A group contract offers advantages and is generally cheaper (Yes/No). |
| Number of Customers in Group | Integer | Number of customers part of the group. |

## 3. Dim_Geography
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| Customer ID | String | Unique identifier (Foreign Key). |
| State | String | The code of the state where the customer lives. |
| Phone Number | String | Contact information of a customer. |

## 4. Dim_Services
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| Customer ID | String | Unique identifier (Foreign Key). |
| Contract Type | String | Month-to-Month, One Year, Two Year. |
| Payment Method | String | E.g., Credit Card, Direct Debit. |
| Unlimited Data Plan | String | Indicates if the customer has free unlimited download capacity with "Yes" or "No". This premium is reflected in the amount of the monthly charge. |
| Data Usage Group | String | Aggregated data usage (e.g., < 5GB, 5-10GB). |
| Intl Plan | String | Has International Plan (Yes/No). |
| Intl Active | String | Actually makes international calls (Yes/No). |
# Classification-Capstone-Project--Card-Default-Prediction
## Introduction: 
With the recent changes in the economic infrastructure and greater thrust toward improving the standard of living have change the common people concept of consumption. People nowadays prefer to spend ahead of time and mortgage their “credit” to the bank to enjoy certain things in advance. But sometimes it result in lack of rational thinking which results in not being able to pay the loan amount within due time. This project is all about predicting such events where the card holder will default in their payment. Such prediction will not only help the lending institution but also help the customers in mainting their good CIBIL score.
## Data Collection: 
This dataset contains information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan
## Data Description:
This dataset consists of 23 input feature variables and a binary target variable which shows the default payment status(Yes=1, No=0). Lets see the meaning of each of the input feature variables.

 X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
 
 X2: Gender (1 = male; 2 = female).
 
 X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
 
 X4: Marital status (1 = married; 2 = single; 3 = others).
 
 X5: Age (year).
 
 X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005;  X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
 
 X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005.
 
 X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.
 
 ## Understanding Data
 
 a) Number of records present in the dataset is 30000.
 
 b) Number of features present in the dataset is 23.
 
 c) All the attribute of the dataset is of integer type.
 
 d) Duplicate Value present in the dataset is 24.
 
 e) No null values are present in the dataset.
 
 ## Cleaning Data and Feature Engineering
 
 a) Duplicate Value: Dropped all the duplicate values because duplicate values result in overfit the model.
 
 b) Missing value treatment: No missing values were present in the dataset.
 
 c) Outlier Treatment: Found No significant Outliers that could effect the performance of classification model.
 
 d) Renaming Columns: Column names were mapped by adding the months name.
 
 e) Removing Inconsistencies present in each of the input variables:
         (i) Education: 
 


# Classification-Capstone-Project--Card-Default-Prediction
## Introduction: 
With the recent changes in the economic infrastructure and greater thrust toward improving the standard of living have change the common people concept of consumption. People nowadays prefer to spend ahead of time and mortgage their “credit” to the bank to enjoy certain things in advance. But sometimes it result in lack of rational thinking which results in not being able to pay the loan amount within due time. This project is all about predicting such events where the card holder will default in their payment. Such prediction will not only help the lending institution but also help the customers in mainting their good CIBIL score.

## Problem Statement:
This project is aimed at predicting the case of customers default payments in Taiwan. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be more valuable than the binary result of classification - credible or not credible clients. 
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
 
 e) **Removed the inconsistencies** found in each of the input variables and replaced the attribute values:
 
 
         (i) Education: Unique values that were present in this columns were 0,1,2,3,4,5,6 
                        Replaced the values 0, 4, 5, 6 with others
                        Replaced 1 with graduate
                        Replaced 2 with university
                        Replaced 3 with high-school
                        
         (ii) Marriage: Unique values that were present in this columns were 1,2,3,0
                        Replaced the values 0,3 with others
                        Replaced the value 1 with marriage
                        Replaced the value 2 with single
                        
         (iii) Gender:  Unique values that were present in this columns were 1,2
                        Replaced 1 with male
                        Replaced 2 with female
                        
  ## Exploratory Data Analysis and Summarizing Data:
    a) Uni-Variate Analysis:
            (i)   Age: Found more number of clients were in the age bracket of 20-40.
            (ii)  Limiting Balance: Most of the clients had the limiting balance below 2000000
            (iii) Found More female card holder with higher default rate
            (iv)  Found that people with higher education level are more likely to get deault in their payments.
            (v)   Married ones are more likely to get default in their payments.
            (vi)  Found that the dataset contains 77% clients that are not expected to default in their payments whereas 23% clients 
                  are expected to default in their payment
            
    b) Bi-Variate Analysis:
            (i)   Age and Gender: Found that the females in age group 20-40 had very a high tendency to default in their payment 
                  compared to males in all age brackets.
            (ii)  Payment and Bill Amount: There was a higher proportion of clients for whom the bill amount is high but payment 
                  done against the same is very low.
            (iii) Age and Maritial Status: In the age group 20 - 30 singles were found more likely to default.
            
  ## Handling Imbalance:
             Implemented SMOTE boosting to oversample the minority class.
             
  ## Data Manipulation:
             Used pandas get dummies to convert the categorical variable into dummy or indicator variables.
             
  ## Feature Selection
             Feature selection increases the predictive power of machine learning algorithms by selecting the most important variables 
             and eliminating redundant and irrelevant features. We removed all the multicollinear features from the dataset prior training 
             the model. For removing multicollinearity we used Vif and correlation heat map.
             
             (a) Correlation Matrix: 
                     (i)   Found that payments in all the months are highly collinear.
                     (ii)  Found that bill amounts in all the months are highly collinear.
                     (iii) Found high correlation between male and  female clients.
                     (iv)  Found high correlation between married and single.
                     
              (b) Vif:  Variation Inflation Factor is another way of measuring multicollinearity.Mathematically, the VIF for a regression
              model variable is equal to the ratio of the overall model variance to the variance of a model that includes only that single 
              independent variable. This ratio is calculated for each independent variable. A high VIF indicates that the associated independent 
              variable is highly collinear with the other variables in the model.
                     (i) Bill amount of all the months found to have high Vif Values.
                     
   ## Important Features
              Removed all the redundant features and collinear features. Important features after removing all the collinear features found
              using Correlation Matrix and Vif are as follows:
              0   LIMIT_BAL
              1   AGE 
              2   PAY_SEP 
              3   BILL_AMT_SEPT  
              4   PAY_AMT_SEPT  
              5   PAY_AMT_AUG  
              6   PAY_AMT_JUL  
              7   PAY_AMT_JUN  
              8   PAY_AMT_MAY  
              9   PAY_AMT_APR  
             10   SEX_female  
             11   EDUCATION_graduate  
             12   EDUCATION_high school  
             13   EDUCATION_other  
             14   EDUCATION_university 
             15   MARRIAGE_married  
             16   MARRIAGE_other  
             
   ## Model Building
                     
                     
      
                    
 


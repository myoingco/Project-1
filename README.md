<h1 align="center"> Project 1 </h1> <br>
Utilize Python scripting to analyze the provided dataset.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Build Process](#build-process)
- [Analysis](#analysis)
- [References](#references)


## Introduction

Our analysis aims to analyze whether there is a correlation between various borrower attributes and loan characteristics and whether the loans were eventually charged off or paid in full. Specifically we plan on performing the following with a dataset of 100,000 loans:

- Understand the risk associated with credit card loans by investigating the relationship between loan status (charged off or paid off) and key variables such as credit score, annual income, debt-to-income ratio, and years of credit history.
- Develop predictive models to forecast the likelihood of loan default based on borrower profiles and loan features.
- Segment borrowers based on demographic characteristics, financial behavior, and loan purposes to identify patterns and trends associated with loan performance.
- By identifying the most influential factors, we will determine the correlation of features contributing in the prediction of the loan default.
- Analyze the trends in loan performance as well as the attributes of borrowers.
- Use findings to mitigate risks.


## Getting Started

Prior to execution, you must have Python as well as VSCode installed. You must also have the necessary installation packages and the csv file downloaded.


## Build Process

1) We imported the raw data and created a dataframe.
2) The following were done to clean our data:
    - Dropped the blank values in the 'Credit Score' and 'Annual Income' columns, as those were key factors within our analysis.
    - Replaced blanks with '0' in 'Months since last delinquent', 'Bankruptcies', and 'Tax Liens'.
    - Removed any rows with a duplicate 'Loan ID'.
    - Reformatted the 'Credit Score' as we noticed some of the data provided had 4 digits.
    - Converted the data within the 'Credit Score' column to an integer, then validated the data.
    - We then added extra columns of data to better conduct our analysis; 'Debt to Income Ratio' and an integer column for 'Fully Paid vs Charged off', '1' representing 'Fully Paid' and '0' representing 'Charged off'.
    - Excluded any outliers from 'Annual Income' as we noticed our data was strongly being skewed.
3) After cleaning our data we began to analyze the various reasons as to why someone would take out a loan by identifying the values in the 'Purpose' column.
    - After itemizing the 'Purpose' column, we then consolidated similar categories.
4) We then created bins to group the 'Credit Scores', classifying them as: "Poor" (0), "Fair" (579), "Good" (739), "Very Good" (799), "Excellent" (850).
    - We then placed the data into the bins and created a dataframe to visualize this data.
5) We then created bins to group the 'Annual Income', classifying them as: "Under 10%" (.09999), "10%-20%" (.19999), "20%-30%" (.29999), "30%-40%" (.4).
    - We then placed the data into the bins and created a dataframe to visualize this data.
3) After cleaning our data we began creating visuals to compare our data and conduct our analysis.


## Analysis

- We first created a bar chart comparing the number of loans that were 'Fully Paid' vs 'Charged Off'.
    - We came to the conclusion that there were more loans that were 'Fully Paid' vs loans that were 'Charged Off' based on the provided data.

![image](https://github.com/myoingco/Project-1/assets/160566342/74c7d84e-a4ac-4c05-acfd-2f075e9195ad)

- We then created a pie chart comparing the type of loans taken out, 'Long Term' vs 'Short Term'.
    - We came to the conclusion that there were more 'Short Term' loans taken out in comparison to the amount of 'Long Term' loans taken out.
 
![image](https://github.com/myoingco/Project-1/assets/160566342/4f46ab5e-188e-4f8f-9a9b-0c479b68f47b)

- We then created a clustered bar graph to compare the various 'Purposes' of the loan and whether or not those loans were 'Charged Off' or 'Fully Paid'.
    - We came to the conclusion that the majority of the loans taken out, regardless of the 'Purpose' were 'Fully Paid', we also concluded that the most popular loan 'Purpose' based on the provided data was for 'Car Loans'.

![image](https://github.com/myoingco/Project-1/assets/160566342/587babfb-0ecb-4c89-9352-632e34fdf271)

- We then created a histogram based on the 'Debt-to-Income Ratio' data we had drawn vs the 'Loan Status'.
    - We came to the conclusion that as the 'Debt-to-Income Ratio' increases, the chances of the loan being 'Charged Off' increases. We also noticed that the chances of the loan being 'Paid Off' vs 'Charged Off' is almost 50/50 within the 'Debt-to-Income Ratio' of '0.35' - '0.40'.

![image](https://github.com/myoingco/Project-1/assets/160566342/d6118094-716e-44b4-9f3e-13e352956ea0)

- We then created a boxplot of the 'Credit Score' and 'Loan Status'.
    - We came to the conclusion that the 'Fully Paid' loans tend to have a higher 'Credit Score' vs the loans that were 'Charged Off'.

![image](https://github.com/myoingco/Project-1/assets/160566342/56ffc26d-f675-45c5-94af-b82cb4f5b802)

- We then created a boxplot of 'Annual Income' and 'Loan Status'.
    - We came to the conclusion that people who have a higher 'Annual Income' are more than likely to have paid off their loans.

![image](https://github.com/myoingco/Project-1/assets/160566342/553351ec-a5c6-4c47-9652-ff8c0a6e05b5)

- We then created a boxplot of 'Debt-to-Income Ratio' and 'Loan Status'.
    - We came to the conclusion that those that had a higher 'Debt-to-Income Ratio', are more than likely to 'Charge Off' their loans.

![image](https://github.com/myoingco/Project-1/assets/160566342/0c46fff2-312b-484d-8fdb-e0474c261649)

- We then created a dataframe of the 'Credit Score' metrics of 'Fully Paid' vs 'Charged Off' loans.
    - We were able to draw the following data for both 'Fully Paid' and 'Charged Off' loans:
        - Count
        - Mean
        - Standard Deviation
        - Minimum
        - Maximum
        - 25%, 50% and 75% quartiles

<img width="651" alt="Screenshot 2024-04-17 at 7 29 00 PM" src="https://github.com/myoingco/Project-1/assets/160566342/84312a6c-99f2-4402-8ef0-eb46429e2349">

- We then created a linear regression for the 'Loan Status' and 'Credit Score'.
    - We came to the conclusion that given the equation y = 0.0031x - 1.47, the correlation coefficient is close to 0.0031; this indicates a very weak positive correlation between x and y.

![image](https://github.com/myoingco/Project-1/assets/160566342/5109820f-7e01-476c-87d2-4c3fa308a22c)

- We then created a linear regression for the 'Loan Status' and 'Annual Income'.
    - We came to the conclusion that given the equation y = -0.0000000727x + 0.65, the correlation coefficient is close to zero -0.0000000727; this indicates a very weak negative correlation between x and y. 

![image](https://github.com/myoingco/Project-1/assets/160566342/565c9e43-02e1-41a6-a4f1-18634f638776)

- We then created a linear regression for the 'Loan Status' and 'Debt-to-Income Ratio'.
    - We came to the conclusion that given the equation y = -0.65x + 0.85, the correlation coefficient is -0.65; this indicates a moderately strong negative correlation between x and y.

![image](https://github.com/myoingco/Project-1/assets/160566342/93beb036-7bef-4f26-a64d-6306051ecfb7)

- We then created a cluststered bar graph, taking the 'Credit Score Rating' and 'Debt-to-Income Ratio' into account.
    - We came to the conclusion that the loans with a rating of 'Fair' and a 'Debt-to-Income Ratio' between '30%-40%' tend to be 'Charged Off' more often than they are being 'Paid Off'.

![image](https://github.com/myoingco/Project-1/assets/160566342/d72e15f7-02b7-4ed7-9016-0a9652eaba42)

## References

[Kaggle](https://www.kaggle.com/datasets/fatmayousufmohamed/credit-card),
[Xpert Learning Assistant](https://bootcampspot.instructure.com/courses/5057/external_tools/313)

Data for this dataset was generated by Kaggle, and is intended for educational purposes only.

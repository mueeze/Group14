# Group14
## Overview
---
We, as a group have chosen the credit card fraud detection predictive models, because it is more applicable to the Modules covered in the course. My role in the group involves data exploration. See Table below which highlights my role and others in my group. My role is to perform Data Exploration on the dataset in Python. The table below is an agreed upon, roles and responsibilities for each group member in Group 14. 


Week 1: Due Jan 25th

|Deliverables:|	Responsible|	Date|
| ----------------------- | ---------------------------------------- |--------------------------|
|README|	Everyone will add their notes below and Amber will complete the final edit|	Amber: Friday Jan 20th|
|ER Database	|Amber	|Friday Jan 20th|
|Machine Learning model|	Amber, Josna, Halango	|Amber: Sat Jan 21st,Halango: Jan 21st and 22nd, Josna :Jan 22-23 |
|Data Exploration	|Jared	|Saturday evening 21st, Sun 22nd and I can do Mon 23rd.|
|Dashboard outline |	Mahbubur	|Saturday 21st. |


## Process used in preparing data exploration in python

I installed various libraries, that included the following: See file [credit_card_fraud_file](https://github.com/mueeze/Group14/blob/Jared-Murray/Credit_card_fraud.ipynb)

These libraries were installed to run split testing and predictive modelling in machine learning. 

Checking and cleaning the credit card transaction data, I used the .loc method on the dataframe credit_card_fraud_df to obtain the credit card transactions time density against fraud and non-fraud. Which was indicated through class 0 and 1. 
See image below
![](https://github.com/mueeze/Group14/blob/Jared-Murray/Credit%20Card%20Transactions%20Time%20Density%20Plot.png)

I created a new credit card dataframe, new_credit_card_fraud_df, that holds and renames the columns 'Hour', 'Class', 'Min', 'Max'. 'Transactions', 'Sum', 'Mean'. Note, in order to clean the data I described the data, dtyped the data and dropped the null values. 

To identify the fraudulent transactions based on the amount, I stored the values in variable fraud and then plot the fraudulent transactions based on time. See Scatter plot below.
![]()

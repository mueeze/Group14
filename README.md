# Group14

## Overview
---
Our group has chosen a dataset about heart disease predictive models. The goal of our selection process was to choose a dataset that was large enough produce accurate and precise predictions. It is a complex dataset with values that needs to be trained, cleaned and split. 

The dataset chosen from Kaggle describes a pool of 4000 participants, male and female of various ages and selected lifestyle characteristics that can be predictive of heart disease development after a 10 year period. 
 
Some of the predictive variables we will explore are sex, ciggarette consumption, cholesterol levels, body mass index, and history of diabetes. The predicted output is whether the person develops coronary heart disease after 10 years: 1 indicating “yes”, 0 indicating “no”. 

We were looking for a dataset with enough relevant input data that would allow us to create a logistic regression model. We wanted a dataset that we could interpret easily that would clearly determine our output: heart disease development. 


The goal of our regression model is to determine How accurately we can predict chances of Cardiac Heart Disease based on various demographic and pre-existing health factors (i.e. age, gender, blood pressure, BMI, cholesterol etc.)? 

An ERD is not necessary in this model because there is only 1 table being used for the predictive model. 

In our dashboard we want to depict a story about the variables that contribute mostly towards the predicted heart diseases. For example:
  - How much does age or gender have an impact on predicting future heart disease
  - How much does pre-existing medical conditions have an impact on future heart disease
  - How much does smoking impact heart disease development
  - Does education have any impact on the development of heart disease
  - Is there a difference between male and female heart disease development

Data cleaning:

The data was cleaned first in the excel file by dropping any null values that were presented as “NA” in each column. The “Education” column was also dropped because it was not relevant to the output. Next, the mean value for column “cigsPerDay” was substituted into any null values in the column. 

## Process used in preparing data exploration in python

We installed various libraries, that included the following: See file [heart_disease](https://github.com/mueeze/Group14/blob/Jared-Murray/heart_disease.ipynb)

After 10 years, 644 participants developed heart disease and 3594 participants did not develop heart disease. 	

![Heart disease](https://user-images.githubusercontent.com/112285856/214711799-8cdcc37d-3cb2-488c-8e44-2b8439147fc7.png)


We stratified instances if heart disease by male and female, where 57.08% of males did not develop heart disease, compared to 42.92% of males who did:

![Male and female](https://user-images.githubusercontent.com/112285856/214711625-ee3df70f-36de-46d2-8052-35d4c0848806.png)


50% of participants who smoked developed heart disease after 10 years:

![smoker](https://user-images.githubusercontent.com/112285856/214711606-328548de-60e8-40f6-b5de-8ac9d7c5ef1f.png)


We also found that participants with hypertension had higher instances of heart disease:

![Hypertension](https://user-images.githubusercontent.com/112285856/214711596-928be1ee-7b0d-4f18-ac16-70621fe07514.png)

All the libraries were installed to run split testing and predictive modelling in machine learning. 

While checking and cleaning the heart disease data, we used the .loc method on the updated_heart_disease_df to obtain the Heart Disease Rates by age and gender. Which was indicated through Male and Female. 
See image below
![](https://github.com/mueeze/Group14/blob/Jared-Murray/Heart%20Disease%20Rate%20Age%20and%20Gender%20Density%20Plot.png)

A new heart disease dataframe was created, updated_heart_disease_df, at first as a csv file to save the cleaned data. It holds and renames the columns 'Male' to 'Gender'. Note, in order to clean the data, it was described, dtyped and it had dropped the null values, as well as the column 'education'.

To identify the glucose intake per age, values were stored in the variable blood_sugar_levels and then plotted the glucose intake based on age. See Scatter plot below. 
![](https://github.com/mueeze/Group14/blob/Jared-Murray/Glucose%20intake%20per%20year.png)


See table below outlining the respective responsibilities of each group member:

Week 1: Due Jan 25th

|Deliverables:|	Responsible|	Date|
| ----------------------- | ---------------------------------------- |--------------------------|
|README|	Everyone will add their notes below and Amber will complete the final edit|	Amber: Friday Jan 20th|
|Machine Learning model|	Amber, Josna, Halango	|Amber: Sat Jan 21st,Halango: Jan 21st and 22nd, Josna :Jan 22-23 |
|Data Exploration	|Jared	|Saturday evening 21st, Sun 22nd and I can do Mon 23rd.|
|Dashboard outline |	Mahbubur	|Saturday 21st. |


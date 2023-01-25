# Group14

## Overview
---
Our group has chosen a dataset about heart disease predictive models. In our selection process we were looking for a large enough dataset to would be accurate and precise. Jared's role in the group involves data exploration. See table below outlining the respective responsibilities of each group member. Jared performs the Data Exploration on the dataset in Python. 

Week 1: Due Jan 25th

|Deliverables:|	Responsible|	Date|
| ----------------------- | ---------------------------------------- |--------------------------|
|README|	Everyone will add their notes below and Amber will complete the final edit|	Amber: Friday Jan 20th|
|Machine Learning model|	Amber, Josna, Halango	|Amber: Sat Jan 21st,Halango: Jan 21st and 22nd, Josna :Jan 22-23 |
|Data Exploration	|Jared	|Saturday evening 21st, Sun 22nd and I can do Mon 23rd.|
|Dashboard outline |	Mahbubur	|Saturday 21st. |


The dataset chosen from Kaggle describes a pool of 4000 participants, male and female of various ages, and selected lifestyle characteristics that can be predictive of heart disease development in 10 years. 
 
Some of the predictive variables are sex, whether they smoke and how many, cholesterol levels, body mass index, and whether they have a history of diabetes. The predicted output is whether the person develops coronary heart disease after 10 years: 1 indicating “yes”, 0 indicating “no”. 

Why did we choose this dataset? We were looking for a dataset with enough relevant input data that would allow us to create a linear regression model. We wanted a dataset that we could interpret easily. We were looking for something with relevant inputs, to determine our output: instances of heart disease. 

We want to determine if we can predict future instances of heart disease, based on the input data using logistic regression models. This will be a supervised learning model because the data is labeled. 

We will be using a classification model to predict the outcome because our output will be 

Project Question:
How accurately can we predict chances of Cardiac Heart Disease based on various demographic and pre-existing health factors (i.e. age, gender, blood pressure, BMI, cholesterol etc.)? 

An ERD is not necessary in this model because there is only 1 table being used for the predictive model. 

In our dashboard we want to depict a story about the variables that contribute mostly towards the predicted heart diseases. For example:
  - How much does age or gender have an impact on predicting future heart disease
  - How much does pre-existing medical conditions have an impact on future heart disease
  - How much does smoking impact heart disease development
  - Does education have any impact on the development of heart disease
  - Is there a difference between male and female heart disease development

Data cleaning:

The data was cleaned first in the excel file by dropping any null values that were presented as “NA” in each column. The “Education” column was dropped because it was not relevant to the output. Next, the mean value for column “cigsPerDay” was substituted into any null values in the column. 

After 10 years, 644 participants developed heart disease and 3594 participants did not develop heart disease. 	

![Heart disease](https://user-images.githubusercontent.com/112285856/214711799-8cdcc37d-3cb2-488c-8e44-2b8439147fc7.png)


We stratified instances if heart disease by male and female, where 57.08% of males did not develop heart disease, compared to 42.92% of males who did:

![Male and female](https://user-images.githubusercontent.com/112285856/214711625-ee3df70f-36de-46d2-8052-35d4c0848806.png)


50% of participants who smoked developed heart disease after 10 years:

![smoker](https://user-images.githubusercontent.com/112285856/214711606-328548de-60e8-40f6-b5de-8ac9d7c5ef1f.png)


We also found that participants with hypertension had higher instances of heart disease:

![Hypertension](https://user-images.githubusercontent.com/112285856/214711596-928be1ee-7b0d-4f18-ac16-70621fe07514.png)



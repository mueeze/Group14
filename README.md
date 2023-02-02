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

# Week 1

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

# Week 2 

## Overview
---
In Week 2 we worked on refinging our machine learning models, to ensure the accurancy score of our models was higher. The dataset is very complex and needs to be cleaned, trained, and split during the data exploration. The dataset has gone through different testing on several machine learning models. Below we will show the data beeing tested with:
	- Random Forest Classifier
	- Support Vector Machine (SVM) vs. Deep Learning Model (DL)
	- Logistic Regression
	- Decision Trees Classifier/ LGBM Classifier/ XGBClassifier/ MLPClassifier

During week 1 preperation we realised that our dataset was unbalanced. The accurancy score we were recieving was to low and since it accured on more than one model we came to the conclusion that it has something to do with our dataset. We tried to investigate the cause by inspecting different columns that could produce a low correlation with the intended output - developing heart disease over a ten year period. 

For example, we tried removing the "diabetes" column because in the initial exploration period this column, showed low correlation to the targeted output. After dropping this column and running the model, the output was the same. This is where we realized we had to use Ramdom Oversampling with SMOTE to balance our dataset to get a more accurate result.


## Results

### Logistic Regression Model

When doing additional data cleaning to ensure the accuracy score of our logistic regression module was higher. Initially, the accuracy score produced by the confusion matrix was around 0.13, which indicated that something was not right in our dataset. Upon further review, we recognized that our confusion matrix was yeilding such a low f1 score because of how unbalanced our dataset was. The total number of patients that developed heart disease was 644, compared to 3594 patients who did not.

When the dataset was unbalanced accuracy result was 0.85, however when looking at the F1-score [0  ----  0.92 / 1  ----  0.05] we are able to see that it is very unbalanced

![Unbalanced](https://user-images.githubusercontent.com/99384585/216222006-dcd96efc-6431-4a67-89b7-e7aa5ed809a7.png)

A Random Oversampling, aswell as a SMOTE was then done to try and balance the dataset. 
	1. Random Oversampling results - Accuracy of 0.66 / F1 score of [0 --- 0.77 / 1 --- 0.35]
	
	![Oversampling](https://user-images.githubusercontent.com/99384585/216222543-fee2435b-ba0e-46d0-8fa2-5c8fa258dee2.png)

	2. SMOTE results - Accuracy of 0.62 / F1 Score of [0 --- 0.73 / 1 --- 0.31]
	
	![SMOTE](https://user-images.githubusercontent.com/99384585/216222849-bd3a2c60-98a6-49ae-94fd-1c92a3ed912e.png)


### Random Oversampling with SMOTE
The approach to Random Oversampling with SMOTE addresses the imbalanced dataset value column, TenYearCHD in the dataframe, heart_disease_df, by oversampling the minority class. The simplest approach involves duplicating examples in the minority class, although these examples don’t add any new information to the model. Instead, a new examples can be synthesized from the existing examples. This is a type of data augmentation for the minority class and is referred to as the Synthetic Minority Oversampling Technique, or SMOTE for short. See image below

![](https://github.com/mueeze/Group14/blob/Jared-Murray/ros.png)

A confusion matrix was generated for resamp_y and y_pred. It was then, plotted with the original dataset versus the Oversampled Minority Class and then a More Balanced Data. 
-	The count of the resamp_y is 0: 3099, 1: 3099
-	The balanced_accuracy_score for the y_pred is 0.5954051894889358
-	The confusion matrix produces an array of 1960, 1139 and 246, 311. The datatype is an integer type. 
-	The Imbalanced Classification Report Average/ Total: precision = 0.79, recall = 0.62, specificity = 0.57, f1-measure = 0.67, geometric mean = 0.59, index balanced accuracy= 0.35 and support =  3656. See Image Below 

	![](https://github.com/mueeze/Group14/blob/Jared-Murray/icr.png)


### Random Forest Classifier
The train_df dataframe pulls from updated_heart_disease.df using a random state of 525, a test size of 0.9 and shuffle = true. I initialized a randomforest classifier with n_jobs = 5, random_state=525, criterion='gini', n_estimators=100, verbose=False. This produces a result of RandomForestClassifier(n_jobs=5, random_state=525, verbose=False). A graph was plotted and to I got a ROC-AUC score = 0.618. 
See Image Below 
	![](https://github.com/mueeze/Group14/blob/Jared-Murray/RFC.png)


### Support Vector Machine (SVM)
TenYearCHD column was used to generate the categorical variable, TenYearCHD_cat. The datatype used in the categorical variable was an integer type. To create a OneHotEncoder instance, I fit and transform the OneHotEncoder into a new dataframe, encode_heart_disease_df. The model was split, trained and fitted to create a StandardScaler instance. I then, created an SVM model with a linear kernel. This produced a SVM model accuracy = 0.848.


### Deep Learning Model (DL)
A Deep Neural Net was created with hidden_nodes_layer1 = 10, hidden_nodes_layer2 = 5. The First and Second Hidden Layer used an activation = "relu". The Output Layer used an activation of "sigmoid". It was then compiled with an optimizer =”adam” and metrics = “accuracy”. The model was then trained with 50 epochs and a verbose = 1. This resulted in a Deep Learning Model with a Loss = 0.419 and an Accuracy = 0.834. 

### Decision Tree Classifier
The dataframe was trained using the different features such as criterion =‘entropy’, random state=0 and max dept taken into account was 30. As a result, the accuracy was 91% which was much higher compared to the unbalanced dataset with large number of features. Matrix:

![Decision tree matrix](https://user-images.githubusercontent.com/99384585/216223472-cdffbd20-e9c6-4006-bc55-803caf930013.jpg)

![DC image](https://user-images.githubusercontent.com/99384585/216223511-0a7e5fcb-1bd3-41e5-9fbb-c3bd6efb0131.jpg)

### Light GBM Classifier

Light GBM is a fast, distributed, high-performance gradient boosting framework based on decision tree algorithm, used for ranking, classification and many other machine learning tasks. The parameters used were boosting type='gbdt’, number of estimators=5000, learning_rate=0.05, objective='binary',metric='accuracy', is_unbalance=True, colsample_bytree=0.7, reg_lambda=3, reg_alpha=3, random_state=500, n_jobs=-1,num_leaves=35 As a result the accuracy was 89%. Matrix:

![LGBMC](https://user-images.githubusercontent.com/99384585/216223665-c17abda1-4796-47fb-bc08-288d09f3c050.jpg)

### XGB Classifier

XGBClassifier is a scikit-learn API compatible class for classification. The various parameters considered were learning_rate=0.05, n_estimators=100, max_depth=4, subsample = 0.9, colsample_bytree = 0.1, gamma=1,random_state=42. The accuracy rate was 69%. Matrix:

![XGB Classifier](https://user-images.githubusercontent.com/99384585/216223759-fab2dfb8-11c8-4c1b-9a59-6003f3346b06.jpg)

### MLPClassifier

MLPClassifier stands for Multi-layer Perceptron classifier (MLP) which in the name itself connects to a Neural Network. It relies on an underlying Neural Network to perform the task of classification.The various parameters considered were solver='adam', learning_rate_init = 0.0005, learning_rate = 'adaptive', activation="relu", max_iter=3000, random_state=10. The accuracy rate was 69% which is the same as we got for XGB Classifier.

### ROC Curve

AUC - ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. his metric considers the trade-offs between precision and recall. This is a ROC summary for all the machine learning models I did.

![ROC](https://user-images.githubusercontent.com/99384585/216223861-54e7f942-b09d-4463-b3d7-7fd251c39c2b.jpg)


Second Week | Second Segment Project Deliverable | Due Feb 1st

|Deliverables:|	Roles and Responsibilities |	Date|
| ----------------------- | ---------------------------------------- |--------------------------|
|README|	Everyone will add their notes below and Halango will complete the final edit|	Halango: Feb 1st|
|ER Database	|Amber	|Feb 1st|
|Machine Learning model|	Amber: Logistic Regession, Josna: Decision Tree/GBM Classifier/XGB Classifier/MLP Classifier, Jared: Random Oversampling with SMOTE, Random Forest Classifier, Support Vector Machine (SVM) vs Deep Learning Model (DL)	|Amber: Feb 1st,Halango: Feb 1st, Josna: Feb 1st, Jared: Feb 1st|
|Dashboard outline |	Mahbubur	|Feb 1st. |

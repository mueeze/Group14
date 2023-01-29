# Group14
## Overview
---
We, as a group have chosen the Cardiac Heart Disease, because it is more applicable to the Modules covered in the course. It is a complex dataset with values that needs to be trained, cleaned and split. My role in the group involves data exploration. See Table below which highlights my role and others in my group. My role is to perform Data Exploration on the dataset in Python. The table below is an agreed upon, roles and responsibilities for each group member in Group 14. 


 Second Week | Second Segment Project Deliverable | Due Feb 1st

|Deliverables:|	Roles and Responsibilities |	Date|
| ----------------------- | ---------------------------------------- |--------------------------|
|README|	Everyone will add their notes below and Amber will complete the final edit|	Amber: Feb 1st|
|ER Database	|Amber	|Feb 1st|
|Machine Learning model|	Amber: Linear Regession, Josna, Halango, Jared: Random Oversampling with SMOTE, Random Forest Classifier, Support Vector Machine (SVM) vs Deep Learning Model (DL)	|Amber: Feb 1st,Halango: Feb 1st, Josna: Feb 1st, Jared: Feb 1st|
|Data Exploration	|Jared	| Completed on Jan 23rd, |
|Dashboard outline |	Mahbubur	|Saturday 21st. |

## Results
### Random Oversampling with SMOTE
My approach to Random Oversampling with SMOTE addresses the imbalanced dataset value column, TenYearCHD in the dataframe, heart_disease_df, by oversampling the minority class. The simplest approach involves duplicating examples in the minority class, although these examples don’t add any new information to the model. Instead, new examples can be synthesized from the existing examples. This is a type of data augmentation for the minority class and is referred to as the Synthetic Minority Oversampling Technique, or SMOTE for short.

A confusion matrix was generated for resamp_y and y_pred. I then, plotted the original dataset versus the Oversampled Minority Class and then a More Balanced Data. 
-	The count of the resamp_y is 0: 3099, 1: 3099
-	The balanced_accuracy_score for the y_pred is 0.5954051894889358
-	The confusion matrix produces an array of 1960, 1139 and 246, 311. The datatype is an integer type. 
-	The Imbalanced Classification Report Average/ Total: precision = 0.79, recall = 0.62, specificity = 0.57, f1-measure = 0.67, geometric mean = 0.59, index balanced accuracy= 0.35 and support =  3656. See Image Below 
-	![]()

### Random Forest Classifier
The train_df dataframe pulls from updated_heart_disease.df using a random state of 525, a test size of 0.9 and shuffle = true. I initialized a randomforest classifier with n_jobs = 5, random_state=525, criterion='gini', n_estimators=100, verbose=False. This produces a result of RandomForestClassifier(n_jobs=5, random_state=525, verbose=False). A graph was plotted and to I got a ROC-AUC score = 0.618. 
See Image Below 
-	![]()

### Support Vector Machine (SVM)
TenYearCHD column was used to generate the categorical variable, TenYearCHD_cat. The datatype used in the categorical variable was an integer type. To create a OneHotEncoder instance, I fit and transform the OneHotEncoder into a new dataframe, encode_heart_disease_df. The model was split, trained and fitted to create a StandardScaler instance. I then, created an SVM model with a linear kernel. This produced a SVM model accuracy = 0.848.
See Image Below 
-	![]()


### Deep Learning Model (DL)
A Deep Neural Net was created with hidden_nodes_layer1 = 10, hidden_nodes_layer2 = 5. The First and Second Hidden Layer used an activation = "relu". The Output Layer used an activation of "sigmoid". It was then compiled with an optimizer =”adam” and metrics = “accuracy”. The model was then trained with 50 epochs and a verbose = 1. This resulted in a Deep Learning Model with a Loss = 0.419 and an Accuracy = 0.834. 


## Conclusion
In Conclusion, the most useful machine learning model in terms of producing predictions and accuracy based on the above testing was 
1.	SVM model accuracy = 0.848
2.	Deep Learning Model Loss = 0.419, Accuracy = 0.834 
3.	Imbalanced Classification Report produces precision = 0.79 and index balanced accuracy = 0.35. Note, this had balanced_accuracy_score of 0.595 
4.	Random Forest Classifier: roc_auc_score = 0.618 
The best results with be obtain by using SVM


First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell Line 1
              | Content Cell Line 2
Content Cell  | Content Cell

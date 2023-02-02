# Group14
# OverView

The original dataset was unbalanced. I tried to identify the top 10 impactful features like 'sysBP', 'glucose','age','totChol','cigsPerDay','diaBP','prevalentHyp','diabetes','BPMeds','male' for the target variable ‘TenYearCHD’. It enabled to have necessary data that would be helpful for the analysis. Using the resampling method, I was able to balance the dataset 

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/Features.JPG)

## Decision Tree Classifier
The dataframe was trained using the different features such as  criterion =‘entropy’, random state=0 and max dept taken into account was 30. 
As a result, the accuracy was 91% which was much higher compared to the unbalanced dataset with large number of features. 
*Matrix:*

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/Decision%20tree%20matrix.JPG)

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/DC%20image.JPG)

## Light GBM Classifier

Light GBM is a fast, distributed, high-performance gradient boosting framework based on decision tree algorithm, used for ranking, classification and many other machine learning tasks. The parameters used were boosting type='gbdt’, number of estimators=5000, learning_rate=0.05, objective='binary',metric='accuracy', is_unbalance=True, colsample_bytree=0.7, reg_lambda=3, reg_alpha=3, random_state=500, n_jobs=-1,num_leaves=35
As a result the accuracy was 89%.
*Matrix:*

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/LGBMC.JPG)

## XGB Classifier

XGBClassifier is a scikit-learn API compatible class for classification. The various parameters considered were learning_rate=0.05, n_estimators=100, max_depth=4, subsample = 0.9, colsample_bytree = 0.1, gamma=1,random_state=42. 
The accuracy rate was 69%.
*Matrix:*

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/XGB%20Classifier.JPG)

## MLPClassifier

MLPClassifier stands for Multi-layer Perceptron classifier (MLP) which in the name itself connects to a Neural Network. It relies on an underlying Neural Network to perform the task of classification.The various parameters considered were solver='adam', learning_rate_init = 0.0005, learning_rate = 'adaptive', activation="relu", max_iter=3000, random_state=10. The accuracy rate was 69% which is the same as we got for XGB Classifier.

## ROC Curve
AUC - ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. his metric considers the trade-offs between precision and recall. This is a ROC summary for all the machine learning models I did. 

![]( https://github.com/mueeze/Group14/blob/Josna-Jose/ROC.JPG)


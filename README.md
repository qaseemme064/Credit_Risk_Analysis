# Credit_Risk_Analysis
Supervised Machine Learning

# **Overview**
The purpose of this analysis is to understand how to utilize Machine Learning statistical algorithms to make predictions based on data patterns provided. In this challenge, we focused on Supervised Learning using a dataset from LendingClub, to evaluate and predict credit risk. This reason why this is called "Supervised Learning" is because the data includes a labeled outcome.

In this project, we used Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:

1) `Oversample` the data using the `RandomOverSampler` and `SMOTE` algorithms.

2) `Undersample` the data using the `ClusterCentroids` algorithm.

3) Used a `combination` approach of oversample and undersampling using the `SMOTEENN` algorithm.

4) Compare two machine learning models that reduce bias, `BalancedRandomForestClassifier` and `EasyEnsembleClassifier`.

We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

# **Resources**
Data : LoanStats_2019Q1.csv
Software : Python, Jupyter Notebook

# **Results**

The results for the six machine learning models including their respective balanced accuracy, precision, and recall scores are as follows:

### **Naive Random Oversampling**

![naive random oversampling](https://user-images.githubusercontent.com/96033163/166177582-f400088f-8315-48b7-a31d-9ddc7473bdc4.png)


1) Balanced Accuracy: `0.641326331226255`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.60/0.68`

### **SMOTE Oversampling**

![smote oversampling](https://user-images.githubusercontent.com/96033163/166177583-aec31653-8e3f-4d44-b776-0637ecf4e2bb.png)



1) Balanced Accuracy: `0.6374415316001305`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.60/0.68`

### **Undersampling**

![undersampling](https://user-images.githubusercontent.com/96033163/166177576-b1562c8e-3461-4ff5-b56e-50ddbf245d8d.png)


1) Balanced Accuracy: `0.6374415316001305`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.61/0.45`

### **Combination of Undersampling & Oversampling**

![combination](https://user-images.githubusercontent.com/96033163/166177580-37db31d1-eb76-4ba4-9f25-8b74fadbbe80.png)


1) Balanced Accuracy: `0.5292734810302525`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.61/0.45`

### **Balanced Random Forest Classifier**

![brfc](https://user-images.githubusercontent.com/96033163/166177579-9f3d8372-9b41-410b-bc51-b078a0ef7da4.png)


1) Balanced Accuracy: `0.7877672625306695`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.67/0.91`

### **Easy Ensemble AdaBoost Classifier**

![easy ensemble](https://user-images.githubusercontent.com/96033163/166178618-dbffe81d-4b4c-4c01-b47b-fb1275639cb6.png)


1) Balanced Accuracy: `0.925427358175101`
2) Precision: The precision is low for High-risk loans and is high for Low-risk loans.
3) Recall: High/Low risk = `0.91/0.94`

# **Summary**
When working with balanced accuracy, the highest compared accuracy between 0 and 1 and is closest to 1 is the best machine learning model. For the credit card data set, the `Easy Ensemble AdaBoost Classifier` is the best model to choose with its 0.925 balanced accuracy. The other models were below 0.80 balanced accuracy. The precision for all models were similar and within an appropriate range. The recall score also needs to fall within 0 and 1, with numbers closer to 1 being the better model. The `Easy Ensemble AdaBoost Classifier` had the highest recall score, making it the final best machine learning model to choose for further credit card analysis.
# be3343
Mahcine learning with MATLAB 

# Dataset Overview
5,136 patient records
Goal: Predict stroke risk, binary classification
## 10 Features and 1 Target 

Numerical: Age, BMI, Average glucose level
Categorical, Nominal: gender, work_type, smoking_status, ever_married, residence_type
Cateogircal, Ordinal: Hypertension, heart_disease

# Data Preprocessing
## Missing Value Handling
Numerical values (BMI, avg glucose level) --> mean imputation
Categorical variables (gender, hypertension, heart disease, ever married, work type, residence type, & smoking status) --> mode imputation

## Encoding
Cateagorial Nominal Variables --> one hot encoding
Categorical Ordinal Variables --> label encoding

## Sampling
The target variable, no stroke vs stroke, is extremely unbalanced (4861 no stroke vs 274 stroke). To correct for this, we employed oversampling of the 'stroke' category.

# Modeling

## Model 1: Logistic Regression

Test Accuracy: 70.51%
Test Precision: 68.62%
Recall: 75.58%
F1-score: 71.93%


## Model 2: Random Forest Tree Bagger

Test Accuracy: 95.82%
Test Precision: 92.28%
Recall: 100%
F1-Score: 95.98%

## Final Results

The Random Forest Model outperformed the Logistic Regression across all metrics. This is because Random Forest is able to learn better from our high-dimensional data. It can find the patterns and make specific decisions regarding the classification prediction. One thing to keep in mind is that Random Forest may easily overfit on simpler datasets.

Recall is an important metric to note of when considering stroke data, since false negatives can be fatal.



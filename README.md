Loan Approval Prediction using Machine Learning & Explainable AI
1. Project Overview

This project predicts loan approval using applicant financial and demographic features.
The objective is to build a machine learning model that is both accurate and explainable, ensuring fairness and transparency in loan decisions.

This project includes:

End-to-end data preprocessing

Exploratory Data Analysis (EDA)

Multiple machine learning models

Explainable AI (XAI) using SHAP and PDP

Model evaluation and comparison

Insights aligned with real-world loan-risk logic

2. Dataset Description

The dataset contains the following features:

CIBIL score

Loan term

Loan amount

Income

Asset values (bank, commercial, residential, luxury)

Education status

Self-employed status

Number of dependents

Target variable: Loan Status (Approved / Not Approved)

A dataset preview (df.head()) is shown inside the notebook.

3. Exploratory Data Analysis

The EDA process includes:

Missing value analysis

Duplicate value checks

Data type inspection

Outlier detection using Z-Score

Histograms and KDE plots for distributions

Count plots for categorical features

Boxplots for financial variables

Correlation heatmap (including target variable)

Target distribution analysis

Univariate and bivariate exploration

Outlier treatment for financial columns

4. Data Preprocessing

The preprocessing pipeline includes:

Encoding categorical variables

Handling missing values

Scaling numerical features

Balancing the dataset using SMOTE

Splitting data into training and testing sets

5. Machine Learning Models Used

The following models were trained and compared:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Gradient Boosting Classifier

AdaBoost Classifier

K-Nearest Neighbors (KNN)

Bagging Classifier (Random Forest as base estimator)

After evaluation, the Random Forest Classifier performed the best and was selected as the final model.

6. Model Evaluation

The models were evaluated using the following metrics:

Accuracy

Precision

Recall

F1-Score

ROC–AUC

7. Explainable AI (XAI)
7.1. Permutation Importance

Identifies the features the model relies on the most.

CIBIL Score, Loan Term, and Loan Amount were observed as the strongest predictors.

7.2. SHAP Summary Plot

Shows how much each feature contributes to the prediction.

High CIBIL values push predictions toward approval.

Low CIBIL values push predictions toward rejection.

Short loan terms increase approval probability.

High loan amounts reduce approval probability.

7.3. Partial Dependence Plot (PDP)

Shows how the model output changes with variations in a single feature.

CIBIL PDP displays a sharp transition from rejection to approval as the score increases.

Loan Term PDP shows decreasing approval probability with longer terms.

These XAI insights match real-world banking logic, adding transparency and interpretability.

8. Key Insights

CIBIL Score is the strongest factor affecting loan approval.

Shorter loan terms lead to higher approval probability.

Higher loan amounts decrease approval chances.

Income contributes moderately to loan decisions.

Asset-related features have limited influence on approval.

XAI validates that the model’s behavior aligns with common loan policies.





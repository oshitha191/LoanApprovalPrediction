Project Overview

This project predicts loan approval using various applicant financial and demographic features.
The goal is to build a machine learning model that is both accurate and explainable, especially because loan decisions affect real people and require fairness and transparency.

The project includes:

End-to-end data preprocessing

Exploratory Data Analysis (EDA)

Multiple machine learning models

Explainable AI (XAI) using SHAP and PDP

Model evaluation & comparison

Insights aligned with real-world financial logic

📂 Dataset Description

The dataset contains information such as:

CIBIL score

Loan term

Loan amount

Income

Asset values (bank, commercial, residential, luxury)

Education status

Self-employed status

Number of dependents

Target: Loan Status (Approved / Not Approved)

A sample of the dataset is shown using df.head() inside the notebook.

🔍 Exploratory Data Analysis

The EDA process includes:

Missing value analysis

Duplicate checks

Feature datatype inspection

Outlier detection using Z-Score

Distribution plots (histograms, KDE)

Count plots for categorical variables

Boxplots for financial variables

Correlation heatmap (including target variable)

Target distribution analysis

Univariate & bivariate analysis

Outlier treatment for financial fields

⚙️ Data Preprocessing

Encoding categorical features

Handling missing values

Scaling numerical variables

Balancing the dataset using SMOTE

Splitting data into training and testing sets

🤖 Machine Learning Models Used

The following ML models were trained and compared:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Gradient Boosting

AdaBoost

K-Nearest Neighbors (KNN)

Bagging Classifier (Random Forest as base estimator)

After evaluation, Random Forest performed the best and was selected as the final model.

📊 Model Evaluation

Evaluation metrics include:

Accuracy

Precision

Recall

F1-Score

ROC–AUC

Confusion Matrix

Screenshots of these metrics are provided in the Medium blog.

🧠 Explainable AI (XAI)

To make the model interpretable and transparent, the following XAI techniques were used:

🔸 Permutation Importance

Shows which features the model relied on the most

CIBIL Score, Loan Term, and Loan Amount were the strongest predictors

🔸 SHAP Summary Plot

Visualizes the impact of each feature on the prediction

High CIBIL (pink) pushes decisions toward approval

Low CIBIL (blue) pushes toward rejection

Short loan terms → higher approval probability

Large loan amounts → lower approval probability

🔸 Partial Dependence Plot (PDP)

Shows how prediction changes with variations in a single feature

CIBIL Score PDP showed a sharp jump from rejection → approval

Loan Term PDP showed approval decreases as term gets longer

These insights align with industry loan-risk logic and add transparency.

💡 Key Insights

CIBIL Score is the top factor influencing loan approval.

Short loan terms significantly increase approval probability.

Very high loan amounts reduce approval chances.

Income has a moderate effect.

Most asset-related features have minimal influence.

XAI confirmed that the model's behavior matches real-world banking rules.




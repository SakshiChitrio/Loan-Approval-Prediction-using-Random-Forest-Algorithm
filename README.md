# Loan Approval Prediction using Random Forest - 75.6% Accuracy

## Problem Statement
Bank ko predict karna hai ki customer ka loan approve hoga ya nahi.

## Dataset
614 loan applications, 13 columns. Target: Loan_Status

## Process
1. EDA - Shape (614,13) checked, null values found
2. Data Cleaning - Filled Gender, Married etc with Mode, LoanAmount with Median
3. Encoding - LabelEncoder for categorical columns
4. Model - RandomForestClassifier, 80% train 20% test
5. Result - 75.6% Accuracy

## Results
- Accuracy: 75.60%
- Confusion Matrix: 18 correctly rejected, 75 correctly approved
- Recall for Approved loans: 94%

## Tech Stack
Python, Pandas, Scikit-learn, Seaborn

## Files
- ML Project.ipynb
- train.csv

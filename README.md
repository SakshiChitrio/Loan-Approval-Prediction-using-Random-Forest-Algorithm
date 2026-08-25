# Loan Approval Prediction using Random Forest Algorithm

## 📌 Problem Statement
Banks face the challenge of assessing loan risk. The objective of this project is to predict whether a loan application will be **Approved or Rejected** based on applicant details like income, credit history, education, and property area.

## 📊 Dataset Information
- **Source:** Kaggle - Loan Prediction Dataset (train_u6lujuX_CVtuZ9i.csv)
- **Shape:** 614 Rows, 13 Columns
- **Target Variable:** Loan_Status (Y/N)
- **Features:** Gender, Married, Dependents, Education, Self_Employed, ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, Property_Area

## 🔍 Exploratory Data Analysis (EDA)
- Checked dataset shape: (614, 13)
- Identified null values: Gender (13), Married (3), Dependents (15), Self_Employed (32), LoanAmount (22), Loan_Amount_Term (14), Credit_History (50)
- Visualized distributions for categorical and numerical features

## 🧹 Data Cleaning & Preprocessing
1.  **Missing Value Handling:** Filled categorical nulls with `Mode` and numerical nulls (LoanAmount, Loan_Amount_Term) with `Median`.
2.  **Removed Column:** Dropped `Loan_ID` as it has no predictive value.
3.  **Encoding:** Used `LabelEncoder` to convert all categorical columns (Gender, Married, Education, Property_Area, Loan_Status) into numerical format (0/1).

## 🤖 Model Building
- **Split:** Train-Test Split (80% Training, 20% Testing) with `random_state=42`
- **Algorithm:** RandomForestClassifier
- **Reason for choice:** Random Forest handles both categorical and numerical data well and prevents overfitting.

## 📈 Results & Evaluation
- **Accuracy:** 75.60%
- **Confusion Matrix:**
    - 18 Correctly Predicted as Rejected
    - 75 Correctly Predicted as Approved
- **Classification Report:**
    - Precision for Approved Loan (Class 1): 75%
    - Recall for Approved Loan (Class 1): 94% (Model is excellent at identifying approved cases)
- **Sample Prediction Tested:** For a custom input [ApplicantIncome=5000 etc], Model Predicted -> Loan Approved.

## 🛠️ Tech Stack
- Python, Pandas, NumPy
- Scikit-learn (RandomForest, LabelEncoder, train_test_split)
- Matplotlib, Seaborn

## 📁 Repository Structure
- `ML Project.ipynb` - Complete code from EDA to prediction
- `train.csv` - Original dataset
- `requirements.txt` - Required libraries

## 🚀 How to Run
1. Clone the repo
2. pip install -r requirements.txt
3. Run the notebook `ML Project.ipynb`

## 👩‍💻 Author
Sakshi Chitrio - Aspiring Data Analyst

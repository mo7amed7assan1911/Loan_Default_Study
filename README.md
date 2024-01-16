# Loan Default Study

## Introduction

🏦 **Business Overview:**
The business revolves around providing financial assistance to individuals or businesses through loans.
When someone applies for a loan, they are requesting a specific amount of money to be lent to them for a defined purpose.
The lending institution evaluates the applicant's creditworthiness, risk profile, and financial stability to decide whether to grant or deny the loan.

💼 **Problem Statement:**
The challenge is to predict whether an approved loan applicant will repay or default based on their provided information. Our objective is to develop a predictive model leveraging applicant data to enhance our ability to anticipate and manage potential risks associated with loan approvals. In particular, we strongly emphasize **optimizing the recall metric to effectively detect applicants more likely to default.**

📊 **Dataset:**
The dataset used for this project consists of two files: current application data and previous application data. You can find it on Kaggle [here](https://www.kaggle.com/datasets/gauravduttakiit/loan-defaulter?select=application_data.csv).

🛠️ **Strategy of Using Both Datasets:**
The previous dataset extracts aggregated information about the applicant's history. It is then merged with the current application data to create the final dataset for analysis.

## Project Phases

### 🚀 Phase 1: Data Assessing & Cleaning

* Handling Missing Values:
  * Utilized appropriate methods to address missing values, including imputation by median and mode.
  * Imputed values of `occupation_type` column by grouping `organization_type & name_education_type` columns to enhance accuracy.

* Categorical Data Transformation:
  * Employed both one-hot encoding and label encoding to convert relevant string columns.

### 🔍 Phase 2: In-depth Analysis of Current Applications
Conducted an in-depth analysis of the current application data, identifying and addressing issues such as missing values, data conversion, and handling imbalanced data.

Our analysis aimed to answer several key questions, including:

**Studying Client Demographics:**
- How does age relate to loan approval?
- Is there a relationship between income and loan approval?
- How are the type of work and housing situation related to loan approval?

**Application Information:**
- Is there an optimal day of the week or time of day for submitting loan requests for higher approval chances?
- Which documents are most important for loan approval?

 #### Key Findings

📊 **Client Demographics:**
![image](https://github.com/mo7amed7assan1911/Loan_Default_Study/assets/55090589/292d3ad1-cc36-4206-ab3e-f6300783ffc9)

- Age follows a relatively normal distribution.
- Most applicants have finished secondary education.
- There is a gender imbalance, with more female applicants.
- Laborers and cleaning staff are the most common occupations.
- Marital status significantly impacts application proportions.

📈 **Applicant Info & Loan Approval:**
- Older applicants are more likely to repay.
- Men have a higher default rate compared to women.
- Higher education levels are associated with lower default rates.

🎯 **Feature Importance:**
- Employed a trick by using a dummy feature to delete each feature that gets lower importance than it.
- Used voting of 3 different models [Random Forest, Logistic Regression, SVM] to rank each feature\
by importance then takes the mean importance per feature.

![image](https://github.com/mo7amed7assan1911/Loan_Default_Study/assets/55090589/ab3054cc-9630-482f-95a5-769be78e0835)

- Then select features with high importance and low VIF.
![image](https://github.com/mo7amed7assan1911/Loan_Default_Study/assets/55090589/0202404e-48f4-4281-be2e-3b5fd6edf7de)


### 📈 Phase 3: Building a Predictive Model for Default Risk Assessment
- Used PCA to handle the Multicollinearity in the promising features.
- Fine-tuned XGBoost model with the PCA components.
- Built predictive **XGBoost Classifier** model on the original dataset with promising features to assess the risk of loan default based on the insights gained from previous phases.
- Got our goal by getting 0.92 Recall & 0.74 AUC score.
## Conclusion

🧾 This project involved a comprehensive analysis of loan application data, aiming to predict loan default risk. It utilized insights from client demographics and applicant information. The final model was built on a selected set of promising features.

---

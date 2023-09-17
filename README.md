# Loan Default Study

## Introduction

🏦 **Business Overview:**
The business revolves around providing financial assistance to individuals or businesses in the form of loans. When someone applies for a loan, they are requesting a specific amount of money to be lent to them for a defined purpose. The lending institution evaluates the applicant's creditworthiness, risk profile, and financial stability to make informed decisions about granting or denying the loan.

💼 **Problem Statement:**
The problem is to predict whether an applicant who is approved for a loan will repay or default based on the applicant's information.

📊 **Dataset:**
The dataset used for this project consists of two files: current application data and previous applications data. You can find it on Kaggle [here](https://www.kaggle.com/datasets/gauravduttakiit/loan-defaulter?select=application_data.csv).

🛠️ **Strategy of Using Both Datasets:**
The previous dataset is used to extract aggregated information about the applicant's history. It is then merged with the current application data to create the final dataset for analysis.

## Project Phases

🚀 **Phase 1: Aggregated Insights from Previous Applications**
In this phase, we extracted key features for each current applicant who has a history in our databases. One of the critical features is `prev_status`, which indicates a combination of approval rate and rejection rate of previous loans. It is set to 1 for applicants who have an approval rate greater than a specified threshold.

🔍 **Phase 2: In-depth Analysis of Current Applications**
We conducted an in-depth analysis of the current application data, identifying and addressing issues such as missing values, data conversion, and handling imbalanced data.

📈 **Phase 3: Building a Predictive Model for Default Risk Assessment**
We built a predictive model to assess the risk of loan default based on the insights gained from previous phases.

## Questions for Analysis

🔍 Our analysis aimed to answer several key questions, including:

**Studying Client Demographics:**
- How does age relate to loan approval?
- Is there a relationship between income and loan approval?
- How are the type of work and housing situation related to loan approval?

**Application Information:**
- Is there an optimal day of the week or time of day for submitting loan requests for higher approval chances?
- Which documents are most important for loan approval?

## Key Findings

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

📄 **Document Importance:**
- Most documents do not significantly impact loan approval or default rates.
- Recommendations are to drop most document-related columns except for `dock_3` and `dock_6`.

🎯 **Feature Importance:**
- Top features from random forest include two of the three columns aggregated from previous applications.

## Conclusion

🧾 This project involved a comprehensive analysis of loan application data, aiming to predict loan default risk. It utilized insights from client demographics, applicant information, and document importance. The final model was built on a selected set of promising features.

---

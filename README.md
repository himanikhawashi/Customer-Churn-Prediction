# Customer-Churn-Prediction

## Overview
This project aims to predict customer churn in a telecom business using machine learning. The goal is to proactively identify high-risk customers and enable targeted retention strategies to reduce customer attrition and improve business performance.

## Dataset
The dataset contains telecom customer information including:
- Usage behavior
- Service plans
- Customer service interactions
- Billing and account details
- Churn status

## Problem Statement
Customer churn leads to significant revenue loss in the telecom industry. This project focuses on building a reliable churn prediction model that flags customers likely to discontinue services, allowing the organization to take timely and targeted actions.

## Models Evaluated
- Logistic Regression  
- Random Forest  
- XGBoost Classifier  

## Evaluation Metrics
The models were evaluated using the following metrics:
- Accuracy  
- Precision (Churn class)  
- Recall (Sensitivity – Churn class)  
- F1-Score (Churn class)  
- ROC-AUC  

SMOTE was applied to handle class imbalance across all models.

## Model Comparison Report

| Metric | Logistic Regression | Random Forest | XGBoost |
|------|---------------------|---------------|---------|
| Accuracy | 77.27% | 93.51% | **95.13%** |
| Precision (Churn) | 34% | 75% | **87%** |
| Recall (Churn) | 63% | **81%** | 77% |
| F1-Score (Churn) | 44% | 78% | **82%** |
| Support (Churn) | 131 | 131 | 131 |
| SMOTE Applied | Yes | Yes | Yes |

## Model Recommendation: XGBoost Classifier

### Why XGBoost?
| Criteria | XGBoost Performance |
|--------|---------------------|
| Highest Accuracy | 95.13% – Best among all tested models |
| Precision (Churn) | 87% – Highly effective in identifying actual churners |
| F1-Score (Churn) | 82% – Strong balance between precision and recall |
| Handles Imbalance | Performs well on SMOTE-balanced data |
| Speed & Scalability | Efficient and scalable for large datasets |
| Robustness | Less prone to overfitting compared to Random Forest |

## Business Interpretation
The XGBoost model provides highly accurate churn predictions while minimizing false positives. This makes it ideal for **targeted retention campaigns**, ensuring that business resources are focused only on customers who are genuinely at risk of churning.

## Key Accomplishments
- Conducted detailed **Exploratory Data Analysis (EDA)** to uncover churn patterns related to usage behavior, service plans, and customer interactions.
- Built a high-performing **XGBoost churn prediction model** with strong accuracy and class-level performance.
- Identified key churn-driving features such as:
  - `day_mins`
  - `cust_serv_calls`
  - `intl_plan`
  - `eve_mins`
- Developed a **CHURN-FLAG** indicator to classify customers as:
  - YES (Likely to Churn)
  - NO (Not Likely to Churn)
- Created a **Churn Risk Scoring System** to categorize customers into:
  - High Risk
  - Medium Risk
  - Low Risk

## Business Strategy Based on Findings

### For Churn-Flagged Customers (CHURN-FLAG = YES)
- Proactive monitoring across all customer touchpoints
- Alert customer care teams during interactions for personalized support
- Auto-prioritization of support tickets for faster resolution
- Targeted communication via email, SMS, or calls for retention offers and feedback

### Request Fulfillment & Follow-up
- Faster resolution of billing and service-related requests
- Regular follow-ups to rebuild customer trust
- Internal alerts for agents when high-risk customers engage with support

### Operational Improvements
- Use churn flags and risk scores to enhance agent training
- Build dashboards to track churn trends and high-risk interactions in real time
- Improve service quality for high-risk customer segments

## Conclusion
The objective of this project was to build a reliable churn prediction system to proactively identify customers likely to discontinue their services. By implementing **CHURN-FLAG** and **Churn Risk Scores**, the project enables telecom businesses to move from reactive churn handling to **proactive retention strategies**.

This project not only predicts churn but also empowers business teams to act strategically—turning churn risk into an opportunity for customer loyalty and long-term value.

This project received an **A++ grade** for its technical depth, evaluation rigor, and strong business impact.

## Tools & Technologies
- Python
- Pandas, NumPy
- scikit-learn
- XGBoost
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn


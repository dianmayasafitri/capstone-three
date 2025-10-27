# Customer Lifetime Value (CLV) Prediction

## Project Overview
This project addresses a key challenge for an automotive insurance company: increasing long-term customer value. Many customers purchase only basic products and discontinue after a period, while retaining existing customers is more cost-efficient than acquiring new ones.
The goal is to build a predictive Machine Learning model to estimate each customer's Lifetime Value (CLV) and derive actionable business strategies for customer segmentation, pricing, and retention.

## Problem Statement
Identify factors driving high CLV among customers.
Predict CLV accurately for all customers.
Translate CLV predictions into actionable business strategies such as pricing simulations, promotional offers, and customer segmentation.

## Research Questions
How to build a high-performing ML model to predict Customer Lifetime Value?
Which factors most influence a customer’s CLV?
How can predicted CLV be applied for actionable business strategies (e.g., segmentation, policy simulations)?

## Dataset
The dataset contains 11 columns, describing customer characteristics and insurance details:


## Methodology
1. Data Preprocessing
Removed duplicates based on key features.
Handled missing values using mean or median imputation.
Addressed outliers via log transformation and RobustScaler.
Encoded categorical features with OneHotEncoder and OrdinalEncoder.
2. Exploratory Data Analysis (EDA)
Identified strong correlations (e.g., Monthly Premium Auto and Total Claim Amount).
Observed skewed distribution of CLV, prompting log transformation for normalization.
3. Feature Engineering
Created separate pipelines for numeric and categorical features.
Removed multicollinearity by dropping Total Claim Amount.
Defined final feature sets for modeling.
4. Model Development
Compared three regression algorithms:
Decision Tree Regressor
Random Forest Regressor
XGBoost Regressor
Evaluated performance using R², RMSE, and MAPE.
Used GridSearchCV for hyperparameter tuning of Random Forest and XGBoost.
5. Model Selection
XGBoost selected as the final model:
R²: 0.814
RMSE: 0.330
MAPE: 2.64%
Pipeline stored in pipeline_final_clv.sav for deployment.

## Explainable AI (Feature Importance)
Using SHAP:
- Top features influencing CLV:
- Number of Policies
- Monthly Premium Auto
- Income

Interpretation: Customers with higher values in these features tend to have higher CLV, indicating loyalty and long-term profit potential.

## Business Implications
- Customer Segmentation: High, Medium, Low CLV groups for targeted marketing.
- Retention & Cross-Selling: Focus on increasing the number of policies per customer.
- Pricing & Policy Simulation: Test impact of premium adjustments and claim ratios on CLV before implementation.

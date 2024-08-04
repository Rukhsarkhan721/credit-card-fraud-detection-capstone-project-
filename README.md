# credit-card-fraud-detection-capstone-project-
This repository contains the code and documentation for my capstone project on Credit Card Fraud Detection, completed as part of the Executive Post Graduation Diploma in Data Science with a specialization in Deep Learning from IIIT Bangalore and upGrad. The project aims to predict fraudulent credit card transactions using machine learning models.

# Problem Statement
Credit card fraud poses a significant threat to financial institutions and their customers, leading to substantial financial losses, erosion of trust, and damage to credibility. With the increasing prevalence of digital payment channels, the number of fraudulent transactions is rising, making it imperative for banks to implement robust fraud detection systems.

# Understanding and Defining Fraud
Credit card fraud involves any dishonest act or behavior to obtain information without proper authorization from the account holder for financial gain. Common methods of committing fraud include:

Skimming: Duplicating information from the magnetic strip of the card.
Manipulation/Alteration: Altering genuine cards to commit fraud.
Counterfeit Cards: Creating fake cards to perform unauthorized transactions.
Stealing/Loss of Cards: Using lost or stolen cards for fraudulent activities.
Fraudulent Telemarketing: Using telemarketing techniques to obtain card details fraudulently.

# Data Dictionary
The dataset includes credit card transactions made by European cardholders in September 2013. The features are as follows:

Time: Seconds elapsed between the first transaction and subsequent transactions.
V1 to V28: Principal components obtained using PCA to ensure confidentiality.
Amount: Transaction amount.
Class: Class label (1 for fraud, 0 for non-fraud).

# Objective
The primary objective of this project is to develop a machine learning model that accurately identifies fraudulent transactions. By achieving this, we aim to help banks and financial institutions:

Reduce Financial Losses: Minimize the monetary impact of fraudulent transactions.
Maintain Trust and Credibility: Ensure customers' trust in the banking system.
Minimize Manual Review: Reduce the time and effort spent on manual transaction reviews.
Proactive Monitoring: Implement proactive fraud detection mechanisms to prevent fraud before it occurs.

# Approach
To tackle this problem, we implemented the following steps:

Data Collection: Utilized a publicly available dataset containing 284,807 transactions over two days, of which 492 are fraudulent.
Data Cleaning and Preprocessing: Handled the high imbalance in the data and prepared it for modeling.
Exploratory Data Analysis: Conducted thorough EDA to understand the data and its patterns.
Model Building: Developed and tested various machine learning models to predict fraudulent transactions.
Evaluation and Optimization: Evaluated model performance and optimized it for better accuracy and precision.

# Model Selection Summary
After a thorough evaluation of various models on oversampled data, the XGBoost model utilizing Random Oversampling and StratifiedKFold Cross-Validation emerged as the top performer.

Performance Metrics:
Model Accuracy: 0.9993
XGBoost ROC Value: 0.9862
Optimal XGBoost Threshold: 0.0009
Insight:
Upon reviewing the results, it's evident that Logistic Regression with L2 Regularization and RepeatedKFold Cross-Validation achieved superior performance without employing any oversampling techniques.

Based on these findings, we have selected the XGBoost model with Random Oversampling and StratifiedKFold CV for further refinement through hyperparameter tuning to maximize its predictive capability.

Technologies and Tools
Programming Languages: Python
Libraries and Frameworks:
Data Manipulation: Pandas, NumPy
Visualization: Matplotlib, Seaborn
Statistical Analysis: Scipy
Machine Learning: Scikit-learn, XGBoost, Imbalanced-learn
Optimization: Scikit-optimize
Data Visualization: Tableau

# Code and Files
data/: Contains the dataset used for the project.
notebooks/: Jupyter notebooks with data exploration, preprocessing, and model training.
src/: Source code for data processing, feature engineering, and model implementation.
reports/: Generated reports and visualizations.

# How to Run
Clone the repository.
Install the required libraries using pip install -r requirements.txt.
Run the notebooks in the notebooks/ directory to reproduce the analysis and results.

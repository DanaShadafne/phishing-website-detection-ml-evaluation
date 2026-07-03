# Phishing Website Detection using Machine Learning

## Project Overview

This project is a critical reproduction and evaluation of the original 
"Phishing Website Detection by Machine Learning Techniques" project.

The goal is to detect phishing websites using machine learning models trained on 
URL and domain-based features.

The reproduction extends the original work by adding additional evaluation metrics,
model comparison, feature importance analysis, ROC analysis, and error analysis.


## Original Source

Original GitHub Repository:
https://github.com/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques


## Dataset

The dataset contains 10,000 website samples:
- 5,000 legitimate websites
- 5,000 phishing websites

Features include:
- URL length
- URL depth
- Prefix/Suffix
- Domain age
- DNS records
- Website traffic
- Redirection behavior


## Models Implemented

The following machine learning models were trained and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XGBoost


## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix


## Main Results

The experiments showed that ensemble-based models achieved the strongest performance.

Random Forest achieved the best overall balance between precision, recall, and F1-score.

XGBoost achieved strong classification performance using gradient boosting.


## Improvements Added

Compared with the original implementation, this reproduction added:

- Extended exploratory data analysis (EDA)
- Feature importance analysis
- Multiple evaluation metrics
- ROC curve comparison
- Confusion matrix analysis
- Critical evaluation of limitations


## How to Run

1. Open the notebook:

phishing_detection_project.ipynb

2. Install required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn xgboost

3. Run all cells.


## Files

- phishing_detection_project.ipynb  
  Complete implementation notebook.

- Phishing Website Detection using Machine Learning.pdf  
  Critical evaluation report.

- DataFiles/  
  Dataset files.


## Conclusion

Machine learning techniques can effectively detect phishing websites using extracted URL and domain features. However, real-world deployment requires updated datasets, continuous retraining, and further evaluation.

# Phishing Website Detection using Machine Learning

## Project Overview

This project is a critical reproduction and evaluation of the original **"Phishing Website Detection by Machine Learning Techniques"** project.

The goal is to detect phishing websites using machine learning models trained on URL and domain-based features.

This reproduction extends the original work by adding additional evaluation methods, including model comparison, feature importance analysis, ROC curve analysis, confusion matrix analysis, and a critical discussion of the original approach.

---

## Original Source

Original project:  
**"Phishing Website Detection by Machine Learning Techniques" by Shreya Gopal**

Original GitHub Repository:  
https://github.com/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques

---

## Dataset

The dataset contains **10,000 website samples**:

- 5,000 legitimate websites
- 5,000 phishing websites

The dataset includes URL-based, domain-based, and website behavior features.

Examples of features:

- URL Length
- URL Depth
- Prefix/Suffix usage
- Domain Age
- DNS Records
- Website Traffic
- Redirection behavior
- Mouse Over behavior
- Right Click behavior

---

## Models Implemented

The following machine learning models were implemented, trained, and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XGBoost

---

## Evaluation Metrics

The models were evaluated using multiple performance metrics:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix

Using multiple metrics provides a better evaluation of phishing detection performance compared with accuracy alone.

---

## Main Results

The experimental results showed that ensemble-based machine learning models achieved the strongest performance.

- Random Forest achieved the best overall balance between Precision, Recall, and F1-score.
- XGBoost also achieved strong performance using gradient boosting.

The feature importance analysis showed that URL-based features, especially URL Length, URL Depth, and Prefix/Suffix patterns, contributed significantly to phishing detection.

---

## Improvements Added

Compared with the original implementation, this reproduction added:

- Extended Exploratory Data Analysis (EDA)
- Feature importance analysis
- Multiple evaluation metrics
- ROC curve comparison
- Confusion matrix analysis
- Error analysis (False Positives and False Negatives)
- Critical evaluation of dataset and methodology limitations

---

## How to Run

1. Open the notebook:

   `phishing_detection_project.ipynb`

2. Install the required Python libraries:

   `pip install pandas numpy matplotlib seaborn scikit-learn xgboost`

3. Run all notebook cells.

---

## Repository Files

- **phishing_detection_project.ipynb**  
  Complete implementation notebook containing preprocessing, training, evaluation, and analysis.

- **Phishing Website Detection using Machine Learning.pdf**  
  Critical reproduction and evaluation report.

- **urldata.csv**  
  Dataset used for training and evaluating the machine learning models.

---

## Conclusion

Machine learning techniques can effectively assist in phishing website detection by learning patterns from URL and domain-based features.

The reproduction confirmed the effectiveness of these approaches while also identifying important limitations. Real-world deployment requires updated datasets, continuous model retraining, and evaluation under realistic cybersecurity conditions.

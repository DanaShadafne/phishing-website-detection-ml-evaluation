# Phishing Website Detection using Machine Learning

## Project Overview

This project is a critical reproduction and extended evaluation of the original **"Phishing Website Detection by Machine Learning Techniques"** project.

The objective is to detect phishing websites using machine learning models trained on URL, domain, and website behavior-based features.

Beyond reproducing the original implementation, this project performs additional experiments to evaluate the reliability, limitations, and real-world applicability of machine learning approaches for phishing detection.

---

## Original Source

Original project:  
**"Phishing Website Detection by Machine Learning Techniques" by Shreya Gopal**

Original GitHub Repository:  
https://github.com/shreyagopal/Phishing-Website-Detection-by-Machine-Learning-Techniques

The original work collected phishing and legitimate website samples, extracted URL/domain-based features, trained machine learning classifiers, and reported XGBoost as the strongest performing model.

This reproduction validates the original results and extends the evaluation using additional analysis methods.

---

## Dataset

The dataset contains **10,000 website samples**:

- 5,000 legitimate websites
- 5,000 phishing websites

The dataset contains extracted features describing URL structure, domain properties, and website behavior.

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
- Web Forwarding behavior

---

## Exploratory Data Analysis (EDA)

The dataset was analyzed before training to better understand data quality and possible limitations.

The analysis includes:

- Dataset structure inspection
- Missing value analysis
- Class distribution analysis
- Duplicate sample analysis
- Duplicate feature pattern analysis
- Low variance feature detection
- Feature correlation analysis

These checks help identify possible dataset bias, redundant features, and sources of overly optimistic performance.

---

## Models Implemented

Four machine learning models were trained and compared:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XGBoost

The models were evaluated to compare traditional linear methods, tree-based approaches, and ensemble learning techniques.

---

## Model Evaluation

The models were evaluated using multiple metrics:

- Accuracy
- Precision
- Recall
- F1-score
- F2-score
- ROC-AUC
- PR-AUC (Average Precision)
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix

Using several metrics provides a more complete evaluation than accuracy alone, especially because phishing detection is a cybersecurity problem where false negatives are highly important.

---

## Main Results

The experiments showed that ensemble-based models achieved the strongest overall performance.

Random Forest provided the best balance between:

- Accuracy
- Recall
- F1-score

XGBoost achieved very high precision but lower recall, meaning it produced fewer false alarms while missing more phishing websites.

For cybersecurity applications, recall is especially important because undetected phishing websites may create security risks.

---

## Additional Validation Experiments

To improve the reliability of the evaluation, additional experiments were added beyond the original implementation.

### Cross Validation

A 5-fold cross-validation experiment was performed to verify that model performance was stable and not dependent on only one train-test split.

### Feature Importance Analysis

Random Forest feature importance was used to identify the most influential phishing indicators.

The most important features included:

- URL Length
- URL Depth
- Prefix/Suffix patterns

### Feature Ablation Study

A feature ablation experiment was performed by training models using only the highest-ranked features.

This tested whether the most important features alone could achieve competitive performance compared with the complete feature set.

### Error Analysis

False Positive and False Negative cases were analyzed.

In phishing detection:
- False Positives incorrectly classify legitimate websites as phishing.
- False Negatives incorrectly classify phishing websites as safe.

False negatives are considered more dangerous because malicious websites remain undetected.

---

## Improvements Compared With Original Implementation

This reproduction extends the original project by adding:

- Extended Exploratory Data Analysis
- Duplicate and leakage analysis
- Low variance feature analysis
- Feature correlation analysis
- Feature importance interpretation
- Feature ablation experiments
- Cross-validation evaluation
- Additional cybersecurity metrics (F2-score and PR-AUC)
- ROC curve comparison
- Confusion matrix analysis
- Critical discussion of limitations

---

## Limitations

Although the models achieved strong results, several limitations remain:

- The dataset is balanced, while real-world phishing frequency is usually much lower.
- Phishing techniques continuously evolve over time.
- Models require updated datasets and retraining for real deployment.
- External validation using newer phishing datasets would improve reliability.

---

## How to Run

1. Clone the repository.

2. Install required dependencies:

```bash
pip install -r requirements.txt

## Repository Files

- **phishing_detection_project.ipynb**  
  Complete implementation notebook containing data analysis, preprocessing, model training, validation experiments, and evaluation.

- **Phishing Website Detection using Machine Learning.pdf**  
  Critical reproduction and evaluation report discussing the original approach, experimental results, limitations, and improvements.

- **urldata.csv**  
  Dataset used for training, testing, and evaluating the machine learning models.

- **requirements.txt**  
  List of Python dependencies required to reproduce the experiments.

---

## Conclusion

This project demonstrates that machine learning techniques can effectively detect phishing websites using URL, domain, and website behavior-based features.

The reproduction confirmed the effectiveness of the original approach while extending the evaluation with additional validation techniques, including cross-validation, feature importance analysis, feature ablation experiments, PR-AUC evaluation, F2-score analysis, and detailed error analysis.

The results show that ensemble models such as Random Forest and XGBoost achieve strong performance. However, real-world phishing detection requires continuous dataset updates, retraining, and evaluation under realistic cybersecurity conditions.

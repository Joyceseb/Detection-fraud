# 🛡️ Credit Card Fraud Detection System
A comprehensive machine learning project for detecting fraudulent credit card transactions using a hybrid dataset approach and advanced ensemble modeling.

# 📌 Project Overview
This project tackles the critical challenge of credit card fraud detection by combining a synthetic dataset (providing rich feature interpretability like Location and Merchant) with a real-world European PCA dataset (providing high-quality anonymized fraud patterns).

The system analyzes transaction patterns, handles extreme class imbalance (fraud < 1%).

# Key Features

**Hybrid Data Approach:** harmonizes synthetic and real-world PCA data for robust training.
**Advanced Preprocessing:**
**Robust Scaling:** Mitigates the impact of significant outliers in financial data.
**Class Balancing:** Addresses the 99:1 imbalance to prevent model bias.
**Multi-Model Evaluation:** Benchmarked 5 different classifiers:
Decision Tree
Random Forest
XGBoost
K-Nearest Neighbors (KNN)
Support Vector Classifier (SVC)

# Model Performance
We evaluated models based on Precision, Recall, and F1-Score, prioritizing the detection of fraud (Recall) while minimizing false alarms (Precision).

## 📊 Model Performance Comparison (Fraud Detection)

| Model          | Recall (Fraud Capture) | F1-Score | Verdict |
|----------------|------------------------|----------|---------|
| **XGBoost**    | 87%                    | High     | 🏆 Best Balance (High recall, fewest false positives) |
| Random Forest  | 95%                    | Medium   | Excellent detection, but aggressive (more false alerts). |
| SVC            | 93%                    | Low      | High recall but poor precision. |
| KNN            | 91%                    | Low      | Struggles with high-dimensional imbalance. |
| Decision Tree  | 78%                    | Low      | Overfits, poor generalization. |

> **Objective:** Maximize fraud detection recall while controlling false positives in a highly imbalanced dataset.

**Conclusion**: XGBoost was selected as the primary champion model due to its superior stability and F1-score, providing the best trade-off between catching fraudsters and not annoying legitimate customers.

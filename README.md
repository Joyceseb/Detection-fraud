# 🛡️ Credit Card Fraud Detection System

A comprehensive machine learning project for detecting fraudulent credit card transactions using a hybrid dataset approach and advanced ensemble modeling.

## 📌 Project Overview

This project tackles the critical challenge of credit card fraud detection by combining a **synthetic dataset** (providing rich feature interpretability like Location and Merchant) with a real-world **European PCA dataset** (providing high-quality anonymized fraud patterns).

The system analyzes transaction patterns, handles extreme class imbalance (fraud < 1%).

## 🚀 Key Features

*   **Hybrid Data Approach:** harmonizes synthetic and real-world PCA data for robust training.
*   **Advanced Preprocessing:**
    *   **Robust Scaling:** Mitigates the impact of significant outliers in financial data.
    *   **Class Balancing:** Addresses the 99:1 imbalance to prevent model bias.
*   **Multi-Model Evaluation:** Benchmarked 5 different classifiers:
    *   Decision Tree
    *   Random Forest
    *   XGBoost
    *   K-Nearest Neighbors (KNN)
    *   Support Vector Classifier (SVC)

## 📊 Model Performance

We evaluated models based on **Precision**, **Recall**, and **F1-Score**, prioritizing the detection of fraud (Recall) while minimizing false alarms (Precision).

| Model | Recall (Fraud Capture) | F1-Score | Verdict |
|-------|------------------------|----------|---------|
| **XGBoost** | **87%** | **High** | 🏆 **Best Balance** (High recall, fewest false positives) |
| Random Forest | 95% | Medium | Excellent detection, but aggressive (more false alerts). |
| SVC | 93% | Low | High recall but poor precision. |
| KNN | 91% | Low | Struggles with high-dimensional imbalance. |
| Decision Tree | 78% | Low | Overfits, poor generalization. |

**Conclusion:** XGBoost was selected as the primary champion model due to its superior stability and F1-score, providing the best trade-off between catching fraudsters and not annoying legitimate customers.

## 🛠️ Installation & Setup

### Prerequisites
*   Python 3.8+
*   pip

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd <repo-name>
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost 
```

### 3. Download Data
The `creditcard.csv` file exceeds GitHub's file size limits and is not included in this repository.
1.  Download the dataset from Kaggle: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).
2.  Unzip the file and place `creditcard.csv` inside the `Data/` folder.


### 🔬 Research & Analysis
To see the full data analysis, visualization, and model training process:
1.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook "Machine_Learning_improved.ipynb"
    ```
2.  Run all cells to reproduce the analysis.

## 📂 Project Structure

*   `Machine_Learning_improved.ipynb` - Main notebook for EDA, preprocessing, and model evaluation.
*   `Data/` - Contains the dataset CSVs.

## 📝 License
This project is open-source. Feel free to use and modify.

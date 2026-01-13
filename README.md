# Financial Fraud Detection using Machine Learning

This repository contains a data science project focused on identifying fraudulent financial transactions using a synthetic dataset of mobile money transactions. The project implements a Random Forest Classifier to handle the inherent class imbalance typical in fraud detection datasets.

## 🚀 Project Overview
Fraud detection is critical for financial institutions to prevent unauthorized activities. This project demonstrates a complete pipeline from raw data loading to model evaluation, achieving high precision and recall in detecting fraudulent patterns.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** * `pandas`, `numpy` (Data Manipulation)
    * `matplotlib`, `seaborn` (Data Visualization)
    * `scikit-learn` (Machine Learning)
    * `statsmodels` (Statistical Analysis - VIF)
    * `pyxlsb` (Handling .xlsb file formats)

## 📊 Dataset Features
The model processes transaction data including:
* **step:** Unit of time in the real world.
* **type:** CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
* **amount:** Amount of the transaction in local currency.
* **oldbalanceOrg / newbalanceOrig:** Initial and new balance of the sender.
* **oldbalanceDest / newbalanceDest:** Initial and new balance of the recipient.
* **isFraud:** The target variable (1 for fraud, 0 for legitimate).

## 🧠 Methodology
1.  **Data Cleaning:** Handled missing values and verified data integrity.
2.  **Feature Engineering:** * Calculated `errorBalanceOrig` and `errorBalanceDest` to capture discrepancies between reported amounts and balance changes.
    * Converted categorical variables into dummy variables.
3.  **Variable Selection:** Used Variance Inflation Factor (VIF) to detect and manage multi-collinearity.
4.  **Model Building:** Implemented a `RandomForestClassifier` with a maximum depth of 10 to prevent overfitting while maintaining high performance.
5.  **Evaluation:** Utilized Precision, Recall, and F1-Score to evaluate model effectiveness on imbalanced data.

## 📈 Results
The model demonstrated exceptional performance on the test set:
* **Precision:** 1.00
* **Recall (Fraud):** 0.98
* **F1-Score:** 0.99
* **Overall Accuracy:** 100%

## 📂 Repository Structure
* `Python Code for Fraud Detection.ipynb`: The primary Jupyter Notebook containing the analysis.
* `Fraud.xlsb`: (Ensure this is in my project directory) The raw transaction data.


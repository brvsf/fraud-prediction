# Fraudulent Transactions Prediction Project

## Overview
This project focuses on analyzing and predicting fraudulent transactions for a financial company using the provided dataset and the **XGBoost** model from scikit-learn. The project includes exploratory data analysis (EDA), data preprocessing, model training, evaluation, and insights for actionable fraud prevention strategies.

---

## Dataset Description

The dataset contains **6,362,620 rows** and **10 columns**, simulating 30 days of transaction data. Below is a brief description of the key features:

- **`step`**: Time unit in hours (1 step = 1 hour, total steps = 744).
- **`type`**: Type of transaction - `CASH-IN`, `CASH-OUT`, `DEBIT`, `PAYMENT`, `TRANSFER`.
- **`amount`**: Transaction amount in local currency.
- **`nameOrig`**: Customer initiating the transaction.
- **`oldbalanceOrg`**: Initial balance of the sender before the transaction.
- **`newbalanceOrig`**: New balance of the sender after the transaction.
- **`nameDest`**: Recipient of the transaction.
- **`oldbalanceDest`**: Initial balance of the recipient before the transaction (missing for merchants).
- **`newbalanceDest`**: New balance of the recipient after the transaction (missing for merchants).
- **`isFraud`**: Indicates whether the transaction was fraudulent.
- **`isFlaggedFraud`**: Flags illegal attempts (e.g., transactions > 200,000).

---

## Project Workflow

### 1. **Exploratory Data Analysis (EDA)**
   - Analyze the distribution of transaction types, amounts, and balances.
   - Visualize correlations between features and fraudulent activity.
   - Identify patterns in flagged and non-flagged fraudulent transactions.

### 2. **Data Preprocessing**
   - Handle missing values and outliers.
   - Encode categorical variables (`type`) using one-hot encoding.
   - Normalize numerical features (`amount`, `oldbalanceOrg`, `newbalanceOrig`, etc.).
   - Create new features to capture useful patterns (e.g., transaction balance differences).

### 3. **Model Training**
   - Use **XGBoost** from scikit-learn for model training.
   - Perform hyperparameter tuning using Grid Search or Random Search.
   - Use stratified sampling to address class imbalance.

### 4. **Model Evaluation**
   - Evaluate the model using metrics such as **AUC-ROC**, **precision**, **recall**, and **F1-score**.
   - Analyze the confusion matrix for true positives, false positives, and false negatives.

### 5. **Insights and Recommendations**
   - Identify key factors predicting fraudulent transactions.
   - Propose actionable prevention strategies to enhance fraud detection.

---

## Setup Instructions

### Prerequisites
Ensure the following are installed:
- Python 3.10 or later
- Required Python packages:
  ```bash
  pip install -r requirements.txt

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/brvsf/fraud-prediction.git
   cd fraud-prediction

2. Download the dataset and place in the `raw_data/` directory.

# Credit Card Fraud Detection

![Banner Image](https://www.practicalecommerce.com/wp-content/uploads/2019/02/Credit-card-fraud.jpg) <!-- Replace with your banner image URL -->

## Project Overview

The Credit Card Fraud Detection project aims to identify fraudulent transactions using a dataset of credit card transactions. The dataset includes various anonymized features and labels indicating whether a transaction is fraudulent or not. The primary objective is to build a model that can accurately detect fraudulent transactions, even in the presence of a highly imbalanced dataset.

## Dataset

The dataset used for this project is the [Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets?search=credit+card+fraud+detection) from Kaggle. It contains 284,807 transactions with 30 feature columns and one target column.

- **Features**: The dataset includes anonymized features (V1 to V28) along with 'Time', 'Amount', and 'Class'.
  - **Time**: Time elapsed since the first transaction in seconds.
  - **Amount**: Transaction amount.
  - **Class**: Label indicating whether the transaction is fraudulent (1) or not (0).

## Data Cleaning and Preparation

1. **Loading Data**:
   - The dataset was loaded using pandas and inspected for missing values, which were not present.

2. **Exploratory Data Analysis (EDA)**:
   - The dataset was examined to understand the distribution of normal and fraudulent transactions. The dataset is highly imbalanced, with 492 fraudulent transactions and 284,315 normal transactions.

3. **Handling Imbalanced Data**:
   - Due to the high imbalance, we used undersampling to balance the dataset:
     - Sampled an equal number of normal transactions as fraudulent transactions.
     - Combined the sampled normal transactions with the fraudulent transactions to create a balanced dataset.

4. **Feature and Target Separation**:
   - Features (`X`) and target (`Y`) were separated.
   - The dataset was split into training and testing sets, with 80% for training and 20% for testing.

## Model Building

1. **Model Selection**:
   - We used Logistic Regression for the classification task.

2. **Model Training**:
   - The model was trained on the balanced training dataset.

3. **Model Evaluation**:
   - Accuracy scores were computed for both training and testing datasets:
     - **Training Data Accuracy**: 95.04%
     - **Testing Data Accuracy**: 91.88%
   - The model performed well on both training and testing data, showing effective detection of fraudulent transactions.

## Key Findings

- The model achieved high accuracy, demonstrating its effectiveness in detecting fraudulent transactions.
- The undersampling technique helped in addressing the class imbalance, leading to better model performance.

## Future Work

- Explore more advanced algorithms like Random Forests or Gradient Boosting for potentially improved performance.
- Implement techniques to handle class imbalance more effectively, such as Synthetic Minority Over-sampling Technique (SMOTE).

## How to Run

To replicate the results, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/credit-card-fraud-detection.git

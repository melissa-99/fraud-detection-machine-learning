---
title: "project workflow"
author: "Andy Melissa"
date: "`r Sys.Date()`"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown
# Credit Card Fraud Detection Using Machine Learning and Imbalanced Data Techniques

## Project Overview
Credit card fraud detection is a critical challenge in financial systems because fraudulent transactions represent only a very small fraction of all transactions. This creates a highly imbalanced dataset that makes traditional machine learning models difficult to train effectively.

The objective of this project is to build and evaluate machine learning models capable of detecting fraudulent transactions while addressing the challenges caused by class imbalance.

This project demonstrates how data science techniques such as exploratory data analysis, feature engineering, imbalanced data handling, and ensemble learning models can be applied to improve fraud detection performance.

---

## Dataset
The dataset used in this project is the **Credit Card Fraud Detection dataset** from Kaggle.

Dataset characteristics:
- 284,807 transactions
- 492 fraudulent transactions
- Highly imbalanced dataset
- Features V1–V28 obtained through PCA transformation
- Additional features: `Time` and `Amount`
- Target variable: `Class`
  - `0` = Normal transaction
  - `1` = Fraudulent transaction

You can download it here:

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- imbalanced-learn
- XGBoost

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
The dataset was explored to understand the structure of the data and the distribution of fraudulent and legitimate transactions. Visualizations were used to highlight the severe class imbalance.

### 2. Data Preprocessing
The dataset was prepared for machine learning by separating features and target variables, scaling numerical features, and splitting the data into training and testing sets.

### 3. Handling Class Imbalance
Because fraudulent transactions represent less than 1% of the dataset, the **SMOTE (Synthetic Minority Oversampling Technique)** method was applied to balance the training dataset.

### 4. Machine Learning Models
Several machine learning models were trained and evaluated:

- Logistic Regression
- Random Forest
- XGBoost

### 5. Model Evaluation
Models were evaluated using multiple performance metrics:

- Precision
- Recall
- F1-score
- ROC-AUC

Special attention was given to **recall**, since detecting fraudulent transactions is critical in financial systems.

### 6. Model Interpretation
Feature importance analysis was performed using the Random Forest model to understand which variables contributed most to fraud detection.

### 7. Threshold Optimization
The classification threshold was adjusted to analyze how fraud detection performance changes when prioritizing recall over precision.

---

## Results

The Random Forest model achieved the best balance between precision and recall, making it the most suitable model for fraud detection in this dataset.

The results demonstrate that ensemble learning methods combined with imbalance handling techniques significantly improve fraud detection performance.

---

## Visualizations

The project includes several visualizations such as:

- Class imbalance distribution
- Transaction amount distribution
- ROC curve comparison
- Feature importance analysis

These visualizations help understand both the dataset and the model behavior.

---

## Conclusion

This project demonstrates how machine learning techniques can be used to detect fraudulent credit card transactions in highly imbalanced datasets. By applying imbalance handling methods and evaluating multiple models, the project highlights the effectiveness of ensemble learning models for fraud detection.

Such systems can assist financial institutions in identifying suspicious activity and reducing financial losses.

---

## Future Improvements

Potential improvements for this project include:

- Hyperparameter tuning
- Deep learning models
- Real-time fraud detection systems
- Deployment as a web application or API

---

## Author

Andy Melissa Nkou Mbida

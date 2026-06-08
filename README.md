# Customer Churn Prediction in E-Commerce Using Machine Learning Techniques

A complete machine learning pipeline for predicting customer churn in an e-commerce platform, comparing supervised classification models and complementing them with unsupervised customer segmentation. Developed as a graduation project.

## Project Overview

This project develops a machine learning system to predict customer churn for an e-commerce platform, using a publicly available real-world dataset of 5,630 customers and 20 behavioral and demographic features. Two classification models — Logistic Regression and Random Forest — are trained and compared, and K-Means clustering is applied to identify distinct customer segments and their associated churn behaviors.

## Key Results

| Metric | Logistic Regression | Random Forest |
|---|---|---|
| Accuracy | 0.8934 | **0.9680** |
| Precision | 0.7708 | **0.9528** |
| Recall | 0.5211 | **0.8521** |
| F1-Score | 0.6218 | **0.8996** |
| AUC | 0.8856 | **0.9898** |

Random Forest substantially outperformed Logistic Regression across all metrics. Most notably, Random Forest reduced the number of missed churners by 69% compared to Logistic Regression — a result with direct business implications.

K-Means clustering identified 4 distinct customer segments with churn rates ranging from 4.9% to 27.5%, demonstrating that churn risk is highly concentrated in identifiable behavioral profiles.

## Repository Structure
## Dataset

The dataset is the publicly available "Ecommerce Customer Churn Analysis and Prediction" dataset hosted on Kaggle:
https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction

It contains 5,630 customer records with 20 attributes covering behavioral, demographic, transactional, and service-related dimensions, plus a binary churn target variable.

## Methodology

1. **Data preprocessing** — Standardization of inconsistent categorical labels, median imputation for missing values, one-hot encoding of categorical variables, stratified 70/30 train/test split, and feature scaling.
2. **Supervised models** — Logistic Regression as an interpretable baseline; Random Forest as a more powerful ensemble approach.
3. **Evaluation** — Accuracy, precision, recall, F1-score, AUC, confusion matrices, and ROC curves.
4. **Unsupervised analysis** — K-Means clustering (K = 4) for customer segmentation, validated via the elbow method.
5. **Interpretation** — Random Forest feature importance ranking and cluster profile analysis.

## How to Run

The analysis was developed in Google Colab. To reproduce:

1. Open `notebook/Customer_Churn_Prediction.ipynb` in Google Colab.
2. Upload `data/E Commerce Dataset.xlsx` to the Colab session.
3. Run all cells (Runtime → Run all).

## Tools Used

- Python 3
- pandas, numpy
- scikit-learn (Logistic Regression, Random Forest, K-Means, StandardScaler, train_test_split, metrics)
- matplotlib, seaborn (visualization)
- Google Colab (development environment)

## Author

**Wasim Marwan Smeirat** — Student ID 202210355  
Department of Business Intelligence and Data Analytics  
Faculty of Administrative and Financial Sciences  
University of Petra  

Supervised by **Dr. Ayman Mansour**  
Graduation Project — Course 307498, Second Semester 2025/2026


# Cardiotocogram Data Analysis for Fetal Health Classification Using Machine Learning

## Overview

Monitoring fetal health is crucial to ensuring the well-being of unborn infants and achieving successful delivery outcomes. Traditional methods of assessing fetal health, such as manual analysis of cardiotocogram (CTG) data, are often time-consuming and susceptible to human error. This project applies machine learning techniques to CTG data to provide healthcare providers with more accurate, objective, and timely assessments of fetal health, enhancing prenatal care.

## Project Goals

This project aims to develop and evaluate machine learning algorithms to classify fetal health based on CTG data. We will explore several models, assess their performance, and investigate how preprocessing techniques, feature selection, and algorithm tuning impact the accuracy and efficiency of classification.

## Dataset

The CTG dataset contains **2,126 records** with **21 features** extracted from CTG exams. These records include fetal health classifications annotated into three classes:
- **Normal**
- **Suspect**
- **Pathological**

## Methodology

### 1. **Data Preprocessing**
- **Correlation Analysis**: A correlation matrix/heatmap was used to identify highly correlated features. Redundant features such as `histogram_median` and `histogram_min` were removed.
- **Standardization**: Numerical features were standardized to have a mean of 0 and a standard deviation of 1.
- **Imbalance Handling**: The **Synthetic Minority Over-sampling Technique (SMOTE)** was applied to address class imbalance by generating synthetic samples for the minority class.
- **Data Splitting**: The dataset was split into **75% training** and **25% testing** sets using the `train_test_split` function from scikit-learn.

### 2. **Machine Learning Models**
We implemented and evaluated the following models:
- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Gradient Boosting**


## Results

- The **Random Forest** model achieved the highest performance with an accuracy of **98.47%**.

| Model                  | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
|------------------------|--------------|---------------|------------|--------------|
| **Random Forest**       | 98.47        | 98.50         | 98.49      | 98.49        |
| **K-Nearest Neighbors** | 95.41        | 95.69         | 95.44      | 95.47        |
| **Gradient Boosting**   | 97.18        | 97.23         | 97.20      | 97.22        |

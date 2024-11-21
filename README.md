# Kernel SVM with Grid Search and k-Fold Cross Validation

This project demonstrates the use of a Kernel Support Vector Machine (SVM) classifier to predict user behavior based on the **Social Network Ads** dataset. It includes steps for data preprocessing, model training, evaluation, and optimization using **Grid Search** and **k-Fold Cross Validation**.

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Workflow](#workflow)
  - [1. Data Preprocessing](#1-data-preprocessing)
  - [2. Model Training](#2-model-training)
  - [3. Model Evaluation](#3-model-evaluation)
  - [4. Model Optimization](#4-model-optimization)
- [Results](#results)
- [Visualizations](#visualizations)
- [How to Run the Code](#how-to-run-the-code)
- [Technologies Used](#technologies-used)

---

## Introduction
The goal of this project is to classify whether a user will purchase a product based on their **Age** and **Estimated Salary** using a **Kernel SVM** model. The model is evaluated for performance and optimized using **Grid Search** and **k-Fold Cross Validation**.

---

## Dataset
The dataset used is **Social_Network_Ads.csv**, which contains the following features:
- **Age**: Age of the user
- **Estimated Salary**: Annual salary of the user
- **Purchased**: Binary target variable (1 = Purchased, 0 = Not Purchased)

---

## Workflow

### 1. Data Preprocessing
1. Load the dataset and split into **independent (X)** and **dependent (y)** variables.
2. Split the data into **training** and **test sets**.
3. Apply **feature scaling** using `StandardScaler` to normalize the input features.

### 2. Model Training
- Train a **Kernel SVM** model with the RBF kernel on the training set using `SVC`.

### 3. Model Evaluation
- Use the **Confusion Matrix** and **Accuracy Score** to evaluate the model's predictions on the test set.
- Apply **k-Fold Cross Validation** to calculate the mean accuracy and standard deviation, ensuring the model's reliability across multiple splits.

### 4. Model Optimization
- Use **Grid Search** to find the best hyperparameters (`C` and `gamma`) for the SVM model.
- Perform **10-fold Cross Validation** during the Grid Search process to select the best-performing parameters.

---

## Results

### Model Evaluation (Before Grid Search)
- **Confusion Matrix**: 
#### [[64 4]

#### [ 3 29]]

- **Accuracy on Test Set**: 93%

### Model Evaluation (After Grid Search)
- **Best Parameters**: `{'C': 0.5, 'gamma': 0.6, 'kernel': 'rbf'}`
- **Best Accuracy from Grid Search**: 90.67%

### k-Fold Cross Validation
- **Mean Accuracy**: 90.33%
- **Standard Deviation**: 6.57%

---

## Visualizations

### Decision Boundary (Training Set)
This visualization shows how the model separates the two classes (Purchased and Not Purchased) based on **Age** and **Estimated Salary**.

<p align="center">
<img src="path_to_training_set_visualization.png" alt="Training Set Decision Boundary" width="600">
</p>

---

## How to Run the Code

1. Clone this repository:
 ```bash
 git clone https://github.com/yourusername/kernel-svm-grid-search.git
 cd kernel-svm-grid-search


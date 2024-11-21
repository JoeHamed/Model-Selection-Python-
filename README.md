# Kernel SVM with Grid Search and k-Fold Cross Validation

This project demonstrates the use of a Kernel Support Vector Machine (SVM) classifier to predict user behavior based on a dataset. It includes steps for data preprocessing, model training, evaluation, and optimization using Grid Search and k-Fold Cross Validation.

## Project Overview

- **Dataset:** `Social_Network_Ads.csv`
- **Goal:** Predict whether a user will purchase a product based on their age and estimated salary.
- **Algorithm:** Support Vector Machine (SVM) with RBF kernel
- **Evaluation:** Accuracy, Confusion Matrix, k-Fold Cross Validation
- **Optimization:** Grid Search for hyperparameter tuning

---

## Workflow

### 1. Importing Libraries
```python
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

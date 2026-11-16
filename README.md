# Student Depression Dataset – Data Preprocessing

## Overview
This project focuses on data preprocessing of a Student Depression Dataset using Python and popular data science libraries. It demonstrates essential preprocessing techniques such as data inspection, data cleaning, outlier detection, categorical encoding, and feature scaling to prepare data for machine learning applications.

## Dataset Information
- **Dataset:** Student Depression Dataset
- **Total Records:** 4,464
- **Total Features:** 13
- **Target Variable:** Depression

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Data Preprocessing Steps

### 1. Data Loading and Inspection
- Loaded the dataset using Pandas.
- Examined dataset dimensions and structure using `shape()` and `info()`.
- Generated statistical summaries using `describe()`.
- Inspected categorical feature distributions.

### 2. Data Cleaning
- Separated numerical and categorical features.
- Checked missing values in numerical and categorical columns.
- Checked for duplicate records.
- No missing values or duplicate records were identified.

### 3. Outlier Detection and Handling
- Visualized numerical features using boxplots.
- Identified potential outliers in `CGPA` and `Cost_without_study`.
- Applied the Interquartile Range (IQR) method for outlier detection.
- Used IQR-based capping to handle extreme values.

### 4. Categorical Encoding

**Label Encoding**
- Applied Label Encoding to the target variable `Depression`.

**Ordinal Encoding**
- Encoded `Health_condition` using a predefined category order:
  - Normal
  - Good
  - Abnormal
  - Critical
- Encoded `Family_background` using a predefined category order:
  - Lower Middle class
  - Middle class
  - Rich class

**One-Hot Encoding**

Applied One-Hot Encoding to the following categorical features:
- Gender
- Relationship_status
- Marital_status
- Living_style
- friend_circle
- Home_division

### 5. Feature Scaling
- Applied StandardScaler to numerical features.
- Standardized numerical features to bring them to a common scale.
- Replaced the original numerical columns with their standardized values.

## Libraries and Modules

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import (
    LabelEncoder,
    OrdinalEncoder,
    OneHotEncoder,
    StandardScaler
)
```

## Key Learning Outcomes
- Understanding dataset structure and statistical summaries.
- Identifying and checking missing values and duplicate records.
- Visualizing and detecting outliers using boxplots.
- Applying IQR-based outlier handling techniques.
- Understanding the differences between Label, Ordinal, and One-Hot Encoding.
- Implementing feature standardization using StandardScaler.
- Preparing numerical and categorical data for machine learning workflows.

# Feature_Selection

This notebook aims to demonstrate different techniques for feature selection. It includes various methods such as imputation, exploratory data analysis (EDA), correlation analysis, and different feature selection techniques like feature importance, VIF (Variance Inflation Factor), forward selection, backward elimination, and RFECV (Recursive Feature Elimination with Cross-Validation).

## Problem Statement
The goal is to apply different feature selection techniques on the "media prediction and its cost" dataset.

## Collecting and Understanding the Data
The dataset is loaded from the file "media prediction and its cost.csv". Basic data exploration is performed, including checking the data's structure, missing values, and performing imputation using SimpleImputer.

## EDA (Exploratory Data Analysis)
Exploratory data analysis is performed to gain insights into the data and identify patterns or relationships. Box plots, bar plots, histograms, and correlation heatmaps are generated to visualize various features and their impact on the target variable (cost).

## Model Building
Linear Regression, KNN (K-Nearest Neighbors), and Decision Tree Regressor models are built to predict the target variable (cost) based on the selected features.

## Feature Selection
Different feature selection techniques are applied to select the most relevant features for the models.

1. Feature Importance: The feature importance is determined using a trained Decision Tree model. Features with cumulative importance greater than a threshold are selected.
2. VIF (Variance Inflation Factor): Features with VIF values below a threshold are selected.
3. Forward Selection/Backward Elimination: SequentialFeatureSelector from the mlxtend library is used to perform forward selection and select the best features based on the highest R-squared score.
4. RFECV (Recursive Feature Elimination with Cross-Validation): Recursive Feature Elimination with Cross-Validation is performed to select the optimal number of features based on the highest R-squared score.

## Selected Features
After applying different feature selection techniques, the following features are identified as important:

- promotion_name
- total_children
- avg_cars_at home(approx)
- avg. yearly_income
- num_children_at_home
- store_city
- store_state
- coffee_bar
- media_type

These features appear multiple times in the analysis, indicating their higher significance in the dataset.

Feel free to explore the code and experiment with different feature selection techniques based on your specific requirements.

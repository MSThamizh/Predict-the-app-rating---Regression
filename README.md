# Predict the App Rating - Regression

## Overview

This project focuses on predicting the ratings of apps from the Google Play Store using machine learning regression techniques. The dataset contains various features such as app category, reviews, size, installs, and price, which are used to predict the app rating. Data preprocessing steps like handling missing values, encoding categorical variables, and feature scaling are applied to improve model performance. The model is trained using Linear Regression, and the performance is evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² score.

## Features

- **Data Preprocessing**:  
  - Removed rows with null values to clean the dataset.
  - Label encoded categorical columns such as `Category`, `Type`, `Content Rating`, and `Genres`.
  - Converted features like `Reviews`, `Size`, `Installs`, and `Price` to appropriate numeric formats for model compatibility.
  - Handled `Size` column with specific logic to convert it into a numeric format based on whether it contains 'K' or 'M' (thousand or million).

- **Model Training**:  
  - Used **Linear Regression** to predict the app rating based on various features.

- **Model Evaluation**:  
  - **MAE (Mean Absolute Error)**: Measures the average magnitude of errors in the predictions.
  - **MSE (Mean Squared Error)**: Quantifies the average of the squared differences between the predicted and actual values.
  - **R² (R-squared)**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.

## Workflow

1. **Data Loading and Cleaning**:
   - Loaded the Google Play Store dataset and removed rows with missing values.
   - Encoded categorical columns using **Label Encoding** to transform them into numerical values.
   - Cleaned the `Size`, `Installs`, and `Price` columns by removing symbols and converting them to appropriate numeric types.

2. **Feature Engineering**:
   - Transformed the `Size` column (denoted in 'K' for thousands or 'M' for millions) into numeric values.
   - Converted `Reviews` and `Installs` to integers and handled commas in the `Installs` column.
   - Handled missing data in the `Size` column using forward filling.

3. **Model Training**:
   - Split the dataset into training and testing sets using an 80/20 split.
   - Trained a Linear Regression model on the training data.

4. **Model Evaluation**:
   - Evaluated the trained model on the test set using **MAE**, **MSE**, and **R²** metrics.

## Technologies Used

- **Languages**: Python  
- **Libraries**: Pandas, Scikit-learn

## References

- **Python Documentation**: [https://docs.python.org/3/](https://docs.python.org/3/)
- **Scikit-learn Documentation**: [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)

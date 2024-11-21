# Predict the App Rating

This project aims to build a machine learning model to predict the rating of a mobile application based on various features such as user reviews, app category, size, content rating, and more. The goal is to help developers and businesses understand the factors that influence app ratings and predict future ratings based on existing data.

## Problem Statement

The objective of this project is to predict the rating of mobile applications using historical data. By leveraging various app features, such as category, size, and user reviews, the model can estimate the app's rating, which can be beneficial for app developers and marketing teams to assess and improve their app's performance in the market.

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


## Technologies Used

- **Languages**: Python  
- **Libraries**: Pandas, Scikit-learn

## References

- **Python Documentation**: [https://docs.python.org/3/](https://docs.python.org/3/)
- **Scikit-learn Documentation**: [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)

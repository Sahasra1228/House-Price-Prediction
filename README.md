# House Price Prediction

## Overview

This project predicts house prices using Machine Learning techniques on the **Kaggle House Prices dataset**. The project includes data cleaning, exploratory data analysis, categorical feature encoding, model building, model evaluation, cross-validation, hyperparameter tuning, and feature-importance analysis.

## Dataset

* **Kaggle House Prices Dataset**
* Training dataset: `train.csv`
* 1,460 house records with multiple numerical and categorical features.

## Steps Followed

* Loaded and inspected the dataset.
* Handled missing values using **median and mode imputation**.
* Performed **Exploratory Data Analysis (EDA)** using:

  * Histograms
  * Scatter plots
  * Box plots
  * Correlation heatmaps
* Separated features and target variable (`SalePrice`).
* Applied **one-hot encoding** to categorical features.
* Split the dataset into **80% training and 20% testing data**.
* Built a **Linear Regression** model.
* Built a **Random Forest Regressor** model.
* Evaluated models using **Mean Absolute Error (MAE)** and **R² Score**.
* Applied **5-fold cross-validation** to evaluate model consistency.
* Performed **hyperparameter tuning using GridSearchCV**.
* Analyzed **feature importance** using the trained Random Forest model.
* Saved the final model using **Joblib**.

## Models Used

### Linear Regression

Used as a baseline regression model for predicting house prices.

### Random Forest Regressor

Used to capture nonlinear relationships between house features and prices.

## Model Results

| Model             |       MAE | R² Score |
| ----------------- | --------: | -------: |
| Linear Regression | 20,347.91 |   0.6473 |
| Random Forest     | 17,504.66 |   0.8973 |

The Random Forest model performed better than Linear Regression on the test dataset.

## Cross-Validation

The Random Forest model was evaluated using **5-fold cross-validation**.

* Mean Cross-Validation R²: **0.8408**

This was used to check how consistently the model performs across different training and validation splits.

## Hyperparameter Tuning

**GridSearchCV** was used to search for suitable Random Forest parameters.

Best parameters:

* `n_estimators`: 100
* `max_depth`: None
* `min_samples_split`: 2

Best Cross-Validation R²:

**0.8387**

The tuning results showed that the original/default Random Forest configuration was already competitive for this dataset.

## Feature Importance

The Random Forest model was used to identify the most important features contributing to house-price predictions.

Top features included:

1. `OverallQual`
2. `GrLivArea`
3. `2ndFlrSF`
4. `TotalBsmtSF`
5. `BsmtFinSF1`
6. `1stFlrSF`
7. `LotArea`
8. `GarageArea`
9. `GarageCars`
10. `YearBuilt`

`OverallQual` was the most influential feature in the model.

## Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Joblib**
* **Jupyter Notebook**

## Project Structure

```text
House-Price-Prediction/
│
├── data/
│   └── train.csv
│
├── house_prise.ipynb
├── house_price_model.pkl
├── README.md
└── .gitignore
```

## Key Learning Outcomes

* Data cleaning and missing-value handling
* Exploratory Data Analysis
* Categorical feature encoding
* Regression model building
* Model evaluation using MAE and R²
* Cross-validation
* Hyperparameter tuning
* Feature-importance analysis
* Model serialization using Joblib

## Author

**Cherukupally Sahasra**

# Regression and Regularization - Learning Notes

## Overview

* Worked on the Algerian Forest Fires Cleaned Dataset.
* Built and evaluated multiple regression models.
* Learned feature selection, standardization, regularization techniques, and cross-validation.

## Data Preparation

* Loaded the cleaned dataset using Pandas.
* Removed unnecessary columns (`day`, `month`, `year`).
* Encoded the target class:

  * Not Fire → 0
  * Fire → 1

## Feature and Target Selection

* Independent Features (X): All columns except FWI.
* Dependent Feature (y): FWI (Fire Weather Index).

```python
X = df.drop('FWI', axis=1)
y = df['FWI']
```

## Train-Test Split

* Split dataset into training and testing sets.
* Used `train_test_split()` with a test size of 25%.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.25, random_state=42
)
```

## Correlation Analysis

* Calculated feature correlations using `corr()`.
* Visualized correlations using a heatmap.
* Identified highly correlated features.

## Multicollinearity

* Learned about multicollinearity (when features are highly correlated).
* Created a custom function to identify correlated features.
* Removed features with correlation greater than 0.85.

## Feature Scaling (Standardization)

* Learned why scaling is important.
* Applied StandardScaler.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

### Key Learning

* Fit on training data.
* Transform both training and test data.
* Prevents data leakage.

## Effect of Standardization

* Compared boxplots before and after scaling.
* Observed that features were brought to a common scale.

## Linear Regression

* Built a Linear Regression model.
* Trained model using:

```python
linreg.fit(X_train_scaled, y_train)
```

### Learned

* `fit()` trains the model.
* `predict()` generates predictions.
* Evaluated model using:

  * MAE (Mean Absolute Error)
  * R² Score

## Lasso Regression (L1 Regularization)

```python
from sklearn.linear_model import Lasso
```

### Learned

* Reduces overfitting.
* Can shrink coefficients to zero.
* Performs automatic feature selection.

## Ridge Regression (L2 Regularization)

```python
from sklearn.linear_model import Ridge
```

### Learned

* Reduces coefficient values.
* Keeps all features.
* Helps reduce overfitting.

## Elastic Net Regression

```python
from sklearn.linear_model import ElasticNet
```

### Learned

* Combination of Lasso and Ridge.
* Uses both L1 and L2 regularization.
* Balances feature selection and coefficient shrinkage.

## Cross Validation

* Learned how to find the best regularization parameter automatically.

```python
from sklearn.linear_model import LassoCV
```

### Learned

* Cross-validation splits data into multiple folds.
* Trains and validates model on different folds.
* Helps choose the best alpha value.

## Evaluation Metrics

### Mean Absolute Error (MAE)

* Average absolute difference between actual and predicted values.

### R² Score

* Measures how well the model explains the variance in data.
* Higher R² indicates better model performance.

## Key Concepts Learned

* Train-Test Split
* Correlation Analysis
* Multicollinearity
* Feature Selection
* Standardization
* Linear Regression
* Ridge Regression
* Lasso Regression
* Elastic Net Regression
* Cross Validation
* Model Evaluation
* MAE
* R² Score

## Final Takeaway

* Standardization improves model performance for regression algorithms.
* Ridge, Lasso, and Elastic Net help reduce overfitting.
* Lasso performs feature selection.
* Cross-validation helps choose the best hyperparameters and build a more reliable model.


## 📚 What I Learned

Through this project, I learned how to build and evaluate a **Multiple Linear Regression** model using Python and Scikit-Learn.

### 1. Multiple Linear Regression

* Understood the concept of Multiple Linear Regression.
* Learned how a target variable can depend on multiple independent variables.
* Learned the equation:

```text
y = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ
```

Where:

* β₀ = Intercept
* β₁, β₂ = Coefficients
* x₁, x₂ = Independent Features

---

### 2. Data Cleaning

* Removed unnecessary columns from the dataset.
* Learned why irrelevant features should be dropped before training.

```python
df.drop(columns=['Unnamed: 0','month','year'])
```

---

### 3. Exploratory Data Analysis (EDA)

* Explored dataset structure using:

  * `head()`
  * `info()`
  * `describe()`

* Identified feature distributions and data types.

---

### 4. Correlation Analysis

* Calculated correlations using:

```python
df.corr()
```

* Learned how correlation helps understand relationships between variables.
* Identified which features strongly influence the target variable.

---

### 5. Data Visualization

* Used Seaborn Pairplots to visualize relationships between features.
* Created scatter plots to study feature interactions.
* Used Regression Plots (`regplot`) to observe linear trends.

---

### 6. Feature Selection

* Selected multiple independent variables:

```python
X = df[['interest_rate','unemployment_rate']]
```

* Learned the difference between:

  * Independent Features (X)
  * Dependent Variable (y)

---

### 7. Train-Test Split

* Split data into training and testing sets.
* Learned the importance of evaluating models on unseen data.

```python
train_test_split(test_size=0.25)
```

---

### 8. Feature Scaling

* Applied Standardization using `StandardScaler`.
* Learned why scaling improves model performance and ensures features are on the same scale.

Formula:

```text
z = (x - μ) / σ
```

---

### 9. Model Training

* Trained a Multiple Linear Regression model using:

```python
LinearRegression()
```

* Learned how the model finds the best-fit coefficients for multiple features.

---

### 10. Cross Validation

* Learned Cross Validation using:

```python
cross_val_score()
```

* Understood how Cross Validation provides a more reliable estimate of model performance.
* Learned why evaluating on multiple folds reduces overfitting risk.

---

### 11. Model Prediction

* Generated predictions using:

```python
regression.predict(X_test)
```

* Compared predicted values with actual values.

---

### 12. Model Evaluation Metrics

Learned important regression metrics:

#### Mean Absolute Error (MAE)

Measures average prediction error.

#### Mean Squared Error (MSE)

Penalizes larger errors more heavily.

#### Root Mean Squared Error (RMSE)

Provides error in the same unit as the target variable.

#### R² Score

Measures how much variance in the target variable is explained by the model.

---

### 13. Adjusted R² Score

Learned the importance of Adjusted R² when multiple features are used.

Benefits:

* Penalizes unnecessary features.
* Gives a more realistic evaluation of model performance.

---

### 14. Residual Analysis

* Calculated residuals:

```python
Residual = Actual - Predicted
```

* Visualized residual distributions.
* Learned how residual plots help validate regression assumptions.

---

### 15. Regression Assumptions

Learned how to check:

* Linearity
* Normal distribution of residuals
* Homoscedasticity (constant variance)
* Independence of errors

using residual plots and KDE plots.

---

### 16. Statsmodels OLS

Implemented Ordinary Least Squares (OLS) using Statsmodels.

```python
sm.OLS()
```

Learned how to interpret:

* Coefficients
* P-values
* R² Score
* Adjusted R² Score
* F-statistic

through the statistical summary report.

---

### 17. Coefficient Interpretation

Used:

```python
regression.coef_
```

to understand how each feature affects the target variable.

---

## 🚀 Key Takeaway

This project helped me understand how Multiple Linear Regression uses multiple independent variables to predict a target variable, evaluate model performance, validate assumptions, and interpret statistical results using both Scikit-Learn and Statsmodels.

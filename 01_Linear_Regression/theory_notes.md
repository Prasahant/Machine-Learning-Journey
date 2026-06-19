# Linear Regression Notes (Simple + Multiple)

## What I Learned

### 1. What is Linear Regression?

* Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.
* It finds the relationship between input features (X) and the target variable (y).

---

## 2. Simple Linear Regression

### Definition

* Simple Linear Regression uses **one independent feature** to predict the target variable.

### Equation

y=θ0​+θ1​x
Where:

* **y** = Predicted value
* **θ₀** = Intercept
* **θ₁** = Slope/Coefficient
* **x** = Input feature

### Example

* Predicting height using weight.
* Predicting salary using years of experience.

### Key Concepts

* Regression Line (Best Fit Line)
* Slope (Coefficient)
* Intercept
* Prediction using `predict()`

---

## 3. Multiple Linear Regression

### Definition

* Multiple Linear Regression uses **more than one independent feature** to predict the target variable.

### Equation

[
y = \theta_0 + \theta_1x_1 + \theta_2x_2 + ... + \theta_nx_n
]

### Example

* Predicting house price using:

  * Area
  * Number of bedrooms
  * Location score

### Advantage

* Usually provides better predictions because multiple factors are considered.

---

## 4. Train-Test Split

We divide the dataset into:

### X_train

* Independent features used for training.

### y_train

* Target values used for training.

### X_test

* Independent features used for testing.

### y_test

* Actual target values used to evaluate the model.

---

## 5. Model Training

```python
reg.fit(X_train, y_train)
```

### Role of fit()

* Trains the model.
* Learns the relationship between X and y.
* Calculates coefficients and intercept.

---

## 6. Prediction

```python
y_pred = reg.predict(X_test)
```

### Role of predict()

* Uses the trained model to predict target values for new data.

---

## 7. Standardization

### Why Standardization is Needed?

* Features may have different scales.
* Large-valued features can dominate smaller-valued features.
* Improves training speed and model performance.

### Formula

[
z = \frac{x-\mu}{\sigma}
]

Where:

* μ = Mean
* σ = Standard Deviation

### Scikit-Learn

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

### Important

* Fit the scaler only on training data.
* Use the same scaler to transform test and new data.

---

## 8. Visualization

```python
plt.scatter(X_train, y_train)
plt.plot(X_train, reg.predict(X_train), 'r')
```

### Meaning

* Scatter Plot → Actual training data points.
* Red Line → Predicted regression line.

---

## 9. Model Parameters

### Coefficient (Slope)

```python
reg.coef_
```

* Shows how much the target changes when a feature increases by one unit.

### Intercept

```python
reg.intercept_
```

* Predicted value when all input features are zero.

---

## 10. Prediction on New Data

```python
scaled_value = scaler.transform([[90]])
prediction = reg.predict(scaled_value)
```

### Important

* If the model is trained on scaled data, new data must also be scaled before prediction.

---

## 11. Evaluation Metrics

### Mean Absolute Error (MAE)

* Average absolute difference between actual and predicted values.

### Mean Squared Error (MSE)

* Average squared error.

### Root Mean Squared Error (RMSE)

* Square root of MSE.

### R² Score

* Measures how well the model explains the variance in the data.
* Range: 0 to 1.
* Higher value indicates better performance.

---

## Summary

* Learned Simple Linear Regression and Multiple Linear Regression.
* Understood train-test split.
* Learned the role of `fit()` and `predict()`.
* Learned coefficients and intercept.
* Learned feature standardization using `StandardScaler`.
* Visualized regression lines.
* Made predictions on new data.
* Evaluated model performance using MAE, MSE, RMSE, and R² Score.


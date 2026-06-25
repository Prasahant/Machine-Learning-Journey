# Polynomial Regression in Machine Learning

## 📌 Project Overview

In this notebook, I learned how Polynomial Regression works and how it can model non-linear relationships between input features and target variables. I generated a quadratic dataset, applied Linear Regression, and then improved the model using Polynomial Features.

---

## 🎯 Learning Objectives

* Understand the limitations of Linear Regression on non-linear data.
* Learn how Polynomial Regression transforms features.
* Compare Linear Regression and Polynomial Regression performance.
* Evaluate models using the R² Score.
* Visualize regression curves and predictions.

---

## 📚 Concepts Learned

### 1. Dataset Generation

Generated synthetic data using a quadratic equation:

[
y = 0.5x^2 + 1.5x + 2 + noise
]

This creates a curved relationship between X and y.

```python
X = 6 * np.random.rand(100,1) - 3
y = 0.5 * X**2 + 1.5 * X + 2 + np.random.rand(100,1)
```

---

### 2. Data Visualization

Used Matplotlib to visualize the generated dataset and understand the non-linear pattern.

```python
plt.scatter(X, y)
```

---

### 3. Train-Test Split

Split the dataset into training and testing sets.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

---

### 4. Linear Regression

Applied Linear Regression directly to the dataset.

```python
from sklearn.linear_model import LinearRegression

regression = LinearRegression()
regression.fit(X_train, y_train)
```

#### Observation

* Linear Regression tries to fit a straight line.
* It cannot capture the curved relationship effectively.
* The model performance is limited on quadratic data.

---

### 5. Model Evaluation using R² Score

```python
from sklearn.metrics import r2_score

score = r2_score(y_test, regression.predict(X_test))
```

#### What I Learned

* R² Score measures how well the model explains the variance in the data.
* Higher R² indicates better model performance.

---

### 6. Polynomial Feature Transformation

Converted original features into polynomial features.

```python
from sklearn.preprocessing import PolynomialFeatures

poly = PolynomialFeatures(degree=2)
X_train_poly = poly.fit_transform(X_train)
X_test_poly = poly.transform(X_test)
```

For degree 2:

[
x \rightarrow [1, x, x^2]
]

---

### 7. Polynomial Regression (Degree = 2)

```python
regression = LinearRegression()
regression.fit(X_train_poly, y_train)
```

#### Observation

* The regression curve closely follows the quadratic data.
* Performance improved significantly compared to simple Linear Regression.

---

### 8. Polynomial Regression (Degree = 3)

```python
poly = PolynomialFeatures(degree=3)
```

#### What I Learned

* Increasing the degree adds more flexibility.
* Higher-degree models can capture more complex patterns.
* Very high degrees may lead to overfitting.

---

### 9. Making Predictions on New Data

Generated new points and predicted outputs.

```python
X_new = np.linspace(-3, 3, 200).reshape(200,1)
X_new_poly = poly.transform(X_new)

y_new = regression.predict(X_new_poly)
```

---

### 10. Visualization of Predictions

```python
plt.plot(X_new, y_new)
```

#### Purpose

* Visualize the fitted polynomial curve.
* Compare actual data points with model predictions.

---

## 🔑 Key Takeaways

* Linear Regression works best for linear relationships.
* Polynomial Regression helps model non-linear patterns.
* PolynomialFeatures creates additional feature combinations.
* R² Score is useful for evaluating regression models.
* Choosing the right polynomial degree is important.
* Higher degrees increase model complexity and may cause overfitting.

---

## 🛠 Libraries Used

* NumPy
* Pandas
* Matplotlib
* Scikit-Learn

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
from sklearn.model_selection import train_test_split
from sklearn.metrics import r2_score
```

---

## 🚀 Skills Gained

✔ Data Visualization
✔ Train-Test Split
✔ Linear Regression
✔ Polynomial Regression
✔ Feature Engineering
✔ Model Evaluation (R² Score)
✔ Prediction on Unseen Data
✔ Machine Learning Workflow

---

## Conclusion

This project helped me understand how Polynomial Regression extends Linear Regression to handle non-linear datasets. By transforming features into polynomial terms, the model was able to fit curved data more accurately and achieve better prediction performance.

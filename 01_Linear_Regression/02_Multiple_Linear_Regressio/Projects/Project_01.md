# Multiple Linear Regression - California Housing Dataset

## Overview

* Worked with the California Housing Dataset from Scikit-Learn.
* Built a Multiple Linear Regression model to predict house prices.
* Performed data exploration, preprocessing, model training, and evaluation.

---

## Dataset Information

### California Housing Dataset

* Number of Samples: **20,640**
* Number of Features: **8**
* Problem Type: **Regression**
* Target Variable: **Median House Value**

### Features

1. MedInc – Median income
2. HouseAge – Median house age
3. AveRooms – Average number of rooms
4. AveBedrms – Average number of bedrooms
5. Population – Population of the block
6. AveOccup – Average occupancy
7. Latitude – Latitude location
8. Longitude – Longitude location

### Target

* Price (Median House Value)

---

## Data Exploration (EDA)

### Performed:

* Created DataFrame using Pandas.
* Checked dataset information using:

  * `head()`
  * `info()`
  * `describe()`
* Verified missing values using:

  * `isnull().sum()`
* Generated correlation matrix using:

  * `corr()`
* Visualized feature relationships using:

  * Heatmap (`sns.heatmap()`)

### Key Learning

* Correlation analysis helps understand relationships between features.
* Heatmaps provide a visual representation of correlations.

---

## Feature Selection

### Independent Features (X)

All columns except target variable.

```python
X = df.iloc[:,:-1]
```

### Dependent Feature (y)

```python
y = df.iloc[:,-1]
```

---

## Train-Test Split

Used train-test split to separate training and testing data.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.33, random_state=42
)
```

### Key Learning

* Training data is used to train the model.
* Testing data is used to evaluate model performance.

---

## Standardization

Used StandardScaler to scale features.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

### Key Learning

* Features may have different ranges.
* Standardization brings all features to a common scale.
* Fit scaler on training data only.
* Transform both training and testing data.

---

## Multiple Linear Regression

### Model Training

```python
from sklearn.linear_model import LinearRegression

reg = LinearRegression()

reg.fit(X_train, y_train)
```

### Key Learning

* `fit()` trains the model.
* Model learns relationships between features and target variable.

---

## Model Parameters

### Coefficients

```python
reg.coef_
```

* Represent the effect of each feature on house price.

### Intercept

```python
reg.intercept_
```

* Base prediction when all feature values are zero.

---

## Predictions

Generated predictions on test data.

```python
y_pred = reg.predict(X_test)
```

### Key Learning

* `predict()` uses the trained model to estimate house prices.

---

## Model Evaluation

### Mean Absolute Error (MAE)

```python
mean_absolute_error(y_test, y_pred)
```

* Average absolute difference between actual and predicted values.

### Mean Squared Error (MSE)

```python
mean_squared_error(y_test, y_pred)
```

* Average squared prediction error.

### Root Mean Squared Error (RMSE)

```python
np.sqrt(mse)
```

* Error expressed in the original unit.

### R² Score

```python
r2_score(y_test, y_pred)
```

* Measures how well the model explains the variance in the target variable.

---

## Residual Analysis

### Residuals

```python
residuals = y_pred - y_test
```

### Visualizations

* KDE Plot of residuals
* Residual vs Prediction Scatter Plot

### Key Learning

* Residuals should ideally be normally distributed.
* Randomly scattered residuals indicate a better model fit.

---

## Data Visualization

### Used:

* Heatmap
* Scatter Plot
* KDE Plot

### Purpose:

* Understand feature relationships.
* Evaluate prediction quality.
* Analyze model errors.

---

## Concepts Learned

* Multiple Linear Regression
* California Housing Dataset
* Exploratory Data Analysis (EDA)
* Correlation Matrix
* Heatmaps
* Train-Test Split
* Standardization
* StandardScaler
* Model Training
* Coefficients and Intercept
* Predictions
* MAE
* MSE
* RMSE
* R² Score
* Residual Analysis
* Model Evaluation

---

## Final Takeaway

Multiple Linear Regression uses multiple input features to predict a continuous target variable. Proper preprocessing, feature scaling, model evaluation, and residual analysis are essential steps in building a reliable regression model.


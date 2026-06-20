# Multiple Linear Regression using California Housing Dataset

## Project Overview

In this project, I built a Multiple Linear Regression model using the California Housing Dataset from Scikit-Learn. The goal was to predict median house prices based on housing and demographic features.

---

## Dataset Information

### California Housing Dataset

* Source: Scikit-Learn (`fetch_california_housing`)
* Number of Samples: **20,640**
* Number of Features: **8**
* Problem Type: **Regression**
* Target Variable: **Median House Value (Price)**

### Features

* MedInc – Median Income
* HouseAge – Median House Age
* AveRooms – Average Rooms
* AveBedrms – Average Bedrooms
* Population – Population in the block
* AveOccup – Average Occupancy
* Latitude – Latitude Location
* Longitude – Longitude Location

---

## Data Preparation

### Created DataFrame

Converted the dataset into a Pandas DataFrame for easier analysis.

```python
df = pd.DataFrame(dataset.data, columns=dataset.feature_names)
df['Price'] = dataset.target
```

### Explored Dataset

* Used `head()`, `info()`, and `describe()`
* Checked missing values using `isnull().sum()`
* Analyzed feature relationships using correlation matrix

---

## Exploratory Data Analysis (EDA)

### Correlation Analysis

```python
df.corr()
```

### Heatmap Visualization

```python
sns.heatmap(df.corr(), annot=True)
```

### Key Learning

* Correlation helps identify relationships between features.
* Heatmaps provide a visual representation of feature dependencies.

---

## Feature Selection

### Independent Features (X)

```python
X = df.iloc[:, :-1]
```

### Dependent Feature (y)

```python
y = df.iloc[:, -1]
```

---

## Train-Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.33,
    random_state=42
)
```

### Learning

* Training data is used to train the model.
* Testing data is used to evaluate model performance.

---

## Feature Scaling (Standardization)

### Why Standardization?

Features have different scales. Standardization brings them to a common scale and improves model performance.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

### Important Concept

* `fit()` learns mean and standard deviation from training data.
* `transform()` applies scaling.
* Always fit on training data only to avoid data leakage.

---

## Multiple Linear Regression

### Model Training

```python
from sklearn.linear_model import LinearRegression

reg = LinearRegression()
reg.fit(X_train, y_train)
```

### Learning

* `fit()` trains the model.
* The model learns coefficients and intercept values.

---

## Model Parameters

### Coefficients

```python
reg.coef_
```

* Represent the effect of each feature on house prices.

### Intercept

```python
reg.intercept_
```

* Base prediction when all feature values are zero.

---

## Predictions

```python
y_pred = reg.predict(X_test)
```

### Learning

* `predict()` generates house price predictions for unseen data.

---

## Model Evaluation

### Mean Absolute Error (MAE)

```python
mean_absolute_error(y_test, y_pred)
```

Measures average prediction error.

### Mean Squared Error (MSE)

```python
mean_squared_error(y_test, y_pred)
```

Penalizes larger errors more heavily.

### Root Mean Squared Error (RMSE)

```python
np.sqrt(mse)
```

Error expressed in original units.

### R² Score

```python
r2_score(y_test, y_pred)
```

Measures how well the model explains the variance in the data.

### Adjusted R²

Accounts for the number of features used in the model.

---

## Residual Analysis

### Residual Calculation

```python
residuals = y_pred - y_test
```

### Visualization

```python
sns.displot(residuals, kind="kde")
```

```python
plt.scatter(y_pred, residuals)
```

### Learning

* Residuals should ideally be normally distributed.
* Randomly scattered residuals indicate a good model fit.

---

## Pickling (Model Serialization)

### What is Pickling?

Pickling is the process of saving a trained machine learning model into a binary file so it can be reused without retraining.

### Save Model

```python
import pickle

pickle.dump(reg, open('house_price.pkl', 'wb'))
```

### Load Model

```python
model = pickle.load(open('house_price.pkl', 'rb'))
```

### Make Predictions

```python
model.predict(X_test)
```

### Learning

* Saves training time.
* Used during model deployment.
* Enables model reuse in production environments.

---

## Concepts Learned

* California Housing Dataset
* Multiple Linear Regression
* Train-Test Split
* Standardization
* StandardScaler
* Correlation Matrix
* Heatmap Visualization
* Model Training
* Coefficients and Intercept
* Predictions
* MAE
* MSE
* RMSE
* R² Score
* Adjusted R²
* Residual Analysis
* Pickling
* Model Serialization

---

## Final Takeaway

Multiple Linear Regression uses multiple input features to predict a continuous target variable. Proper preprocessing, standardization, model evaluation, residual analysis, and model serialization are important steps in building and deploying a reliable machine learning model.

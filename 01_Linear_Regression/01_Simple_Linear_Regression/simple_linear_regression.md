## 📚 What I Learned

During this project, I learned the complete workflow of building a Simple Linear Regression model using Python and Scikit-Learn.

### 1. Data Exploration

* Loaded a dataset using Pandas.
* Inspected the dataset structure and features.
* Understood the relationship between Weight and Height.

### 2. Data Visualization

* Created scatter plots using Matplotlib.
* Visualized the linear relationship between independent and dependent variables.
* Used Seaborn Pairplot for exploratory data analysis.

### 3. Correlation Analysis

* Calculated correlation between features using `df.corr()`.
* Learned how correlation helps identify the strength of relationships between variables.

### 4. Feature Selection

* Understood the difference between:

  * Independent Variable (X)
  * Dependent Variable (y)
* Learned why X should be a 2D DataFrame and y can be a 1D Series.

### 5. Train-Test Split

* Split data into training and testing sets.
* Learned the importance of evaluating models on unseen data.
* Used `random_state` for reproducible results.

### 6. Feature Scaling

* Learned Standardization using `StandardScaler`.
* Understood the formula:

```text
z = (x - mean) / standard deviation
```

* Applied scaling on training data using `fit_transform()`.
* Applied the same scaling on test data using `transform()`.

### 7. Simple Linear Regression

* Implemented Linear Regression using Scikit-Learn.
* Trained the model using training data.
* Learned the linear regression equation:

```text
y = θ₀ + θ₁x
```

where:

* θ₀ = Intercept
* θ₁ = Coefficient (Slope)

### 8. Understanding Coefficients

* Learned how to interpret the slope of a regression line.
* Understood that the coefficient shows how much the target variable changes for a one-unit change in the feature.

### 9. Model Visualization

* Plotted the best-fit regression line.
* Compared actual data points with predicted values.

### 10. Making Predictions

* Predicted heights for test data.
* Predicted height for new unseen weights.
* Learned that new data must be scaled before prediction.

### 11. Model Evaluation Metrics

Learned how to evaluate regression models using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

### 12. R² Score

* Learned that R² measures how well the model explains the variance in the target variable.
* Understood that higher R² values indicate better model performance.

### 13. Adjusted R²

* Learned why Adjusted R² is preferred when multiple features are present.
* Understood how it penalizes unnecessary features.

### 14. Ordinary Least Squares (OLS)

* Used the Statsmodels library.
* Generated a detailed regression summary.
* Learned how OLS calculates the best-fit line by minimizing residual errors.

### 15. End-to-End Machine Learning Workflow

Successfully completed:

* Data Loading
* Data Visualization
* Correlation Analysis
* Train-Test Split
* Feature Scaling
* Model Training
* Prediction
* Model Evaluation
* Statistical Analysis

### 🚀 Key Takeaway

This project helped me understand how a machine learning model learns the relationship between variables and uses that relationship to make predictions on unseen data.


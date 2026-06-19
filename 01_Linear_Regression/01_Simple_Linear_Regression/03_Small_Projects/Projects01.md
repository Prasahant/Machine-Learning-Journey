📈 Simple Linear Regression - Height vs Weight Prediction
📖 Project Overview

This project demonstrates the implementation of Simple Linear Regression using Python and Scikit-Learn.

The objective is to predict a person's Height based on their Weight by finding the best-fit linear relationship between the two variables.

🎯 Objective

To understand the complete Machine Learning workflow:

Loading and exploring data
Feature and target selection
Train-Test Split
Feature Standardization
Training a Linear Regression model
Making predictions
Visualizing results
Evaluating model performance
📂 Dataset Information

The dataset contains two variables:

Feature	Description
Weight	Independent Variable (Input)
Height	Dependent Variable (Target)

The goal is to learn the relationship:

Height = θ₀ + θ₁(Weight)

Where:

θ₀ = Intercept
θ₁ = Slope/Coefficient
🛠️ Technologies Used
Python
NumPy
Pandas
Matplotlib
Scikit-Learn
Jupyter Notebook
🔄 Machine Learning Workflow
1. Import Libraries

Imported essential libraries for data manipulation, visualization, and machine learning.

2. Load Dataset

Loaded the Height-Weight dataset using Pandas.

3. Data Visualization

Used scatter plots to visualize the relationship between Weight and Height.

4. Feature Selection
X = df[['Weight']]
y = df['Height']
X → Independent Feature
y → Dependent Feature
5. Train-Test Split
train_test_split(X, y, test_size=0.20, random_state=42)
80% Training Data
20% Testing Data
6. Feature Standardization

Applied Z-Score Standardization:

z = (x - μ) / σ

Where:

x = Data Point
μ = Mean
σ = Standard Deviation

Used:

StandardScaler()
7. Model Training
LinearRegression()

The model learns the best-fit line:

y = mx + c
8. Prediction

Predicted heights for unseen data using the trained model.

9. Visualization

Plotted:

Actual Data Points
Regression Line

to visualize model performance.

📊 Model Evaluation

The model can be evaluated using:

R² Score
Mean Squared Error (MSE)
Mean Absolute Error (MAE)

A higher R² score indicates a better fit of the regression line.

📈 Sample Prediction

Example:

scaled_weight = scaler.transform([[90]])
prediction = reg.predict([scaled_weight[0]])

Prediction:

Weight = 90 kg
Predicted Height ≈ 172.64 cm
📚 Key Concepts Learned
Simple Linear Regression
Independent and Dependent Variables
Train-Test Split
Feature Scaling
Standardization
Model Training
Prediction
Data Visualization
Regression Line
R² Score

🚀 Conclusion

This project provides a foundational understanding of Simple Linear Regression and demonstrates how Machine Learning models can learn relationships between variables and make predictions on unseen data.

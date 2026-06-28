# Logistic Regression - Complete Learning Journey

<p align="center">
  <img src="https://img.shields.io/badge/Machine%20Learning-Logistic%20Regression-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Python-Scikit--Learn-yellow?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">
</p>

## 📌 Project Overview

This repository contains my complete learning journey of **Logistic Regression**, one of the most fundamental supervised Machine Learning algorithms used for **classification problems**.

Instead of learning only the theory, I implemented Logistic Regression step by step on different datasets and explored various real-world concepts including:

* Binary Classification
* Multiclass Classification
* Handling Imbalanced Datasets
* ROC Curve
* AUC Score
* Threshold Analysis
* Hyperparameter Tuning
* Model Evaluation Metrics
* GridSearchCV
* Cross Validation

The notebooks are organized in a progressive manner, starting from the basics and moving toward more advanced concepts.

---

# 📂 Repository Structure

```
Logistic-Regression/
│
├── logistic_implementation.ipynb
├── LogReg_Imbalance_dataset.ipynb
├── LogReg_ROC.ipynb
├── multiclass_classification.ipynb
│
└── README.md
```

---

# 📖 Notebook Explanation

---

## 1️⃣ logistic_implementation.ipynb

### Objective

This notebook focuses on building a Logistic Regression model from scratch using Scikit-Learn.

### Topics Covered

* Introduction to Logistic Regression
* Binary Classification
* Data Loading
* Data Visualization
* Feature Selection
* Train-Test Split
* Model Training
* Model Prediction
* Model Accuracy
* Hyperparameter Tuning
* GridSearchCV
* Cross Validation

### Important Concepts Learned

### Why Logistic Regression?

Unlike Linear Regression, Logistic Regression predicts probabilities instead of continuous values.

It transforms the linear equation into probabilities using the **Sigmoid Function**.

[
P(y=1)=\frac{1}{1+e^{-z}}
]

where

[
z=wX+b
]

The output always lies between

```
0 and 1
```

making it suitable for classification.

---

### Train-Test Split

Learned how to split data into

* Training Data
* Testing Data

using

```python
train_test_split()
```

This prevents overfitting and evaluates the model on unseen data.

---

### Model Training

Implemented

```python
LogisticRegression()
```

and trained the classifier using

```python
model.fit(X_train,y_train)
```

---

### Hyperparameter Tuning

Explored different parameters such as

* penalty
* solver
* C
* class_weight

using

```python
GridSearchCV()
```

to improve model performance.

---

### Cross Validation

Learned why cross validation is important.

Instead of evaluating the model on one split, multiple folds are created.

Benefits

* Better generalization
* Less overfitting
* Reliable performance estimate

---

# 2️⃣ LogReg_Imbalance_dataset.ipynb

## Objective

This notebook explains how Logistic Regression behaves on **Imbalanced Datasets**.

---

### Topics Covered

* Class Imbalance
* Class Weight
* Precision
* Recall
* F1 Score
* Confusion Matrix
* Balanced Logistic Regression

---

### What is an Imbalanced Dataset?

A dataset where one class contains significantly more samples than the other.

Example

```
Normal Customers = 980

Fraud Customers = 20
```

The model may predict every customer as normal and still achieve

```
98% Accuracy
```

which is misleading.

---

### Why Accuracy is Not Enough

Learned that

High Accuracy

≠

Good Model

Instead we should evaluate

* Precision
* Recall
* F1 Score

---

### Confusion Matrix

Studied

* True Positive
* True Negative
* False Positive
* False Negative

and learned how they affect model evaluation.

---

### Precision

Measures

> Out of all predicted positive samples,
> how many are actually positive?

Useful when

False Positives are costly.

---

### Recall

Measures

> Out of all actual positive samples,
> how many did the model correctly identify?

Useful when

False Negatives are dangerous.

---

### F1 Score

Balances

* Precision
* Recall

using their harmonic mean.

Useful for imbalanced datasets.

---

### Class Weight

Implemented

```python
class_weight
```

to give more importance to minority class samples.

---

# 3️⃣ LogReg_ROC.ipynb

## Objective

Understanding model performance using

* ROC Curve
* AUC Score
* Threshold Selection

---

### Topics Covered

* Probability Prediction
* ROC Curve
* Dummy Classifier
* Logistic Regression Comparison
* Threshold Analysis

---

### Probability Prediction

Instead of directly predicting

```
0 or 1
```

Logistic Regression predicts

```python
predict_proba()
```

Example

```
0.15

0.82

0.95
```

---

### ROC Curve

The ROC Curve plots

```
True Positive Rate
```

against

```
False Positive Rate
```

for multiple threshold values.

A better classifier stays closer to the

top-left corner.

---

### AUC Score

Area Under Curve

Measures

Overall classification capability.

Interpretation

```
1.0 → Perfect Model

0.9 → Excellent

0.8 → Good

0.7 → Fair

0.5 → Random Guess
```

---

### Dummy Classifier

Compared Logistic Regression with a

Dummy Model

to understand whether the classifier is actually learning meaningful patterns.

---

### Threshold Analysis

Instead of always using

```
0.5
```

learned that threshold values can be adjusted according to business requirements.

---

# 4️⃣ multiclass_classification.ipynb

## Objective

Learning how Logistic Regression works for

more than two classes.

---

### Topics Covered

* Binary vs Multiclass Classification
* Softmax Function
* OvR Strategy
* Multinomial Logistic Regression
* Confusion Matrix
* Accuracy

---

### Binary Classification

Only two classes.

Example

```
Spam

Not Spam
```

---

### Multiclass Classification

More than two classes.

Example

```
Setosa

Versicolor

Virginica
```

---

### One-vs-Rest (OvR)

Creates

one classifier

for each class.

Example

```
Class A vs Others

Class B vs Others

Class C vs Others
```

Prediction comes from the classifier with the highest confidence.

---

### Multinomial Logistic Regression

Instead of multiple binary models,

a single model predicts probabilities for every class simultaneously.

Uses the

Softmax Function.

---

# 🛠 Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

# 📚 Machine Learning Concepts Learned

### Supervised Learning

✔ Classification

✔ Training

✔ Testing

---

### Logistic Regression

✔ Sigmoid Function

✔ Probability Prediction

✔ Decision Boundary

✔ Binary Classification

✔ Multiclass Classification

---

### Data Preparation

✔ Feature Selection

✔ Train-Test Split

✔ Handling Imbalanced Data

---

### Model Evaluation

✔ Accuracy

✔ Precision

✔ Recall

✔ F1 Score

✔ Confusion Matrix

✔ ROC Curve

✔ AUC Score

✔ Classification Report

---

### Model Optimization

✔ Hyperparameter Tuning

✔ GridSearchCV

✔ Cross Validation

✔ Solver Selection

✔ Regularization

✔ Class Weight

---
# 📚 Detailed Learning Outcomes

## 1. The Mathematical Intuition Behind Logistic Regression

Logistic Regression is a supervised machine learning algorithm used for classification problems. Unlike Linear Regression, which predicts continuous numerical values, Logistic Regression predicts the probability that an observation belongs to a particular class.

It first computes a weighted sum of the input features:

```text
z = w₁x₁ + w₂x₂ + ... + wₙxₙ + b
```

Instead of using this value directly as the prediction, Logistic Regression passes it through the Sigmoid Function, which converts any real number into a probability between 0 and 1.

---

## 2. Why Logistic Regression is Suitable for Classification Instead of Linear Regression

Linear Regression predicts values that can range from negative infinity to positive infinity, making it unsuitable for classification tasks where predictions should represent probabilities.

For example, a Linear Regression model may predict:

```text
1.42
-0.65
2.81
```

These values cannot be interpreted as probabilities.

Logistic Regression solves this issue by using the Sigmoid Function, ensuring that predictions always lie between 0 and 1. A decision threshold (commonly 0.5) is then used to classify observations into different classes.

---

## 3. How the Sigmoid Function Converts Linear Outputs into Probabilities

The Sigmoid Function transforms any real-valued input into a probability.

Formula:

```text
P(y=1) = 1 / (1 + e^(-z))
```

Properties:

* Output ranges between 0 and 1.
* Large positive values become probabilities close to 1.
* Large negative values become probabilities close to 0.
* Values near zero produce probabilities around 0.5.

This allows Logistic Regression to estimate the likelihood that a sample belongs to the positive class.

---

## 4. How to Train and Evaluate a Classification Model Using Scikit-Learn

The complete machine learning workflow includes:

* Loading the dataset.
* Splitting the dataset into training and testing sets.
* Creating a Logistic Regression model.
* Training the model using the training data.
* Making predictions on unseen data.
* Evaluating performance using classification metrics.

Typical workflow:

```python
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

Evaluation metrics include:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC-AUC Score

---

## 5. The Importance of Splitting Data into Training and Testing Sets

A model should be evaluated on data that it has never seen before.

The dataset is divided into:

* Training Set (used for learning patterns)
* Testing Set (used for evaluating performance)

A common split is:

```text
75% Training
25% Testing
```

Benefits include:

* Preventing overfitting.
* Measuring generalization performance.
* Simulating real-world predictions.

---

## 6. Why Hyperparameter Tuning Improves Model Performance

Hyperparameters control the learning process of the algorithm and must be chosen before training.

Examples include:

* C
* penalty
* solver
* class_weight

Instead of guessing the best values, GridSearchCV systematically tests multiple combinations to identify the optimal configuration using cross-validation.

Benefits:

* Better predictive performance.
* Reduced overfitting.
* Improved model stability.

---

## 7. How Cross Validation Provides a More Reliable Estimate of Model Performance

A single train-test split may produce biased results depending on the selected samples.

Cross Validation divides the dataset into multiple folds.

Example (5-Fold Cross Validation):

* Fold 1 → Validation
* Fold 2 → Validation
* Fold 3 → Validation
* Fold 4 → Validation
* Fold 5 → Validation

Each fold serves as the validation set once, and the average performance is reported.

Advantages:

* Uses all data efficiently.
* Produces a more reliable evaluation.
* Reduces dependence on one random split.

---

## 8. Why Accuracy Alone Can Be Misleading for Imbalanced Datasets

Consider a fraud detection dataset:

```text
990 Legitimate Transactions
10 Fraudulent Transactions
```

If the model predicts every transaction as legitimate, the accuracy is:

```text
99%
```

Despite this high accuracy, the model completely fails to detect fraud.

Therefore, for imbalanced datasets, metrics like Precision, Recall, and F1 Score provide a much better evaluation than Accuracy alone.

---

## 9. How Precision, Recall, and F1 Score Provide Better Insights

### Precision

Precision answers:

> Out of all predicted positive samples, how many were actually positive?

High Precision indicates few False Positives.

Useful when False Positives are expensive.

Examples:

* Spam detection
* Medical diagnosis

---

### Recall

Recall answers:

> Out of all actual positive samples, how many were correctly identified?

High Recall indicates few False Negatives.

Useful when missing positive cases is costly.

Examples:

* Cancer detection
* Fraud detection

---

### F1 Score

The F1 Score combines Precision and Recall into a single metric using their harmonic mean.

It is especially useful when dealing with imbalanced datasets because it balances both types of errors.

---

## 10. How to Interpret a Confusion Matrix

A Confusion Matrix summarizes prediction results.

It consists of:

* True Positive (TP)
* True Negative (TN)
* False Positive (FP)
* False Negative (FN)

It helps identify:

* Correct predictions.
* Incorrect predictions.
* Types of classification errors.

Many evaluation metrics are derived directly from the Confusion Matrix.

---

## 11. How ROC Curves and AUC Scores Measure Classifier Performance

The ROC Curve plots:

* True Positive Rate (Recall)
* False Positive Rate

for different classification thresholds.

A good classifier has a curve closer to the top-left corner.

The Area Under the Curve (AUC) summarizes this performance.

Interpretation:

```text
AUC = 1.0  → Perfect Classifier
AUC > 0.9 → Excellent
AUC > 0.8 → Good
AUC = 0.5 → Random Guess
```

Higher AUC values indicate better discrimination between classes.

---

## 12. How Adjusting Classification Thresholds Affects Predictions

The default classification threshold is usually:

```text
0.5
```

Changing this threshold changes the balance between Precision and Recall.

Lower Threshold:

* Higher Recall
* Lower Precision

Higher Threshold:

* Higher Precision
* Lower Recall

Threshold selection depends on the application's requirements.

---

## 13. The Difference Between Binary and Multiclass Logistic Regression

### Binary Classification

Predicts between two classes.

Examples:

* Spam vs Not Spam
* Fraud vs Not Fraud
* Pass vs Fail

---

### Multiclass Classification

Predicts among more than two classes.

Examples:

* Iris flower species
* Handwritten digit recognition
* Animal classification

Scikit-Learn supports multiclass classification using strategies such as:

* One-vs-Rest (OvR)
* Multinomial Logistic Regression (Softmax)

---

## 14. Practical Experience Implementing Logistic Regression on Real-World Datasets

Throughout these notebooks, I gained practical experience in building complete machine learning pipelines.

This included:

* Loading datasets.
* Cleaning and preparing data.
* Splitting data into training and testing sets.
* Training Logistic Regression models.
* Performing hyperparameter tuning.
* Applying Cross Validation.
* Handling imbalanced datasets using class weights.
* Evaluating models using multiple performance metrics.
* Plotting ROC Curves.
* Comparing Logistic Regression with Dummy Classifiers.
* Building both Binary and Multiclass classification models.

These hands-on implementations strengthened both my theoretical understanding and practical skills in applying Logistic Regression to real-world classification problems.


---



# 📖 Conclusion

This repository represents a comprehensive hands-on exploration of Logistic Regression. It begins with the fundamentals of binary classification and progresses to advanced topics such as class imbalance, ROC-AUC analysis, hyperparameter tuning, and multiclass classification. Through these notebooks, I gained both theoretical understanding and practical implementation skills, building a strong foundation for tackling real-world classification problems with Machine Learning.


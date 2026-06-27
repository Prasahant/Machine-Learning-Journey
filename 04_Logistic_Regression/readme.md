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

# 🎯 Key Takeaways

Through these notebooks, I learned:

* The mathematical intuition behind Logistic Regression.
* Why Logistic Regression is suitable for classification instead of Linear Regression.
* How the Sigmoid function converts linear outputs into probabilities.
* How to train and evaluate a classification model using Scikit-Learn.
* The importance of splitting data into training and testing sets.
* Why hyperparameter tuning improves model performance.
* How Cross Validation provides a more reliable estimate of model performance.
* Why accuracy alone can be misleading for imbalanced datasets.
* How Precision, Recall, and F1 Score provide deeper insights into classification quality.
* How to interpret a Confusion Matrix.
* How ROC Curves and AUC Scores measure classifier performance across different thresholds.
* How adjusting classification thresholds affects model predictions.
* The differences between Binary and Multiclass Logistic Regression.
* Practical experience implementing Logistic Regression on real-world datasets.

---

# 🚀 Future Improvements

* Feature Engineering
* Feature Scaling
* Regularization Comparison (L1 vs L2 vs Elastic Net)
* SMOTE for Imbalanced Data
* Pipeline Implementation
* Model Deployment using Flask/FastAPI
* Explainability with SHAP and LIME

---

# 📖 Conclusion

This repository represents a comprehensive hands-on exploration of Logistic Regression. It begins with the fundamentals of binary classification and progresses to advanced topics such as class imbalance, ROC-AUC analysis, hyperparameter tuning, and multiclass classification. Through these notebooks, I gained both theoretical understanding and practical implementation skills, building a strong foundation for tackling real-world classification problems with Machine Learning.


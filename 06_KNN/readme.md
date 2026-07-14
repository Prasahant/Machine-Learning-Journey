# 🤖 K-Nearest Neighbors (KNN)

> A complete hands-on implementation and theory of the **K-Nearest Neighbors (KNN)** algorithm covering both **Classification** and **Regression**, along with hyperparameter tuning using **GridSearchCV**.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success)
![Status](https://img.shields.io/badge/Completed-brightgreen)

---

# 📌 Overview

K-Nearest Neighbors (KNN) is a **Supervised Machine Learning** algorithm used for both:

- ✅ Classification
- ✅ Regression

Unlike many machine learning algorithms, KNN is a **Lazy Learning** algorithm because it does not build a model during training. Instead, it stores the training data and predicts the output based on the nearest data points.

![Uploading Screenshot 2026-07-14 111005.png…]()

---

# 📂 Repository Contents

```
06_KNN/
│
├── KNN_Classification.ipynb
├── KNN_Regression.ipynb
├── images/
│   └── knn_banner.png
└── README.md
```

---

# 📖 Topics Covered

## 📍 Introduction to KNN
- What is KNN?
- Why KNN?
- Working Principle
- Advantages & Disadvantages
- Applications

---

## 📍 Distance Metrics

Implemented different distance calculations:

- Euclidean Distance
- Manhattan Distance
- Minkowski Distance
- Cosine Distance (Theory)

### Euclidean Distance

\[
d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}
\]

---

## 📍 KNN Classification

Learned

- Binary Classification
- Multi-class Classification
- Majority Voting
- Decision Boundary
- Choosing K
- Effect of Small and Large K

Example Applications

- Spam Detection
- Disease Prediction
- Digit Recognition
- Customer Classification

---

## 📍 KNN Regression

Learned

- Continuous Value Prediction
- Average of Nearest Neighbors
- Weighted Average Prediction

Example Applications

- House Price Prediction
- Salary Prediction
- Temperature Prediction

---

# 📊 Discrete vs Continuous Target

### Classification

Predicts **Discrete Values**

Examples

- Spam / Not Spam
- Cat / Dog
- Pass / Fail

---

### Regression

Predicts **Continuous Values**

Examples

- House Price
- Temperature
- Salary
- Sales

---

# 📍 Feature Scaling

Since KNN depends on distance calculations, feature scaling is essential.

Covered

- StandardScaler
- MinMaxScaler

---

# 📍 Hyperparameter Tuning

Implemented **GridSearchCV** for selecting the optimal value of **K**.

Example

```python
param_grid = {
    "n_neighbors": range(1,11)
}
```

Used

- Cross Validation
- Accuracy Comparison
- Best K Selection

---

# 📍 Cross Validation

Implemented

- Train-Test Split
- K-Fold Cross Validation
- GridSearchCV

---

# 📍 KD Tree

Learned

- What is KD Tree?
- Tree Construction
- Splitting using X and Y axis
- Nearest Neighbor Search
- Pruning
- Time Complexity

---

# 📍 Ball Tree

Covered

- Ball Tree Construction
- Ball Center
- Radius
- Ball Pruning
- Faster Neighbor Search

---

# 📍 Variants of KNN

- KD Tree
- Ball Tree
- Brute Force Search

---

# 📈 Workflow

```text
Collect Dataset
        │
        ▼
Data Preprocessing
        │
        ▼
Feature Scaling
        │
        ▼
Choose K
        │
        ▼
Train KNN
        │
        ▼
GridSearchCV
        │
        ▼
Prediction
        │
        ▼
Model Evaluation
```

---

# 🛠️ Libraries Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

# 📊 Evaluation Metrics

### Classification

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Regression

- MAE
- MSE
- RMSE
- R² Score

---

# 🎯 Applications of KNN

- Recommendation Systems
- Image Recognition
- Face Recognition
- Medical Diagnosis
- Customer Segmentation
- Fraud Detection
- House Price Prediction
- Stock Price Prediction

---

# 📚 What I Learned

✔ Supervised Learning

✔ Instance-Based Learning

✔ Lazy Learning

✔ Distance Metrics

✔ Classification

✔ Regression

✔ Feature Scaling

✔ Hyperparameter Tuning

✔ GridSearchCV

✔ Cross Validation

✔ KD Tree

✔ Ball Tree

✔ Model Evaluation

---

# 🚀 Future Improvements

- Implement Weighted KNN from scratch
- Visualize Decision Boundaries
- Compare KNN with Logistic Regression
- Compare different Distance Metrics
- Implement KNN without using Scikit-Learn
- Performance comparison of KD Tree vs Ball Tree

---

# 📖 References

- Scikit-Learn Documentation
- Machine Learning by Tom M. Mitchell
- Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow
- Pattern Recognition and Machine Learning by Christopher Bishop

---

## ⭐ If you found this repository helpful

Give this repository a ⭐ and follow my **Machine Learning Journey** for more practical implementations and theory notes.

Happy Learning! 🚀

# Naive Bayes - Complete Learning Journey

<p align="center">
  <img src="https://img.shields.io/badge/Machine%20Learning-Naive%20Bayes-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Python-Scikit--Learn-yellow?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">
</p>

---

# 📌 Project Overview

This repository documents my complete learning journey of **Naive Bayes**, one of the simplest yet highly effective supervised Machine Learning algorithms used for **classification problems**.

Instead of only understanding the theoretical concepts, I implemented Naive Bayes on multiple datasets to gain practical experience in data preprocessing, feature encoding, model training, prediction, and evaluation.

During this journey, I explored different aspects of Naive Bayes including:

- Bayes' Theorem
- Conditional Probability
- Prior Probability
- Posterior Probability
- Likelihood
- Gaussian Naive Bayes
- Bernoulli Naive Bayes
- Multinomial Naive Bayes
- Feature Encoding
- Label Encoding
- One-Hot Encoding
- Classification Metrics
- Model Evaluation
- Prediction on New Data

This repository follows a hands-on learning approach, beginning with the mathematical intuition behind Bayes' Theorem and progressing toward real-world implementations using Scikit-Learn.

---

# 📂 Repository Structure

```

05_Naive_Bayes/
│
├── Naive_Bayes_Implementation.ipynb
├── assignment.ipynb
│
└── README.md

```

---

# 📖 Notebook Explanation

---

# 1️⃣ Naive_Bayes_Implementation.ipynb

## Objective

This notebook introduces the fundamentals of Naive Bayes and demonstrates how to build a complete Gaussian Naive Bayes classifier using the famous Iris Dataset.

---

## Topics Covered

- Introduction to Naive Bayes
- Bayes' Theorem
- Iris Dataset
- Feature Matrix (X)
- Target Variable (y)
- Train-Test Split
- Gaussian Naive Bayes
- Model Training
- Model Prediction
- Accuracy Score
- Confusion Matrix
- Classification Report

---

## Important Concepts Learned

### Understanding the Iris Dataset

The Iris Dataset is one of the most widely used datasets for classification problems.

It contains:

- 150 flower samples
- Four numerical features
- Three flower species

Features include:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

Target Classes:

- Setosa
- Versicolor
- Virginica

---

### Loading Dataset

Learned how to load datasets directly from Scikit-Learn.

```python
from sklearn.datasets import load_iris

X, y = load_iris(return_X_y=True)
```

Instead of manually downloading the dataset, Scikit-Learn provides built-in datasets for experimentation.

---

### Feature Matrix and Target Variable

Learned the standard notation used in Machine Learning.

```
X → Input Features

y → Target Variable
```

For the Iris Dataset:

```
X

Sepal Length
Sepal Width
Petal Length
Petal Width
```

```
y

Setosa
Versicolor
Virginica
```

---

### Train-Test Split

Learned why datasets are divided into

- Training Data
- Testing Data

using

```python
train_test_split()
```

Benefits:

- Prevents overfitting
- Measures generalization
- Simulates unseen real-world data

---

### Gaussian Naive Bayes

Implemented

```python
GaussianNB()
```

to classify Iris flowers.

The model estimates the probability of each class assuming that numerical features follow a Gaussian (Normal) distribution.

---

### Model Training

Trained the classifier using

```python
model.fit(X_train, y_train)
```

During training, the model learns

- Prior Probability
- Mean of each feature
- Variance of each feature

for every class.

---

### Model Prediction

Generated predictions on unseen samples using

```python
model.predict(X_test)
```

The trained classifier predicts the class having the highest posterior probability.

---

### Model Evaluation

Evaluated model performance using

- Accuracy Score
- Classification Report
- Confusion Matrix

to understand the strengths and weaknesses of the classifier.

---

# 2️⃣ assignment.ipynb

## Objective

This notebook demonstrates how Gaussian Naive Bayes can be applied to a real-world categorical dataset after performing the necessary preprocessing.

---

## Topics Covered

- Tips Dataset
- Feature Selection
- Label Encoding
- Gaussian Naive Bayes
- Training
- Prediction
- New Sample Prediction
- Inverse Label Transformation
- Accuracy Evaluation

---

## Important Concepts Learned

### Working with Real-World Data

Unlike the Iris dataset, this dataset contains both

- Numerical Features
- Categorical Features

Examples include:

```
total_bill

tip

sex

day

time

size
```

This required preprocessing before training.

---

### Feature Encoding

Learned why machine learning algorithms cannot directly process text values.

Examples

```
Male

Female

Lunch

Dinner

Sun

Sat
```

must first be converted into numerical representations.

Implemented

```python
LabelEncoder()
```

to transform categorical variables into numeric labels.

---

### Target Encoding

Converted

```
Yes

No
```

into

```
1

0
```

allowing the classifier to predict binary outcomes.

---

### Prediction on New Data

Created new observations manually and predicted whether the customer belongs to the target class.

Example workflow:

```python
model.predict(new_data)
```

This demonstrates how trained machine learning models are used in production.

---

### Inverse Transformation

After prediction, numerical labels were converted back into meaningful categories using

```python
inverse_transform()
```

This improves readability of predictions.

Example:

```
1

↓

Yes
```

```
0

↓

No
```

---

# 🔄 Complete Machine Learning Workflow

```
Dataset

↓

Feature Selection

↓

Train-Test Split

↓

Feature Encoding

↓

Gaussian Naive Bayes

↓

Model Training

↓

Prediction

↓

Accuracy Evaluation

↓

Prediction on New Data
```

---

# 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

# 📚 Machine Learning Concepts Learned

## Supervised Learning

✔ Classification

✔ Training

✔ Testing

✔ Prediction

---

## Probability Concepts

✔ Bayes' Theorem

✔ Prior Probability

✔ Posterior Probability

✔ Conditional Probability

✔ Likelihood

---

## Naive Bayes

✔ Gaussian Naive Bayes

✔ Bernoulli Naive Bayes

✔ Multinomial Naive Bayes

✔ Independence Assumption

✔ Probability Estimation

---

## Data Preparation

✔ Feature Selection

✔ Label Encoding

✔ One-Hot Encoding

✔ Train-Test Split

✔ Handling Categorical Features

---

## Model Evaluation

✔ Accuracy

✔ Confusion Matrix

✔ Classification Report

✔ Prediction

✔ Generalization

---

---

# 🧠 Understanding Naive Bayes

Naive Bayes is a **probabilistic supervised machine learning algorithm** used for solving classification problems.

Instead of learning complex mathematical relationships like Decision Trees or Support Vector Machines, Naive Bayes predicts the most probable class using **Bayes' Theorem**.

It is called **"Naive"** because it assumes that every feature contributes independently to the prediction, even though this assumption is rarely true in real-world datasets.

Despite this simple assumption, Naive Bayes performs exceptionally well on many real-world classification tasks.

---

# 📖 Bayes' Theorem

The entire Naive Bayes algorithm is based on Bayes' Theorem.

\[
P(A|B)=\frac{P(B|A)\times P(A)}{P(B)}
\]

Where,

| Symbol | Meaning |
|----------|------------|
| P(A) | Prior Probability |
| P(B) | Evidence |
| P(B|A) | Likelihood |
| P(A|B) | Posterior Probability |

In Machine Learning,

```
Posterior Probability

=

Likelihood

×

Prior Probability

÷

Evidence
```

The model predicts the class having the highest posterior probability.

---

# 🎯 Why is it called "Naive"?

Naive Bayes assumes

```
Feature 1

is independent of

Feature 2

Feature 3

Feature 4
```

For example,

Suppose we are predicting whether a customer is a smoker.

Features:

- Total Bill
- Tip
- Gender
- Day
- Time
- Size

Naive Bayes assumes that each feature contributes independently to the prediction.

Although this assumption is unrealistic, it greatly simplifies probability calculations and often produces excellent results.

---

# 📌 Types of Naive Bayes

There are three major variants of Naive Bayes.

---

# 1️⃣ Gaussian Naive Bayes

Gaussian Naive Bayes is used when input features are **continuous numerical values**.

Examples

- Height
- Weight
- Salary
- Temperature
- Petal Length
- Sepal Width

The algorithm assumes that every feature follows a **Normal (Gaussian) Distribution**.

Examples from this repository

✔ Iris Dataset

✔ Tips Dataset

Since numerical values such as

```
total_bill

tip

petal_length
```

are continuous,

Gaussian Naive Bayes becomes the most suitable choice.

Implemented using

```python
from sklearn.naive_bayes import GaussianNB

model = GaussianNB()
```

---

# 2️⃣ Bernoulli Naive Bayes

Bernoulli Naive Bayes is designed for **binary features**.

Possible values

```
0

1
```

Examples

```
Spam

Not Spam
```

```
Purchased

Not Purchased
```

```
Yes

No
```

```
True

False
```

This algorithm assumes every feature is binary.

Example

```
Contains Word "Free"

1

Contains Word "Money"

0
```

---

# 3️⃣ Multinomial Naive Bayes

Multinomial Naive Bayes is mainly used for **count data**.

Examples

- Word Frequency
- Document Classification
- News Classification
- Email Spam Detection

Sample Features

```
Free

Money

Offer

Lottery
```

Feature values

```
Free

5

Money

3

Offer

7
```

Instead of continuous values, the algorithm works on frequencies.

---

# 📊 Choosing the Right Naive Bayes Algorithm

| Feature Type | Recommended Algorithm |
|---------------|------------------------|
| Continuous Numerical Data | Gaussian Naive Bayes |
| Binary Features | Bernoulli Naive Bayes |
| Count Data | Multinomial Naive Bayes |

---

# 🔄 Why Gaussian Naive Bayes Was Used

In this repository, most datasets contain continuous numerical features.

Examples

```
Sepal Length

Petal Width

Tip

Total Bill

Size
```

Since these are continuous variables,

Gaussian Naive Bayes provides the best fit.

---

# 📈 Data Preprocessing

Machine Learning algorithms cannot understand text.

Example

```
Male

Female

Lunch

Dinner

Sunday

Saturday
```

These values must first be converted into numbers.

---

# 🔤 Label Encoding

Label Encoding converts categories into integer values.

Example

```
Male

↓

1

Female

↓

0
```

Another example

```
Yes

↓

1

No

↓

0
```

Implemented using

```python
from sklearn.preprocessing import LabelEncoder
```

---

# 🔠 One-Hot Encoding

One-Hot Encoding creates separate binary columns for each category.

Example

```
Day
```

Original

```
Sun

Sat

Fri
```

After Encoding

```
Sun Sat Fri

1   0   0

0   1   0

0   0   1
```

One-Hot Encoding prevents the model from assuming an artificial ordering between categories.

---

# 📊 Train-Test Split

The dataset is divided into

```
Training Dataset

↓

Model Learning

↓

Testing Dataset

↓

Performance Evaluation
```

Advantages

✔ Better Generalization

✔ Prevents Overfitting

✔ Fair Performance Measurement

---

# 🏋️ Model Training

Training is performed using

```python
model.fit(X_train, y_train)
```

During training,

the algorithm learns

- Prior Probability
- Mean
- Variance
- Class Probability

for every feature.

---

# 🔮 Prediction

After training,

new observations are classified using

```python
model.predict(X_test)
```

or

```python
model.predict(new_data)
```

The algorithm computes posterior probabilities for every class and predicts the class having the highest probability.

---

# 📉 Model Evaluation

The classifier was evaluated using

## Accuracy Score

Measures the percentage of correct predictions.

---

## Confusion Matrix

Provides

- True Positive
- True Negative
- False Positive
- False Negative

allowing detailed error analysis.

---

## Classification Report

Includes

✔ Precision

✔ Recall

✔ F1 Score

✔ Support

These metrics provide deeper insight than accuracy alone.

---

# 🎯 Prediction on New Data

One of the most important concepts explored in this repository is making predictions on unseen data.

Example workflow

```
User Input

↓

Preprocessing

↓

Feature Encoding

↓

Model Prediction

↓

Output Label

↓

Inverse Transformation
```

This simulates how trained machine learning models are deployed in real-world applications.

---

# 🔄 Inverse Label Transformation

Predictions are initially generated as numbers.

Example

```
1
```

Instead of displaying

```
1
```

we convert it back into

```
Yes
```

using

```python
inverse_transform()
```

making predictions more meaningful for end users.

---
---

# 🌍 Real-World Applications of Naive Bayes

Although Naive Bayes is one of the simplest machine learning algorithms, it is widely used in many real-world applications because of its speed, efficiency, and surprisingly strong performance.

## 📧 Spam Email Detection

One of the most common applications of Naive Bayes is spam filtering.

The algorithm analyzes words contained in emails and calculates the probability that an email belongs to either the **Spam** or **Not Spam** category.

---

## 😊 Sentiment Analysis

Companies use Naive Bayes to determine whether customer reviews are:

- Positive 😊
- Negative 😞
- Neutral 😐

Examples include:

- Amazon Reviews
- Flipkart Reviews
- Movie Reviews
- Restaurant Reviews

---

## 📰 News Article Classification

News articles can automatically be categorized into topics such as:

- Sports
- Politics
- Business
- Technology
- Entertainment

based on the words present in the article.

---

## 🏥 Medical Diagnosis

Naive Bayes assists doctors by predicting the probability of diseases based on symptoms, medical history, and laboratory results.

Examples:

- Diabetes Prediction
- Heart Disease Prediction
- Cancer Classification

---

## 💳 Fraud Detection

Banks use probabilistic models to identify suspicious transactions by analyzing customer spending behavior and transaction history.

---

## 🛒 Recommendation Systems

Naive Bayes can be used to estimate the probability that a customer will purchase a particular product based on previous behavior.

---

# ✅ Advantages of Naive Bayes

✔ Extremely simple to understand and implement.

✔ Very fast during both training and prediction.

✔ Performs well on small datasets.

✔ Works efficiently with high-dimensional data.

✔ Requires comparatively less training data.

✔ Handles multiclass classification naturally.

✔ Performs surprisingly well even with the independence assumption.

✔ Highly scalable.

✔ Suitable for real-time prediction systems.

✔ Excellent baseline model for classification tasks.

---

# ⚠️ Limitations of Naive Bayes

❌ Assumes all features are independent.

❌ Performance decreases when features are highly correlated.

❌ Gaussian Naive Bayes assumes normally distributed numerical features.

❌ Bernoulli Naive Bayes is limited to binary features.

❌ Multinomial Naive Bayes is mainly suitable for count data.

❌ Probability estimates may not always represent true probabilities.

---

# 📚 Detailed Learning Outcomes

Through this repository, I learned how to:

- Understand the intuition behind Bayes' Theorem.
- Differentiate between prior, likelihood, evidence, and posterior probability.
- Apply Gaussian Naive Bayes to continuous numerical datasets.
- Understand the purpose of Bernoulli and Multinomial Naive Bayes.
- Load datasets using Scikit-Learn.
- Prepare feature matrices (`X`) and target vectors (`y`).
- Split datasets into training and testing sets.
- Encode categorical features using Label Encoding.
- Understand when One-Hot Encoding is more appropriate.
- Train a Gaussian Naive Bayes classifier.
- Generate predictions on unseen data.
- Convert encoded predictions back to their original labels.
- Evaluate model performance using Accuracy Score.
- Interpret a Confusion Matrix.
- Analyze Precision, Recall, and F1-Score using a Classification Report.
- Build an end-to-end classification workflow.
- Recognize suitable real-world use cases for each Naive Bayes variant.
- Understand the strengths and limitations of probabilistic classifiers.
- Gain practical experience with Scikit-learn's Naive Bayes API.

---

# 🎯 Key Takeaways

✔ Naive Bayes is based on Bayes' Theorem.

✔ It is a supervised machine learning algorithm for classification.

✔ It predicts the class with the highest posterior probability.

✔ Gaussian Naive Bayes is ideal for continuous numerical data.

✔ Bernoulli Naive Bayes is suitable for binary features.

✔ Multinomial Naive Bayes is designed for count-based features.

✔ Proper preprocessing and feature encoding significantly improve model performance.

✔ Despite its "naive" assumption, the algorithm often performs remarkably well in practice.

---

# 🚀 Future Improvements

As I continue my Machine Learning journey, I plan to expand this repository by exploring:

- Feature Scaling
- Hyperparameter Tuning
- Cross Validation
- Pipeline Integration
- Probability Calibration
- Model Comparison with Logistic Regression, Decision Trees, and SVM
- Advanced Text Classification using Multinomial Naive Bayes
- Real-world NLP Projects

---

# 📈 Skills Gained

### Machine Learning

- Supervised Learning
- Classification
- Model Evaluation
- Prediction
- Probability-Based Learning

### Python Libraries

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

### Data Preprocessing

- Label Encoding
- One-Hot Encoding
- Train-Test Split
- Feature Selection

### Model Evaluation

- Accuracy Score
- Confusion Matrix
- Classification Report
- Prediction Analysis

---

# 📌 Repository Highlights

✔ Hands-on implementation of Naive Bayes.

✔ Clean and beginner-friendly Jupyter notebooks.

✔ Practical examples using both built-in and real-world datasets.

✔ Covers preprocessing, training, evaluation, and prediction.

✔ Demonstrates prediction on new unseen data.

✔ Explains the intuition behind Bayes' Theorem and different Naive Bayes variants.

---

# 🤝 Contributions

Contributions, suggestions, and improvements are always welcome.

If you find this repository helpful:

⭐ Star the repository

🍴 Fork the project

📢 Share it with others who are learning Machine Learning

---

# 📖 References

- Scikit-Learn Documentation
- Python Documentation
- Machine Learning by Tom M. Mitchell
- Pattern Recognition and Machine Learning by Christopher Bishop

---

# 🎓 Conclusion

This repository represents my practical learning journey with the **Naive Bayes algorithm**. Through these notebooks, I explored both the theoretical foundations and hands-on implementation of probabilistic classification using Scikit-learn.

Starting from Bayes' Theorem and probability concepts, I learned how to preprocess data, encode categorical features, train Gaussian Naive Bayes models, evaluate performance, and make predictions on unseen data. I also developed an understanding of when to use **Gaussian**, **Bernoulli**, and **Multinomial Naive Bayes** based on the nature of the input features.

This project has strengthened my understanding of supervised learning, classification techniques, and end-to-end machine learning workflows, serving as another milestone in my ongoing Machine Learning Journey.

---

<p align="center">

### ⭐ If you found this repository helpful, don't forget to give it a Star!

**Happy Learning! 🚀**

</p>

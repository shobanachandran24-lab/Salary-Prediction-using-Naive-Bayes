# 💼 Salary Prediction using Naive Bayes

A binary classification project that predicts whether an individual's annual
income is **<=50K** or **>50K** using the Adult Census Income dataset and a
Gaussian Naive Bayes classifier.

## 📌 Project Overview

The objective is to classify a person's salary into one of two classes based on
demographic and employment details such as age, education, occupation, marital
status and weekly working hours. The notebook covers data cleaning, encoding of
categorical variables, model training and evaluation.

## 🧠 About Naive Bayes

Naive Bayes is a probabilistic classification algorithm based on **Bayes' Theorem**:

P(Class | Features) = [ P(Features | Class) × P(Class) ] / P(Features)

- **P(Class | Features)** – probability of a class given the input features (posterior)
- **P(Features | Class)** – probability of the features given the class (likelihood)
- **P(Class)** – overall probability of the class (prior)
- **P(Features)** – probability of the features (evidence)

**Why "Naive"?**
The algorithm assumes that all features are independent of each other given the
class. This is rarely true in real data, but it makes the calculation simple and fast.

**Gaussian Naive Bayes**
This project uses `GaussianNB`, which assumes the values of each feature follow a
normal (Gaussian) distribution within each class. For every class it learns the
mean and variance of each feature, then predicts the class with the highest
posterior probability.

## 📂 Dataset

- **File:** `Salary.csv` (Salary / Census Income dataset)
- **Rows:** 32,560
- **Columns:** 15 (14 input features + 1 target)

| Column | Type | Description |
|--------|------|-------------|
| `age` | Numerical | Age of the person |
| `workclass` | Categorical | Employment type (Private, State-gov, Self-emp, etc.) |
| `fnlwgt` | Numerical | Census final weight |
| `education` | Categorical | Highest education level (Bachelors, HS-grad, Masters, etc.) |
| `education_num` | Numerical

# Iris Flower Classification using Support Vector Machines (SVM)

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange?style=for-the-badge&logo=scikit-learn)
![Machine Learning](https://img.shields.io/badge/ML-Classification-green?style=for-the-badge)

This repository features a machine learning implementation to classify species of the Iris flower. Using the **Iris dataset**, I developed a **Support Vector Machine (SVM)** classifier to accurately distinguish between three species: *Setosa*, *Versicolor*, and *Virginica*.

## 📌 Project Overview
* **Data Acquisition**: Loading the iris dataset via `sklearn.datasets`.
* **Visualization**: Plotting features to analyze class separation.
* **Model Training**: Utilizing the `SVC` (Support Vector Classifier) algorithm.
* **Evaluation**: Measuring accuracy and comparing predictions against actual test labels.

## 🧠 Mathematical Intuition

The goal of a Support Vector Machine is to find the **Optimal Hyperplane** in an $n$-dimensional space that distinctly classifies the data points.

### 1. The Decision Boundary
For binary classification, the prediction is determined by the linear function:
$$f(x) = w^T x + b$$
Where:
* $w$ is the weight vector (normal to the hyperplane).
* $b$ is the bias (offset from the origin).
* The decision rule is $\text{sign}(f(x))$, where $+1$ represents one class and $-1$ the other.

### 2. Maximizing the Margin
SVM finds the line that maximizes the **margin**—the distance between the hyperplane and the nearest data points, known as **Support Vectors**.



The distance from a point $x_i$ to the hyperplane is given by:
$$\frac{|w^T x_i + b|}{\|w\|}$$

To find the optimal margin, we minimize $\frac{1}{2}\|w\|^2$ subject to the constraint:
$$y_i(w^T x_i + b) \geq 1$$

### 3. The Kernel Trick
While the Iris dataset has some linear separability, SVMs can handle non-linear data by using a **Kernel function** (such as RBF or Polynomial) to map features into a higher-dimensional space where linear separation becomes possible.

## 🛠️ Technical Workflow
The `svm.ipynb` notebook follows these structured steps:
1. **Importing Libraries**: Using `numpy`, `pandas`, `matplotlib`, and `sklearn`.
2. **Data Preparation**: Splitting data into 80% training and 20% testing sets using `train_test_split`.
3. **Model Fitting**: Training the SVM model on the feature matrix ($X$) and target vector ($y$).
4. **Performance Metrics**: The model achieved an accuracy of approximately **96.67%** during testing.

## 📊 Results
The model effectively maps input features to their respective botanical classes:
* **Iris Setosa** (Class 0)
* **Iris Versicolor** (Class 1)
* **Iris Virginica** (Class 2)

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/Muhammad-Israr-baig/svm-iris.git](https://github.com/Muhammad-Israr-baig/svm-iris.git)

## Author: Israr Baig | Polymath | Machine Learning Enthusiast

---
title: "Coding Machine learning models from scratch"
excerpt: "This Jupyter Notebook provides a comprehensive implementation of machine learning algorithms from scratch using only NumPy and Pandas. It covers a wide range of algorithms, starting from basic regression models like Linear Regression to advanced techniques such as Gradient Descent, K-Means Clustering, Decision Trees, and Random Forests. The notebook emphasizes understanding the mathematical intuition behind each algorithm and coding them step-by-step without relying on external libraries like Sklearn"
collection: portfolio
---

🔗 **Notebook Link:** [Coding Machine learning models from scratch](https://www.kaggle.com/code/suvroo/ml-models-using-only-numpy-pandas-from-scratch)  


## Overview
This project is a detailed exploration of machine learning algorithms implemented entirely from scratch using **NumPy** and **Pandas**. It aims to provide a deeper understanding of the inner workings of these algorithms by focusing on their mathematical foundations and practical coding implementations. The notebook also includes preprocessing steps, dataset preparation, and evaluation metrics for each algorithm.


## Tech Stack
- **Python**: Core programming language for implementation.
- **NumPy**: For numerical computations.
- **Pandas**: For dataset manipulation and preprocessing.
- **Matplotlib & Seaborn**: For data visualization.
- **Sklearn (optional)**: For comparison with built-in implementations.



## Features

### Algorithms Implemented:
1. **Regression Models**:
   - Linear Regression
   - Ridge Regression (with Gradient Descent)
   - Multiple Linear Regression

2. **Optimization Techniques**:
   - Gradient Descent (Batch, Stochastic, Mini-Batch)
   - Perceptron Learning Algorithm

3. **Clustering Algorithms**:
   - K-Means Clustering

4. **Tree-Based Models**:
   - Decision Tree Classifier
   - Random Forest Classifier

5. **Evaluation Metrics**:
   - R² Score
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)

## Workflow

### 1. Dataset Preparation
- Titanic dataset is used for classification tasks.
- College placement dataset is used for regression tasks.
- Custom datasets are generated for clustering and optimization demonstrations.

### 2. Algorithm Implementation
- Each algorithm is implemented step-by-step using mathematical formulas.
- Includes custom classes and methods for training and prediction.

### 3. Visualization
- Loss curves for optimization techniques.
- Decision boundaries for classification models.
- Cluster assignments for K-Means.

### 4. Evaluation
- Metrics like R² Score, MAE, MSE are computed to assess model performance.
- Comparison with Scikit-learn implementations for validation.


### Linear Regression Example:
```python
class LinR:
    def fit(self, X_train, y_train):
        # Compute slope and intercept using least squares method
        self.m = np.cov(X_train, y_train)[0][1] / np.var(X_train)
        self.b = y_train.mean() - self.m * X_train.mean()

    def predict(self, X_test):
        return self.m * X_test + self.b

lr = LinR()
lr.fit(X_train, y_train)
y_pred = lr.predict(X_test)
```

### Gradient Descent Example:
```python
class GDRegressor:
    def fit(self, X, y):
        # Initialize parameters
        self.m = np.random.randn()
        self.b = np.random.randn()
        for _ in range(self.epochs):
            # Update parameters using gradient descent formula
            self.m -= self.lr * (-2 * np.sum((y - (self.m * X + self.b)) * X))
            self.b -= self.lr * (-2 * np.sum(y - (self.m * X + self.b)))
```

### K-Means Clustering Example:
```python
class KMeans:
    def fit_predict(self, X):
        # Randomly initialize centroids
        self.centroids = X[np.random.choice(X.shape[0], self.n_clusters)]
        # Iteratively assign clusters and update centroids
        for _ in range(self.max_iter):
            cluster_labels = [np.argmin([np.linalg.norm(x-c) for c in self.centroids]) for x in X]
            self.centroids = [X[np.array(cluster_labels) == i].mean(axis=0) for i in range(self.n_clusters)]
```



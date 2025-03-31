---
title: "Coding Deep learning optimizers from scratch"
excerpt: "This project provides a comprehensive exploration of optimization algorithms used in deep learning, focusing on their implementation both from scratch and using Keras. It covers popular optimizers such as Gradient Descent, Momentum, Adam, RMSProp, and others, explaining their mathematical foundations, challenges, and practical applications. The notebook also demonstrates how these optimizers adjust model parameters to minimize loss functions, using examples with synthetic data and neural networks."
collection: portfolio
---

🔗 **Notebook Link:** [Coding Deep learning optimizers from scratch](https://www.kaggle.com/code/suvroo/all-dl-optimizers-both-from-scratch-and-keras)  



## Overview
This project explores the **optimization algorithms** that are critical for training deep learning models. It includes:
1. Mathematical intuition behind each optimizer.
2. Implementation of optimizers from scratch.
3. Practical usage with TensorFlow/Keras on real-world datasets.
4. Visualization of optimization processes and loss convergence.

## Tech Stack
- **Python**: Core programming language for implementation.
- **NumPy**: For numerical computations in custom implementations.
- **TensorFlow/Keras**: For building and training neural networks.
- **Matplotlib & Seaborn**: For data visualization and analysis.

## Features
1. **Optimizer Concepts**:
   - Explains key concepts like gradient descent, learning rate scheduling, momentum, and adaptive learning rates.
   - Discusses challenges like saddle points, local minima, and the importance of learning rate tuning.

2. **Optimizers Implemented**:
   - **Gradient Descent (Batch, Stochastic, Mini-batch)**.
   - **Momentum-based Optimizers (e.g., NAG)**.
   - **Adaptive Optimizers (Adagrad, RMSProp, Adam)**.

3. **Implementation from Scratch**:
   - Custom Python implementations of all optimizers for a simple linear regression problem.

4. **Keras-Based Neural Network Training**:
   - Demonstrates the use of optimizers with Keras on datasets like the Diabetes dataset.
   - Builds multi-layer perceptrons (MLPs) with different activation functions.

5. **Visualization**:
   - Plots loss curves for different optimizers to compare their convergence rates.
   - Visualizes exponentially weighted moving averages (EWMA) for momentum-based optimizers.

## Workflow

### 1. Mathematical Intuition
- Provides detailed explanations of each optimizer's formula and working mechanism.
- Example: Exponentially Weighted Moving Average (EWMA) is explained with visualizations.

### 2. Implementation from Scratch
- Implements each optimizer step-by-step using NumPy.
- Demonstrates optimization on a simple linear regression model.

### 3. Neural Network Training with Keras
- Builds a feedforward neural network to classify the Diabetes dataset.
- Trains the model using different optimizers like SGD, Adam, RMSProp, etc.














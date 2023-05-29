---
description: This note provides an overview of the multivariate normal distribution, including mean and variance, statistical independence, and conditional probability, as well as an introduction to Model Predictive Control (MPC), a popular control scheme used in various applications. The note also covers the main results required to derive the optimal estimator for MPC, including joint independent normals and linear transformation of a normal.
---
# Multivariate Normal Distribution and Model Predictive Control - An Overview

## Multivariate Normal Distribution

### Introduction
This section discusses the multivariate normal distribution, mean and variance, statistical independence, and conditional probability. It is assumed that readers are familiar with the terms used in this section.

### Notation
- Let X, y, and z be vectors of random variables.
- x ~ N(m, P) denotes that random variable x is normally distributed with mean m and covariance P.
- Px(x) = n(x, m, P) denotes the probability density of x.

### Joint Independent Normals
- If x and y are normally distributed and statistically independent, then their joint density is given by Px,y(x, y) = n(x, mx, Px) n(y, my, Py).

### Linear Transformation of a Normal
- If x is normally distributed with mean m and variance P, and y is a linear transformation of x, y = Ax, then y is distributed with mean Am and variance APA'.
- x ~ N(m, P) and y = Ax, then y ~ N(Am, APA').

## Model Predictive Control - An Overview

### Introduction
Model Predictive Control (MPC) is a popular control scheme used in various applications. It involves predicting the future behavior of a system and optimizing a control action based on a cost function. 

### Optimal Estimator
To derive the optimal estimator, we require the following main results conditioned on additional random variables:

- Joint independent normals
- Linear transformation of a normal

### Joint Independent Normals
If pxlz(x|z) is normal, and y is statistically independent of x and z and normally distributed, then the conditional joint density of (x, y) given z is:

Pxylz(x, y|z) = n(x, mx, Px) n(y, my, Py)

### Linear Transformation of a Normal
If Pxiz(x|z) = n(x, m, P) and y = Ax, then Pyiz(y|z) = n(y, Am, APA').
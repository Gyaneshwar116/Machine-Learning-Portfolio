# Linear Regression: Mathematical Foundations and Implementation

## Introduction

Linear Regression is a supervised learning algorithm used to model the relationship between a dependent variable and one or more independent variables.

The primary objective is to learn a function that maps input features to a continuous target variable while minimizing prediction error.

Despite being one of the oldest machine learning algorithms, Linear Regression remains a fundamental building block for understanding more advanced models and statistical learning techniques.

---

## Problem Statement

Given a dataset:

D = {(x₁,y₁),(x₂,y₂),...,(xₙ,yₙ)}

Our goal is to find a function:

f(x) = β₀ + β₁x

that best approximates the underlying relationship between features and target values.

---

## Geometric Interpretation

Linear Regression attempts to fit a hyperplane in feature space.

### Single Feature

A straight line:

y = β₀ + β₁x

### Multiple Features

A hyperplane:

y = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ

The model seeks the hyperplane that minimizes the total prediction error across all observations.

---

## Model Parameters

### Intercept (β₀)

Represents the predicted output when all features equal zero.

### Coefficients (β)

Measure the expected change in the target variable for a one-unit increase in the feature while holding all other features constant.

---

## Prediction Function

For each observation:

ŷ = β₁X+β₀

where:

- X = Feature Matrix
- β₁= Coefficient Vector
- ŷ = Predicted Values
- β₀= Intercept

---

## Residuals

The difference between actual and predicted values is called the residual.

eᵢ = yᵢ - ŷᵢ

Residual analysis provides insight into model assumptions and predictive performance.

A good model should produce residuals that appear random rather than exhibiting systematic patterns.

---

## Cost Function

The model learns by minimizing the Residual Sum of Squares (RSS).

RSS = Σᵢ₌₁ⁿ(yᵢ - ŷᵢ)²

Squaring the residuals serves two purposes:

1. Removes sign differences.
2. Penalizes large errors more heavily.

---

## Ordinary Least Squares (OLS)

Linear Regression typically uses the Ordinary Least Squares estimator.

The optimization objective is:

min β Σᵢ₌₁ⁿ(yᵢ - ŷᵢ)²

The analytical solution is:

β = (XᵀX)⁻¹Xᵀy

This closed-form solution directly computes the optimal coefficient vector.

Scikit-Learn's LinearRegression() is based on least-squares optimization.

---

## Assumptions of Linear Regression

### 1. Linearity

Features and target should have a linear relationship.

### 2. Independence of Errors

Residuals should not be correlated.

### 3. Homoscedasticity

Error variance should remain constant across predictions.

### 4. Normality of Residuals

Residuals should approximately follow a normal distribution.

### 5. No Multicollinearity

Independent variables should not be highly correlated.

Violation of these assumptions can reduce model reliability and interpretability.

---

## Bias-Variance Perspective

Linear Regression is considered a relatively low-variance and high-bias model.

Characteristics include:

- Stable predictions
- Fast training
- Strong interpretability
- Limited ability to capture non-linear relationships

This makes it an excellent baseline model for many machine learning tasks.

---

## Evaluation Metrics

### Mean Absolute Error (MAE)

MAE = (1/n) Σ|y - ŷ|

Measures average prediction error.

### Mean Squared Error (MSE)

MSE = (1/n) Σ(y - ŷ)²

Penalizes large errors more strongly.

### Root Mean Squared Error (RMSE)

RMSE = √MSE

Provides error in the original unit of the target variable.

### R² Score

R² = 1 - SSR/SST

Measures the proportion of variance explained by the model.

Interpretation:

- R² = 1 → Perfect Fit
- R² = 0 → No Explained Variance

---

## Limitations

Linear Regression struggles when:

- Relationships are non-linear
- Strong outliers exist
- Multicollinearity is present
- Feature interactions are complex

In such situations, more sophisticated models such as Decision Trees, Random Forests, Gradient Boosting, or Neural Networks may be more appropriate.

---

## Why Linear Regression Still Matters

Linear Regression serves as the foundation for understanding:

- Regularized Regression (Ridge, Lasso, Elastic Net)
- Generalized Linear Models
- Statistical Inference
- Feature Importance Analysis
- Model Interpretability

Many advanced machine learning algorithms build upon concepts introduced by Linear Regression.

---

## Key Takeaway

Linear Regression is not merely a line-fitting technique but a statistical optimization framework that estimates the relationship between variables by minimizing squared prediction errors. Understanding its mathematical foundations, assumptions, and limitations provides the basis for mastering more advanced machine learning algorithms.

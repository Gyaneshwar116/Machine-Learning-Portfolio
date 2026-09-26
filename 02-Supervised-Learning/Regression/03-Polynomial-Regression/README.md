# Polynomial Regression: Modeling Non-Linear Relationships

## Introduction

Polynomial Regression is an extension of Linear Regression that enables the model to capture non-linear relationships between features and the target variable.

While Linear Regression assumes a straight-line relationship, Polynomial Regression introduces higher-order terms that allow the model to fit curved patterns present in the data.

Despite its name, Polynomial Regression is still considered a linear model because it remains linear with respect to its coefficients.

---

## Why Polynomial Regression?

Linear Regression works well when the relationship between variables is approximately linear.

However, many real-world datasets contain curved relationships.

Examples:

- Experience vs Salary Growth
- Temperature vs Electricity Consumption
- Age vs Healthcare Cost
- Advertising Spend vs Revenue

In these situations, a straight line may underfit the data, while Polynomial Regression can better represent the underlying pattern.

---

## Prediction Function

### Linear Regression

ŷ = β₀ + β₁x

### Polynomial Regression

ŷ = β₀ + β₁x + β₂x² + β₃x³ + ⋯ + βₙxⁿ

where:

- ŷ = Predicted value
- β₀ = Intercept
- βₙ = Learned coefficients
- xⁿ = Polynomial feature

The additional polynomial terms allow the model to learn curved relationships.

---

## How the Algorithm Works

The algorithm first creates polynomial features from the original input variable.

Example:

Given:

X = [2]

Degree = 3

The transformed features become:

[2, 2², 2³]

[2, 4, 8]

The Linear Regression model is then trained on these transformed features.

Thus, Polynomial Regression is essentially:

> Polynomial Feature Engineering + Linear Regression

---

## Cost Function

Like Linear Regression, Polynomial Regression minimizes the Residual Sum of Squares (RSS).

RSS = Σ(yᵢ - ŷᵢ)²

The objective is to find coefficient values that produce the smallest overall prediction error.

---

## Model Complexity

The degree of the polynomial controls model complexity.

### Degree 1

Linear relationship

y = β₀ + β₁x

### Degree 2

Quadratic relationship

y = β₀ + β₁x + β₂x²

### Degree 3

Cubic relationship

y = β₀ + β₁x + β₂x² + β₃x³

Higher degrees increase flexibility but also increase the risk of overfitting.

---

## Bias-Variance Tradeoff

### Low Degree

- High Bias
- Low Variance
- Underfitting Risk

### High Degree

- Low Bias
- High Variance
- Overfitting Risk

Choosing an appropriate polynomial degree is critical for achieving good generalization performance.

---

## Evaluation Metrics

Model performance can be evaluated using:

### R² Score

Measures explained variance.

R² = 1 - RSS/TSS

### MAE

Measures average prediction error.

### RMSE

Measures prediction error in the original target unit.

Lower MAE and RMSE values indicate better predictive accuracy.

---

## Advantages

- Captures non-linear relationships
- More flexible than Linear Regression
- Easy to implement and interpret
- Useful when data exhibits curvature

---

## Limitations

- Sensitive to outliers
- Can overfit with high polynomial degrees
- Poor extrapolation outside training range
- Increased model complexity

---

## Key Takeaway

Polynomial Regression extends Linear Regression by introducing higher-order feature terms, allowing the model to learn non-linear relationships while still using linear optimization techniques.

Selecting an appropriate polynomial degree is essential to balance model flexibility and generalization.


# Simple Linear Regression: Computing Coefficients Using RSS

This guide explains how the coefficients `b₀` (intercept) and `b₁` (slope) in simple linear regression are computed by minimizing the **Residual Sum of Squares (RSS)**.

---

## 📘 Objective

In simple linear regression, we aim to model the relationship between a predictor variable `X` and a response variable `Y` using a straight line:

```
Ŷᵢ = b₀ + b₁Xᵢ
```

Where:
- `Ŷᵢ`: Predicted value of `Y`
- `b₀`: Intercept (value of `Y` when `X = 0`)
- `b₁`: Slope (change in `Y` per unit change in `X`)

---

## 🎯 Minimizing the Residual Sum of Squares (RSS)

To find the best-fit line, we minimize the **Residual Sum of Squares**:

```
RSS = Σ(Yᵢ - Ŷᵢ)² = Σ(Yᵢ - b₀ - b₁Xᵢ)²
```

RSS measures the total squared distance between the observed and predicted values.

---

## 🧠 Deriving the Coefficients

We minimize RSS by taking partial derivatives with respect to `b₀` and `b₁`, and setting them to zero.

### 🔹 Step 1: Compute the Slope `b₁`

```
b₁ = Σ((Xᵢ - X̄)(Yᵢ - Ȳ)) / Σ((Xᵢ - X̄)²)
```

This is the **slope** of the regression line. It reflects how much `Y` changes for a one-unit increase in `X`.

---

### 🔹 Step 2: Compute the Intercept `b₀`

Once `b₁` is known, calculate the **intercept**:

```
b₀ = Ȳ - b₁X̄
```

This ensures the regression line passes through the point `(X̄, Ȳ)`, the mean of the data.

---

## 🔁 Summary of Final Formulas

- **Slope (b₁):**
```
b₁ = Σ((Xᵢ - X̄)(Yᵢ - Ȳ)) / Σ((Xᵢ - X̄)²)
```

- **Intercept (b₀):**
```
b₀ = Ȳ - b₁X̄
```

---

## 🔢 Example

Given:
- `X = [1, 2, 3]`
- `Y = [2, 4, 5]`

Steps:
1. Compute means: `X̄ = 2`, `Ȳ ≈ 3.67`
2. Calculate `b₁` using the slope formula.
3. Use `b₀ = Ȳ - b₁X̄` to get the intercept.

---

## ✅ Notes

- This approach assumes a linear relationship between `X` and `Y`.
- The goal is to minimize prediction error by finding the best-fit line using least squares.
- These formulas are the foundation for more advanced regression techniques.



## 📘 Standard Errors in Simple Linear Regression

This document explains how to compute and interpret the **standard errors** of the regression coefficients in simple linear regression.

---

### 🔢 Equation

\[
\text{SE}(\hat{\beta}_0)^2 = \sigma^2 \left( \frac{1}{n} + \frac{\bar{x}^2}{\sum_{i=1}^n (x_i - \bar{x})^2} \right), \quad
\text{SE}(\hat{\beta}_1)^2 = \frac{\sigma^2}{\sum_{i=1}^n (x_i - \bar{x})^2}
\]

- \(\hat{\beta}_0\): Estimated **intercept**
- \(\hat{\beta}_1\): Estimated **slope**
- \(\bar{x}\): Mean of the predictor variable \(x\)
- \(\sigma^2\): **Error variance**, estimated from residuals
- \(n\): Number of observations

---

### 📘 What Do These Formulas Represent?

These equations give the **variances** of the least squares estimates of the slope and intercept. The **standard errors** (SE) are the square roots of these variances:

- \(\text{SE}(\hat{\beta}_0)\): measures uncertainty in the **intercept**
- \(\text{SE}(\hat{\beta}_1)\): measures uncertainty in the **slope**

---

### 🧠 Intuition Behind the Components

#### SE(\(\hat{\beta}_1\)) – Slope

\[
\text{SE}(\hat{\beta}_1)^2 = \frac{\sigma^2}{\sum (x_i - \bar{x})^2}
\]

- **Numerator**: \(\sigma^2\) = noise in the outcome variable \(y\)
- **Denominator**: variability in predictor \(x\)
- More spread in \(x\) → more reliable slope estimate → smaller SE

---

#### SE(\(\hat{\beta}_0\)) – Intercept

\[
\text{SE}(\hat{\beta}_0)^2 = \sigma^2 \left( \frac{1}{n} + \frac{\bar{x}^2}{\sum (x_i - \bar{x})^2} \right)
\]

- **Includes two parts**:
  - \(1/n\): uncertainty from sample size
  - \(\bar{x}^2 / \sum (x_i - \bar{x})^2\): increases if \(\bar{x}\) is far from 0
- If \(\bar{x}\) is far from 0 or \(x\) is not spread out → intercept becomes less reliable

---

### 📈 Interpretation Summary

| Term | Meaning | Grows When... |
|------|---------|----------------|
| \(\sigma^2\) | Variance of error terms | Data is noisy (high residuals) |
| \(\sum (x_i - \bar{x})^2\) | Spread of x-values | x-values are concentrated |
| \(\text{SE}(\hat{\beta}_1)\) | Slope uncertainty | x is not spread out or y is noisy |
| \(\text{SE}(\hat{\beta}_0)\) | Intercept uncertainty | \(\bar{x}\) is far from 0 or x is not spread |

---

### 🧮 Estimating \(\sigma^2\)

\[
\hat{\sigma}^2 = \frac{RSS}{n - 2}, \quad \text{where } RSS = \sum (y_i - \hat{y}_i)^2
\]

- RSS: Residual Sum of Squares (total squared error)
- \(n - 2\): Degrees of freedom (2 parameters: slope + intercept)

---

### ✅ TL;DR

- Standard errors help quantify how **reliable** your regression estimates are.
- More data, more spread in \(x\), and less noise in \(y\) → smaller standard errors.
- These are essential for computing **confidence intervals** and **hypothesis tests** in regression.

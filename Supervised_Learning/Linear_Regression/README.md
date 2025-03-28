
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

```
SE(β₀)^2 = σ² * [1/n + (x̄² / Σ(xᵢ - x̄)²)]
SE(β₁)^2 = σ² / Σ(xᵢ - x̄)²
```

- `β₀`: Estimated **intercept**
- `β₁`: Estimated **slope**
- `x̄`: Mean of the predictor variable `x`
- `σ²`: **Error variance**, estimated from residuals
- `n`: Number of observations

---

### 📘 What Do These Formulas Represent?

These equations give the **variances** of the least squares estimates of the slope and intercept. The **standard errors** (SE) are the square roots of these variances:

- `SE(β₀)`: measures uncertainty in the **intercept**
- `SE(β₁)`: measures uncertainty in the **slope**

---

### 🧠 Intuition Behind the Components

#### SE(β₁) – Slope

```
SE(β₁)^2 = σ² / Σ(xᵢ - x̄)²
```

- **Numerator**: `σ²` = noise in the outcome variable `y`
- **Denominator**: variability in predictor `x`
- More spread in `x` → more reliable slope estimate → smaller SE

---

#### SE(β₀) – Intercept

```
SE(β₀)^2 = σ² * [1/n + (x̄² / Σ(xᵢ - x̄)²)]
```

- **Includes two parts**:
  - `1/n`: uncertainty from sample size
  - `x̄² / Σ(xᵢ - x̄)²`: increases if `x̄` is far from 0
- If `x̄` is far from 0 or `x` is not spread out → intercept becomes less reliable

---

### 📈 Interpretation Summary

| Term                | Meaning                    | Grows When...                         |
|---------------------|----------------------------|----------------------------------------|
| `σ²`               | Variance of error terms    | Data is noisy (high residuals)         |
| `Σ(xᵢ - x̄)²`       | Spread of x-values         | x-values are concentrated              |
| `SE(β₁)`           | Slope uncertainty          | x is not spread out or y is noisy      |
| `SE(β₀)`           | Intercept uncertainty      | `x̄` is far from 0 or x is not spread  |

---

### 🧮 Estimating σ²

```
σ̂² = RSS / (n - 2), where RSS = Σ(yᵢ - ŷᵢ)²
```

- RSS: Residual Sum of Squares (total squared error)
- `n - 2`: Degrees of freedom (2 parameters: slope + intercept)

---

### ✅ TL;DR

- Standard errors help quantify how **reliable** your regression estimates are.
- More data, more spread in `x`, and less noise in `y` → smaller standard errors.
- These are essential for computing **confidence intervals** and **hypothesis tests** in regression.


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

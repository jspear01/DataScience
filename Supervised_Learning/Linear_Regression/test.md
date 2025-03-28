
# Simple Linear Regression: Computing Coefficients Using RSS

This guide explains how the coefficients \( b_0 \) (intercept) and \( b_1 \) (slope) in simple linear regression are computed by minimizing the **Residual Sum of Squares (RSS)**.

---

## 📘 Objective

In simple linear regression, we aim to model the relationship between a predictor variable \( X \) and a response variable \( Y \) using a straight line:

\[ \hat{Y}_i = b_0 + b_1 X_i \]

Where:
- \( \hat{Y}_i \): Predicted value of \( Y \)
- \( b_0 \): Intercept (value of \( Y \) when \( X = 0 \))
- \( b_1 \): Slope (change in \( Y \) per unit change in \( X \))

---

## 🎯 Minimizing the Residual Sum of Squares (RSS)

To find the best-fit line, we minimize the **Residual Sum of Squares**:

\[
RSS = \sum_{i=1}^n (Y_i - \hat{Y}_i)^2 = \sum_{i=1}^n (Y_i - b_0 - b_1 X_i)^2
\]

RSS measures the total squared distance between the observed and predicted values.

---

## 🧠 Deriving the Coefficients

We minimize RSS by taking partial derivatives with respect to \( b_0 \) and \( b_1 \), and setting them to zero.

### 🔹 Step 1: Compute the Slope \( b_1 \)

\[
b_1 = \frac{\sum (X_i - \bar{X})(Y_i - \bar{Y})}{\sum (X_i - \bar{X})^2}
\]

This is the **slope** of the regression line. It reflects how much \( Y \) changes for a one-unit increase in \( X \).

---

### 🔹 Step 2: Compute the Intercept \( b_0 \)

Once \( b_1 \) is known, calculate the **intercept**:

\[
b_0 = \bar{Y} - b_1 \bar{X}
\]

This ensures the regression line passes through the point \( (\bar{X}, \bar{Y}) \), the mean of the data.

---

## 🔁 Summary of Final Formulas

- **Slope (b₁):**
  \[
  b_1 = \frac{\sum (X_i - \bar{X})(Y_i - \bar{Y})}{\sum (X_i - \bar{X})^2}
  \]

- **Intercept (b₀):**
  \[
  b_0 = \bar{Y} - b_1 \bar{X}
  \]

---

## 🔢 Example

Given:
- \( X = [1, 2, 3] \)
- \( Y = [2, 4, 5] \)

Steps:
1. Compute means: \( \bar{X} = 2 \), \( \bar{Y} \approx 3.67 \)
2. Calculate \( b_1 \) using the slope formula
3. Use \( b_0 = \bar{Y} - b_1 \bar{X} \) to get the intercept

---

## ✅ Notes

- This approach assumes a linear relationship between \( X \) and \( Y \).
- The goal is to minimize prediction error by finding the best-fit line using least squares.
- These formulas are the foundation for more advanced regression techniques.

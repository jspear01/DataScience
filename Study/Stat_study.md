# Probability Concepts

## Conditional Probability

We are often interested in knowing the probability of an event **A** occurring, given that another event **B** has already occurred. This is known as the **conditional probability** of **A given B**, and it can be calculated using **Bayes' Rule**:



$$
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}
$$

### Bayes' Rule Components

- **P(A)**: The **prior** — the initial probability of event A.
- **P(B|A)**: The **likelihood** — the probability of observing B given that A occurred.
- **P(A|B)**: The **posterior** — the updated probability of A given that B occurred.

### Independence

If the conditional probability **P(A|B)** equals the prior **P(A)**, then **A** and **B** are said to be **independent**. In this case, knowledge of **B** does not affect our belief about the occurrence of **A**:

$$
P(A|B) = P(A) \Rightarrow A \perp B
$$

### Conditional Independence

Two events **A** and **B** can also be **conditionally independent** given a third event **C**. This means that once **C** has occurred, **A** and **B** do not provide additional information about each other:

$$
P(A \cap B | C) = P(A|C) \cdot P(B|C)
$$

In other words, given that **C** occurred, the joint probability of **A** and **B** factorizes into the product of their individual conditional probabilities.


# 🧠 Bayes' Theorem Examples

Bayes’ Theorem allows us to update our beliefs based on new evidence. It is defined as:

```latex
P(A | B) = \frac{P(B | A) \cdot P(A)}{P(B)}
```

Where:
- **P(A | B)** is the posterior (updated probability of A given B)
- **P(B | A)** is the likelihood
- **P(A)** is the prior (initial belief)
- **P(B)** is the marginal probability of B

---

## 🏥 Example 1: Medical Diagnosis

A disease affects 1% of a population. A diagnostic test correctly identifies the disease 99% of the time (**true positive**), but also has a 5% **false positive** rate.

**Question:** What is the probability a person has the disease if they test positive?

### 📊 Given:
- P(Disease) = 0.01  
- P(No Disease) = 0.99  
- P(Positive | Disease) = 0.99  
- P(Positive | No Disease) = 0.05  

### 🧮 Solution

We want to compute:

```latex
P(Disease | Positive) = \frac{P(Positive | Disease) \cdot P(Disease)}{P(Positive)}
```

First, compute the total probability of testing positive:

```latex
P(Positive) = P(Positive | Disease) \cdot P(Disease) + P(Positive | No Disease) \cdot P(No Disease)
```

Plug in the values:

```latex
P(Positive) = 0.99 \cdot 0.01 + 0.05 \cdot 0.99 = 0.0099 + 0.0495 = 0.0594
```

Now calculate the final result:

```latex
P(Disease | Positive) = \frac{0.0099}{0.0594} \approx 0.1667
```

### 📌 Interpretation:

Even with a positive test, there's only about a **16.67% chance** the person actually has the disease. This is due to the low base rate (prior probability) of the disease.

---

## 🎓 Example 2: Student Cheating Detection

A proctor believes 2% of students cheat. A detection algorithm correctly flags cheating behavior 90% of the time, but falsely flags honest students 10% of the time.

**Question:** If a student is flagged, what’s the probability they actually cheated?

### 📊 Given:
- P(Cheat) = 0.02  
- P(No Cheat) = 0.98  
- P(Flagged | Cheat) = 0.90  
- P(Flagged | No Cheat) =



## Permutations and Combinations

This guide explains the difference between **permutations** and **combinations** — essential concepts in combinatorics used for counting and arranging items.

---

### Permutation: *Order Matters*

A **permutation** is an arrangement of objects **in a specific order**.

**Formula:**

$$
P(n, r) = \frac{n!}{(n - r)!}
$$



- `n` = total number of distinct items  
- `r` = number of items to arrange  
- `!` = factorial (e.g., `5! = 5 × 4 × 3 × 2 × 1 = 120`)

**Example:**
How many ways can you arrange 3 letters from the word **"ABCDE"**?

- `n = 5` (letters)  
- `r = 3` (we choose 3 of them in order)

```
P(5, 3) = 5! / (5 - 3)! = 120 / 2 = 60
```

✅ There are **60** different arrangements.

---

#### ➕ Combination: *Order Doesn’t Matter*

A **combination** is a selection of objects **without considering order**.

**Formula:**
```
C(n, r) = n! / [r! × (n - r)!]
```

- `n` = total number of distinct items  
- `r` = number of items to choose

**Example:**
How many ways can you **choose** 3 letters from the word **"ABCDE"** (order doesn't matter)?

- `n = 5`  
- `r = 3`

```
C(5, 3) = 5! / (3! × (5 - 3)!) = 120 / (6 × 2) = 10
```

✅ There are **10** unique combinations.

---

#### Quick Summary

| Concept      | Key Idea            | Formula                     | When to Use                                      |
|--------------|---------------------|-----------------------------|--------------------------------------------------|
| Permutation  | Order **matters**   | `P(n, r) = n! / (n - r)!`   | Arranging people in a line, password generation |
| Combination  | Order **doesn't**   | `C(n, r) = n! / [r!(n−r)!]` | Picking lottery numbers, choosing a team        |

---

**Real-Life Examples**

### Permutations
- **Seating arrangements** for 3 friends on 5 chairs
- **Lock codes** where digit order matters (e.g., `123` ≠ `321`)

### Combinations
- Choosing 3 toppings for a pizza from a list of 10
- Selecting a committee from a group of people

---

## Quick Tip to Remember

- **Permutation** = **Position matters** (like arranging people in a line).
- **Combination** = **Chill with order** (like selecting lottery numbers).

---


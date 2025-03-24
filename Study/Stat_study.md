
# Permutations and Combinations

This guide explains the difference between **permutations** and **combinations** — essential concepts in combinatorics used for counting and arranging items.

---

## Permutation: *Order Matters*

A **permutation** is an arrangement of objects **in a specific order**.

### Formula:
```
P(n, r) = n! / (n - r)!
```

- `n` = total number of distinct items  
- `r` = number of items to arrange  
- `!` = factorial (e.g., `5! = 5 × 4 × 3 × 2 × 1 = 120`)

### Example:
How many ways can you arrange 3 letters from the word **"ABCDE"**?

- `n = 5` (letters)  
- `r = 3` (we choose 3 of them in order)

```
P(5, 3) = 5! / (5 - 3)! = 120 / 2 = 60
```

✅ There are **60** different arrangements.

---

## ➕ Combination: *Order Doesn’t Matter*

A **combination** is a selection of objects **without considering order**.

### Formula:
```
C(n, r) = n! / [r! × (n - r)!]
```

- `n` = total number of distinct items  
- `r` = number of items to choose

### Example:
How many ways can you **choose** 3 letters from the word **"ABCDE"** (order doesn't matter)?

- `n = 5`  
- `r = 3`

```
C(5, 3) = 5! / (3! × (5 - 3)!) = 120 / (6 × 2) = 10
```

✅ There are **10** unique combinations.

---

## Quick Summary

| Concept      | Key Idea            | Formula                     | When to Use                                      |
|--------------|---------------------|-----------------------------|--------------------------------------------------|
| Permutation  | Order **matters**   | `P(n, r) = n! / (n - r)!`   | Arranging people in a line, password generation |
| Combination  | Order **doesn't**   | `C(n, r) = n! / [r!(n−r)!]` | Picking lottery numbers, choosing a team        |

---

## Real-Life Examples

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


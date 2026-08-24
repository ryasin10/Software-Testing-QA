# 📊 Equivalence Partitioning & Boundary Value Analysis

## Overview
**Equivalence Partitioning (EP)** and **Boundary Value Analysis (BVA)** are fundamental Black-Box test design techniques used to select optimal input data sets and minimize total test cases.

---

## 1. Equivalence Partitioning (EP)
EP divides the input domain into valid and invalid partitions (groups). It operates on the premise that if one condition in a partition works, all other conditions in that same partition will behave identically.

### Example: Age Field (Valid: 18 - 60)
* **Partition 1 (Invalid):** Age < 18 (e.g., 10)
* **Partition 2 (Valid):** 18 <= Age <= 60 (e.g., 30)
* **Partition 3 (Invalid):** Age > 60 (e.g., 70)

---

## 2. Boundary Value Analysis (BVA)
BVA focuses on testing values at the boundaries (edges) of input ranges, where defect density is highest.

### BVA Technique Types:
* **Two-Value BVA:** Tests exact Minimum, Maximum, and values just outside ($Min-1$, $Min$, $Max$, $Max+1$).
* **Three-Value BVA:** Tests $Min-1$, $Min$, $Min+1$, $Max-1$, $Max$, and $Max+1$.

### Example: Age Field (Valid Range: 18 to 60)
* **Boundary Values to Test:** `17` (Invalid), `18` (Valid Min), `19` (Valid), `59` (Valid), `60` (Valid Max), `61` (Invalid).

---

## ⚡ Key Differences

| Feature | Equivalence Partitioning | Boundary Value Analysis |
| :--- | :--- | :--- |
| **Focus** | Representative values inside sets/ranges. | Edge values at the borders of ranges. |
| **Best Used For** | Large input ranges or discrete lists. | Continuous numerical ranges. |

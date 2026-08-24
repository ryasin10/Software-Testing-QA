# 📑 Decision Table Testing

## Overview
**Decision Table Testing** is a structured black-box technique used to test complex business logic involving multiple combinations of inputs (conditions) and outputs (actions).

---

## 🏗️ Structure of a Decision Table
A Decision Table consists of four main quadrants:
1. **Conditions:** Inputs or business rules to evaluate.
2. **Condition Entries:** Boolean values (`T`/`F` or `Yes`/`No`) representing input states.
3. **Actions:** System outputs or results triggered by conditions.
4. **Action Entries:** Flags (`X` or `-`) indicating which action executes for a rule.

---

## 📊 Example: E-Commerce Free Shipping Logic
**Rules:** Free shipping is granted if the user is a Premium Member **OR** spends over $100.

| Conditions & Actions | Rule 1 | Rule 2 | Rule 3 | Rule 4 |
| :--- | :---: | :---: | :---: | :---: |
| **Is Premium Member?** | Yes | Yes | No | No |
| **Order Total > $100?** | Yes | No | Yes | No |
| **Apply Free Shipping?** | **X** | **X** | **X** | **-** |
| **Apply Standard Shipping** | **-** | **-** | **-** | **X** |

---

## 💡 Benefits of Decision Tables
* **Handles Complex Rules:** Ideal for financial, insurance, and e-commerce rule validation.
* **Prevents Missing Requirements:** Ensures all logical combinations ($2^n$ rules for $n$ boolean conditions) are systematically analyzed.

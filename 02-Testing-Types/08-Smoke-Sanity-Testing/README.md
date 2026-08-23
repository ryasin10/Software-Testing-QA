# Smoke and Sanity Testing

## Overview

Smoke Testing and Sanity Testing are both used to quickly check whether a software build is suitable for further testing.

However, they have different purposes and scopes.

---

# Smoke Testing

## What is Smoke Testing?

Smoke Testing is a preliminary testing process used to verify that the major and critical functions of a new software build are working.

The main question is:

> **Is the build stable enough for further testing?**

---

## Example

Suppose a new build of an e-commerce application is released.

Smoke Testing may check:

```text
Application Opens       ✓
Login                    ✓
Search                   ✓
Add to Cart              ✓
Checkout                 ✓
```

If critical functions are broken:

```text
Login ❌
```

The build may be rejected for further testing.

---

## Characteristics of Smoke Testing

- Broad testing
- Shallow testing
- Focuses on critical functionality
- Performed on a new build
- Helps determine whether the build is testable

### Easy Memory

> **Smoke = Is the build OK enough to test?**

---

# Sanity Testing

## What is Sanity Testing?

Sanity Testing is a focused testing process used to verify that a specific change or functionality works correctly after a minor change or fix.

The main question is:

> **Does the recent change work correctly?**

---

## Example

Suppose the developer fixes the Shopping Cart calculation.

Sanity Testing focuses mainly on the affected area:

```text
Shopping Cart
    ↓
Add Item
    ↓
Change Quantity
    ↓
Calculate Total
```

We do not necessarily test the entire application.

---

## Characteristics of Sanity Testing

- Narrow testing
- Deeper testing of a specific area
- Focuses on recent changes
- Usually performed after minor changes or bug fixes
- Helps determine whether the changed functionality works

### Easy Memory

> **Sanity = Does the recent change make sense and work correctly?**

---

# Smoke vs Sanity Testing

| Smoke Testing | Sanity Testing |
|---|---|
| Broad and shallow | Narrow and deep |
| Checks major functionality | Checks a specific changed area |
| Usually performed on a new build | Usually performed after a change or fix |
| Determines whether the build is stable enough for testing | Determines whether the recent change works |
| Covers critical features | Focuses on related functionality |

---

# Example

Imagine a banking application.

A new build is received.

### Smoke Testing

We quickly check:

```text
Login
Transfer
Balance
Logout
```

The goal is to verify that the major functions are working.

### Sanity Testing

Suppose the developer fixed a problem with money transfers.

We focus on:

```text
Transfer
   ↓
Enter Amount
   ↓
Select Account
   ↓
Confirm Transfer
   ↓
Verify Result
```

The goal is to verify the specific changed area.

---

# Smoke Testing vs Regression Testing

Smoke Testing checks whether the build is stable enough for testing.

Regression Testing checks whether changes have negatively affected existing functionality.

```text
New Build
    ↓
Smoke Testing
    ↓
Stable?
    ↓
Further Testing
    ↓
Regression Testing
```

---

# Smoke Testing vs Sanity Testing

A simple way to remember:

```text
Smoke
  ↓
Broad
  ↓
"Can we test this build?"

Sanity
  ↓
Narrow
  ↓
"Does this specific change work?"
```

---

## Key Takeaways

- **Smoke Testing** is broad and shallow.
- **Sanity Testing** is narrow and deep.
- Smoke Testing checks the stability of a new build.
- Sanity Testing focuses on a specific change or fix.
- Smoke Testing answers: **"Is the build testable?"**
- Sanity Testing answers: **"Does the recent change work correctly?"**

## Important Definitions

> **Smoke Testing:** A preliminary check of critical functionality to determine whether a build is stable enough for further testing.

> **Sanity Testing:** A focused check of specific functionality after a change or fix to verify that it works correctly.

# Regression Testing

## What is Regression Testing?

Regression Testing is the process of re-running existing test cases after changes have been made to the software.

The goal is to verify that the changes have **not negatively affected existing functionality**.

### Simple Question

> **"I changed something. Did I break something else?"**

---

## Example

Suppose a developer fixes the Payment functionality.

The tester should not only test Payment.

They may also check:

```text
Login          ✓
Search         ✓
Shopping Cart  ✓
Payment        ✓
Checkout       ✓
```

The goal is to make sure the change did not introduce new problems.

---

## When is Regression Testing Performed?

Regression Testing can be performed after:

- Bug fixes
- New features
- Requirement changes
- Performance changes
- Integration with external systems
- Other significant software changes

---

# Regression Testing Approaches

## 1. Retest All

All existing test cases are executed again.

```text
1000 Test Cases
      ↓
Run all 1000 again
```

### Advantage

- High coverage.

### Disadvantage

- Time-consuming.
- Expensive for large applications.

---

## 2. Regression Test Selection

Instead of executing every test case, testers select the test cases related to the changes and affected areas.

Example:

If the Shopping Cart was changed:

```text
Add Item
Remove Item
Update Quantity
Calculate Total
Checkout
```

These tests may be selected instead of testing the entire application.

---

## 3. Test Case Prioritization

Test cases can be prioritized based on factors such as:

- Business impact
- Criticality
- Frequently used functionality
- Historical defects

Example:

```text
Payment       → High Priority
Login         → High Priority
Profile       → Medium Priority
Theme         → Low Priority
```

High-priority tests are executed first.

---

# Types of Regression Testing

## Unit Regression Testing

Focuses on the modified unit or section of the application.

---

## Regional Regression Testing

Tests the modified area and the areas that may be affected by the change.

```text
Affected Area
      +
Modified Area
      ↓
Regression Testing
```

---

## Full Regression Testing

Tests the entire application.

This can be useful after major or core changes or before important releases.

```text
A
B
C
D
E
F
↓
All tested again
```

---

## Corrective Regression Testing

Used when there is no significant modification to the existing functionality and existing test cases can be executed to verify continued behavior.

---

## Selective Regression Testing

A selected subset of existing test cases is executed based on the changed modules, dependencies, and criticality.

The main goal is to save time and resources.

---

# Automated Regression Testing

Regression Testing is a good candidate for automation because the same test cases may need to be executed repeatedly.

```text
New Build
    ↓
Automated Regression Tests
    ↓
PASS / FAIL
```

### Benefits

- Faster execution
- Repeatable
- Consistent
- Saves effort over repeated test cycles
- Can be integrated into CI/CD pipelines

---

# Regression Testing vs Retesting

These two concepts are often confused.

## Retesting

Retesting verifies that a **specific defect has been fixed**.

Example:

```text
Login Bug
    ↓
Developer fixes it
    ↓
Retesting
    ↓
Does Login work now?
```

### Goal

> **Verify the specific bug fix.**

---

## Regression Testing

Regression Testing checks whether the fix or change has affected other existing functionality.

```text
Login Fix
    ↓
Regression Testing
    ↓
Login ✓
Registration ✓
Logout ✓
Profile ✓
Session ✓
```

### Goal

> **Verify that existing functionality has not been negatively affected.**

---

# Smoke + Sanity + Retesting + Regression

These concepts can be remembered together:

```text
New Build
    ↓
Smoke Testing
    ↓
"Is the build stable enough to test?"
    ↓
Sanity Testing
    ↓
"Does the recent change work?"
    ↓
Retesting
    ↓
"Is the specific bug fixed?"
    ↓
Regression Testing
    ↓
"Did the change break anything else?"
```

The exact order can vary depending on the team's testing process.

---

# Regression Testing Example

Suppose a developer fixes a bug in the Shopping Cart.

### Step 1 — Retesting

Test the failed test case again:

```text
Add item
Expected Total = $100
Actual Total = $100
PASS
```

### Step 2 — Regression Testing

Check related functionality:

```text
Add Item        ✓
Remove Item     ✓
Quantity        ✓
Discount        ✓
Checkout        ✓
Payment         ✓
```

The purpose is to verify that the fix did not break existing functionality.

---

## Key Takeaways

- Regression Testing is performed **after software changes**.
- It checks whether existing functionality still works.
- **Retest All** means executing all test cases.
- **Regression Test Selection** means selecting relevant tests.
- **Prioritization** means running important tests first.
- Automation is highly useful for regression testing.
- **Retesting = verify the specific fix.**
- **Regression = check for side effects of the change.**

## Important Definition

> **Regression Testing is the process of re-running existing tests after software changes to ensure that existing functionality has not been negatively affected.**

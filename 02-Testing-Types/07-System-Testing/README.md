# System Testing

## What is System Testing?

System Testing is a testing level where the **complete and integrated software system** is tested as a whole.

The goal is to verify that the complete system meets its specified requirements.

---

## Main Idea

```text
Unit Testing
     ↓
Integration Testing
     ↓
System Testing
     ↓
Acceptance Testing
```

System Testing comes after the system's components have been integrated.

---

## What Does System Testing Check?

System Testing can verify:

- Functional requirements
- Non-functional requirements
- End-to-end workflows
- System behavior
- Interaction between different parts of the application

---

## Example

Imagine an online shopping application.

Instead of testing only the Login module or Cart module, System Testing checks the complete flow:

```text
Open Website
     ↓
Login
     ↓
Search Product
     ↓
Add to Cart
     ↓
Checkout
     ↓
Payment
     ↓
Order Confirmation
```

The complete system is tested from the user's perspective.

---

## Main Goal

> **To verify that the complete integrated system works according to the specified requirements.**

---

## System Testing Example

### Requirement

A user should be able to purchase a product.

### System Test

```text
1. Login
2. Search for product
3. Select product
4. Add product to cart
5. Proceed to checkout
6. Enter payment information
7. Complete payment
8. Verify order confirmation
```

The entire workflow is tested.

---

## System Testing vs Integration Testing

| Integration Testing | System Testing |
|---|---|
| Tests interactions between components | Tests the complete system |
| Focuses on interfaces and communication | Focuses on end-to-end behavior |
| Smaller scope | Larger scope |
| Components are tested together | Entire integrated application is tested |

### Simple Difference

> **Integration Testing:** Do the components work together?

> **System Testing:** Does the complete system work correctly?

---

## System Testing vs Unit Testing

```text
Unit Testing
    ↓
Individual component

Integration Testing
    ↓
Components working together

System Testing
    ↓
Complete system
```

---

## Types of System Testing

System Testing can include different types of testing depending on the system and requirements, such as:

- Functional Testing
- Performance Testing
- Security Testing
- Usability Testing
- Compatibility Testing
- Recovery Testing

These tests can be used to verify different aspects of the complete system.

---

## Characteristics

### Complete System

The entire integrated application is tested.

### End-to-End

Testing can cover complete user workflows.

### Requirement-Based

Tests are based on system requirements.

### Realistic Environment

Testing is usually performed in an environment that is similar to the real operating environment.

---

## Key Takeaways

- System Testing tests the **complete integrated system**.
- It verifies whether the system meets its requirements.
- It can include both functional and non-functional testing.
- It focuses on complete workflows and end-to-end behavior.
- It is performed after Integration Testing.

## Important Definition

> **System Testing is the process of testing the complete and integrated software system to verify that it meets its specified requirements.**

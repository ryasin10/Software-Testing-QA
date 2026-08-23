# Unit Testing

## What is Unit Testing?

Unit Testing is a software testing level where the smallest testable parts of an application are tested individually.

A **unit** can be a:

- Function
- Method
- Class
- Small module

The main goal is to verify that each unit works correctly in isolation.

---

## Simple Example

Suppose we have a function that calculates the total price:

```javascript
function calculateTotal(price, quantity) {
    return price * quantity;
}
```

We can test it independently:

```text
Input:
price = 10
quantity = 3

Expected Result:
30
```

If the function returns `30`, the test passes.

---

## Main Goal

The main goal of Unit Testing is:

> **To verify that individual units of code work correctly and independently.**

Unit Testing helps developers find defects early, before the units are combined with other parts of the application.

---

## Unit Testing Process

```text
Write Unit
    ↓
Define Expected Result
    ↓
Create Test
    ↓
Execute Test
    ↓
Compare Actual vs Expected
    ↓
Pass / Fail
```

---

## Characteristics of Unit Testing

### 1. Small Scope

Unit tests focus on small and specific parts of the application.

### 2. Isolated

The unit is usually tested independently from other components.

### 3. Fast

Because the tests are small and focused, they can usually execute quickly.

### 4. Repeatable

The same unit test can be executed repeatedly.

### 5. Early Bug Detection

Unit Testing helps detect defects early in the development process.

---

## Example

Imagine we have a calculator application.

It contains:

```text
add()
subtract()
multiply()
divide()
```

Instead of testing the entire calculator at once, we can test each function separately.

### Test `add()`

```text
add(5, 3)
Expected: 8
Actual: 8
Result: PASS
```

### Test `multiply()`

```text
multiply(5, 3)
Expected: 15
Actual: 15
Result: PASS
```

Each function is tested as an individual unit.

---

## Unit Testing and Dependencies

Sometimes a unit depends on another component, such as:

- Database
- API
- External service
- Another module

In Unit Testing, these dependencies are often replaced with test doubles such as:

- Stubs
- Mocks
- Fakes

This helps keep the unit test isolated.

---

## Advantages of Unit Testing

### Early Bug Detection

Bugs can be found early before the code is integrated with other components.

### Easier Debugging

Because the test focuses on a small unit, it is easier to identify where the problem is.

### Supports Refactoring

Developers can modify or improve code while using unit tests to verify that the behavior has not changed unexpectedly.

### Reduces Debugging Cost

Finding and fixing defects earlier can reduce the effort required later.

### Improves Code Quality

Writing unit tests encourages developers to create smaller and more focused components.

### Fast Feedback

Unit tests can usually be executed quickly and provide immediate feedback.

---

## Disadvantages of Unit Testing

### Cannot Test the Complete System

Unit Testing focuses on individual units and does not verify the complete application.

### Integration Problems May Be Missed

A unit may work correctly by itself but fail when interacting with another component.

### Test Maintenance

Unit tests may need to be updated when the code changes.

### Initial Development Effort

Writing unit tests requires additional development time.

---

## Unit Testing vs Integration Testing

| Unit Testing | Integration Testing |
|---|---|
| Tests individual units | Tests multiple modules together |
| Focuses on isolated behavior | Focuses on interaction |
| Small scope | Larger scope |
| Usually fast | Usually more complex |
| Finds unit-level defects | Finds communication/integration problems |

### Simple Difference

```text
Unit Testing
    ↓
"Does this unit work?"

Integration Testing
    ↓
"Do these units work together?"
```

---

## Unit Testing vs System Testing

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

Each level has a wider scope than the previous one.

---

## Who Performs Unit Testing?

Unit Testing is commonly performed by **developers** during development.

It is closely connected to the implementation of individual functions, methods, classes, or modules.

---

## When Should Unit Testing Be Done?

Unit Testing should be performed during development, especially when:

- A new function is created.
- A method is changed.
- A bug is fixed.
- Code is refactored.
- New functionality is added.

Unit tests can then be executed repeatedly as the code evolves.

---

## Unit Testing in the Testing Levels

Unit Testing is the first level in the common testing hierarchy:

```text
Unit Testing
      ↓
Integration Testing
      ↓
System Testing
      ↓
Acceptance Testing
```

### Unit Testing

Tests individual components.

### Integration Testing

Tests interactions between components.

### System Testing

Tests the complete integrated system.

### Acceptance Testing

Checks whether the system satisfies business or user requirements.

---

## Key Takeaways

- Unit Testing tests **individual units** of software.
- A unit can be a function, method, class, or small module.
- The unit is usually tested in **isolation**.
- Unit tests are generally **fast and repeatable**.
- They help detect bugs early.
- They make debugging easier.
- Unit Testing does not replace Integration or System Testing.
- Developers commonly write and execute unit tests.

---

## Important Definition

> **Unit Testing is the process of testing individual and isolated units of software to verify that each unit behaves as expected.**

# Integration Testing

## What is Integration Testing?

Integration Testing is a testing level where two or more software components or modules are combined and tested to verify that they work correctly together.

The main focus is on **interactions and communication between components**.

### Simple Example

Suppose we have:

```text
Login Module
     +
Database
     ↓
Integration Test
```

We want to verify that the Login Module can correctly communicate with the Database.

---

## Main Goal

> **To verify that integrated components work correctly together.**

A component may work correctly by itself but fail when interacting with another component.

---

## Integration Testing Approaches

There are several approaches to Integration Testing.

### 1. Big Bang Integration Testing

All modules are integrated together at the same time and then tested.

```text
Module A ─┐
Module B ─┤
Module C ─┼──→ Integrate Everything → Test
Module D ─┘
```

### Advantages

- Simple approach.
- All modules are integrated together.

### Disadvantages

- Difficult to identify the source of a failure.
- Defects are discovered later.
- Testing can become difficult when the system is large.

---

## 2. Incremental Integration Testing

Modules are integrated and tested gradually instead of integrating everything at once.

```text
Module A
   ↓
A + B
   ↓
A + B + C
   ↓
A + B + C + D
```

This makes it easier to identify integration problems.

---

# Top-Down Integration Testing

In Top-Down Integration Testing, testing starts from the **top-level modules** and moves toward lower-level modules.

```text
       A
      / \
     B   C
    / \
   D   E
```

Testing starts with:

```text
A
↓
B + A
↓
C + A
↓
D + E + B + A
```

When lower-level modules are not yet available, **Stubs** can be used.

---

## Stub

A **Stub** is a temporary component that simulates a lower-level module that has not been implemented or integrated yet.

```text
Top Module
    ↓
Stub
    ↓
Expected Response
```

### Easy Memory

> **Top-Down → Stub**

---

# Bottom-Up Integration Testing

In Bottom-Up Integration Testing, testing starts with the **lowest-level modules** and moves upward.

```text
       A
      / \
     B   C
    / \
   D   E
```

Testing starts from:

```text
D + E
   ↓
B
   ↓
A
```

When higher-level modules are not yet available, **Drivers** can be used.

---

## Driver

A **Driver** is a temporary program or component that calls and controls a lower-level module during testing.

```text
Driver
   ↓
Lower-Level Module
   ↓
Result
```

### Easy Memory

> **Bottom-Up → Driver**

---

# Sandwich Integration Testing

Sandwich Testing combines:

- Top-Down Integration
- Bottom-Up Integration

Testing can proceed from both directions.

```text
        Top
       ↓   ↑
      Middle
       ↑   ↓
      Bottom
```

It can reduce some limitations of using only one integration direction.

---

# Stub vs Driver

| Stub | Driver |
|---|---|
| Used in Top-Down Integration | Used in Bottom-Up Integration |
| Simulates a lower-level module | Simulates a higher-level module |
| Called by the module being tested | Calls the module being tested |
| Helps when lower modules are unavailable | Helps when higher modules are unavailable |

### Easy Memory

```text
Top-Down
   ↓
 Stub

Bottom-Up
   ↓
 Driver
```

---

# Unit Testing vs Integration Testing

| Unit Testing | Integration Testing |
|---|---|
| Tests individual units | Tests multiple components together |
| Focuses on isolated behavior | Focuses on interactions |
| Small scope | Larger scope |
| Usually faster | Usually more complex |
| Finds unit-level defects | Finds communication/integration defects |

---

## Key Takeaways

- Integration Testing checks whether components work correctly together.
- It focuses on **interactions and communication**.
- **Big Bang** integrates everything at once.
- **Incremental** integration combines modules gradually.
- **Top-Down → Stub**.
- **Bottom-Up → Driver**.
- **Sandwich → Top-Down + Bottom-Up**.

## Important Definition

> **Integration Testing verifies that combined software components communicate and work correctly together.**

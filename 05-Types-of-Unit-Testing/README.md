# Types of Unit Testing

## Overview

Unit Testing can be performed using different approaches depending on how the unit and its dependencies are tested.

The main approaches include:

- White Box Testing
- Black Box Testing
- Gray Box Testing

---

# 1. White Box Unit Testing

**White Box Testing** is a testing approach where the tester has knowledge of the internal code and implementation of the unit.

The tester can examine:

- Source code
- Logic
- Conditions
- Loops
- Branches
- Internal paths

### Example

Suppose we have:

```javascript
function checkAge(age) {
    if (age >= 18) {
        return "Allowed";
    } else {
        return "Not Allowed";
    }
}
```

A White Box test considers the internal logic:

```text
age >= 18
    ↓
Allowed

age < 18
    ↓
Not Allowed
```

The goal is to make sure the different internal paths are tested.

### Main Focus

> **How does the code work internally?**

---

# 2. Black Box Unit Testing

**Black Box Testing** focuses on the behavior of the unit without looking at its internal implementation.

The tester provides inputs and checks the outputs.

```text
Input
  ↓
Unit
  ↓
Output
```

### Example

For:

```javascript
calculateTotal(10, 3)
```

We expect:

```text
Expected Result = 30
```

The tester focuses on whether the output is correct, not how the function calculates it internally.

### Main Focus

> **What does the unit do?**

---

# 3. Gray Box Unit Testing

**Gray Box Testing** combines ideas from White Box and Black Box Testing.

The tester has **partial knowledge** of the internal implementation but primarily tests the behavior of the application.

### Main Focus

> **Test the behavior while having some knowledge of the internal structure.**

---

# White Box vs Black Box vs Gray Box

| Type | Knowledge of Internal Code | Main Focus |
|---|---|---|
| White Box | Full knowledge | Internal logic and code paths |
| Black Box | No internal knowledge required | Inputs and outputs |
| Gray Box | Partial knowledge | Behavior + some internal knowledge |

---

# Simple Comparison

```text
White Box
    ↓
I know how the code works
    ↓
Test internal logic


Black Box
    ↓
I don't need to know the code
    ↓
Test input and output


Gray Box
    ↓
I know some internal information
    ↓
Test behavior using partial knowledge
```

---

# Another Way to Understand Them

Imagine a calculator.

## White Box

You can see the calculator's code.

You check:

```text
if condition
else condition
loop
calculation logic
```

You want to verify that the internal logic works correctly.

---

## Black Box

You cannot see the code.

You only provide:

```text
5 + 3
```

And check:

```text
Expected: 8
Actual: 8
```

---

## Gray Box

You know some information about how the calculator is implemented, but you mainly interact with it through inputs and outputs.

---

# Why Are Different Approaches Used?

Different approaches provide different levels of visibility.

### White Box

Useful when detailed knowledge of the implementation is available.

### Black Box

Useful when the main concern is the expected behavior.

### Gray Box

Useful when some internal knowledge is available but complete access to the implementation is not required.

---

# Key Takeaways

- **White Box Testing** focuses on internal code and logic.
- **Black Box Testing** focuses on inputs and outputs.
- **Gray Box Testing** combines behavioral testing with partial knowledge of the internal implementation.
- The main difference is the amount of knowledge the tester has about the internal implementation.

---

## Easy Memory Trick

> **White Box = See inside**

> **Black Box = Don't see inside**

> **Gray Box = See partially inside**

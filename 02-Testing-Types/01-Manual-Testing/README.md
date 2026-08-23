# Manual Testing

## What is Manual Testing?

Manual Testing is a software testing process where test cases are executed manually by a tester without using automation scripts.

The tester interacts with the application, provides inputs, observes the results, and compares the actual result with the expected result.

### Simple Example

Suppose we have a Login page:

1. Open the Login page.
2. Enter a valid username.
3. Enter a valid password.
4. Click the Login button.
5. Check whether the user is redirected to the Dashboard.

If the actual result matches the expected result, the test **passes**.

---

## How Manual Testing Works

The basic process is:

```text
Requirement
    ↓
Test Scenario
    ↓
Test Case
    ↓
Execute Test Manually
    ↓
Compare Actual vs Expected Result
    ↓
Pass / Fail
    ↓
Report Defects
```

---

## Main Characteristics

### 1. Human Execution

The tester performs the test steps manually.

### 2. No Automation Scripts

The test is not executed automatically by a testing script.

### 3. Human Observation

The tester can observe the application and identify unexpected behavior that may not have been specifically described in the test case.

### 4. Flexible

The tester can change the testing approach while testing based on what they discover.

---

## Advantages of Manual Testing

### Easy to Start

Manual testing does not require programming or automation framework setup.

### Flexible

Testers can change their testing steps based on the application's behavior.

### Good for Exploratory Testing

Manual testing is very useful when the tester needs to explore the application and find unexpected issues.

### Useful for Usability Testing

A human tester can evaluate whether the application is easy and comfortable to use.

### Useful for New Features

When a feature is still changing frequently, manual testing can be more convenient than creating automation scripts immediately.

---

## Disadvantages of Manual Testing

### Time-Consuming

Repeating the same test cases manually can take a lot of time.

### Human Error

Testers can make mistakes when entering data or following test steps.

### Difficult for Repetitive Testing

Running hundreds of the same test cases manually is inefficient.

### Less Suitable for Large Regression Suites

Large regression test suites can become difficult and expensive to execute manually.

---

## When to Use Manual Testing?

Manual Testing is especially useful for:

- Exploratory Testing
- Usability Testing
- UI Testing
- Ad-hoc Testing
- Testing frequently changing features
- Scenarios that require human judgment

---

## Manual Testing Example

Imagine an online shopping application.

A tester may manually test:

```text
Open Website
     ↓
Login
     ↓
Search for a Product
     ↓
Open Product
     ↓
Add to Cart
     ↓
Checkout
     ↓
Confirm Order
```

The tester checks each step and verifies that the actual behavior matches the expected behavior.

---

## Manual Testing vs Automation Testing

| Manual Testing | Automation Testing |
|---|---|
| Tests are executed by a human | Tests are executed using scripts/tools |
| Slower for repetitive tests | Faster for repetitive tests |
| More flexible | Less flexible during frequent changes |
| Good for exploratory testing | Good for repetitive and regression testing |
| Can involve human judgment | Produces consistent execution |
| No automation framework required | Requires automation tools/frameworks |

---

## Key Points

- Manual Testing is performed by a **human tester**.
- It does not depend on automated test scripts.
- It is flexible and useful for **exploratory and usability testing**.
- It can be **time-consuming** for repetitive tasks.
- It is useful when requirements or features are still changing.
- Automation is usually more suitable for large, repetitive, and regression test suites.

---

## Important Definition

> **Manual Testing is the process of testing software manually without using automation scripts to verify that the application behaves as expected.**

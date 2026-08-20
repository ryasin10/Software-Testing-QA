# Manual Testing vs Automated Testing

## Overview

Manual Testing and Automated Testing are two different approaches used to verify software quality.

The main difference is **how the test cases are executed**.

- **Manual Testing:** A human tester executes the test steps.
- **Automation Testing:** Test scripts and tools execute the test steps automatically.

---

## Manual Testing

Manual Testing is performed by a tester without using automation scripts.

The tester:

1. Reads the test case.
2. Performs the test steps.
3. Enters the required data.
4. Observes the result.
5. Compares the actual result with the expected result.
6. Reports defects if the test fails.

### Example

```text
Open Login Page
      ↓
Enter Username
      ↓
Enter Password
      ↓
Click Login
      ↓
Check Dashboard
```

A tester performs these steps manually.

---

## Automation Testing

Automation Testing uses scripts and testing tools to execute test cases automatically.

### Example

```text
Automation Script
       ↓
Open Login Page
       ↓
Enter Username
       ↓
Enter Password
       ↓
Click Login
       ↓
Check Dashboard
       ↓
Pass / Fail
```

The script performs the test steps without requiring the tester to manually perform every action.

---

# Key Differences

| Manual Testing | Automation Testing |
|---|---|
| Performed by a human tester | Performed using scripts and tools |
| Slower for repetitive tests | Faster for repetitive tests |
| More flexible | More structured |
| Good for exploratory testing | Good for repetitive and regression testing |
| Human judgment can be used directly | Results are checked according to programmed conditions |
| No automation script is required | Automation scripts are required |
| Lower initial setup | Requires initial setup and development |
| Repeated execution takes more time | Tests can be repeated quickly |
| Maintenance is mainly test execution effort | Scripts require maintenance when the application changes |

---

# Advantages of Manual Testing

### Flexibility

A tester can change the testing approach based on what they observe.

### Human Judgment

A tester can identify usability issues and unexpected behavior using human observation.

### Good for Exploratory Testing

It is useful when the tester does not want to follow only predefined test steps.

### Good for Frequently Changing Features

Manual testing can be practical when a feature is still being developed or changed frequently.

---

# Advantages of Automation Testing

### Faster Execution

Automated tests can execute repetitive test cases quickly.

### Repeatability

The same tests can be executed many times.

### Consistency

The same steps are performed in the same way during every execution.

### Regression Testing

Automation is especially useful for regression testing because regression tests are executed repeatedly after software changes.

### CI/CD Integration

Automated tests can be integrated into CI/CD pipelines.

```text
Code Change
    ↓
Build
    ↓
Automated Tests
    ↓
Pass / Fail
```

---

# Disadvantages of Manual Testing

- Time-consuming for repetitive tasks.
- Human errors can occur.
- Large regression suites are difficult to execute manually.
- Repeated test execution requires more tester effort.

---

# Disadvantages of Automation Testing

- Requires initial development effort.
- Automation scripts need maintenance.
- Changes in the application can break automation scripts.
- Requires technical knowledge of automation tools and programming.
- Not every test is suitable for automation.
- Some testing activities require human judgment.

---

# When Should We Use Manual Testing?

Manual Testing is suitable for:

- Exploratory Testing
- Usability Testing
- Ad-hoc Testing
- Frequently changing features
- Testing that requires human judgment
- Initial testing of new or unstable features

---

# When Should We Use Automation Testing?

Automation Testing is suitable for:

- Regression Testing
- Repetitive Test Cases
- Large Test Suites
- Frequent Test Execution
- Data-driven Testing
- Cross-browser Testing
- CI/CD pipelines

---

# Example

Imagine an e-commerce application.

A tester needs to check the following flow:

```text
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

### Manual Approach

The tester performs these steps manually every time.

### Automation Approach

An automation script performs the same steps automatically.

If this test needs to be executed after every new build, automation can save significant time.

---

# Can We Use Both?

Yes.

Manual and Automation Testing are not alternatives where only one must be chosen.

They can be used together.

```text
Manual Testing
    ↓
Exploratory / Usability / Human Judgment

Automation Testing
    ↓
Regression / Repetitive / Frequent Testing
```

A testing team can use each approach where it provides the most value.

---

# Key Takeaways

- **Manual Testing = Human execution.**
- **Automation Testing = Script/tool-based execution.**
- Manual Testing is flexible and useful for exploratory and usability testing.
- Automation Testing is fast, repeatable, and consistent.
- Automation is especially useful for Regression Testing.
- Automation requires development and maintenance effort.
- Not every test should be automated.
- The best approach is often to use **Manual and Automation Testing together**.

---

## Quick Memory

> **Manual = Human + Flexible**

> **Automation = Script + Repeatable + Fast**

> **Exploratory / Usability → Manual**

> **Regression / Repetitive → Automation**

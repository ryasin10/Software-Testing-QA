# ✍️ How to Write Test Cases

## Overview
A **Test Case** is a set of execution conditions, input values, execution steps, and expected results developed to verify whether a software application satisfies a specific business requirement.

---

## 🏗️ Standard Test Case Format

| Field Name | Description | Example |
| :--- | :--- | :--- |
| **Test Case ID** | Unique identifier | `TC_AUTH_001` |
| **Test Scenario** | High-level module feature being tested | Check User Login with valid credentials |
| **Test Description** | Brief summary of what is tested | Verify that a registered user can log in with correct credentials |
| **Pre-conditions** | Prerequisites before test execution | User account is created and active |
| **Test Steps** | Sequential step-by-step instructions | 1. Navigate to `/login`<br>2. Enter valid email<br>3. Enter valid password<br>4. Click 'Login' button |
| **Test Data** | Specific inputs used for testing | Email: `test@user.com`, Pass: `Pass123!` |
| **Expected Result** | Intended correct system behavior | User is redirected to `/dashboard` and sees welcome banner |
| **Actual Result** | Observed behavior during execution | User successfully redirected to `/dashboard` |
| **Status** | Final outcome | `PASS` / `FAIL` / `BLOCKED` |

---

## ⚙️ Best Practices for Writing Effective Test Cases
* **Keep Steps Simple & Direct:** Any tester should be able to execute the test without asking questions.
* **Self-Contained & Independent:** Test cases should not depend on the state or execution of other test cases.
* **Include Positive & Negative Cases:** Test valid inputs as well as invalid inputs, boundary values, and edge cases.
* **Ensure Repeatability:** Produce identical results when executed multiple times by different testers.

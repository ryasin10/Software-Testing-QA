# Software Testing Life Cycle (STLC)

---

# 1. What is Software Testing Life Cycle?

**Software Testing Life Cycle (STLC)** is a structured process that contains a series of testing activities performed to make sure that software meets its requirements and has good quality.

STLC focuses specifically on the **testing process**, from analyzing requirements until testing is completed and the test cycle is closed.

The main phases of STLC are:

1. Requirement Analysis.
2. Test Planning.
3. Test Case Development.
4. Test Environment Setup.
5. Test Execution.
6. Test Cycle Closure.

Each phase has its own:

* Activities.
* Entry criteria.
* Exit criteria.
* Deliverables.

---

# 2. Why is STLC Important?

STLC gives the testing process a clear structure instead of testing randomly.

It helps the QA team:

* Understand what needs to be tested.
* Plan testing activities.
* Create test cases.
* Prepare the testing environment.
* Execute tests.
* Report defects.
* Retest fixed defects.
* Measure testing progress.
* Document the final testing results.

STLC also encourages testers to think about testing from an early stage instead of waiting until development is finished.

---

# 3. STLC vs SDLC

STLC and SDLC are related, but they are not the same.

## SDLC

**Software Development Life Cycle (SDLC)** covers the complete process of developing software.

It can include:

```text
Requirements
     ↓
Design
     ↓
Development
     ↓
Testing
     ↓
Deployment
     ↓
Maintenance
```

## STLC

**Software Testing Life Cycle (STLC)** focuses specifically on testing.

```text
Requirement Analysis
        ↓
Test Planning
        ↓
Test Case Development
        ↓
Environment Setup
        ↓
Test Execution
        ↓
Test Closure
```

### Main Difference

**SDLC = building the software**

**STLC = testing the software**

STLC works alongside SDLC to make sure quality is considered throughout the development process.

---

# 4. Six Phases of STLC

The six main phases are:

| Phase                  | Main Purpose                               |
| ---------------------- | ------------------------------------------ |
| Requirement Analysis   | Understand what needs to be tested         |
| Test Planning          | Decide how testing will be performed       |
| Test Case Development  | Create test cases and test data            |
| Test Environment Setup | Prepare the environment                    |
| Test Execution         | Run tests and report defects               |
| Test Cycle Closure     | Complete testing and prepare final reports |

---

# 5. Phase 1 – Requirement Analysis

Requirement Analysis is the **first phase** of STLC.

The QA team studies the requirements from a testing point of view.

The goal is to understand:

* What the system should do.
* What features need to be tested.
* Which requirements are testable.
* Functional requirements.
* Non-functional requirements.
* Business requirements.
* Security requirements.
* Environmental requirements.

Testers may communicate with:

* Business analysts.
* Product managers.
* Developers.
* Customers.
* Other stakeholders.

---

## Activities in Requirement Analysis

The QA team can:

* Analyze requirements.
* Identify testable requirements.
* Identify test conditions.
* Identify risks.
* Prioritize requirements.
* Identify missing or unclear requirements.
* Determine the required testing approach.
* Start preparing the Requirement Traceability Matrix.

---

## Requirement Traceability Matrix

The **RTM** helps connect requirements with test cases.

For example:

```text
Requirement
     ↓
Test Scenario
     ↓
Test Case
     ↓
Test Result
```

This helps make sure that every important requirement is covered by testing.

---

## Deliverables

Typical outputs include:

* Requirement Traceability Matrix (RTM).
* Feasibility information.
* Testing requirements.
* Initial test strategy information.

---

# 6. Phase 2 – Test Planning

After understanding the requirements, the team plans how testing will be performed.

This phase defines the overall testing approach.

The test plan can describe:

* Testing scope.
* Testing objectives.
* Testing strategy.
* Testing resources.
* Testing schedule.
* Required tools.
* Testing responsibilities.
* Automation approach.
* Risks.
* Dependencies.
* Estimated effort.

---

# 7. Test Strategy

The test strategy explains how the team plans to test the software.

It can define:

* Types of testing.
* Testing levels.
* Manual testing.
* Automation testing.
* Tools.
* Environments.
* Risk areas.
* Testing priorities.

The strategy should match the requirements and project needs.

---

# 8. Resource and Role Allocation

The team decides who will be responsible for different testing activities.

For example:

```text
QA Manager
    ↓
Test Lead
    ↓
Testers
    ↓
Automation Engineers
```

Different people may be responsible for:

* Test planning.
* Test case creation.
* Manual execution.
* Automation.
* Defect reporting.
* Test reporting.

---

# 9. Test Estimation

The team also estimates how much time and effort will be required for testing.

The estimation can consider:

* Number of requirements.
* Number of test cases.
* Number of testers.
* Testing complexity.
* Automation needs.
* Testing environment.
* Project deadlines.

---

# 10. Tools Selection

The team decides which tools will be used.

Examples can include:

* Selenium.
* JUnit.
* TestNG.
* Jira.
* Test management tools.
* Automation frameworks.

The tools should be selected based on project requirements.

---

## Deliverables of Test Planning

Typical outputs include:

* Test Plan.
* Test Strategy.
* Effort Estimation.
* Testing schedule.
* Resource plan.

The test plan should be reviewed and approved before moving to the next stages.

---

# 11. Phase 3 – Test Case Development

In this phase, the QA team creates detailed test cases based on the requirements and test plan.

A test case normally contains:

* Test case ID.
* Test description.
* Preconditions.
* Test steps.
* Test data.
* Expected result.
* Actual result.
* Pass/Fail status.

---

# 12. Test Case Design

Testers transform requirements into test scenarios and test cases.

For example, for a login page:

### Requirement

The user should be able to log in using a valid username and password.

### Test Cases

```text
1. Valid username + valid password
2. Invalid username + valid password
3. Valid username + invalid password
4. Empty username
5. Empty password
6. Empty username and password
```

This allows testers to cover both normal and abnormal situations.

---

# 13. Test Data

Test data is prepared for executing the test cases.

Examples include:

* Valid usernames.
* Invalid usernames.
* Valid passwords.
* Invalid passwords.
* Different input values.
* Boundary values.
* Special characters.

Good test data helps improve test coverage.

---

# 14. Test Case Review

Test cases should be reviewed before execution.

Reviewing helps identify:

* Missing scenarios.
* Incorrect expected results.
* Duplicate test cases.
* Incorrect steps.
* Missing test data.
* Requirements that are not covered.

Peer reviews can improve the quality of test cases.

---

# 15. Automation Scripts

If automation is required, the team can start preparing automation scripts.

Automation is especially useful for:

* Repetitive tests.
* Regression testing.
* Smoke testing.
* Frequently executed tests.
* Stable features.

Not every test needs to be automated.

---

## Deliverables

Typical outputs include:

* Test cases.
* Test scenarios.
* Test data.
* Automation scripts.
* Reviewed test artifacts.

---

# 16. Phase 4 – Test Environment Setup

The testing environment is the place where the application will be tested.

It includes the required:

* Hardware.
* Software.
* Operating system.
* Database.
* Application server.
* Network configuration.
* Test data.
* Tools.

The environment should be similar enough to the real environment to allow reliable testing.

---

# 17. Steps of Environment Setup

The environment setup can include:

### Step 1 – Identify Requirements

Determine the required:

* Hardware.
* Software.
* Operating system.
* Database.
* Network.
* Servers.

### Step 2 – Install Required Software

Install and configure:

* Operating systems.
* Databases.
* Application servers.
* Testing tools.

### Step 3 – Configure Data and Connectivity

Prepare:

* Test data.
* Database connections.
* Network connections.
* Application configuration.

### Step 4 – Perform Smoke Testing

A basic smoke test is performed to make sure that the environment and application are ready for detailed testing.

---

# 18. Why is Test Environment Important?

If the environment is not working correctly, testers may receive incorrect results.

For example, a test may fail because:

* The server is down.
* The database is not connected.
* The application was not deployed correctly.
* Required software is missing.
* Network configuration is incorrect.

Therefore, the environment should be checked before starting full test execution.

---

## Deliverables

Typical outputs include:

* Environment setup checklist.
* Environment configuration.
* Smoke test results.
* Ready-to-use testing environment.

---

# 19. Phase 5 – Test Execution

This is the phase where testers actually run the test cases.

The QA team executes the prepared test cases against the application.

Test execution can include:

* Manual testing.
* Automated testing.
* Regression testing.
* Retesting.
* Sanity testing.

---

# 20. Test Result

Each executed test case receives a result such as:

* Pass.
* Fail.
* Blocked.
* Not Executed.

Example:

| Test Case                 | Expected Result    | Actual Result | Status |
| ------------------------- | ------------------ | ------------- | ------ |
| Login with valid data     | User logs in       | User logs in  | Pass   |
| Login with wrong password | Error message      | Error message | Pass   |
| Empty password            | Validation message | No message    | Fail   |

---

# 21. Defect Reporting

When the actual result does not match the expected result, a defect may be reported.

A good defect report should include:

* Defect title.
* Description.
* Steps to reproduce.
* Expected result.
* Actual result.
* Severity.
* Priority.
* Screenshots.
* Logs or other evidence.

---

# 22. Defect Life Cycle

A defect can move through different statuses.

For example:

```text
New
 ↓
Assigned
 ↓
Open
 ↓
Fixed
 ↓
Retest
 ↓
Closed
```

If the problem still exists:

```text
Retest
   ↓
Reopen
   ↓
Developer Fix
   ↓
Retest
```

The exact defect workflow can differ between organizations.

---

# 23. Retesting

**Retesting** means testing a defect again after the developer says that it has been fixed.

Example:

```text
Test failed
    ↓
Bug reported
    ↓
Developer fixes bug
    ↓
Tester retests
    ↓
Pass → Close
Fail → Reopen
```

The purpose is to verify that the specific defect has actually been fixed.

---

# 24. Regression Testing

Regression testing checks whether new changes have broken existing functionality.

For example:

A developer fixes the login feature.

The tester should not only test login again, but may also test related functionality such as:

* Logout.
* User profile.
* Session management.
* Password reset.

This helps make sure that the new change did not create new problems.

---

# 25. Sanity Testing

Sanity testing is a focused check performed after changes or fixes to make sure the important functionality works correctly before spending time on full testing.

For example, after receiving a new build with a payment fix, testers can quickly check the payment flow before running a large regression suite.

---

# 26. Testing Metrics

During execution, teams can track different metrics.

Examples include:

* Number of executed test cases.
* Pass percentage.
* Fail percentage.
* Number of defects.
* Defect severity.
* Defect density.
* Test coverage.
* Defect resolution time.

These metrics help the team understand the quality and progress of testing.

---

# 27. Phase 6 – Test Cycle Closure

The final phase is **Test Cycle Closure**.

This phase happens when testing activities are completed and the team evaluates the overall testing process.

The team checks:

* Whether testing objectives were achieved.
* Whether exit criteria were met.
* Number of tests executed.
* Number of defects found.
* Defect status.
* Overall test results.
* Lessons learned.

---

# 28. Test Closure Report

A final test closure report can contain:

* Testing scope.
* Testing activities.
* Test execution results.
* Pass/Fail statistics.
* Defect statistics.
* Remaining risks.
* Quality assessment.
* Recommendations.
* Lessons learned.

---

# 29. Retrospective

A retrospective is used to look back at the testing process.

The team discusses:

* What went well?
* What went wrong?
* What problems occurred?
* What could be improved?
* What should be changed in the next project?

The goal is continuous improvement.

---

# 30. Metrics at Test Closure

The team can collect and analyze metrics such as:

* Defect density.
* Defect severity.
* Test execution trends.
* Pass percentage.
* Test coverage.
* Defect resolution trends.

These metrics help stakeholders understand the quality of the software.

---

# 31. Entry and Exit Criteria

Each STLC phase should have **Entry Criteria** and **Exit Criteria**.

These criteria work like quality gates.

---

## Entry Criteria

Entry criteria define what must be available before starting a phase.

Example:

Before starting Test Case Development:

* Requirements should be available.
* Requirements should be understood.
* Test planning should be completed.

---

## Exit Criteria

Exit criteria define what must be completed before finishing a phase.

Example:

Before finishing Test Case Development:

* Test cases are written.
* Test cases are reviewed.
* Test data is prepared.
* Automation scripts are ready if needed.

---

# 32. Entry and Exit Criteria for Each Phase

| STLC Phase            | Entry Criteria                            | Exit Criteria                                       |
| --------------------- | ----------------------------------------- | --------------------------------------------------- |
| Requirement Analysis  | Requirements available and finalized      | Requirements analyzed and RTM created               |
| Test Planning         | Requirement analysis completed            | Test plan approved and resources allocated          |
| Test Case Development | Test plan approved                        | Test cases reviewed and test data ready             |
| Environment Setup     | Environment requirements defined          | Environment ready and smoke testing passed          |
| Test Execution        | Test cases and build are ready            | Planned tests executed and critical defects handled |
| Test Closure          | Execution completed and exit criteria met | Closure report completed and artifacts archived     |

---

# 33. Automation in STLC

Test automation can be integrated into different STLC phases.

Automation feasibility can be considered early.

Testers should think about:

* Is the feature stable?
* Is the test repetitive?
* Will the test be reused?
* Is automation worth the effort?
* Is the expected result predictable?

---

# 34. When Should We Automate?

Good candidates for automation include:

* Regression tests.
* Smoke tests.
* Repetitive functional tests.
* Frequently executed tests.
* Stable features.
* Tests that need to run across multiple environments.

Tests that require human judgment may be better suited for manual testing.

Examples include:

* Exploratory testing.
* Some usability testing.
* Some visual checks.

---

# 35. Benefits of Test Automation

Automation can help:

* Reduce repetitive manual work.
* Increase consistency.
* Run tests faster.
* Increase test coverage.
* Run regression tests more frequently.
* Detect defects earlier.

However, automation does not replace the need for proper test planning and test design.

Automation mainly makes test execution faster and more repeatable.

---

# 36. STLC in Agile

STLC can also be used in Agile projects.

The main difference is that STLC phases are not always strictly sequential.

Instead, testing activities can overlap.

For example:

```text
Sprint
  ↓
Requirements
  ↓
Development
  ↓
Testing
  ↓
Feedback
  ↓
Fixes
  ↓
Retesting
```

The process repeats during every sprint.

---

# 37. Agile STLC

In Agile:

* Requirements can change.
* Testing starts early.
* Developers and testers work together.
* Test cases can be created while development is happening.
* Testing happens continuously.
* Feedback is provided quickly.
* Regression testing is repeated frequently.

This makes STLC more iterative than the traditional sequential approach.

---

# 38. STLC and CI/CD

STLC can also be integrated into **CI/CD pipelines**.

Automated tests can run automatically when developers commit new code.

A simplified process is:

```text
Code Commit
     ↓
Build
     ↓
Automated Tests
     ↓
Results
     ↓
Deploy
```

This allows teams to find problems quickly.

Tools such as:

* Jenkins.
* GitHub.
* Automation frameworks.

can be used to support continuous testing.

---

# 39. Metrics and Quality Reports

Testing teams can use centralized dashboards to monitor quality.

Important metrics include:

* Test coverage.
* Test execution rate.
* Defect density.
* Defect severity.
* Defect resolution time.
* Defect escape rate.
* Pass percentage.

These metrics help stakeholders understand:

* Testing progress.
* Current quality.
* Major risks.
* Release readiness.

---

# 40. Common Problems in STLC

There are several problems that can affect the testing process.

---

## Problem 1 – Testing Starts Too Late

If testing begins only near the end of development, defects can become more expensive and difficult to fix.

### Solution

Use **Shift-Left Testing**.

Testing should start during:

* Requirements.
* Design.
* Development.

---

## Problem 2 – Unclear Requirements

If requirements are unclear, testers may create incorrect test cases.

### Solution

Testers should:

* Ask questions early.
* Communicate with stakeholders.
* Review requirements.
* Identify missing information.
* Use risk-based testing.

---

## Problem 3 – Limited Resources

A team may not have enough:

* Testers.
* Time.
* Devices.
* Environments.
* Testing tools.

### Solution

Prioritize testing based on risk and business impact.

---

## Problem 4 – Too Much Manual Repetition

Running the same tests manually again and again can waste time.

### Solution

Use automation for suitable repetitive tests.

---

## Problem 5 – Poor Communication

Poor communication between testers, developers, and business analysts can cause:

* Missing requirements.
* Incorrect test cases.
* Delayed defect fixes.
* Poor test coverage.

### Solution

Encourage communication between all team members and keep testing information clear and organized.

---

# 41. Best Practices for STLC

Good practices include:

### 1. Start Testing Early

Do not wait until development is finished.

### 2. Understand Requirements

Make sure requirements are clear and testable.

### 3. Use Traceability

Connect requirements to test cases using the RTM.

### 4. Prioritize Based on Risk

Focus first on features with high business impact or high risk.

### 5. Review Test Cases

Have test cases reviewed before execution.

### 6. Automate Suitable Tests

Automate repetitive and stable tests.

### 7. Track Defects Properly

Use a clear defect tracking process.

### 8. Measure Testing

Use useful metrics to understand testing progress and quality.

### 9. Learn From Every Cycle

Use the closure phase to identify improvements for future testing.

---

# 42. STLC Example

Let's take an **online shopping application**.

## Requirement Analysis

The system should allow users to:

* Log in.
* Search for products.
* Add products to the cart.
* Pay for orders.

Testers analyze these requirements.

---

## Test Planning

The team decides:

* What will be tested.
* Who will test it.
* Which tools will be used.
* How much time is available.
* Which tests should be automated.

---

## Test Case Development

Testers create cases such as:

```text
Login with valid credentials
Login with invalid credentials
Search for existing product
Search for unavailable product
Add product to cart
Remove product from cart
Complete payment
```

---

## Environment Setup

The team prepares:

* Application server.
* Database.
* Browser.
* Test accounts.
* Test data.
* Payment test environment.

---

## Test Execution

Testers execute the test cases.

If payment fails unexpectedly, a defect is reported.

After the developer fixes it:

```text
Retest
   ↓
Pass
   ↓
Regression Testing
```

---

## Test Closure

At the end, the team prepares a report containing:

* Number of tests.
* Passed tests.
* Failed tests.
* Defects.
* Remaining risks.
* Overall quality.

---

# 43. STLC Complete Flow

```text
Requirement Analysis
        ↓
    Test Planning
        ↓
 Test Case Development
        ↓
 Test Environment Setup
        ↓
    Test Execution
        ↓
 Test Cycle Closure
```

The process can repeat whenever a new version or release needs testing.

---

# 44. STLC vs V-Model

STLC and V-Model are related but different.

### STLC

Focuses specifically on the testing activities:

```text
Requirements
     ↓
Test Planning
     ↓
Test Cases
     ↓
Environment
     ↓
Execution
     ↓
Closure
```

### V-Model

Connects development phases with corresponding testing phases:

```text
Requirements  → Acceptance Testing
System Design → System Testing
Architecture  → Integration Testing
Module Design → Unit Testing
Coding
```

### Main Difference

**STLC describes the testing life cycle.**

**V-Model describes a development model where development and testing activities are connected.**

---

# 45. Key Points to Remember

1. STLC stands for **Software Testing Life Cycle**.
2. STLC is a structured testing process.
3. It focuses specifically on software testing.
4. STLC is different from SDLC.
5. STLC contains six main phases.
6. Requirement Analysis is the first phase.
7. Test Planning defines the testing strategy.
8. Test Case Development creates test cases and test data.
9. Environment Setup prepares the testing environment.
10. Test Execution runs the actual tests.
11. Test Closure completes and evaluates the testing cycle.
12. Each phase has Entry and Exit Criteria.
13. RTM helps maintain traceability between requirements and tests.
14. Defects should be reported clearly.
15. Retesting checks whether a specific defect has been fixed.
16. Regression testing checks that new changes did not break existing functionality.
17. Smoke testing can help verify environment/build readiness.
18. Automation can reduce repetitive testing work.
19. Testing can be integrated into Agile.
20. STLC can also be integrated into CI/CD.
21. Risk-based testing helps when time and resources are limited.
22. Testing should start early.
23. Clear communication is important.
24. Test metrics help measure testing progress and quality.
25. The closure phase helps the team learn and improve future testing cycles.

---

# 46. Quick Revision

```text
STLC

1. Requirement Analysis
        ↓
2. Test Planning
        ↓
3. Test Case Development
        ↓
4. Test Environment Setup
        ↓
5. Test Execution
        ↓
6. Test Cycle Closure
```

### Easy way to remember:

**Requirements → Plan → Cases → Environment → Execute → Close**

---

# 47. Conclusion

The **Software Testing Life Cycle (STLC)** provides a structured way to perform software testing.

Instead of testing randomly, the QA team follows organized phases starting from requirement analysis and ending with test cycle closure.

STLC helps testers:

* Understand requirements.
* Plan testing.
* Create test cases.
* Prepare environments.
* Execute tests.
* Report and retest defects.
* Perform regression testing.
* Measure quality.
* Document the final results.
* Improve future testing processes.

STLC can be used with traditional development models as well as modern approaches such as **Agile and CI/CD**.

The most important idea is:

**Testing is not one activity that happens at the end. It is a complete process that starts early and continues until the testing cycle is properly closed.**


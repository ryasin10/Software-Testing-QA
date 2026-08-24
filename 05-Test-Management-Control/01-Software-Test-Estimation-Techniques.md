# ⏱️ Software Test Estimation Techniques

## Overview
**Test Estimation** is a management activity that predicts the effort, time, cost, and human resources required to complete testing activities for a specific software project.

---

## 🎯 Key Test Estimation Techniques

| Technique | Description | Best Used For |
| :--- | :--- | :--- |
| **Work Breakdown Structure (WBS)** | Breaks down the testing project into small, manageable sub-components and tasks. | Structural planning & granular effort tracking. |
| **3-Point Estimation (PERT)** | Uses three estimates: Optimistic ($O$), Most Likely ($M$), and Pessimistic ($P$) using the formula: $Estimate = \frac{O + 4M + P}{6}$ | Risk-heavy or ambiguous projects. |
| **Function Point Analysis (FPA)** | Estimates effort based on functional size, inputs, outputs, files, and queries. | Large enterprise applications with clear SRS. |
| **Experience-Based (Delphi Method)** | Collects anonymous estimates from multiple QA experts until a consensus is reached. | Complex or legacy systems with limited documentation. |

---

## 💡 Best Practices for Test Estimation
* **Include Buffer Effort:** Add a 10% - 15% buffer time for unexpected scope changes or bug fixes.
* **Consider Non-Testing Factors:** Account for environment setup, team communication, and test data generation.
* **Review Historical Data:** Use metrics from previous projects to improve future estimation accuracy.

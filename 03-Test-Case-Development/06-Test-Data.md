# 🗄️ Test Data Generation

## Overview
**Test Data** is the input data provided to a software application during test execution. Quality test data allows QA teams to verify expected outcomes, boundary conditions, and system behavior under various realistic scenarios.

---

## 🎯 Types of Test Data
* **Positive Data:** Valid inputs that test normal user workflows.
* **Negative Data:** Invalid or unexpected inputs to verify error handling and validation logic.
* **Boundary Data:** Values on the limits of input fields (e.g., max string length, min/max integers).
* **Null / Empty Data:** Tests system reaction when mandatory fields are omitted.
* **Corrupt Data:** Malformed data formats to test stability and exception handling.

---

## ⚡ Approaches to Generate Test Data

| Method | Description | Pros | Cons |
| :--- | :--- | :--- | :--- |
| **Manual Creation** | Data entered manually by testers. | Accurate and highly tailored. | Time-consuming for large volumes. |
| **Production Data Copy** | Copying real user data from production (sanitized). | Highly realistic. | Security & privacy risks (GDPR). |
| **Automated Data Generators** | Using scripts or tools (e.g., Faker) to auto-generate data. | Fast, scalable, and safe. | May lack complex business context. |

---

## 💡 Best Practices for Test Data Management
1. **Data Privacy (Masking):** Always anonymize Sensitive Data (PII) copied from production.
2. **Data Cleanup:** Clean up temporary test data after execution to avoid DB bloating.
3. **Reusable Data Sets:** Maintain standard baseline datasets for regression execution.

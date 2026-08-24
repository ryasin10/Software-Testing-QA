# 🔗 Requirements Traceability Matrix (RTM)

## Overview
A **Requirements Traceability Matrix (RTM)** is a document that maps and traces user requirements with corresponding test cases. It ensures that 100% of defined requirements are tested and verified throughout the testing lifecycle.

---

## 🎯 Primary Purpose of RTM
* **Zero Gap Coverage:** Guarantees no requirement is missed or left untested.
* **Impact Analysis:** Helps determine which test cases need execution when a requirement changes.
* **Project Status Tracking:** Provides clear visibility into testing progress and requirement compliance.

---

## 📋 Types of Traceability
1. **Forward Traceability:** Maps requirements to test cases (ensures requirements are properly covered).
2. **Backward (Reverse) Traceability:** Maps test cases back to requirements (ensures code isn't adding unaccounted scope).
3. **Bi-Directional Traceability:** Combines both forward and backward mapping into a single matrix.

---

## 📊 RTM Structure Example

| Requirement ID | Requirement Description | Test Scenario ID | Test Case ID | Test Status |
| :--- | :--- | :--- | :--- | :--- |
| `REQ_001` | User must log in with email and password | `TS_AUTH_01` | `TC_AUTH_001` | `PASS` |
| `REQ_001` | User must log in with email and password | `TS_AUTH_01` | `TC_AUTH_002` | `FAIL` |
| `REQ_002` | User must reset password via email link | `TS_AUTH_02` | `TC_AUTH_003` | `PASS` |

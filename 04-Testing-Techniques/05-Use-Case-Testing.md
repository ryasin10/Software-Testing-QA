# 👤 Use Case Testing

## Overview
**Use Case Testing** is a functional black-box technique that evaluates an entire application by executing end-to-end user transactions. It tests the system from the user's perspective to ensure functional requirements align with real-world scenarios.

---

## 🧩 Key Components of a Use Case
* **Actor:** User or external system interacting with the application (e.g., *Customer*, *Admin*).
* **Pre-conditions:** Prerequisites required before executing the use case.
* **Basic Flow (Happy Path):** Standard, error-free path to achieve the objective.
* **Alternate / Exception Flows:** Secondary branches or error handling paths.
* **Post-conditions:** State of the system after execution completes.

---

## 📋 Example Use Case: Withdraw Cash from ATM

```text
Actor: Cardholder
Pre-condition: ATM is active and cash is available.

Basic Flow:
1. Cardholder inserts debit card.
2. System prompts for PIN.
3. Cardholder enters valid PIN.
4. System displays transaction menu.
5. Cardholder selects 'Withdrawal' and enters amount.
6. System dispenses cash and ejects card.

Alternate Flow (Insufficient Funds):
5a. Entered amount exceeds account balance.
5b. System displays "Insufficient Funds" error.
5c. System returns to main menu.
```

---

## 💡 Benefits of Use Case Testing
* **End-to-End Verification:** Validates system integrations across complete user journeys.
* **Discovers Integration Defects:** Identifies flaws between connected software components.
* **Business Requirement Alignment:** Ensures software meets operational user needs.

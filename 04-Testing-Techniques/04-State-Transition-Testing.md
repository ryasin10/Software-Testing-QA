# 🔄 State Transition Testing

## Overview
**State Transition Testing** is a dynamic black-box technique used when system behavior depends on current state and past historical inputs. It tests how the system transitions from one valid/invalid state to another based on triggers (events).

---

## 🔑 Key Components
* **States:** Conditions or modes the system stays in (e.g., *Logged Out*, *Logged In*, *Account Locked*).
* **Transitions:** Changes from one state to another.
* **Events / Inputs:** Actions that trigger transitions (e.g., *Enter Invalid Password*).
* **Actions / Outputs:** System response resulting from a transition (e.g., *Display Error Message*).

---

## 🗺️ State Transition Example: ATM PIN Verification

```mermaid
stateDiagram-v8
    [*] --> Idle
    Idle --> PinEntered : Enter PIN
    PinEntered --> Authenticated : Valid PIN
    PinEntered --> Attempt1Failed : Invalid PIN (1st)
    Attempt1Failed --> Authenticated : Valid PIN
    Attempt1Failed --> Attempt2Failed : Invalid PIN (2nd)
    Attempt2Failed --> AccountLocked : Invalid PIN (3rd)
    Authenticated --> [*]
    AccountLocked --> [*]
```

---

## 📊 State Transition Matrix Example

| Current State | Valid PIN Event | Invalid PIN Event |
| :--- | :--- | :--- |
| **Idle** | Authenticated | Attempt 1 Failed |
| **Attempt 1 Failed** | Authenticated | Attempt 2 Failed |
| **Attempt 2 Failed** | Authenticated | Account Locked |
| **Account Locked** | N/A | N/A |

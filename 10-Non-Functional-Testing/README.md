# Non-Functional Testing

## What is Non-Functional Testing?

Non-Functional Testing focuses on **how well the system works** rather than what functionality it provides.

### Simple Difference

> **Functional Testing = What does the system do?**

> **Non-Functional Testing = How well does the system do it?**

---

## Example

Suppose we have a Login feature.

### Functional Testing

```text
Enter Username
Enter Password
Click Login
     ↓
User successfully logs in
```

Question:

> **Does Login work?**

### Non-Functional Testing

```text
1000 Users
    ↓
Login
    ↓
Response < 2 seconds?
System Stable?
Secure?
```

Questions:

> **How fast is Login?**

> **Can the system handle many users?**

> **Is the Login secure?**

---

# Main Types of Non-Functional Testing

## 1. Performance Testing

Performance Testing evaluates how well the system performs under specific conditions.

It can consider:

- Response time
- Speed
- Throughput
- Resource usage

### Example

```text
Page should load within 3 seconds.
```

---

# 2. Load Testing

Load Testing checks how the system behaves under the **expected or normal workload**.

### Example

If the system is expected to support 1,000 users:

```text
1,000 Users
     ↓
System
     ↓
Does it perform correctly?
```

### Main Question

> **Can the system handle the expected load?**

---

# 3. Stress Testing

Stress Testing pushes the system **beyond its expected capacity**.

### Example

```text
Expected = 1,000 users

Stress Test:
2,000
3,000
5,000
10,000
```

### Main Question

> **What happens when the system is pushed beyond its expected limit?**

---

# 4. Scalability Testing

Scalability Testing checks whether the system can handle increasing workload or demand.

### Example

```text
1,000 Users   ✓
5,000 Users   ✓
10,000 Users  ✓
100,000 Users ?
```

### Main Question

> **Can the system grow as demand increases?**

---

# 5. Usability Testing

Usability Testing evaluates whether the application is easy to understand and use.

It can consider:

- Ease of use
- User understanding
- Navigation
- Interface clarity

### Example

Can a new user easily:

```text
Find Login
    ↓
Find Search
    ↓
Add Product
    ↓
Complete Checkout
```

### Main Question

> **Is the system easy to use?**

---

# 6. Security Testing

Security Testing evaluates whether the system and its data are protected from unauthorized access and security threats.

It can include:

- Authentication
- Authorization
- Data protection
- Unauthorized access

### Example

```text
Normal User
    ↓
Try to access Admin Page
    ↓
Access Denied ✓
```

### Main Question

> **Is the system secure?**

---

# 7. Reliability Testing

Reliability Testing checks whether the system can perform consistently without failure over time.

### Example

```text
1 hour   ✓
5 hours  ✓
10 hours ✓
24 hours ✓
```

### Main Question

> **Can the system continue working reliably?**

---

# 8. Recovery Testing

Recovery Testing checks whether the system can recover after a failure.

### Example

```text
System Running
      ↓
Server Failure
      ↓
Recovery
      ↓
System Works Again
```

### Main Question

> **Can the system recover after failure?**

---

# 9. Compatibility Testing

Compatibility Testing checks whether the software works correctly in different environments.

Examples:

```text
Chrome      ✓
Firefox     ✓
Edge        ✓

Windows     ✓
macOS       ✓

Desktop     ✓
Mobile      ✓
```

It can include different:

- Browsers
- Operating systems
- Devices
- Configurations

### Main Question

> **Does the software work correctly across different environments?**

---

# 10. Volume Testing

Volume Testing checks how the system behaves when handling large amounts of data.

### Example

```text
1,000 records
     ↓
100,000 records
     ↓
1,000,000 records
```

### Main Question

> **Can the system handle large volumes of data?**

---

# 11. Endurance Testing

Endurance Testing checks the system under a workload for an extended period of time.

### Example

```text
1,000 Users
     ↓
1 hour
     ↓
6 hours
     ↓
24 hours
```

### Main Question

> **Can the system maintain stable performance over a long period?**

---

# Important Differences

## Performance vs Load vs Stress vs Scalability

| Type | Main Question |
|---|---|
| Performance | How well does the system perform? |
| Load | Can it handle the expected load? |
| Stress | What happens beyond the expected limit? |
| Scalability | Can it grow as demand increases? |

### Example

```text
Performance
→ Response time = 2 seconds

Load
→ 1,000 users

Stress
→ Push beyond 1,000 users

Scalability
→ Grow from 1,000 to 100,000 users
```

---

# Functional vs Non-Functional Testing

| Functional Testing | Non-Functional Testing |
|---|---|
| Focuses on what the system does | Focuses on how well the system works |
| Tests functionality | Tests quality attributes |
| Checks expected behavior | Checks performance, security, usability, etc. |
| Example: Can the user login? | Example: How fast is login? |
| Example: Can the user checkout? | Example: Can 10,000 users checkout? |

---

# Example: Online Banking

## Functional Testing

```text
Transfer $100
      ↓
Money transferred successfully
```

Question:

> **Does the transfer functionality work?**

## Non-Functional Testing

```text
10,000 Users
      ↓
Transfer Money
      ↓
Fast?
Secure?
Stable?
```

This can involve:

- Performance
- Load
- Security
- Reliability
- Scalability

---

# Key Takeaways

- Non-Functional Testing focuses on **how well the system works**.
- It evaluates quality characteristics rather than only functionality.
- Important types include:
  - Performance
  - Load
  - Stress
  - Scalability
  - Usability
  - Security
  - Reliability
  - Recovery
  - Compatibility
  - Volume
  - Endurance
- Load Testing checks expected workload.
- Stress Testing goes beyond expected capacity.
- Scalability Testing checks whether the system can grow.
- Non-Functional Testing complements Functional Testing.

---

## Important Definition

> **Non-Functional Testing evaluates the quality attributes of a software system, such as performance, security, usability, reliability, and scalability, rather than only testing its functional behavior.**

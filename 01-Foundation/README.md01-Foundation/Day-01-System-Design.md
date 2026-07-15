# Day 01 — Introduction to System Design

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand what a System is.
- Understand what a Software System is.
- Explain System Design.
- Differentiate Functional and Non-Functional Requirements.
- Understand the difference between HLD and LLD.

---

# What is a System?

A **System** is a collection of multiple components working together to achieve a common goal.

### Examples

- Hospital
- Banking System
- Car
- E-commerce Platform

---

# What is a Software System?

A Software System consists of multiple software components working together.

Example:

```text
User
   │
   ▼
Frontend
   │
   ▼
Backend
   │
   ▼
Database
```

---

# What is System Design?

System Design is the process of planning the architecture of a software system before implementation.

> Design first, Code second.

---

# Why Do We Need System Design?

A good system should be:

- Scalable
- Reliable
- Secure
- Fast
- Maintainable
- Highly Available

---

# Functional Requirements

Functional Requirements describe **what the system should do**.

### Examples

- User Login
- Signup
- Upload Images
- Send Messages
- Search Users

---

# Non-Functional Requirements

Non-Functional Requirements describe **how well the system should perform**.

### Examples

- Fast response time
- Secure authentication
- High availability
- Low latency
- Support millions of users

---

# High-Level Design (HLD)

High-Level Design provides the overall architecture of the system.

Example:

```text
User
   │
   ▼
Frontend
   │
   ▼
Backend API
   │
   ▼
Database
```

---

# Low-Level Design (LLD)

Low-Level Design focuses on implementation details.

Example:

```text
Controller
   │
   ▼
Service
   │
   ▼
Repository
   │
   ▼
Database
```

---

# HLD vs LLD

| HLD | LLD |
|------|------|
| Architecture | Code Structure |
| Services | Classes |
| Components | Methods |
| APIs | Business Logic |

---

# Key Takeaways

- A system consists of multiple components.
- Software applications are systems.
- System Design is planning before coding.
- Functional Requirements define **what** the system does.
- Non-Functional Requirements define **how well** it performs.
- HLD focuses on architecture.
- LLD focuses on implementation.

---

# Interview Questions

1. What is System Design?
2. What is the difference between Functional and Non-Functional Requirements?
3. Explain HLD vs LLD.
4. Why should System Design be done before coding?

---

# Summary

```
System
    ↓
Software System
    ↓
System Design
    ├── Functional Requirements
    ├── Non-Functional Requirements
    ├── High-Level Design
    └── Low-Level Design
```

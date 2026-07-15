# 📘 Day 01 — Introduction to System Design

> **Module:** Foundation
>
> **Difficulty:** 🟢 Beginner
>
> **Estimated Time:** 45–60 Minutes

---

# 🎯 Learning Objectives

After completing this lesson, you will be able to:

- Define a System.
- Understand a Software System.
- Explain System Design.
- Differentiate Functional and Non-Functional Requirements.
- Understand High-Level Design (HLD) and Low-Level Design (LLD).
- Explain why System Design is important before coding.

---

# 📖 What is a System?

A **System** is a collection of multiple components working together to achieve a common goal.

Every component has a specific responsibility.

When all components work together, they achieve the desired outcome.

## Examples

### 🏥 Hospital

```
Doctor
Nurse
Reception
Laboratory
Pharmacy
Billing

↓

Hospital System
```

---

### 🚗 Car

```
Engine
Battery
Steering
Brakes
Fuel System

↓

Car
```

---

# 💻 What is a Software System?

A Software System is a collection of software components working together.

Example: Instagram

```
                User
                  │
                  ▼
             Frontend
                  │
                  ▼
             Backend API
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
 Authentication Database Storage
        │
        ▼
 Notification Service
```

Each component has a different responsibility.

---

# 🏗️ What is System Design?

System Design is the process of planning the architecture of a software system before writing code.

Instead of immediately coding, we first decide:

- How many servers?
- Which database?
- Authentication method?
- Where will images be stored?
- How will users communicate?
- How will the application scale?

> **Design First → Code Later**

---

# 🎯 Why Do We Need System Design?

Imagine your application has only **100 users**.

A single server may be enough.

Now imagine:

- 10,000 users
- 1 Million users
- 100 Million users

Without proper planning:

- Server crashes
- Database becomes slow
- Website hangs
- Payments fail
- Messages are delayed

System Design helps us build software that continues to work as the number of users grows.

---

# 🎯 Goals of System Design

A good system should be:

- ⚡ Fast
- 📈 Scalable
- 🔒 Secure
- 🛡 Reliable
- 🌍 Highly Available
- 🔧 Easy to Maintain

---

# 📋 Functional Requirements

Functional Requirements describe **WHAT the system should do.**

Examples (Instagram)

- User Signup
- User Login
- Upload Photos
- Upload Reels
- Upload Stories
- Send Messages
- Like Posts
- Comment on Posts
- Search Users
- Follow Users
- Receive Notifications

Think of Functional Requirements as **Features**.

---

# ⚙️ Non-Functional Requirements

Non-Functional Requirements describe **HOW WELL the system should perform.**

Examples

- Login should complete within 2 seconds.
- Image upload should be fast.
- Messages should be delivered in real time.
- Data should be encrypted.
- System should support millions of users.
- 99.99% uptime.
- Reliable under heavy traffic.

Think of Non-Functional Requirements as **Quality Attributes**.

---

# 📊 Functional vs Non-Functional Requirements

| Functional | Non-Functional |
|------------|----------------|
| What the system does | How well the system performs |
| Login | Login within 2 seconds |
| Payment | Secure payment |
| Upload Image | Fast upload |
| Send Message | Reliable delivery |

---

# 🏢 High-Level Design (HLD)

High-Level Design gives the overall architecture of the application.

Example:

```
                   User
                     │
                     ▼
          React / Mobile App
                     │
                     ▼
              Backend API
                     │
      ┌──────────────┼──────────────┐
      ▼              ▼              ▼
 Authentication   Business Logic   Cache
      │              │              │
      └──────────────┼──────────────┘
                     ▼
                 Database
```

HLD focuses on:

- Components
- Services
- Databases
- Communication

---

# 🔧 Low-Level Design (LLD)

Low-Level Design focuses on implementation details.

Example

```
ProductController
        │
        ▼
ProductService
        │
        ▼
ProductRepository
        │
        ▼
Entity Framework
        │
        ▼
SQL Server
```

LLD focuses on:

- Classes
- Methods
- Interfaces
- Objects
- Relationships

---

# 📊 HLD vs LLD

| High-Level Design | Low-Level Design |
|-------------------|------------------|
| Architecture | Code Structure |
| Components | Classes |
| Services | Methods |
| APIs | Business Logic |
| Databases | Tables |

---

# 🌍 Real World Example

Suppose you are building a Food Delivery App.

```
Customer
      │
      ▼
 Mobile App
      │
      ▼
Backend API
      │
 ┌────┼─────┐
 ▼    ▼     ▼
Auth Orders Restaurant
 │     │      │
 └─────┼──────┘
       ▼
   SQL Database
       │
       ▼
     Redis
```

This is a High-Level Design because it shows the major building blocks.

---

# 🧠 Key Takeaways

- A system consists of multiple components working together.
- Software applications are systems.
- System Design is planning before implementation.
- Functional Requirements describe features.
- Non-Functional Requirements describe quality.
- HLD focuses on architecture.
- LLD focuses on implementation.

---

# ❌ Common Mistakes

### Mistake 1

Starting coding without understanding requirements.

---

### Mistake 2

Confusing Functional Requirements with Non-Functional Requirements.

---

### Mistake 3

Thinking HLD and LLD are the same.

---

# 💼 Interview Questions

### Beginner

- What is System Design?
- Why is System Design important?
- What is a Software System?
- Explain Functional Requirements.

### Intermediate

- Difference between Functional and Non-Functional Requirements?
- Difference between HLD and LLD?

---

# 📝 Assignment

## Question 1

Write five Functional Requirements of Instagram.

---

## Question 2

Write five Non-Functional Requirements of Instagram.

---

## Question 3

Draw the High-Level Design of a Food Delivery Application.

---

# 📚 Summary

```
                    SYSTEM
                       │
                       ▼
              Software System
                       │
                       ▼
               System Design
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
 Functional     Non-Functional        HLD
 Requirements    Requirements          │
                                       ▼
                                      LLD
```

---

# 📖 Glossary

| Term | Meaning |
|------|---------|
| System | Multiple components working together |
| Software System | Collection of software components |
| Functional Requirement | What the system should do |
| Non-Functional Requirement | How well the system should perform |
| HLD | High-Level Design |
| LLD | Low-Level Design |

---

# 🚀 Next Lesson

**Day 02 — Client-Server Architecture & Request Lifecycle**

Topics:

- Client
- Server
- Browser
- Request
- Response
- What happens when you type google.com in your browser?

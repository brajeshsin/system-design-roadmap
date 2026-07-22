# 📚 Day 2 - Client, Server, Request & Response

> **Module:** Foundation
> **Day:** 2/50
> **Difficulty:** ⭐ Beginner
> **Estimated Reading Time:** 20–30 Minutes

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

* Understand what a Client is.
* Understand what a Server is.
* Understand how Request and Response work.
* Understand Client–Server Architecture.
* Differentiate between Frontend, Backend, API, Database, and Cloud.
* Explain the complete flow of a web application.
* Answer common interview questions confidently.

---

# 📖 Introduction

Almost every modern software application follows the **Client–Server Architecture**.

Examples include:

* Amazon
* Flipkart
* Instagram
* Facebook
* WhatsApp
* YouTube
* Netflix
* Banking Applications
* UPI Applications
* Crypto Exchanges
* Village Delivery Applications

Whenever you open one of these applications, your device communicates with a remote server.

This communication happens through **HTTP/HTTPS Requests and Responses**.

Understanding this architecture is the foundation of System Design.

---

# 🌍 Real Life Example

Imagine you visit a restaurant.

```
Customer
   │
   ▼
Waiter
   │
   ▼
Kitchen
   │
   ▼
Food
   │
   ▼
Customer
```

Mapping it to Software Engineering:

| Restaurant | Software           |
| ---------- | ------------------ |
| Customer   | Client             |
| Waiter     | Request & Response |
| Kitchen    | Server             |
| Food       | Response/Data      |

The customer never cooks the food.

Similarly,

A client never directly accesses the database.

---

# 🖥️ What is a Client?

## Definition

A **Client** is any application, browser, or device that sends a request to a server in order to access data or services.

Simply,

> **Client = Starts Communication**

The client collects user input and requests the server to perform an action.

---

# Why Do We Need a Client?

Imagine Amazon has only backend servers.

There is no website.

There is no mobile app.

Can users place orders?

❌ No.

Users need an interface to communicate with the server.

That interface is called the **Client**.

Without a client:

* Users cannot login.
* Users cannot browse products.
* Users cannot search.
* Users cannot place orders.
* Users cannot receive responses.

---

# Client Responsibilities

A client is responsible for:

* Displaying User Interface (UI)
* Taking user input
* Sending HTTP requests
* Receiving HTTP responses
* Showing data to users
* Basic validation
* Managing application state

A client should **NOT** contain critical business logic.

---

# Types of Clients

## 1. Web Browser

Examples

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

---

## 2. Web Frontend

Examples

* React
* Angular
* Vue.js
* Next.js

---

## 3. Mobile Client

Examples

* Android App
* iOS App
* Flutter
* React Native

---

## 4. API Clients

Examples

* Postman
* Swagger UI
* Insomnia
* curl

---

# Common Client Examples

* Browser
* React Frontend
* Angular
* Vue
* Mobile App
* Flutter App
* Postman
* Swagger UI

---

# Client Working Flow

```
User

↓

Clicks Login Button

↓

React Frontend

↓

Creates HTTP Request

↓

Sends Request to Server
```

---

# Example

User clicks

```
Login
```

React sends

```http
POST /login
```

The client waits until the server returns a response.

---

# Common Mistakes

❌ React is a Server

Wrong.

React runs inside the browser.

React is a **Client**.

---

❌ Browser stores application data permanently.

Wrong.

The browser only displays data.

Actual business data lives on servers and databases.

---

# 🖥️ What is a Server?

## Definition

A **Server** is a software application or machine that receives requests from clients, processes them, performs business logic, communicates with databases or other services if required, and returns a response.

Simply,

> **Server = Processes Requests + Returns Responses**

---

# Why Do We Need a Server?

Suppose a user wants to log in.

The server needs to:

* Verify email and password
* Check whether the account exists
* Generate authentication tokens
* Apply business rules
* Return the correct response

This cannot be safely done on the client.

---

# Server Responsibilities

A server is responsible for:

* Authentication
* Authorization
* Business Logic
* Validation
* Database Communication
* Security
* Logging
* Error Handling
* API Processing

---

# Types of Servers

## Web Server

Responsible for serving static content and forwarding requests.

Examples:

* Apache HTTP Server
* Nginx
* IIS

---

## Application Server

Responsible for executing business logic.

Examples:

* ASP.NET Core API
* Node.js + Express
* Spring Boot
* Django
* Flask
* Laravel

---

## Database Server

Responsible for storing and retrieving data.

Examples:

* SQL Server
* MySQL
* PostgreSQL
* MongoDB
* Oracle

---

## Cache Server

Stores frequently used data.

Examples:

* Redis
* Memcached

---

## File Server

Stores files such as images and videos.

Examples:

* Amazon S3
* Azure Blob Storage
* Google Cloud Storage

---

# Real Production Architecture

```
                 Internet
                     │
                     ▼
             Nginx / Apache
                     │
                     ▼
            ASP.NET Core API
                     │
        ┌────────────┴────────────┐
        ▼                         ▼
     Redis Cache             SQL Server
        │                         │
        └────────────┬────────────┘
                     ▼
              JSON Response
                     │
                     ▼
                React Client
```

---

# Difference Between Web Server and Application Server

| Web Server          | Application Server         |
| ------------------- | -------------------------- |
| Serves static files | Runs business logic        |
| Handles HTTP        | Processes application code |
| Example: Nginx      | Example: ASP.NET Core      |

---

# 📤 What is a Request?

A **Request** is a message sent by the client to the server asking it to perform an operation.

Example:

```
User clicks Login

↓

POST /login
```

---

# HTTP Request Structure

```
POST /login HTTP/1.1

Headers

Body
```

---

# Common HTTP Methods

## GET

Retrieve data.

Example

```http
GET /products
```

---

## POST

Create new data.

```http
POST /users
```

---

## PUT

Replace existing data.

```http
PUT /users/10
```

---

## PATCH

Update partial data.

```http
PATCH /users/10
```

---

## DELETE

Delete data.

```http
DELETE /users/10
```

---

# 📥 What is a Response?

A response is the result returned by the server after processing the request.

Example

```json
{
    "success": true,
    "message": "Login Successful",
    "token": "JWT_TOKEN"
}
```

---

# Common HTTP Status Codes

| Code | Meaning               |
| ---- | --------------------- |
| 200  | OK                    |
| 201  | Created               |
| 204  | No Content            |
| 400  | Bad Request           |
| 401  | Unauthorized          |
| 403  | Forbidden             |
| 404  | Not Found             |
| 500  | Internal Server Error |

---

# Complete Client–Server Flow

```
User

↓

Browser / React

↓

HTTP Request

↓

Nginx

↓

ASP.NET Core API

↓

Business Logic

↓

SQL Server

↓

Business Logic

↓

JSON Response

↓

React

↓

User Screen
```

---

# Real Project Example (Village Delivery App)

```
User

↓

Mobile App / React

↓

GET /shops

↓

ASP.NET Core API

↓

SQL Server

↓

Shop List

↓

JSON Response

↓

React App

↓

User sees all nearby shops
```

---

# Cloud vs Server

Many beginners confuse Cloud Platforms with Servers.

| Cloud Platform        | Server? |
| --------------------- | ------- |
| AWS                   | ❌ No    |
| Microsoft Azure       | ❌ No    |
| Google Cloud Platform | ❌ No    |
| DigitalOcean          | ❌ No    |

Cloud providers offer infrastructure where you can deploy servers.

For example:

```
AWS

↓

EC2 Virtual Machine

↓

ASP.NET Core API

↓

SQL Server
```

Here:

* AWS = Cloud Platform
* EC2 = Server
* ASP.NET Core = Application

---

# Common Mistakes

❌ React = Backend

Wrong.

React is a Frontend Library.

---

❌ API = Database

Wrong.

API communicates with the database.

---

❌ Browser directly talks to Database

Wrong.

Communication should happen through APIs.

---

❌ AWS is a Server

Wrong.

AWS provides servers and cloud services.

---

# 🧠 Think Like an Engineer

Suppose your React application directly connects to SQL Server.

What problems will occur?

* Database credentials become public.
* Anyone can modify data.
* No business validation.
* Major security risk.

Therefore,

Always place an API between the Client and Database.

---

# 💼 Interview Questions & Answers

### Q1. What is a Client?

**Answer:**
A client is an application or device that initiates communication with a server by sending requests and displaying the server's response to the user.

---

### Q2. What is a Server?

**Answer:**
A server receives client requests, executes business logic, communicates with databases or other services, and returns the appropriate response.

---

### Q3. What is the difference between Client and Server?

| Client              | Server                  |
| ------------------- | ----------------------- |
| Sends requests      | Processes requests      |
| Displays UI         | Executes business logic |
| Runs on user device | Runs on remote machine  |

---

### Q4. Can React directly connect to SQL Server?

**Answer:**
No. React should communicate with a backend API, and the backend API communicates with the database.

---

### Q5. Is Postman a Client?

**Answer:**
Yes. Postman is an API client used to send HTTP requests and receive responses.

---

### Q6. Is AWS a Server?

**Answer:**
No. AWS is a cloud platform that provides services such as virtual machines (EC2), storage (S3), databases (RDS), and networking.

---

### Q7. Why do we need APIs?

**Answer:**
APIs provide a secure and structured way for clients to communicate with servers. They hide database implementation, enforce business rules, and improve security.

---

# 📝 Assignment

1. List 10 examples of Clients.
2. List 10 examples of Servers.
3. Explain the Client–Server Architecture in your own words.
4. Explain why React should not connect directly to SQL Server.
5. Draw the complete flow of your Village Delivery application.

---

# 📌 Key Takeaways

* A Client starts communication.
* A Server processes requests.
* Requests are sent using HTTP/HTTPS.
* Responses are returned by the server.
* APIs sit between clients and databases.
* Cloud platforms host servers but are not servers themselves.
* Understanding Client–Server Architecture is the foundation of modern web applications.

---

# 📚 Further Reading

* HTTP & HTTPS
* REST APIs
* Browser Architecture
* DNS
* TCP/IP
* Reverse Proxy (Nginx)
* Load Balancer
* Authentication & Authorization

#

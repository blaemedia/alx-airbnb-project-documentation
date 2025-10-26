
# 🏠 Airbnb Clone Backend — Detailed Requirement Specifications

This document outlines the **backend requirement specifications** for the Airbnb Clone Project.  
It includes the major modules, API endpoints, input/output specifications, validation rules, and performance benchmarks.

---



---

## 1️⃣ User Authentication System

### 🎯 **Objective**
Provide a secure user registration and login system using **JWT-based authentication** with role management for **Guests**, **Hosts**, and **Admins**.

---

### **API Endpoints**

| Method | Endpoint | Description |
|--------|-----------|-------------|
| `POST` | `/api/v1/auth/register` | Register a new user |
| `POST` | `/api/v1/auth/login` | Authenticate a user and issue a JWT token |
| `GET` | `/api/v1/auth/profile` | Fetch logged-in user profile (Protected) |
| `PUT` | `/api/v1/auth/profile` | Update user details |
| `POST` | `/api/v1/auth/logout` | Logout user and invalidate token |

---

### **Input / Output Specification**

#### 📝 **Register User**
**Request Body:**
```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "password": "StrongPass#2024",
  "role": "host"
}
`````
### *Response (201 - Created):*

```json
{
  "message": "User registered successfully",
  "user": {
    "id": "u1001",
    "name": "Jane Doe",
    "email": "jane@example.com",
    "role": "host"
  },
  "token": "jwt_token_here"
}
`````
### *🔐 Login User Request Body:*
```json
{
  "email": "jane@example.com",
  "password": "StrongPass#2024"
}
`````
### *Response (200 - OK):*
```json
{
{
  "message": "Login successful",
  "token": "jwt_token_here",
  "expiresIn": 3600
}
}
`````


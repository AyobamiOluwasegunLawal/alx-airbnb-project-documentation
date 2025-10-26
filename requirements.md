# 🏡 Airbnb Clone Backend - Requirement Specifications

This document outlines the detailed requirement specifications for three critical backend features of the **Airbnb Clone** project.  
The focus is on **User Authentication**, **Property Management**, and **Booking System**, including their API endpoints, input/output data, validation rules, and performance criteria.

---

## 🔐 1. User Authentication

### **Description**
Handles user registration, login, and authentication using JWT (JSON Web Token). Supports role-based access control for **Guests**, **Hosts**, and **Admins**.

### **API Endpoints**

| Method | Endpoint | Description |
|--------|-----------|-------------|
| `POST` | `/api/v1/auth/register` | Register a new user (guest or host). |
| `POST` | `/api/v1/auth/login` | Authenticate user credentials and issue a JWT token. |
| `GET` | `/api/v1/auth/profile` | Retrieve the authenticated user’s profile. |

---

### **Input / Output Specifications**

#### **POST /api/v1/auth/register**
**Input (JSON):**
```json
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john@example.com",
  "password": "StrongPass123!",
  "role": "host"
}


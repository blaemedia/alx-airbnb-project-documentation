# 🧩 Airbnb Clone Backend — User Stories

## 📘 Overview
This document translates the **use case diagram** for the Airbnb Clone backend into **Agile user stories**.  
Each story defines a feature or functionality from the user’s perspective, focusing on **who** the user is, **what** they want to do, and **why** it’s important.

---

## 👤 User Roles
- **Guest** – Users who book properties for accommodation.
- **Host** – Users who list their properties for rent.
- **Admin** – Platform administrators who monitor and manage users, listings, and payments.
- **Payment Gateway (External)** – Handles payment processing.
- **Email Service (External)** – Sends system notifications.

---

## 🧑‍💻 User Stories by Role

### **1. Guest User Stories**
| ID | User Story | Acceptance Criteria |
|----|-------------|--------------------|
| G1 | As a **guest**, I want to **register or log in** so that I can access my account and book properties. | Registration/login form validates input, issues JWT token upon success. |
| G2 | As a **guest**, I want to **search for properties** by location, price, and amenities so that I can find a suitable place to stay. | Search results update dynamically with filters. |
| G3 | As a **guest**, I want to **view detailed information** about a property so that I can make an informed decision before booking. | Each property page shows title, photos, price, reviews, and amenities. |
| G4 | As a **guest**, I want to **book a property** for specific dates so that I can reserve my stay. | Booking confirmation generated and stored in the database. |
| G5 | As a **guest**, I want to **make a secure payment** for my booking so that my reservation is confirmed. | Integration with Payment Gateway ensures payment verification. |
| G6 | As a **guest**, I want to **cancel a booking** (based on policy) so that I can modify my travel plans. | System checks cancellation rules before approval. |
| G7 | As a **guest**, I want to **review and rate** properties I’ve stayed in so that others can know about my experience. | Reviews are tied to completed bookings only. |
| G8 | As a **guest**, I want to **receive email notifications** for booking confirmations, cancellations, and payment updates. | Email Service automatically triggers relevant notifications. |

---

### **2. Host User Stories**
| ID | User Story | Acceptance Criteria |
|----|-------------|--------------------|
| H1 | As a **host**, I want to **register and verify my account** so that I can list my properties. | Verified host status required before adding listings. |
| H2 | As a **host**, I want to **add a new property listing** with photos, price, and description so that guests can find and book it. | Listing saved in the database and visible to guests. |
| H3 | As a **host**, I want to **edit or delete my property listings** so that I can manage availability or remove old listings. | Host-only access to their own listings. |
| H4 | As a **host**, I want to **view bookings** made on my properties so that I can prepare for guests. | Dashboard shows booking history and status. |
| H5 | As a **host**, I want to **receive payout (cash out)** after a guest’s stay so that I can earn income from my property. | Payment Gateway processes payout after booking completion. |
| H6 | As a **host**, I want to **respond to guest reviews** so that I can maintain my property reputation. | Only hosts of that property can respond. |
| H7 | As a **host**, I want to **receive notifications** when a new booking is made or canceled. | Real-time email or in-app notification triggered automatically. |

---

### **3. Admin User Stories**
| ID | User Story | Acceptance Criteria |
|----|-------------|--------------------|
| A1 | As an **admin**, I want to **view and manage all users** so that I can control access and handle disputes. | Admin dashboard lists all users with role-based controls. |
| A2 | As an **admin**, I want to **manage property listings** so that I can remove or approve inappropriate content. | Admin can update, deactivate, or delete listings. |
| A3 | As an **admin**, I want to **monitor bookings and payments** so that I can ensure smooth transactions. | Dashboard provides payment and booking summaries. |
| A4 | As an **admin**, I want to **view transaction history** so that I can audit platform revenue. | Payment logs retrievable and filterable by date/user. |
| A5 | As an **admin**, I want to **receive alerts** for failed payments or security breaches so that I can act quickly. | System logs and sends notifications to admin email. |

---

### **4. System & External Service Stories**
| ID | User Story | Acceptance Criteria |
|----|-------------|--------------------|
| S1 | As a **system**, I want to **store images and profile photos** in cloud storage so that file management is efficient. | Files uploaded to AWS S3 or Cloudinary. |
| S2 | As a **system**, I want to **send email notifications** for important events so that users stay informed. | Integration with SendGrid or Mailgun API. |
| S3 | As a **payment gateway**, I want to **verify and process all payments** so that funds are securely handled. | Payment API confirms success/failure before booking confirmation. |
| S4 | As a **system**, I want to **log errors and handle exceptions** so that debugging and maintenance are easy. | Centralized error handler and logs in the backend. |

---

## 🧠 Notes
- Each user story can be expanded into **tasks** for database design, API endpoint creation, and testing.  


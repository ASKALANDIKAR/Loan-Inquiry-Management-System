# 📊 Loan Inquiry Management System (Navkar Finance)

## 📌 Overview
The **Loan Inquiry Management System (Navkar Finance)** is a full-stack web application designed to efficiently manage loan inquiries for both customers and administrators.

Customers can submit loan applications and track their status in real time, while administrators can review, approve, or reject inquiries through a centralized dashboard featuring data visualization and status tracking.

---

## 🛠️ Tech Stack

### Frontend
- React.js  
- Bootstrap  
- React Router  
- React Toastify  
- Chart.js  

### Backend
- Spring Boot  
- Spring Data JPA  
- Spring Security (JWT)  

### Database
- MySQL  

### Build & Tools
- Maven (Backend)  
- npm (Frontend)  
- Postman  
- VS Code  
- IntelliJ IDEA  
- Git & GitHub  

---

## ✨ Features

### 👤 Customer Features
- Secure user registration and login  
- Submit loan inquiries through a validated form  
- View personal loan applications with real-time status updates  
- Receive updates for **Approved**, **Rejected**, or **Pending** loan requests  

### 🧑‍💼 Admin Features
- View all customer loan inquiries in a structured dashboard  
- Approve, reject, or keep loan inquiries pending  
- Visualize loan status distribution using **Chart.js pie charts**  
- Real-time data updates with toast notifications and auto-refresh  

---

## 🔒 Security
- JWT-based authentication and authorization  
- Encrypted user credentials stored in MySQL  
- Role-based access control for **Admin** and **Customer**  

---

## 🧩 API Endpoints

### 🔑 Authentication
| Method | Endpoint | Description |
|------|---------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive JWT token |

### 🧾 Loan Inquiries
| Method | Endpoint | Description |
|------|---------|-------------|
| POST | `/api/inquiries/inquiry` | Submit a new loan inquiry |
| GET | `/api/inquiries/my` | Get inquiries of the logged-in customer |
| PATCH | `/api/inquiries/{id}/status?status=APPROVED/REJECTED` | Update inquiry status (Admin only) |
| GET | `/api/inquiries` | Get all loan inquiries (Admin only) |

---

## 🧱 Project Structure

```text
LoanFinanceSystem/
├── backend/
│   ├── controller/        # REST Controllers (Auth & Loan Inquiries)
│   ├── service/           # Business Logic (LoanInquiryService)
│   ├── repository/        # JPA Repositories
│   ├── entity/            # Entity & Enum Classes (User, LoanInquiry, LoanStatus)
│   ├── LoanApplication.java
│   └── application.properties
│
├── frontend/
│   ├── components/        # React Components (Login, Register, Dashboard, etc.)
│   ├── services/          # Axios API Services
│   ├── App.js
│   └── package.json
│
└── README.md
```
---

## ⚙️ Installation & Setup

### 🧩 Backend Setup

1. Clone the repository:
```bash
git clone https://github.com/Tejas767/Loan-Inquiry-Management-System.git
cd backend
```

2. Configure your MySQL database in `application.properties`.

3. Run the backend server:
```bash
mvn spring-boot:run
```

📍 Backend runs at: **http://localhost:8080**

---

### 💻 Frontend Setup

1. Navigate to the frontend folder:
```bash
cd frontend
npm install
npm start
```

📍 Frontend runs at: **http://localhost:3000**

---

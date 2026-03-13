# 🏦 Unified Bank

<h3 align="center">
Full Stack Digital Banking System
</h3>

<p align="center">
Modern Fintech Platform built with FastAPI + React
</p>

<p align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Inter&size=22&duration=3000&color=6366F1&center=true&vCenter=true&width=700&lines=Full+Stack+Banking+System;FastAPI+Backend+Architecture;React+Fintech+Dashboard;Loan+%2B+FD+%2B+Credit+Card+Modules;Financial+Analytics+Engine;Production+Ready+Backend+Design">

</p>

<p align="center">

<img src="https://img.shields.io/badge/FastAPI-Backend-green?style=for-the-badge&logo=fastapi">
<img src="https://img.shields.io/badge/React-Frontend-blue?style=for-the-badge&logo=react">
<img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge&logo=postgresql">
<img src="https://img.shields.io/badge/Redis-Caching-red?style=for-the-badge&logo=redis">
<img src="https://img.shields.io/badge/Celery-Async%20Tasks-green?style=for-the-badge">
<img src="https://img.shields.io/badge/Docker-Containerized-blue?style=for-the-badge&logo=docker">

</p>

🚀 A modern **full-stack banking platform** built using **FastAPI, PostgreSQL, Redis, Celery, and React**.

This project simulates a real **digital banking environment** where users can manage accounts, perform transactions, apply for loans, create fixed deposits, use credit cards, and view financial analytics.

# ✨ Features

## 🔐 Authentication

* Secure user registration
* MPIN login system
* JWT authentication
* Account lock after multiple failed attempts

## 💳 Account Management

* Create bank accounts
* Multiple accounts per user
* Balance tracking


## 💸 Transactions

Users can perform:

* Deposit
* Withdraw
* Transfer between accounts

Transaction history works like a **bank passbook**.


## 🏦 Loans

Users can apply for loans with automatic **EMI calculation**.

Loan module includes:

* loan amount
* interest rate
* tenure
* EMI calculation
* remaining balance tracking


## 📈 Fixed Deposits

Investment simulation with:

* deposit amount
* interest rate
* tenure
* maturity calculation


## 💳 Credit Card System

Credit card module includes:

* card number generation
* credit limit
* used credit
* remaining credit tracking


## 📊 Financial Analytics

Dashboard provides:

* expense pie chart
* financial health score
* AI-generated financial tips


# 🧠 System Architecture

```
            React Frontend
                  │
                  │ REST API
                  ▼
             FastAPI Backend
                  │
            Service Layer
                  │
   ┌──────────────┼──────────────┐
   │              │              │
PostgreSQL      Redis          Celery
 Database       Cache       Background Jobs
   │                             │
   │                             ▼
   │                    Email Notifications
   │
   ▼
Banking Data Models
```

# ⚙️ Technology Stack

## Backend

* Python
* FastAPI
* PostgreSQL
* SQLAlchemy
* JWT Authentication

Infrastructure:

* Redis
* Celery
* Docker
* Nginx

## Frontend

* React
* Vite
* Recharts (analytics charts)
* Modern dashboard UI

# 📂 Project Structure

```
banking-system
│
├── backend
│   ├── app
│   │   ├── models
│   │   ├── schemas
│   │   ├── routes
│   │   ├── services
│   │   ├── middleware
│   │   ├── utils
│   │   └── analytics
│   │
│   ├── tasks
│   ├── docker
│   └── nginx
│
└── frontend
    ├── src
    │   ├── pages
    │   ├── components
    │   ├── services
    │   ├── layout
    │   └── charts
```


# 🧩 Backend Modules

```
Authentication
Accounts
Transactions
Loans
Fixed Deposits
Credit Cards
Analytics
Notifications
```

Architecture pattern:

```
Route → Service → Database Model
```

---

# 🔗 API Endpoints

## Authentication

```
POST /auth/register
POST /auth/login
GET  /auth/me
```

---

## Accounts

```
POST /accounts/create
GET  /accounts
```

## Transactions

```
POST /transactions/deposit
POST /transactions/withdraw
POST /transactions/transfer
GET  /transactions/history/{account_id}
```

## Loans

```
POST /loans/apply
GET  /loans
```

## Fixed Deposits

```
POST /fd/create
GET  /fd
```

## Credit Cards

```
POST /credit-card/apply
GET  /credit-card
```

## Analytics

```
GET /analytics
```

# 💰 EMI Calculation

Loan EMI formula:

```
EMI = P × r × (1+r)^n / ((1+r)^n − 1)
```

Where:

```
P = principal loan amount
r = monthly interest rate
n = tenure in months
```

# 🖥 Dashboard Preview

Navigation inside dashboard:

```
🏠 Dashboard
💳 Accounts
💸 Transfer
📜 Transactions
📈 Investments (FD)
💳 Credit Card
🏦 Loans
📊 Analytics
```

Analytics dashboard includes:

* Expense Breakdown Chart
* Financial Health Score
* AI Financial Tips

# 🚀 Running the Project

## Clone Repository

```
git clone https://github.com/yourusername/unified-bank.git
cd unified-bank
```

# Backend Setup

Create virtual environment

```
python -m venv venv
```

Activate environment

Mac / Linux

```
source venv/bin/activate
```

Windows

```
venv\Scripts\activate
```

Install dependencies

```
pip install -r requirements.txt
```

Run backend server

```
uvicorn app.main:app --reload
```

Backend runs at

```
http://127.0.0.1:8000
```

API docs

```
http://127.0.0.1:8000/docs
```

# Frontend Setup

Navigate to frontend

```
cd frontend
```

Install dependencies

```
npm install
```

Run frontend

```
npm run dev
```

Frontend runs at

```
http://localhost:5173
```

# 🛠 Infrastructure

### Redis

Used for:

* caching
* message queue

### Celery

Handles background tasks such as:

* email notifications
* async jobs

### Docker

Containerized deployment.

### Nginx

Acts as reverse proxy.

# 🔒 Security Features

* JWT authentication
* hashed MPIN storage
* login attempt limits
* account locking mechanism

# 📈 Future Improvements

Possible enhancements:

* real-time transaction updates using WebSockets
* fraud detection system
* mobile banking UI
* multi-factor authentication
* payment gateway integration

# 👨‍💻 Author

Meet Limbachiya
B.Tech CSE — Artificial Intelligence & Data Science

# ⭐ Support

If you found this project helpful, please consider giving it a **star ⭐ on GitHub**.

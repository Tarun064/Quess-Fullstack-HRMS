# HRMS Lite - Human Resource Management System

A professional, full-stack Human Resource Management System built with modern technologies. This application allows admins to manage employee records and track daily attendance with an intuitive, responsive interface.

## 🚀 Overview
HRMS Lite is designed for small to medium-sized organizations to streamline employee data management and daily attendance tracking. It provides a lightweight yet powerful solution with real-time updates and interactive dashboards.

## ✨ Features

### Employee Management
- **Add & Manage**: Register new employees with unique IDs, email addresses, and departments.
- **Dynamic Directory**: Search and filter employee records in a clean, interactive table.
- **Lifecycle Management**: Safely remove employee records with confirmation prompts.

### Attendance Tracking
- **Daily Check-ins**: Quickly mark employees as "Present" or "Absent" for any specific date.
- **Attendance History**: View historical records for individual employees or the entire organization.
- **Smart Filtering**: Filter by employee and date range (From/To) to track participation.
- **Live Summary**: Instantly see total "Present" and "Absent" counts when viewing an employee's record.

### Dashboard & Analytics
- **Key Metrics**: Real-time overview of total employees and attendance statistics.
- **Responsive UI**: Optimized for both desktop and mobile viewing with modern aesthetics.

## 🛠 Tech Stack

**Frontend:**
- **React 18** - UI library with functional components and hooks.
- **Vite** - Lightning-fast frontend build tool.
- **Vanilla CSS** - Custom, premium styling (no heavy frameworks).
- **React Router** - Seamless single-page application navigation.

**Backend:**
- **FastAPI** - High-performance Python web framework.
- **Motor** - Asynchronous driver for MongoDB.
- **Pydantic** - Robust data validation and settings management.

**Database:**
- **MongoDB** - Document-based NoSQL database for flexible data modeling.

---

## 📁 Project Structure

```text
hrms-lite/
├── backend/            # FastAPI Backend
│   ├── app/            # Application logic
│   │   ├── models/     # Pydantic/MongoDB schemas
│   │   ├── routers/    # API endpoints (Employees, Attendance)
│   │   └── main.py     # FastAPI entry point
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/           # React Frontend
│   ├── src/
│   │   ├── pages/      # Dashboard, Employees, Attendance
│   │   ├── components/ # Layout, Loading, Error states
│   │   ├── api/        # Axios-like custom client
│   │   └── App.jsx     # Main entry
│   ├── package.json
│   └── .env.example
│
└── README.md           # This file
```

---

## ⚡ Quick Start

### Prerequisites
- **Node.js 18+** & npm
- **Python 3.10+**
- **MongoDB** (Local instance or Atlas URI)

### Backend Setup
1. **Navigate & Setup ENV**:
   ```bash
   cd backend
   copy .env.example .env  # Edit with your MONGODB_URI
   ```
2. **Virtual Environment**:
   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # Mac/Linux:
   source venv/bin/activate
   ```
3. **Install & Run**:
   ```bash
   pip install -r requirements.txt
   uvicorn app.main:app --reload
   ```
   *Docs available at `http://localhost:8000/docs`*

### Frontend Setup
1. **Navigate & Setup ENV**:
   ```bash
   cd frontend
   copy .env.example .env  # Set VITE_API_URL=http://localhost:8000
   ```
2. **Install & Run**:
   ```bash
   npm install
   npm run dev
   ```
   *App available at `http://localhost:5173`*

---

## 🔒 Security & Validation
- **CORS Support**: Origin restricted to allowed frontend URLs.
- **Unique Constraints**: Prevent duplicate Employee IDs and Emails.
- **Input Sanitization**: Pydantic models ensure data integrity on every request.

---

## 🚢 Deployment & Environment
- **Backend**: Suitable for Render, Railway, or Vercel (using serverless functions).
- **Frontend**: Best hosted on Vercel or Netlify.
- **Database**: Recommended to use MongoDB Atlas for production.

## 📝 Assumptions & Limitations
- **Auth**: Currently an admin-only system without user login.
- **Identity**: Employee ID is assumed to be a business-level unique identifier.
- **Scope**: Focused on core HR needs (Records + Attendance); Payroll/Leaves are current limitations.

---
*Developed as part of the Quess Assessment.*

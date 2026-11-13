# Aura Dental Clinic Management & Patient Engagement Platform

[![Repository](https://img.shields.io/badge/GitHub-JeevananthanV%2Fdental__clinic-blue?logo=github)](https://github.com/JeevananthanV/dental_clinic)
[![Next.js](https://img.shields.io/badge/Next.js-16%20(App%20Router)-black?logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![Express](https://img.shields.io/badge/Backend-Node%20%2B%20Express-339933?logo=express&logoColor=white)](https://expressjs.com)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB%20%2B%20Mongoose-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com)

A modern, production-ready, full-stack dental clinic web application designed to streamline clinic operations, automate appointment scheduling, and enhance patient engagement.

---

## 🔗 Repository Links

| Detail | Link |
|---|---|
| **GitHub Repository** | [https://github.com/JeevananthanV/dental_clinic](https://github.com/JeevananthanV/dental_clinic) |
| **Author** | [Jeevananthan V](https://github.com/JeevananthanV) |
| **Frontend Portal** | `http://localhost:3000` |
| **Backend API** | `http://localhost:5000/api` |

---

## 🚀 Overview

**Aura Dental** is a comprehensive dental clinic software solution. It bridges the gap between patient-facing clinic marketing and internal clinical administration. By integrating a high-performance, SEO-optimized **Next.js 16** frontend with a secure, scalable **Express.js & MongoDB** backend, the platform automates booking workflows, secures patient records, and simplifies content management for clinic administrators.

---

## 🛠️ Tech Stack

### Frontend (Client)
- **Framework**: Next.js 16 (App Router), React 19
- **Styling**: Tailwind CSS (v4)
- **Animations**: Framer Motion & GSAP (for premium animations and micro-interactions)
- **Form Handling & Validation**: React Hook Form & Zod

### Backend (Server)
- **Runtime**: Node.js & Express.js
- **Database**: MongoDB with Mongoose ODM
- **Media Storage**: Cloudinary (media upload assets)
- **Email Notifications**: Nodemailer (SMTP)
- **Security & Protection**: JSON Web Tokens (JWT) with Refresh Tokens, BCrypt.js (password hashing), Helmet (HTTP headers protection), Express Rate Limit, Express Mongo Sanitize, and XSS Clean

---

## ✨ Key Features

### 🦷 Patient Portal
- **Dynamic Landing Page**: Showcases treatments, client reviews, meet the doctors, and interactive trust metrics.
- **Treatment Explorer**: Dedicated, dynamic pages for service categories (Diagnostics & Care, Restorations, and Cosmetic/Specialized).
- **Appointment Booking Engine**: Interactive forms with validation to book appointments.
- **Patient Insights & Care**: Resource pages for FAQs, testimonials, dental insights (blog), and insurance info.

### 🛡️ Admin Command Center
- **Dynamic Dashboard**: Quick overview statistics (total appointments, patients, pending requests, and new messages).
- **Appointment Manager**: Change status (Pending, Confirmed, Cancelled, Completed) with automatic email notifications.
- **Patient Management Database**: Manage patient records, contact history, and historical appointments.
- **CMS Controller**: Direct panels to manage treatment listings, update FAQ items, upload testimonials, and change clinic-wide configurations (e.g. business hours, contact numbers).
- **Audit & Security Logs**: Tracks administrative activity logs to maintain operational accountability.

---

## 📦 Project Directory Structure

```
Dental_Clinic/
├── app/                  # Next.js App Router (Pages, layouts, styles)
├── components/           # Reusable React components
├── constants/            # Client-side constants & static configurations
├── hooks/                # Custom React hooks
├── lib/                  # Shared utilities and libraries (e.g. API clients)
├── public/               # Static assets (images, icons, etc.)
├── server/               # Express.js backend API
│   ├── config/           # Database and system configs
│   ├── controllers/      # Route controllers (auth, appointments, CMS, etc.)
│   ├── middleware/       # JWT auth, rate-limit, security, and error handling
│   ├── models/           # Mongoose schemas & database models
│   ├── routes/           # RESTful API route endpoints
│   ├── services/         # Third-party integrations (Nodemailer, Cloudinary)
│   ├── validators/       # Input request validators (Joi)
│   └── server.js         # Backend entry point
├── CASE_STUDY.md         # Comprehensive clinic case study
└── README.md
```

---

## ⚙️ Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18.x or higher recommended)
- [MongoDB](https://www.mongodb.com/) (running locally or MongoDB Atlas URI)

---

## 🔧 Installation & Setup

### Clone Repository

```bash
git clone https://github.com/JeevananthanV/dental_clinic.git
cd dental_clinic
```

### 1. Setup the Environment Variables

#### Client (Root Folder)
Create `.env.local` based on `.env.example`:
```bash
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

#### Server (`/server` Folder)
Navigate to `/server` and create `.env` based on `server/.env.example`:
```bash
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_REFRESH_SECRET=your_jwt_refresh_secret_key
```

### 2. Run the Application

#### Start Backend Server
```bash
cd server
npm install
npm run dev
```

#### Start Frontend Client
In a new terminal window:
```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

---

## 👨‍💻 Author

**Jeevananthan V** — [@JeevananthanV](https://github.com/JeevananthanV)

## License

MIT

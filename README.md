# Aura Dental Clinic Management & Patient Engagement Platform

A modern, production-ready, full-stack web application designed to streamline clinic operations, automate appointment scheduling, and enhance patient engagement.

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
```

---

## ⚙️ Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18.x or higher recommended)
- [MongoDB](https://www.mongodb.com/) (running locally or MongoDB Atlas URI)

---

## 🔧 Installation & Setup

### 1. Setup the Environment Variables

Configure both the Client and Server by creating environment files from the provided examples.

#### Client (Root Folder)
Create a `.env` or `.env.local` file at the root directory and copy the contents of `.env.example`:
```bash
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

#### Server (`/server` Folder)
Navigate to the `/server` folder, create a `.env` file, and fill in the placeholders based on `server/.env.example`:
```bash
# Server port & details
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000

# Database
MONGO_URI=your_mongodb_connection_string

# Authentication
JWT_SECRET=your_jwt_secret_key
JWT_REFRESH_SECRET=your_jwt_refresh_secret_key

# Third-party Services (Cloudinary & SMTP Email)
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

EMAIL_HOST=smtp.mailtrap.io
EMAIL_PORT=2525
EMAIL_USER=your_smtp_user
EMAIL_PASS=your_smtp_password
```

### 2. Run the Application

You must run the Frontend and the Backend concurrently.

#### Start Backend Server
```bash
cd server
npm install
npm run dev
```

#### Start Frontend Client
In a new terminal window, navigate back to the root directory:
```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the application running.

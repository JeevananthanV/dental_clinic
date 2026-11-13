# Aura Dental Clinic — Setup Guide

Welcome to the **Aura Dental Clinic Management Platform** setup guide. This system features a Next.js 16 (App Router) frontend and an Express.js + MongoDB backend.

- **GitHub Repository**: [https://github.com/JeevananthanV/dental_clinic](https://github.com/JeevananthanV/dental_clinic)
- **Author**: Jeevananthan V

---

## 📋 System Prerequisites

- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher
- **MongoDB**: Local MongoDB instance or MongoDB Atlas URI

---

## 📥 1. Clone the Repository

```bash
git clone https://github.com/JeevananthanV/dental_clinic.git
cd dental_clinic
```

---

## ⚙️ 2. Environment Variables Configuration

### Server Environment (`server/.env`)

```env
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=aura_dental_secret_jwt_2026
JWT_REFRESH_SECRET=aura_dental_refresh_jwt_2026
```

### Client Environment (`.env.local`)

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

---

## 📦 3. Install Dependencies

```bash
# 1. Install Backend Dependencies
cd server
npm install

# 2. Install Frontend Dependencies
cd ..
npm install
```

---

## 🚀 4. Running Locally

### Terminal 1: Backend Server (Port 5000)

```bash
cd server
npm run dev
```

### Terminal 2: Frontend Client (Port 3000)

```bash
npm run dev
```
Open `http://localhost:3000` in your browser.

---

## 🏗️ 5. Production Build

```bash
npm run build
```

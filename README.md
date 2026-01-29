# DASGUPTA MAITI & ASSOCIATES - CA Consultancy Platform

![MERN Stack](https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge&logo=mongodb)
![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production%20Ready-blue?style=for-the-badge)

A comprehensive, full-stack web application designed for **Dasgupta Maiti & Associates**, a premier Chartered Accountancy firm. This platform streamlines client interactions, document management, and career opportunities, providing a modern digital presence for the firm.

## 🚀 Project Overview

This project is a bespoke web solution built using the **MERN Stack (MongoDB, Express.js, React.js, Node.js)**. It features a dynamic Content Management System (CMS) that allows the firm to manage services, publications, news, and career applications efficiently.

### ✨ Key Features

*   **Dynamic CMS**: Fully integrated admin panel to manage:
    *   **Services**: Add, update, or remove professional services.
    *   **Newsroom**: Post latest financial updates and firm news.
    *   **Publications**: Upload and share resources (PDFs, docs).
    *   **Careers**: Post job openings and manage incoming applications.
*   **Secure Authentication**: Role-based access control (RBAC) with **JWT** and **Bcrypt** for secure admin management.
*   **Media Management**: Seamless image and document uploads using **Cloudinary**.
*   **Smart Search**: Global search functionality to find resources, services, and news instantly.
*   **Advanced Contact System**: Integrated with **Nodemailer** and **Zoho Mail API** for reliable client communication.
*   **SEO Optimized**: Built with `react-helmet-async` for optimal search engine visibility.
*   **Responsive Design**: Fully responsive UI built with **React Bootstrap**, ensuring a seamless experience across all devices.

## 🛠️ Tech Stack

### Frontend
*   **Core**: React.js, ReactDOM
*   **Styling**: React Bootstrap, CSS3
*   **State & Routing**: React Router DOM
*   **Utilities**: Axios, Lucide React, React Icons, React Toastify
*   **SEO**: React Helmet Async

### Backend
*   **Runtime**: Node.js
*   **Framework**: Express.js
*   **Database**: MongoDB (Mongoose ODM)
*   **Authentication**: JSON Web Token (JWT), BcryptJS
*   **File Storage**: Cloudinary, Multer
*   **Email Services**: Nodemailer, Zoho Mail API
*   **Validation**: Express Validator

## 🔧 Installation & Setup

Follow these steps to set up the project locally.

### Prerequisites
*   Node.js (v16+)
*   MongoDB (Local or Atlas URI)
*   Cloudinary Account
*   Zoho Mail Account (for email features)

### 1. Clone the Repository
```bash
git clone https://github.com/premrajsingh/CAweb.git
cd CAweb
```

### 2. Install Dependencies
Install dependencies for both backend and frontend:

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..
```

### 3. Environment Configuration
Create a `.env` file in the root directory and configure the following variables:

```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Cloudinary (File Uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Security
JWT_SECRET=your_secure_jwt_secret
NODE_ENV=development

# URLs
BASE_URL=http://localhost:5000
FRONTEND_URL=http://localhost:3000

# Email Service (Zoho Mail)
SMTP_HOST=smtp.zoho.com
SMTP_PORT=587
SMTP_USER=your_email@domain.com
SMTP_PASS=your_password
SMTP_FROM=your_email@domain.com
ADMIN_EMAIL=admin_email@domain.com

# Zoho API (Optional: For advanced mail features)
ZOHO_CLIENT_ID=your_client_id
ZOHO_CLIENT_SECRET=your_client_secret
ZOHO_REFRESH_TOKEN=your_refresh_token
ZOHO_ACCOUNT_ID=your_account_id
ZOHO_EMAIL=your_zoho_email
```

### 4. Run the Application

**Development Mode:**
Run both backend and frontend concurrently:
```bash
npm run dev
```

**Production Build:**
```bash
npm run build
npm start
```

## 📂 Project Structure

```bash
├── backend/            # Express.js Backend
│   ├── models/         # Mongoose Schemas (Admin, Service, Career, etc.)
│   ├── routes/         # API Routes (Auth, Contact, Services, etc.)
│   ├── controllers/    # Request Handlers
│   ├── middleware/     # Auth & Error Middleware
│   └── utils/          # Helper functions (Email, Cloudinary)
├── frontend/           # React.js Frontend
│   ├── public/         # Static assets
│   └── src/            # Components, Pages, and Assets
├── dist/               # Production Build
└── project_deploy/     # Deployment scripts and configurations
```

## 📬 API Documentation

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/auth/login` | POST | Admin login |
| `/api/services` | GET/POST | Manage consultancy services |
| `/api/careers` | GET/POST | Manage job postings |
| `/api/contact` | POST | Submit contact form |
| `/api/publications` | GET/POST | Manage firm publications |

## 🚀 Deployment

This project is configured for deployment on **Render** or **Railway**.
- `render.yaml` included for Infrastructure as Code (IaC) deployment on Render.
- `railway.json` included for Railway deployment.

Ensure all environment variables are correctly set in your deployment dashboard.

---
**Developed by Prem Raj Singh**

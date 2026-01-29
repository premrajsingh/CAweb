# DASGUPTA MAITI & ASSOCIATES - CA Consultancy Platform

<div align="center">
  <img src="frontend/public/cawebsite_logo.png" alt="DMA Logo" width="200"/>
  <br/>
  
  [![MERN Stack](https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge&logo=mongodb)](https://mongodb.com)
  [![React](https://img.shields.io/badge/React-18.x-blue?style=for-the-badge&logo=react)](https://reactjs.org)
  [![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org)
  [![Live Demo](https://img.shields.io/badge/Demo-Live_Site-FF5722?style=for-the-badge&logo=googlechrome)](https://dasguptamaitiassociates.com/)
</div>

---

## 🚀 Executive Summary

**Dasgupta Maiti & Associates (DMA)** is a high-performance, full-stack web platform engineered to digitize the operations of a premier Chartered Accountancy firm. 

This project goes beyond a simple website; it is a **comprehensive digital office** featuring a custom-built Content Management System (CMS), secure role-based authentication, and an automated deployment pipeline. It serves as the central hub for client interactions, financial auditing services, and firm-wide resource management.

> **Key Achievement**: Implemented a scalable "Search-First" architecture ensuring 100% discoverability of financial regulations and firm services.

---

## 🏗️ System Architecture

The application follows a modern **Service-Oriented Architecture (SOA)**, separating concerns between a responsive frontend and a robust API-first backend.

```mermaid
graph TD
    User((User/Client))
    Admin((Firm Admin))
    
    subgraph Frontend [React.js Client]
        UI[Responsive UI]
        Router[React Router]
        State[Axios / Context API]
    end
    
    subgraph Backend [Node.js & Express API]
        Auth[Auth Middleware (JWT)]
        Controllers[Business Logic]
        Services[Email & File Services]
    end
    
    subgraph Data_Layer [Persistence & Storage]
        MongoDB[(MongoDB Atlas)]
        Cloudinary[Cloudinary Media]
    end
    
    subgraph External [Third Party Services]
        Zoho[Zoho Mail API]
    end

    User -->|HTTPS| UI
    Admin -->|Secure Login| UI
    UI -->|JSON API| Auth
    Auth -->|Validated Request| Controllers
    Controllers -->|CRUD| MongoDB
    Controllers -->|Aggregations| MongoDB
    Services -->|Uploads| Cloudinary
    Services -->|SMTP/API| Zoho
```

---

## ✨ Engineering Highlights

### 1. 🛡️ Enterprise-Grade Security
*   **RBAC (Role-Based Access Control)**: Custom middleware ensures only authorized partners can access sensitive admin panels.
*   **JWT Authentication**: Stateless authentication with `bcrypt` encryption for password hashing.
*   **Secure Headers**: Implemented `cors` and best-practice security headers to prevent XSS and injection attacks.

### 2. ⚡ Automated Deployment Pipeline
Designed a custom **DevOps script** (`deploy_prep.sh`) to streamline the build and deployment process:
*   **One-Click Build**: Automatically builds the React frontend and bundles it with the Node.js backend.
*   **Artifact Optimization**: Excludes dev-dependencies and generates a clean `project_deploy.zip` ready for cPanel/GoForHost deployment.
*   **Environment Safety**: Automatically handles `.env` exclusion for security during transport.

### 3. 🔍 Advanced SEO & Discovery
*   **Dynamic Metadata**: Utilized `react-helmet-async` to inject dynamic meta-tags for every service and news article, ensuring high visibility on search engines.
*   **Sitemap Generation**: Custom backend route `/sitemap.xml` dynamically generates XML maps for Google indexing.
*   **Global Search**: Integrated a MongoDB aggregation pipeline to perform full-text search across Services, News, and Publications simultaneously.

### 4. 📧 Reliable Communication Infrastructure
*   **Failover Email System**: Integrated **Zoho Mail API** as a robust alternative to standard SMTP, solving common `ETIMEDOUT` issues on cloud hosting platforms like Render.
*   **Contact Form Intelligence**: Validates user inputs with `express-validator` before processing requests.

---

## 📸 Application Gallery

| **Modern Dashboard** | **Dynamic Newsroom** |
|:---:|:---:|
| <img src="frontend/public/desktop-bg-final-v3.png" width="400" alt="Home Hero"/> | <img src="frontend/public/newsroom.jpg" width="400" alt="Newsroom"/> |
| *High-conversion Landing Page* | *Real-time Financial Updates* |

---

## 🛠️ Technical Stack

| Component | Technology | Description |
|-----------|------------|-------------|
| **Frontend** | **React.js** | Functional components, Hooks, Custom Context. |
| **Styling** | **React Bootstrap** | Responsive grid system and accessible components. |
| **Backend** | **Node.js + Express** | High-throughput async REST API. |
| **Database** | **MongoDB (Mongoose)** | NoSQL schema design with complex relationships. |
| **File Storage** | **Cloudinary** | Optimized CDNs for serving PDF publications & images. |
| **Email** | **Nodemailer + Zoho** | Transactional email delivery. |

---

## 📂 Project Structure

```bash
├── backend/
│   ├── models/         # Database Schemas (Strict Typing)
│   ├── middleware/     # Auth & Error Handling Interceptors
│   ├── routes/         # RESTful API Endpoints
│   └── utils/          # Reusable Helper Functions
├── frontend/
│   ├── src/
│   │   ├── pages/      # Page Views
│   │   └── components/ # Reusable UI Blocks
├── deploy_prep.sh      # ⚡ Custom CI/CD Build Script
└── README.md           # Documentation
```

## 🔧 Setup & Installation

**Prerequisites:** Node.js v16+, MongoDB URI.

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/premrajsingh/CAweb.git
    cd CAweb
    ```

2.  **Install & Configure**
    ```bash
    npm install              # Install backend deps
    cd frontend && npm install # Install frontend deps
    ```

3.  **Run Development Server**
    ```bash
    # Runs both React & Node simultaneously
    npm run dev
    ```

---

## 📬 Contact to Recruiters

This project demonstrates my ability to build **production-ready, full-stack applications** solving real-world business problems. I am ready to bring this same engineering rigor to your team.

**Prem Raj Singh**  
[GitHub Profile](https://github.com/premrajsingh)

# DASGUPTA MAITI & ASSOCIATES - CA Consultancy Platform

<div align="center">
  <img src="frontend/public/cawebsite_logo.png" alt="DMA Logo" width="200"/>
  <br/>
  
  [![MERN Stack](https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge&logo=mongodb)](https://mongodb.com)
  [![React](https://img.shields.io/badge/React-18.x-blue?style=for-the-badge&logo=react)](https://reactjs.org)
  [![Node.js](https://img.shields.io/badge/Node.js-18.x-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org)
  [![Live Demo](https://img.shields.io/badge/Demo-Live_Site-FF5722?style=for-the-badge&logo=googlechrome)](https://dasguptamaitiassociates.com/)
  ![Project Type](https://img.shields.io/badge/Project%20Type-Freelance%20%2F%20Commercial-blueviolet?style=for-the-badge)
</div>

---

## 🚀 Executive Summary

**Dasgupta Maiti & Associates (DMA)** is a high-performance, full-stack commercial web platform engineered to digitize the operations of a premier Chartered Accountancy firm.

> 💼 **Freelance Project**: This application was designed, developed, and delivered as a **freelance solution** for the client *Dasgupta Maiti & Associates*. It is currently deployed and serving as their official digital presence. 

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
*   **Unified Search Engine**: Integrated a multi-collection search utility to perform case-insensitive lookups across Services and Publications.
*   **Automated Sitemaps**: Dynamic XML generation for search engine crawlers.

### 4. 📧 Resilient Communication Infrastructure
*   **Zoho REST API Integration**: Implemented a modern OAuth2-based mail system using Zoho's REST API. This ensures high-deliverability and bypasses common SMTP port restrictions (e.g., Port 587/465 blocks) on cloud platforms like Render.com.
*   **Input Validation**: Integrated `express-validator` to ensure data integrity for contact forms and career applications.

### 5. 🛠️ Intelligent Data Migration
*   **PDF Service Importer**: Developed a custom utility (`pdfImporter.js`) using `pdf-parse` to programmatically extract and structure service data from legacy PDF documents, converting them into Mongoose-ready seed files.

---

## 📸 Application Gallery

| **Production Home** | **Expert Insights** |
|:---:|:---:|
| <img src="frontend/public/home_bg_new.png" width="400" alt="Home Hero"/> | <img src="frontend/public/newsroom.jpg" width="400" alt="Newsroom"/> |
| *Unified Commercial Platform* | *Real-time Regulatory Updates* |

---

## 🛠️ Technical Stack

| Component | Technology | Role |
|-----------|------------|-------------|
| **Frontend** | **React.js 18** | Functional architecture with Context API for state management. |
| **Styling** | **React Bootstrap** | Responsive design with custom glassmorphism components. |
| **Backend** | **Node.js + Express** | Scalable RESTful API with automated static serving. |
| **Database** | **MongoDB (Mongoose)** | Complex NoSQL schemas with Slug-based routing. |
| **File Systems** | **Cloudinary + Multer** | Cloud-based media management and PDF parsing. |
| **Emailing** | **Nodemailer + Zoho** | Fail-safe transactional email delivery system. |

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

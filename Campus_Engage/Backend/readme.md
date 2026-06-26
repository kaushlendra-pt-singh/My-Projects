# CampusEngage 🎓
> A distributed, full-stack campus engagement and dynamic networking platform engineered for high-performance student interaction and secure, stateless authentication.

[![React](https://img.shields.io/badge/Frontend-React%20%28Vite%29-61dafb?logo=react)](https://react.dev/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js%20%2F%20Express-339933?logo=node.js)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB%20Atlas-47a248?logo=mongodb)](https://www.mongodb.com/cloud/atlas)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🚀 Architectural Overview

CampusEngage is architected as a decoupled, full-stack application leveraging a highly responsive **React 18 (Vite)** single-page application client and a distributed **Express/Node.js** backend API endpoint cluster. The system is designed from the ground up to solve engagement latency, secure stateful transitions across multi-role student categories, and scale database traffic efficiently.

### Key Engineering Highlights:
*   **Stateless JWT Authentication:** Implemented an enterprise-grade authentication pipeline utilizing secure JSON Web Tokens (JWT) distributed via HTTP-only, SameSite cookies to mitigate XSS and CSRF vulnerabilities.
*   **Database Scalability:** Migrated legacy relational structures to highly optimized **MongoDB Atlas hosted clusters**, designing precise indexing schemas on compound fields to significantly minimize query search times during concurrent peak campus traffic.
*   **Robust Security Routing:** Engineered server-side route-protection middleware and configured automated Cross-Origin Resource Sharing (CORS) whitelisting to safeguard distributed API pathways.

---

## 🛠️ Tech Stack

*   **Frontend:** React.js (Vite), Tailwind CSS, Framer Motion, Context API / Axios Client
*   **Backend:** Node.js, Express.js, JWT Auth, Cors, Dotenv
*   **Database & Storage:** MongoDB Atlas (Mongoose ODM)
*   **Deployment & Infrastructure:** Render (Backend API Cluster), Netlify / Vercel (Frontend Client hosting)

---

## 🗺️ System Architecture Diagram

```text
  [ React (Vite) Client ] 
            │
            ▼  (HTTPS / Secure HTTP-Only JWT Cookies)
    [ Express API Gateway ]
            │
    ┌───────┴───────┐
    ▼ (Middleware)  ▼ (Controllers)
 [CORS / Auth]   [Routing Engine]
                    │
                    ▼ (Mongoose ODM)
         [ MongoDB Atlas Cluster ]

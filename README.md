# Patient Registration & Telemedicine Architecture (KPPMCH)

**70–80% Registration Time Reduction | PDPA-Compliant | Municipal-Scale Deployment**

A high-performance, serverless registration framework and telemedicine platform engineered to bridge the gap between public healthcare intake and internal clinical workflows via real-time data synchronization.

[![Next.js](https://img.shields.io/badge/Frontend-Next.js-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![Google Apps Script](https://img.shields.io/badge/Backend-Google_Apps_Script-4285F4?style=flat-square&logo=google-apps-script&logoColor=white)](https://developers.google.com/apps-script)
[![Status](https://img.shields.io/badge/Status-Production_Ready-green?style=flat-square)](https://kppmch-register.vercel.app/PatientRegister)
[![Adopted By](https://img.shields.io/badge/Adopted_By-Kamphaeng_Phet_Municipality-28a745?style=flat-square&logo=government)](https://www.kppmu.go.th/news-detail?hd=1&id=124000)

---

## 1. Executive Overview
**KPPMCH** is a robust telemedicine and registration ecosystem designed for **Municipal-Scale healthcare services**. By utilizing a **Serverless Architecture**, the system mitigates hospital congestion and enhances data transmission efficiency between citizens and medical personnel through real-time synchronization across the municipal district.

---

## 2. System Architecture & Data Flow
The system employs a **Decoupled Serverless Pattern** to ensure high availability, low latency, and zero-infrastructure overhead. This architecture is purpose-built to handle high-concurrency registration events within a clinical environment.

### 🔄 Logical Data Flow
```mermaid
graph TD
    A[Patient / User] -->|1. Interaction / Notification| B[LINE Messaging API]
    B -->|2. Webhook / Redirect| C[Next.js Application]
    C -->|3. Data Validation & Submission| D[RESTful API - Google Apps Script]
    D -->|4. ACID Transaction| E[(Google Sheets Database)]
    E -->|5. Real-time Update| F[Nursing Station / Clinical Staff]
    F -->|6. Status Notification| B

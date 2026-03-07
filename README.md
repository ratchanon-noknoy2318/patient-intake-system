# Patient Registration & Telemedicine Architecture (KPPMCH)

**70–80% Registration Efficiency Gain | PDPA-Compliant | Municipal-Scale Deployment**

A high-performance, serverless registration framework and telemedicine platform engineered to bridge the gap between public healthcare intake and internal clinical workflows via real-time data synchronization.

[![Next.js](https://img.shields.io/badge/Frontend-Next.js-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![Google Apps Script](https://img.shields.io/badge/Backend-Google_Apps_Script-4285F4?style=flat-square&logo=google-apps-script&logoColor=white)](https://developers.google.com/apps-script)
[![Status](https://img.shields.io/badge/Status-Production_Ready-green?style=flat-square)](https://kppmch-register.vercel.app/PatientRegister)
[![Adopted By](https://img.shields.io/badge/Adopted_By-Kamphaeng_Phet_Municipality-28a745?style=flat-square&logo=government)](https://www.kppmu.go.th/news-detail?hd=1&id=124000)

---

## 1. Executive Overview
**KPPMCH** is a robust telemedicine and registration ecosystem designed for **Municipal-Scale healthcare services**. By utilizing a **Serverless Architecture**, the system mitigates hospital congestion and enhances data transmission efficiency between citizens and medical personnel through real-time synchronization across the municipal district.

---

## 2. System Architecture & Design Philosophy

The architecture adheres to **Serverless Principles**, prioritizing horizontal scalability and low operational overhead. By decoupling the ingestion layer from the persistence layer, the system ensures data integrity even during high-concurrency registration spikes.

### 🔄 Architectural Flow (Sequential Ingestion)
```mermaid
graph TD
    User[Patient / User] -->|1. Interaction| LINE_In[LINE Messaging API]
    LINE_In -->|2. Redirect| WebApp[Next.js Application]
    WebApp -->|3. Data Validation| API[RESTful API - Google Apps Script]
    API -->|4. ACID Transaction| DB[(Cloud Persistence Layer)]
    DB -->|5. Trigger Alert| Notify[LINE Messaging Gateway]
    Notify -->|6. Triage Delivery| Nursing[LINE Flex Message Interface]

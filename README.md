# Telemedicine Intake System

Production-grade telemedicine intake platform deployed in a real hospital, reducing patient intake workload by 80%.

![System Screenshot](https://kppmch-register.vercel.app/og-image.png)

Live System: https://kppmch-register.vercel.app/PatientRegister  
Deployment Reference: https://www.kppmu.go.th/news-detail?hd=1&id=124000  

---

## Overview

A production-ready web platform that digitizes and automates patient intake and pre-consultation workflows for telemedicine services.

The system replaces manual, paper-based processes with a structured, reliable, and scalable intake pipeline used in real municipal healthcare operations.

---

## Impact

- 80% reduction in patient intake workload  
- Eliminated paper-based workflows  
- Improved data consistency and accuracy  
- Accelerated pre-consultation processing time  
- Deployed in live hospital operations  

---

## Problem

Traditional telemedicine intake workflows relied on manual processes:

- Paper-based registration and consent  
- Manual data entry  
- Inconsistent pre-consultation screening  

Resulting in:

- Operational bottlenecks  
- Delays in patient processing  
- High administrative overhead  
- Increased risk of human error  

---

## Solution

Designed and implemented a centralized intake system that automates the entire onboarding workflow:

- Digital patient registration with structured forms  
- Real-time validation for accurate data collection  
- Automated data pipeline  
- Centralized and accessible data storage  
- Pre-consultation data availability for healthcare staff  

---

## Architecture


```
[Patient]
    ↓
[Next.js (Frontend + API Routes)]
    ↓
[Validation Layer]
    ↓
[Google Sheets (Storage)]
    ↓
[Healthcare Staff]
```


---

## Tech Stack

**Application Layer**
- Next.js (App Router)  
- Node.js  

**Data Layer**
- Google Sheets API  

**UI**
- TailwindCSS  

---

## Engineering Decisions

**Google Sheets as a data store**
- Enabled rapid deployment with minimal infrastructure  
- Provided direct access for non-technical stakeholders  
- Reduced system complexity  

**Monolithic Next.js architecture**
- Simplified development and deployment  
- Supported rapid iteration cycles  

**Form-driven workflow**
- Aligned with real clinical intake processes  
- Minimized training requirements  
- Ensured structured and consistent data  

---

## Challenges

- Handling inconsistent and unstructured user input  
- Designing for non-technical healthcare staff  
- Maintaining data accuracy for clinical usage  
- Integrating into existing workflows without disruption  
- Balancing simplicity with production reliability  

---

## Deployment

Deployed and actively used in municipal telemedicine operations in Kamphaeng Phet, Thailand.  
The system supports real-world patient intake and pre-consultation workflows in a live healthcare environment.

---

## Project Structure


```
/app    → Next.js application (UI, routing, API routes)
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone <REPO_URL>
cd <PROJECT_FOLDER>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run development server

```bash
npm run dev
```

---

## References

* Municipal deployment reference: https://www.kppmu.go.th/news-detail?hd=1&id=124000

---

## Author

**Ratchanon Noknoy**
Software Engineer

---

## License

MIT License © 2025–2026 Ratchanon Noknoy

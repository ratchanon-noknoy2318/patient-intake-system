# Telemedicine Intake System

A production-grade web platform for automating patient intake and pre-consultation screening in telemedicine workflows.

![Municipal Deployment](https://img.shields.io/badge/Deployment-Active%20in%20Kamphaeng%20Phet-brightgreen)  

Designed to streamline patient onboarding, reduce administrative overhead, and provide healthcare staff with structured patient data prior to consultations.

Deployed and actively used in municipal healthcare operations in Kamphaeng Phet, Thailand.

---

## Overview

The system digitizes and standardizes the telemedicine intake process, replacing manual, paper-based workflows with an automated, structured, and validation-driven pipeline.

It enables:

- Digital patient registration
- Consent collection
- Pre-consultation screening
- Structured data access for healthcare staff

---

## Impact

- Reduced patient intake workload by ~80%
- Eliminated paper-based intake workflows
- Improved data consistency and accuracy
- Enabled faster and more efficient consultations
- Successfully deployed in real-world municipal healthcare operations

---

## Problem

Traditional telemedicine intake workflows relied on manual processes where healthcare staff had to:

- Collect patient registration details manually  
- Handle consent documentation  
- Perform preliminary screening  

This led to:

- Operational bottlenecks  
- Increased consultation latency  
- Inconsistent and error-prone data  
- High administrative burden on staff  

---

## Solution

A web-based intake system that digitizes and automates the entire onboarding workflow:

- Online intake form for patients  
- Input validation to ensure data quality  
- Automated data collection pipeline  
- Centralized structured storage  
- Pre-consultation data access for healthcare staff  

---

## Architecture

Patient submits intake form via web interface:


```
[Patient]
    ↓
[Next.js (Frontend + API Routes)]
    ↓
[Data Validation Layer]
    ↓
[Google Sheets (Storage)]
    ↓
[Specialist Professional Nurse]
```



### Design Considerations

- Data validation enforced at submission to ensure clinical reliability  
- Built based on real requirements from nursing staff  
- Integrated seamlessly into existing healthcare workflows  
- Optimized for usability by non-technical users  
- Prioritized simplicity, reliability, and maintainability  

---

## Tech Stack

**Frontend / Backend**
- Next.js (App Router)
- Node.js

**Data Layer**
- Google Sheets API

**UI**
- TailwindCSS

---

## Architecture & Design Decisions

**Google Sheets as a data store**
- Chosen for rapid deployment and accessibility
- Eliminates need for complex database infrastructure
- Allows non-technical stakeholders to inspect data directly

**Monolithic Next.js architecture**
- Simplifies development and deployment
- Reduces system complexity
- Supports fast iteration cycles

**Form-driven workflow**
- Aligns with clinical intake processes
- Minimizes training requirements for users
- Ensures consistent data structure

---

## Challenges

- Handling unstructured and inconsistent user input  
- Designing for non-technical healthcare users  
- Ensuring data accuracy for clinical workflows  
- Integrating with existing manual processes without disruption  
- Balancing simplicity with production reliability  

---

## Deployment

The system is deployed and actively used in municipal telemedicine operations in Kamphaeng Phet, Thailand, supporting real-world patient intake and pre-consultation screening workflows.

---


## Project Structure

```
app/   Next.js application (UI, routing, API routes)
```
---

## References

- Municipal announcement: https://www.kppmu.go.th/news-detail?hd=1&id=124000

## Getting Started
1. Clone the repo
2. Install dependencies: npm install
3. Run development server: npm run dev

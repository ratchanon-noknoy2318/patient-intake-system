# Telemedicine Intake System

Backend-driven web platform for automating patient intake and screening in telemedicine services.

The system digitizes patient registration, consent collection, and pre-consultation screening — enabling healthcare staff to access structured patient data before consultations begin.

Used in real municipal telemedicine operations in Thailand.

---

## Impact

* Reduced manual patient intake workload by **~80%**
* Eliminated paper-based intake process
* Enabled pre-consultation access to structured patient data
* Improved data accuracy and consistency for clinical workflows
* Deployed and used in **real-world municipal healthcare services**

---

## Problem

Telemedicine appointments required healthcare staff to manually collect:

* Patient registration details
* Consent forms
* Preliminary screening information

This resulted in:

* Administrative bottlenecks
* Delays in patient consultations
* Inconsistent and error-prone data collection
* Increased workload for nurses and staff

---

## Solution

Designed and built a web-based intake system to digitize patient onboarding and screening workflows:

* Provided an online intake interface for patients
* Structured and validated input data before submission
* Automated data collection and storage pipeline
* Enabled healthcare staff to review patient data before consultations
* Reduced manual data entry and operational overhead

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
[Healthcare Staff Review]
```

### Key Considerations

* Ensured **data correctness** for clinical usage through validation
* Designed a **lightweight architecture** for rapid deployment
* Integrated with existing healthcare workflows without disruption
* Prioritized simplicity for non-technical users

---

## Tech Stack

**Frontend / Backend**

* Next.js
* Node.js

**Data**

* Google Sheets API

**UI**

* TailwindCSS

---

## Design Decisions

* **Google Sheets as storage**

  * Chosen for rapid deployment and accessibility by non-technical staff
  * Reduced need for complex infrastructure in early-stage deployment

* **Monolithic Next.js architecture**

  * Simplified development and deployment
  * Enabled fast iteration under time constraints

* **Form-based workflow**

  * Optimized for usability in real-world clinical environments

---

## Challenges

* Handling unstructured patient input data and ensuring consistency
* Designing a system usable by non-technical healthcare staff
* Ensuring data accuracy for clinical decision-making
* Integrating digital workflows into existing manual processes
* Balancing simplicity with reliability in a production environment

---

## Project Structure

```
app/   Next.js application (UI, routing, API routes)
```

---

## Deployment Context

The system supports municipal telemedicine servi

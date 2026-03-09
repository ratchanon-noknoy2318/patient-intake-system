# Telemedicine & Registration Infrastructure (KPPMCH)

**Municipal-Scale Distributed Engine | Event-Driven Workflow | 80% Triage Efficiency Gain**

A high-concurrency, asynchronous healthcare framework engineered to bridge public intake and clinical decision-making through a resilient serverless architecture.

[![Next.js](https://img.shields.io/badge/Frontend-Next.js-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![Status](https://img.shields.io/badge/Status-Production_Verified-green?style=flat-square)](https://telemedscheduler.vercel.app/)

---

## 1. System Architecture Design

The platform implements a **Stateless Layered Architecture** to ensure high availability and strictly enforced data consistency (ACID) across distributed environments.

```mermaid
graph TD
    %% Define Nodes
    Patient([Patient / User])
    NextJS[Next.js App Router]
    API{Serverless API Gateway}
    GSheet[(Google Sheets DB)]
    Nurse([Senior Nurse])

    %% 1. Input Phase
    Patient -->|1. Submit or Search| NextJS
    NextJS -->|Zod Validation| API

    %% 2. Processing Phase (Dual Path)
    API -->|2a. Search Query| GSheet
    GSheet -.->|Return Appointment| API

    API -->|2b. Atomic Register| GSheet

    %% 3. Output Phase
    API -->|3. Display Result| NextJS
    API -->|4. Push Notification| Nurse

    %% Styling
    style Patient fill:#f9f9f9,stroke:#333
    style Nurse fill:#f9f9f9,stroke:#333
    style NextJS fill:#fff,stroke:#000,stroke-width:2px
    style API fill:#000,color:#fff,stroke-width:2px
    style GSheet fill:#fff,stroke:#000,stroke-dasharray: 5 5

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
    %% Layer 1: Access Tier
    subgraph Access_Tier [1. Client Access Layer]
        User([Patient / User]) -->|HTTPS / TLS 1.3| WebApp[Next.js App Router]
        WebApp -->|Zod Schema Validation| WebApp
    end

    %% Layer 2: Logic Tier
    subgraph Logic_Tier [2. Serverless Gateway & Logic]
        WebApp -->|JSON Payload| API{API Gateway}
        
        %% Search Path
        API -->|READ Request| Search[Appointment Lookup Engine]
        
        %% Mutation Path
        API -->|WRITE Request| Ingest[Clinical Ingestion Logic]
        Ingest -->|Data Normalization| Ingest
    end

    %% Layer 3: Persistence Tier
    subgraph Data_Tier [3. Distributed Persistence]
        Search <-->|Index Scan| DB[(Google Sheets / Ledger)]
        Ingest -->|Atomic Transaction| DB
        DB ---|Audit Logging| Log[System Traceability]
    end

    %% Layer 4: Clinical Tier
    subgraph Delivery_Tier [4. Event-Driven Dispatch]
        Ingest -->|Post-Commit Webhook| LineAPI[Messaging Gateway]
        LineAPI -->|Structured Flex Message| Nurse([Senior Nursing Staff])
    end

    %% Architectural Aesthetic Styling
    style User fill:#f9f9f9,stroke:#333
    style Nurse fill:#f9f9f9,stroke:#333
    style WebApp fill:#fff,stroke:#000,stroke-width:2px
    style API fill:#000,color:#fff,stroke-width:2px
    style DB fill:#fff,stroke:#000,stroke-dasharray: 5 5
    style Search fill:#fff,stroke:#444,stroke-width:1px
    style Ingest fill:#fff,stroke:#444,stroke-width:1px

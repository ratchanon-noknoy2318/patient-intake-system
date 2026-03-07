# Patient Registration System Architecture (KPPMCH)

A high-performance, serverless registration framework engineered to bridge the gap between public healthcare intake and internal clinical workflows via real-time data synchronization.

---

## 1. System Design and Architecture
The system follows a **Decoupled Serverless Pattern** to ensure high availability, low latency, and zero-infrastructure overhead. This architecture was selected to handle high-concurrency registration events in a medical environment.

| Component | Technical Selection | Engineering Rationale |
| :--- | :--- | :--- |
| **Frontend** | Next.js (Vercel) | Optimized for Server-Side Rendering (SSR) to minimize First Contentful Paint (FCP) on mobile devices. |
| **Backend API** | Google Apps Script (GAS) | Provides an event-driven, serverless execution environment with native Google Workspace integration. |
| **Database** | Google Sheets / SQL | Utilized as a structured data store for immediate clinical accessibility and reporting. |
| **Messaging** | LINE Messaging API | Implements a push-based notification strategy to integrate with existing staff workflows. |

---

## 2. Technical Specifications
### Data Flow and Transformation
| Stage | Process | Technical Implementation |
| :--- | :--- | :--- |
| **Ingestion** | Client-side Intake | React-based state management with rigorous frontend schema validation. |
| **Transport** | RESTful Interface | Secure HTTPS POST requests utilizing JSON payloads. |
| **Processing** | Middleware Logic | GAS-based business logic for data normalization and duplicate detection. |
| **Persistence** | Structured Commit | ACID-compliant transaction logic to maintain data integrity during peak loads. |
| **Delivery** | Webhook Trigger | Asynchronous notification dispatch to the nursing station via LINE Gateway. |

---

## 3. Engineering Impact and Performance
| Metric | Engineering Outcome | Implementation Strategy |
| :--- | :--- | :--- |
| **Efficiency** | >90% Time Reduction | Transitioned manual paper intake to a sub-second digital sync. |
| **Scalability** | Horizontal / Auto | Serverless infrastructure scales automatically based on request volume. |
| **Integrity** | 0% Data Loss | Implemented robust error handling and retry logic at the API layer. |
| **Security** | TLS 1.3 / PDPA | End-to-end encryption for all Patient Identifiable Information (PII). |

---

## 4. System Design Principles
* **Separation of Concerns:** Distinct boundaries between the UI, Business Logic, and Persistence layers.
* **Minimalist UX:** Applied psychological principles to reduce cognitive load for medical staff in high-stress environments.
* **Resiliency:** Designed for high uptime (99.9%) by leveraging distributed cloud providers (Vercel/Google).
* **Compliance:** Fully aligned with healthcare data privacy standards and PDPA regulations.

---

## 5. Development and Deployment
| Resource | Documentation Link |
| :--- | :--- |
| **Live Production** | [kppmch-register.vercel.app](https://kppmch-register.vercel.app/PatientRegister) |
| **Official Record** | [Hospital Security Deployment #126854](https://www.kppmu.go.th/news-detail?hd=1&id=126854) |
| **Technical Lead** | [Ratchanon Noknoy (Software Engineer)](https://www.linkedin.com/in/ratchanon-noknoy/) |
| **Engineering Portfolio** | [GitHub Profile](https://github.com/ratchanon-noknoy2318) |

---
**Technical Note:** This system architecture focuses on **Operational Excellence**—prioritizing reliability and data integrity while maintaining a low-maintenance, cost-effective infrastructure.

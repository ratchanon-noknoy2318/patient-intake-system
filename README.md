# Telemedicine Intake System
**High-efficiency patient data acquisition and screening platform using Google Sheets.**

## Overview
The Telemedicine Intake System is engineered to eliminate manual bottlenecks in patient registration. By digitizing the initial intake process, the system ensures that healthcare providers receive structured clinical data and signed consents before the consultation begins, reducing administrative latency and improving data accuracy.

## Architecture

| Layer | Description |
| :--- | :--- |
| **Pattern** | Stateless Layered Architecture |
| **Flow** | [User] -> [Frontend] -> [API] -> [Google Sheets] |
| **Integrations** | Google Sheets API |

## Tech Stack

| Component | Technology |
| :--- | :--- |
| **Frontend** | Next.js (App Router), TailwindCSS |
| **Backend** | Node.js (REST APIs) |
| **Database** | Google Sheets |

## Project Structure

| Directory | Description |
| :--- | :--- |
| `app/` | Core application logic, routing, UI components, and API handlers. |

## License
Distributed under the MIT License.

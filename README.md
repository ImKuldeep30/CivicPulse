# CivicPulse: AI-Powered Civic Governance, Issue Tracking & Public RAG Agent Platform

CivicPulse is an integrated civic technology platform designed to bridge the gap between citizens and municipal governance. It combines transparent civic complaint reporting, spatial intelligence, community mobilization, and a domain-grounded Retrieval-Augmented Generation (RAG) assistant into a single, unified system.

---

## 📌 Project Overview

Modern civic issue reporting often suffers from fragmented departmental channels, limited status visibility, and information barriers between citizens and administrative bodies. **CivicPulse** provides:
- A single, transparent portal to report and monitor localized civic infrastructure problems.
- Geospatial mapping to highlight geographic concentrations of issues and constituency boundaries.
- An AI-powered civic assistant that provides verifiable, source-grounded answers to citizen queries regarding municipal laws, procedures, and escalation pathways.
- Incentivized community participation through civic scoring and local initiative campaigns.

---

## 🌟 Major Features

### 1. Geotagged Issue Reporting & Lifecycle Tracking
- **Evidence-Based Submission:** Report complaints with photographic evidence, automated geolocation (GPS), and categorizations.
- **Automated Routing:** Automatically routes complaints to the appropriate administrative department.
- **Lifecycle Tracking:** Follow complaints through distinct stages (`Reported` → `Verified` → `In-Progress` → `Resolved`) with status history and audit logging.

### 2. Interactive Geospatial Visualization (Map Module)
- **Interactive Map:** Visualize civic issues with color-coded markers, cluster views, and category filters.
- **Spatial Intelligence:** Powered by PostGIS for viewport filtering, radius/distance searches, and administrative constituency boundary mapping.

### 3. Smart RAG Public Response Agent
- **Grounded Civic Q&A:** A natural-language AI agent powered by Retrieval-Augmented Generation (RAG).
- **Domain Knowledge Base:** Answers procedural, legal, and municipal questions grounded in indexed government manuals, municipal bylaws, and grievance datasets.
- **Source Traceability:** Cites referenced documents with retrieval metadata and provides fallbacks to official channels for unsupported queries.

### 4. Civic Participation & Scoring Engine
- **Incentivized Engagement:** Rewarding constructive participation through a weighted civic score formula:
  $$\text{CivicScore} = w_r R + w_u U + w_c C$$
  *(where $R$ = validated reports, $U$ = community upvotes, and $C$ = campaign participation)*.
- **Anti-Abuse Safeguards:** Verification mechanisms to detect and prevent duplicate or malicious entries.

### 5. Community Campaigns
- Allows authorized local organizers to coordinate and mobilize constituency-level community drives (e.g., cleanliness drives, local awareness) and track collective progress.

### 6. Real-Time Events & Administrative Moderation
- **Real-Time Updates:** Decoupled status propagation and notification events via WebSockets and Redis Pub/Sub.
- **Admin Dashboard:** Role-Based Access Control (RBAC), verification queues, status transitions, and civic spatial analytics.

---

## 🛠️ Technology Stack

| Layer / Subsystem | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend** | React, Vite, Tailwind CSS | Responsive, component-driven client interface and dashboard |
| **Backend** | Node.js, Express *(FastAPI in core synopsis)* | RESTful APIs, WebSockets, business logic, and routing |
| **Database & GIS** | PostgreSQL + PostGIS | Relational storage and spatial geometry queries |
| **Caching & Messaging**| Redis | High-speed cache and Pub/Sub event broker |
| **Geospatial Mapping** | Mapbox GL JS / Leaflet | Interactive maps, boundary visualization, and marker clustering |
| **AI Orchestration** | LangChain / LlamaIndex | Document chunking, vector embeddings, and RAG pipeline |
| **Vector Database** | Qdrant / ChromaDB | Semantic retrieval and similarity indexing for municipal documents |
| **DevOps & Tooling** | Docker, Git/GitHub, Postman, pytest/jest | Service containerization, source control, and API testing |

---

## 📁 Repository Structure

```text
Major Project/
├── README.md               # Project documentation
├── frontend/               # Client-side React application
│   ├── src/
│   │   ├── App.jsx         # Root React component
│   │   ├── main.jsx        # React entry point
│   │   └── index.css       # Tailwind CSS configuration
│   ├── package.json
│   └── vite.config.js
└── backend/                # Server-side Node.js application
    ├── server.js           # Express API server entry point
    └── package.json
```

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/)

### 1. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```
The frontend application will be running at `http://localhost:5173`.

### 2. Backend Setup
```bash
cd backend
npm install
node server.js
```
The API server will be running at `http://localhost:5000`.

---

## 👥 Project Team
- **Kuldeep Kohli** (Roll No: 2319013)
- **Vaibhav Sharma** (Roll No: 2319797)
- **Kanchan Kumar Mandal** (Roll No: 2318934)
- **Shubham Pandey** (Roll No: 2319625)

**Supervisor:** Mrs. Manisha Aeri, Assistant Professor  
**Department:** Computer Science and Engineering, Graphic Era Hill University, Dehradun

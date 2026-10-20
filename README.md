# 🌊 Salinity Shield AI

**Smart Salinity Ingress & Coastal Farmland Protection Advisor**  
*Gujarat Hackathon 2026 — AI Agent Track (Powered by IBM Bob, IBM Granite & watsonx.ai)*

[![IBM Granite](https://img.shields.io/badge/IBM%20Granite-watsonx.ai-blue?style=flat&logo=ibm)](https://www.ibm.com/granite)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green?style=flat&logo=node.js)](https://nodejs.org/)
[![Fastify](https://img.shields.io/badge/Backend-Fastify-black?style=flat&logo=fastify)](https://fastify.dev/)
[![React](https://img.shields.io/badge/Frontend-React%2018%20%2B%20Vite-61dafb?style=flat&logo=react)](https://react.dev/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL%20%2B%20Prisma-336791?style=flat&logo=postgresql)](https://www.prisma.io/)
[![Socket.IO](https://img.shields.io/badge/Realtime-Socket.IO-010101?style=flat&logo=socket.io)](https://socket.io/)
[![Tailwind CSS](https://img.shields.io/badge/Styles-Tailwind%20CSS-38bdf8?style=flat&logo=tailwindcss)](https://tailwindcss.com/)

---

## 📌 Executive Summary

Coastal districts of Gujarat (**Bhavnagar, Jamnagar, and Kutch**) face aggressive seawater intrusion into groundwater aquifers and arable farmland. Unchecked salinity destroys soil microbiomes, lowers crop yields, degrades potable groundwater, and jeopardizes agricultural livelihoods.

**Salinity Shield AI** is an event-driven, multi-agent agricultural intelligence platform engineered to protect coastal farmlands. Rather than acting as a simple conversational chatbot, the platform combines **deterministic environmental risk modeling** with **autonomous IBM Granite AI agents** to deliver real-time monitoring, predictive ingress forecasting, What-If mitigation simulations, transparent decision traces, and multilingual farmer advisories (English, Hindi, and Gujarati).

---

## 🏛️ System Architecture

Salinity Shield AI separates deterministic mathematical computation from generative reasoning to ensure zero hallucination in critical risk assessments:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        DATA INGESTION LAYER                            │
│  IoT Soil/Water Sensors │ Manual Entry │ Automated Edge Simulator     │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                        BACKEND PIPELINE (Fastify)                      │
│  1. Zod Schema Validation                                              │
│  2. PostgreSQL Persistence (Prisma ORM)                                │
│  3. Historical 30-Day Trend & Rolling Variance Analysis               │
│  4. Deterministic Risk Engine (ECe, TDS, SAR, pH, Water Table Depth)   │
│  5. Explainable Risk Scorer & Forecast Engine                          │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                    AGENT ORCHESTRATOR & DISPATCHER                     │
│  Determines Severity: LOW ➔ MEDIUM ➔ HIGH ➔ CRITICAL                   │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │ (Dynamic Agent Activation)
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│               IBM GRANITE AGENTIC LAYER (watsonx.ai)                  │
│  • Monitoring Agent: Interprets telemetry & ingress velocity           │
│  • Crop Advisory Agent: Salt-tolerant cultivars (Gujarat agro-zones)   │
│  • Irrigation Advisory Agent: Leaching fraction & blending strategies  │
│  • Land Reclamation Agent: Gypsum dosing, sub-surface drainage, biochar│
│  • Farmer Alert Agent: Multilingual SMS/Voice alerts (EN / HI / GU)   │
│  • Farmland Health Agent & Context-Aware Chat Advisor                 │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │
                                   ▼
┌────────────────────────────────────────────────────────────────────────┐
│                    PRESENTATION & REAL-TIME DISPATCH                   │
│  Socket.IO Push Stream ➔ React 18 + Vite Interactive Web Suite        │
│  (Live Telemetry, Geospatial Heatmaps, What-If Sandbox, Decision Trace)│
└────────────────────────────────────────────────────────────────────────┘
```

---

## ✨ Key Capabilities

| Module | Description |
|---|---|
| **🔴 Real-Time Telemetry** | Low-latency bi-directional sync via Socket.IO; live sensor feeds without page reloads. |
| **⚙️ Deterministic Risk Engine** | Mathematically rigorous risk evaluation (ECe, SAR, groundwater depth, salinity trend) with no AI math hallucination. |
| **🧠 Explainable Decision Tracing** | Full breakdown showing exactly which parameters, thresholds, and historical deltas triggered each alert. |
| **🤖 Autonomous Agent Swarm** | Specialized IBM Granite agents dynamically invoked based on environmental risk severity. |
| **🔮 Predictive Salinity Forecast** | Multi-week ingress trajectory modeling with confidence bands. |
| **🧪 "What-If" Mitigation Sandbox** | Interactive scenario simulator: test gypsum application, freshwater leaching, and monsoon retention before real-world execution. |
| **🗺️ Geospatial Vulnerability Maps** | Dual mapping support with Leaflet OpenStreetMap and Google Maps (AdvancedMarker). |
| **🌐 Multilingual Farmer Advisories** | Instant actionable advisories translated into **English**, **Hindi (हिंदी)**, and **Gujarati (ગુજરાતી)**. |
| **📡 Edge Sensor Simulator** | Built-in scenario runner (Stable, Gradual Salinization, Rapid Ingress) for live demonstration. |

---

## 🤖 Dynamic Multi-Agent Orchestration

Agents are activated dynamically according to the calculated risk score:

| Risk Level | Composite Score | Activated IBM Granite Agents |
|---|---|---|
| **🟢 LOW** | 0 – 25 | Monitoring Agent |
| **🟡 MEDIUM** | 26 – 50 | Monitoring Agent + Crop Advisory Agent |
| **🟠 HIGH** | 51 – 75 | Monitoring Agent + Crop Advisory + Irrigation Advisor + Land Reclamation + Farmer Alert Agent |
| **🔴 CRITICAL** | 76 – 100 | Full Swarm: All 5 Specialist Agents + Urgent Multilingual Alert Dispatch |

---

## 💻 Technology Stack

### Frontend
- **Framework:** React 18 with Vite
- **Styling:** Tailwind CSS, PostCSS, Autoprefixer
- **State & Data Fetching:** TanStack React Query (v5)
- **Real-Time Client:** Socket.IO Client
- **Charts & Visualizations:** Recharts (responsive time-series charts)
- **Geospatial Maps:** Leaflet & `@vis.gl/react-google-maps`
- **Icons:** Lucide React

### Backend
- **Runtime:** Node.js 18+ (ES Modules)
- **API Framework:** Fastify v4 (High throughput HTTP engine)
- **Real-Time Gateway:** Socket.IO v4
- **ORM & Database:** Prisma ORM with PostgreSQL
- **Schema Validation:** Zod
- **Testing:** Node.js native test runner

### AI & Cloud Integration
- **Foundation Model:** IBM Granite (`ibm/granite-13b-instruct-v2` / `ibm/granite-4-h-small`)
- **AI Infrastructure:** IBM watsonx.ai REST APIs with IAM token exchange
- **Agent Architecture:** Structured JSON prompt templates with strict schema enforcement
- **High-Availability Fallback:** Offline deterministic demo mode ensuring 100% testability even without cloud API access

---

## 🗂️ Project Structure

```
salinity-shield/
├── client/                               # Frontend React Application
│   ├── public/                           # Static assets
│   ├── src/
│   │   ├── components/
│   │   │   ├── charts/SalinityCharts.jsx # Historical trend & variance charts
│   │   │   ├── landing/                  # Landing page hero, impact, technology
│   │   │   ├── ui/                       # Data badges, metric cards, headers
│   │   │   ├── ActivityTimeline.jsx      # Agent execution timeline
│   │   │   ├── ExplainableRiskScore.jsx  # Risk factor breakdown component
│   │   │   ├── GoogleRiskMap.jsx         # Google Maps interface
│   │   │   ├── LeafletRiskMap.jsx        # OpenStreetMap Leaflet interface
│   │   │   ├── ReadingForm.jsx           # Sensor data entry modal
│   │   │   └── SensorSimulator.jsx       # Real-time simulation controller
│   │   ├── hooks/                        # React Query and Socket.IO hooks
│   │   ├── lib/                          # Axios API client, Socket helper, utilities
│   │   ├── pages/
│   │   │   ├── AIAdvisoryPage.jsx        # Specialist agent recommendations
│   │   │   ├── AlertsPage.jsx            # Alert inbox with priority filters
│   │   │   ├── Dashboard.jsx             # Coastal overview & regional summary
│   │   │   ├── DecisionTracePage.jsx     # Explainable AI logs & scoring traces
│   │   │   ├── FarmDetail.jsx            # Farm-specific telemetry & timeline
│   │   │   ├── FarmsList.jsx             # Farm inventory management
│   │   │   ├── ForecastPage.jsx          # Predictive salinity projection
│   │   │   ├── HeatmapPage.jsx           # Ingress vulnerability heatmap
│   │   │   ├── LandingPage.jsx           # Modern presentation & overview
│   │   │   ├── LiveMonitoring.jsx        # Real-time streaming console
│   │   │   ├── SimulatorPage.jsx         # Edge sensor simulation laboratory
│   │   │   └── WhatIfPage.jsx            # Counterfactual intervention sandbox
│   │   ├── App.jsx                       # Application shell & routes
│   │   ├── index.css                     # Global design system
│   │   └── main.jsx                      # App bootstrap
│   ├── package.json
│   ├── tailwind.config.js
│   └── vite.config.js
│
├── server/                               # Backend Server & AI Engine
│   ├── prisma/
│   │   ├── schema.prisma                 # Database schema definition
│   │   └── seed.js                       # Demo coastal farm dataset seeder
│   ├── src/
│   │   ├── ai/
│   │   │   ├── agents/                   # IBM Granite agent implementations
│   │   │   │   ├── chatAdvisor.js
│   │   │   │   ├── coastalFarmlandHealthAgent.js
│   │   │   │   ├── cropAdvisoryAgent.js
│   │   │   │   ├── farmerAlertAgent.js
│   │   │   │   ├── irrigationAgent.js
│   │   │   │   ├── landReclamationAgent.js
│   │   │   │   └── monitoringAgent.js
│   │   │   ├── prompts/                  # Prompt engineering templates
│   │   │   ├── graniteService.js         # IBM Granite service layer
│   │   │   ├── orchestrator.js           # Multi-agent coordinator
│   │   │   └── watsonxClient.js          # watsonx.ai REST client
│   │   ├── engine/
│   │   │   ├── forecastEngine.js         # Salinity projection curves
│   │   │   ├── riskEngine.js             # Mathematical risk scoring
│   │   │   ├── riskExplainer.js          # Decision explanation engine
│   │   │   └── whatIfEngine.js           # What-If mitigation model
│   │   ├── pipeline/
│   │   │   └── readingPipeline.js        # End-to-end ingestion pipeline
│   │   ├── routes/                       # Fastify route endpoints
│   │   │   ├── analytics.routes.js
│   │   │   ├── chat.routes.js
│   │   │   ├── farm.routes.js
│   │   │   └── reading.routes.js
│   │   ├── validation/schemas.js         # Zod schemas
│   │   ├── tests/                        # Automated unit & engine tests
│   │   └── server.js                     # Server entry point
│   ├── package.json
│   └── .env.example
│
├── .gitignore                            # Repository ignore rules
├── 3-MINUTES VIDEO                       # Video presentation link
├── install.bat                           # Windows one-click installer
├── run.bat                               # Windows one-click runner
├── package.json                          # Root monorepo scripts
└── README.md                             # Project documentation
```

---

## 🚀 Quick Start Guide

### Prerequisites
- **Node.js** >= 18.0.0
- **npm** >= 9.0.0
- **PostgreSQL** instance (local or hosted like Supabase / ElephantSQL / IBM Cloud Databases)

---

### Step 1: Clone & Configure Environment

```bash
git clone https://github.com/VyasVraj/-Smart-Salinity-Ingress-Coastal-Farmland-Protection-Advisor-.git
cd -Smart-Salinity-Ingress-Coastal-Farmland-Protection-Advisor-
```

#### Server Configuration
Copy `server/.env.example` to `server/.env`:
```bash
cp server/.env.example server/.env
```

Edit `server/.env` with your settings:
```env
# IBM watsonx.ai / Granite Credentials
IBM_PROJECT_ID=your_watsonx_project_id
IBM_WATSON_API_KEY=your_ibm_cloud_api_key
IBM_WATSON_AI_URL=https://us-south.ml.cloud.ibm.com
IBM_GRANITE_MODEL_ID=ibm/granite-4-h-small

# Database Connection
DATABASE_URL="postgresql://postgres:your_password@localhost:5432/salinity_shield"

# Server Settings
PORT=5000
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```
*(Note: If IBM credentials are not provided, the platform automatically runs in realistic fallback demo mode).*

#### Client Configuration (Optional)
If using Google Maps:
```bash
cp client/.env.example client/.env
```
Provide `VITE_GOOGLE_MAPS_API_KEY` (Leaflet OpenStreetMap works out-of-the-box without keys).

---

### Step 2: One-Click Installation (Windows)

Double-click `install.bat` or run:
```bat
install.bat
```

*Or manually via npm:*
```bash
npm run install:all
```

---

### Step 3: Database Migration & Seeding

Initialize the PostgreSQL schema and load the Gujarat coastal farm dataset:
```bash
# Push Prisma schema to PostgreSQL
npm run db:push

# Seed Gujarat demo farms (Bhavnagar, Jamnagar, Kutch)
npm run db:seed
```

---

### Step 4: Run the Application

Double-click `run.bat` or execute:
```bash
npm run dev
```

The application will be live at:
- **Web Dashboard:** [http://localhost:5173](http://localhost:5173)
- **Fastify API Server:** [http://localhost:5000](http://localhost:5000)

---

## 🧪 Testing

Execute deterministic risk engine test suite:
```bash
npm run test:risk
```
Validates:
- Threshold classification for ECe, TDS, SAR, and Water Table Depth
- Trend velocity detection (IMPROVING, STABLE, WORSENING, RAPIDLY_WORSENING)
- Correct dynamic agent activation mapping

---

## 🎬 Demonstration Walkthrough

1. **Dashboard Overview:**  
   Inspect the three seeded coastal farms reflecting diverse ecological conditions:
   - 🟢 **Bhavnagar Coastal Farm A:** Low salinity, baseline stability.
   - 🟡 **Jamnagar Farmland B:** Moderate ECe with gradual salinization trend.
   - 🔴 **Kutch Arid Coastal C:** Critical ingress, high SAR, low water table.

2. **Sensor Simulation Experience:**  
   Navigate to **Simulator**, select **Jamnagar Farmland B**, choose **"Rapid Ingress Scenario"**, and click **Start Simulation**.

3. **Observe the Event Pipeline in Real-Time:**  
   - Sensor telemetry streams via WebSocket.
   - Risk score elevates from `34 (MEDIUM)` to `78 (CRITICAL)`.
   - Orchestrator activates the full Granite Agent Swarm.
   - Instant multilingual alerts generated in **English**, **Hindi**, and **Gujarati**.

4. **Explore What-If Mitigation:**  
   Open the **What-If Sandbox** to model remedial actions (e.g., adding 2.5 tons/ha gypsum and applying 20% leaching fraction) and observe the projected recovery curves.

5. **Review Explainable Decision Trace:**  
   Visit **Decision Trace** to examine the mathematical justification and agent prompt logs behind every system action.

---

## 🎥 Pitch Video & Presentation

- **3-Minute Pitch Video:** [Google Drive Video Link](https://drive.google.com/drive/folders/13DJwawwS5bvLA_B9uzODMZjDSDXbYYIb?usp=drive_link)
- **Project Presentation Deck:** `Smart Salinity Ingress & Coastal Farmland Protection Advisor.pptx`
- **Problem Statement Documentation:** `problem_statement.pdf`

---

## 📄 License & Attribution

Developed for the **Gujarat Hackathon 2026** under the **AI Agent Track (IBM Bob & IBM Granite)**.  
Built with ❤️ for the coastal farming communities of Gujarat, India.

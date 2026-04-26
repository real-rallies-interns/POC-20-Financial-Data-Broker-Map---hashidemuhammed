# Financial Data Broker Map

**Real Rails Intelligence Library · PoC #20 · Open Banking Rail**

![Archetype Relational](https://img.shields.io/badge/Archetype-Relational-blue)
![Rail Open Banking](https://img.shields.io/badge/Rail-Open_Banking-cyan)
![VAR PASS](https://img.shields.io/badge/VAR-PASS-brightgreen)
![Stack Next.js 16 + FastAPI](https://img.shields.io/badge/Stack-Next.js_16_%2B_FastAPI-black)

A Data Sovereignty Tool designed to map the complex lineage of financial data. Most users believe their financial data stays between them and their bank. In reality, once consent is granted, that data enters a complex web of Aggregators, Brokers, and Resellers. This dashboard visualizes the data sprawl, tracking it from the source through to third-party endpoints.

## What It Does
The dashboard ingests a synthetic network of Open Banking permissions and renders an interactive **React Flow** relational graph following strict Obsidian Black (#030712) guidelines.

- **The 70% Visualization Stage:** Displays the data hops from Banks (Source of Truth) → Aggregators (Delegated Access) → Apps/Brokers (Anonymized Tracking). High-risk permission paths (e.g., data resale) are visually highlighted.
- **The 30% Intelligence Sidebar:** Clicking any node in the graph triggers a "Handshake" event, dynamically populating the sidebar's Node Insights section with the entity's Risk Level, Access Scope, and necessary compliance warnings (CFPB Section 1033 / GDPR).

## Local Execution Instructions
This project requires Node.js (v18+) and Python (v3.10+).

1. **Start the FastAPI Backend:**
   Open a terminal in the root directory and run:
   ```powershell
   .\run_backend.ps1
   ```
   *The API will run on http://127.0.0.1:8000*

2. **Start the Next.js Frontend:**
   Open a second terminal in the root directory and run:
   ```powershell
   .\run_frontend.ps1
   ```
   *The dashboard will run on http://localhost:3000*

## Handover Artifacts Included
- `repomix-output.xml`: The complete unified codebase.
- `Visualization_Audit_Report.md`: Passed visual compliance audit.
- `Functional_UAT.csv`: Passed functional interaction test cases.
# POC-20-Financial-Data-Broker-Map---hashidemuhammed
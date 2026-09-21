# 📂 Workspace Architecture & Directory Guide

This workspace is cleanly organized into two distinct security and energy intelligence applications:

---

## 🏢 1. `WattSentinel-AI-Dashboard/` (IoT Energy Monitoring & Smart Control)
**Port:** `http://localhost:5500`  
**Purpose:** AI Enabled IoT Energy Monitoring, TNEB LT-1A Bill Calculation Engine, ESP32 + PZEM-004T Residential Telemetry, LoRa SX1276 Node Management, and Realtime Smart Relay Control.

### Key Files:
- **`index.html`** — Master Single-Page Dashboard containing all 11 views (Overview, Live Telemetry, Energy Analytics, TNEB Bill Calculator, Smart Load Controls, LoRa Mesh, Firebase Security Audit, AI Copilot, etc.).
- **`login.html`** — Secure RBAC Authentication Portal with live video background & particle telemetry.
- **`reset-password.html`** — Standalone Password Reset & OTP Handshake portal.
- **`app.js`** — Core Frontend Logic Engine: Chart.js telemetry instances, real-time simulated sensors, relay controls, view navigation router, and AI optimizer.
- **`app-config.js`** — Central configuration repository (branding, navigation map, Firebase endpoints, pricing slabs).
- **`firebase-config.js`** — Firebase Realtime Database and Auth initialization.
- **`server.js`** — Node.js HTTP backend server with SMTP Email, WhatsApp webhook, and receipt notification dispatch.
- **`package.json`** — NPM script configurations (`npm start`, `npm run dev`, `npm run check`).
- **`style.css` / `styles.css`** — Ultra-modern glassmorphic design system and CSS tokens.
- **`tools/`** — Diagnostic scripts, view generators, asset splitters, and Firebase RTDB seeders.

---

## 🛡️ 2. `Root / SentinelAI-X-Dashboard` (Enterprise Biometric & Threat Grid)
**Port:** `http://localhost:5173` (or `http://localhost:5000` via `app.py`)  
**Purpose:** Multi-Lab Biometric Access Control, AI Threat Grid, Clearances, and Security Audit Logs.

### Key Files:
- **`index.html`** — SentinelAI-X Enterprise Security Command Center.
- **`login.html`** — SentinelAI-X 2FA / OTP Enterprise Access Login.
- **`reset-password.html`** — Enterprise Password Reset & Verification Engine.
- **`script.js`** — Frontend Security & Biometric Threat Grid UI controller.
- **`style.css`** — Dark Cyberpunk glassmorphism design system for SentinelAI-X.
- **`server.js`** — Node.js Enterprise 2FA OTP & Static server (Port 5173).
- **`app.py`** — Python Flask CORS API server for Enterprise Accounts & RBAC verification.
- **`email_service.py`** — Python SMTP 2FA security mailer.
- **`package.json`** — Root NPM configuration.
- **`AGENTS.md`** — Project lock directives and architecture safety rules.

---

## 🚀 Quick Run Commands:

| Application | Command | URL |
| :--- | :--- | :--- |
| **WattSentinel-AI** | `cd WattSentinel-AI-Dashboard && node server.js` | [http://localhost:5500](http://localhost:5500) |
| **SentinelAI-X Node** | `node server.js` | [http://localhost:5173](http://localhost:5173) |
| **SentinelAI-X Flask** | `python app.py` | [http://localhost:5000](http://localhost:5000) |

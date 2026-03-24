# 🛡️ Information Security Risk Register — NimbusTech Solutions

> **Mock Project** · ISO 31000 / NIST RMF · Cloud Startup (10 employees)

A fully-documented enterprise risk register built for a fictional 10-person SaaS startup called **NimbusTech Solutions**. Demonstrates core risk management skills including likelihood/impact scoring, heat-map visualisation, residual-risk tracking, and executive reporting, aligned to **ISO 31000** and the **NIST Risk Management Framework (RMF)**.
---

## 📊 Workbook Overview

The Excel workbook (`NimbusTech_Risk_Register.xlsx`) contains **three tabs**:

### Tab 1 · Risk Register
| Column | Description |
|---|---|
| Risk ID | Unique identifier (R-001 … R-012) |
| Description | Plain-English risk statement |
| Category | Cybersecurity / IAM / Cloud / Vendor / Legal |
| Likelihood (1–5) | Probability of occurrence |
| Impact (1–5) | Business severity if realised |
| **Risk Score** | `= Likelihood × Impact` (Excel formula) |
| Rating | HIGH / MEDIUM / LOW with conditional colour fill |
| Mitigation Measures | Specific, actionable controls |
| Owner | Accountable role |
| **Residual Risk** | Post-control remaining score |
| Review Date | Scheduled reassessment date |

### Tab 2 · Heat Map
5 × 5 Likelihood/Impact grid with colour-coded cells:

| Score Range | Rating | Colour |
|---|---|---|
| ≥ 16 | 🔴 HIGH | Red |
| 9 – 15 | 🟠 MEDIUM | Amber |
| 4 – 8 | 🟡 ELEVATED | Yellow |
| 1 – 3 | 🟢 LOW | Green |

Each cell that contains an active risk is labelled with the corresponding Risk ID.

### Tab 3 · Summary Dashboard
- KPI tiles: Total / High / Medium / Low risk counts
- Top 5 risks ranked by score with owner and review dates

---

## 🔍 Risk Inventory (12 Risks)

| ID | Risk | Score | Rating |
|---|---|---|---|
| R-001 | Data Breach via External Attacker | **20** | 🔴 HIGH |
| R-002 | Phishing Attack on Employees | **16** | 🔴 HIGH |
| R-003 | Misconfigured S3 Bucket | **15** | 🟠 MEDIUM |
| R-004 | Credential Reuse / Weak Passwords | **16** | 🔴 HIGH |
| R-005 | Insider Threat | **10** | 🟠 MEDIUM |
| R-006 | Third-Party Supply Chain Attack | **12** | 🟠 MEDIUM |
| R-007 | Ransomware / Malware | **15** | 🟠 MEDIUM |
| R-008 | Cloud Service Outage | **12** | 🟠 MEDIUM |
| R-009 | Unpatched Dependencies | **12** | 🟠 MEDIUM |
| R-010 | Insufficient Logging & Monitoring | **9** | 🟠 MEDIUM |
| R-011 | GDPR / Regulatory Non-Compliance | **10** | 🟠 MEDIUM |
| R-012 | DDoS Attack on Public Endpoints | **8** | 🟡 ELEVATED |

---


## Frameworks Referenced

| Framework | Application |
|---|---|
| **ISO 31000:2018** | Risk management principles and guidelines |
| **NIST RMF (SP 800-37)** | Categorise → Select → Implement → Assess → Authorise → Monitor |
| **NIST CSF 2.0** | Govern · Identify · Protect · Detect · Respond · Recover |
| **CIS Controls v8** | Specific technical mitigations (patching SLAs, MFA, logging) |


# NimbusTech Solutions
## Information Security Risk Summary Report
**Version:** 1.0 | **Date:** March 23, 2025 | **Prepared by:** Risk Analyst | **Classification:** INTERNAL

---

## Executive Summary

NimbusTech Solutions operates a cloud-native SaaS platform with a team of ten employees. As part of our commitment to ISO 31000 risk governance, this report summarises the findings of our inaugural Information Security Risk Assessment. Twelve risks were identified across six categories. Three risks received a **HIGH** rating (Risk Score ≥ 16) and require immediate executive attention. Nine risks were rated **MEDIUM** or **ELEVATED** and are subject to scheduled mitigation within the next 90 days. No risks were rated as acceptable without control action.

---

## Risk Landscape at a Glance

| Rating | Count | % of Register |
|---|---|---|
| 🔴 HIGH (≥ 16) | 3 | 25% |
| 🟠 MEDIUM (9–15) | 8 | 67% |
| 🟡 ELEVATED (4–8) | 1 | 8% |
| 🟢 LOW (1–3) | 0 | 0% |

The overall risk posture is **elevated**. The concentration of HIGH and MEDIUM risks reflects the startup's early-stage security maturity and the inherent exposure of cloud-hosted services to external threats.

---

## Top 3 Risks & Recommended Actions

---

### 🔴 Risk #1 — Data Breach via External Attacker
**Risk ID:** R-001 | **Score:** 20 (Likelihood 4 × Impact 5) | **Owner:** CTO

**Description:**
A malicious external actor exploits a vulnerability in NimbusTech's application layer, cloud configuration, or API endpoints to exfiltrate customer data. Given that NimbusTech processes user PII and payment metadata, a successful breach would trigger GDPR notification obligations, potential regulatory fines (up to 4% of annual turnover), reputational damage, and customer churn.

**Recommended Actions:**
1. **Immediate (0–30 days):** Enable AWS CloudTrail and GuardDuty across all accounts; ensure all S3 buckets have Block Public Access enforced at the organisational level.
2. **Short-term (30–60 days):** Deploy a Web Application Firewall (WAF) in front of all public-facing endpoints; encrypt all data at rest using AES-256 and in transit using TLS 1.3+.
3. **Ongoing:** Schedule quarterly external penetration tests with a certified provider; review and rotate all IAM access keys every 90 days.

**Residual Risk after controls:** Score reduced to **4** (LOW).

---

### 🔴 Risk #2 — Credential Reuse / Weak Passwords
**Risk ID:** R-004 | **Score:** 16 (Likelihood 4 × Impact 4) | **Owner:** IT Lead

**Description:**
Employees reusing passwords across personal and corporate accounts, or using weak passwords that are susceptible to brute-force or credential-stuffing attacks. With ten employees having access to production systems, cloud consoles, and customer data, a single compromised account can provide a threat actor with a lateral movement foothold across the entire environment.

**Recommended Actions:**
1. **Immediate (0–14 days):** Enforce Multi-Factor Authentication (MFA) on all corporate accounts like cloud console, GitHub, GSuite, Slack, and any SaaS tools with production data access. Zero exceptions.
2. **Short-term (14–30 days):** Deploy a company-wide password manager (e.g., 1Password Teams or Bitwarden Business); enforce a minimum password policy of 16 characters and uniqueness across services.
3. **Short-term (30–60 days):** Integrate SSO (e.g., Okta or Google Workspace SSO) for all internal tools to centralise access control and simplify off-boarding.

**Residual Risk after controls:** Score reduced to **4** (LOW).

---

### 🔴 Risk #3 — Phishing Attack on Employees
**Risk ID:** R-002 | **Score:** 16 (Likelihood 4 × Impact 4) | **Owner:** IT Lead

**Description:**
A threat actor sends a convincing phishing email targeting one or more NimbusTech employees to steal credentials, deliver malware, or initiate a business email compromise (BEC) fraud. With a small team, a single successful phish — especially targeting an admin-level account — could result in full cloud account takeover, data exfiltration, or fraudulent financial transfers.

**Recommended Actions:**
1. **Immediate (0–30 days):** Implement email authentication standards: SPF, DKIM, and DMARC with a `reject` policy on the company domain to prevent spoofing.
2. **Short-term (30–60 days):** Subscribe to an email security gateway (e.g., Proofpoint Essentials or Microsoft Defender for Office 365) with advanced phishing and impersonation detection.
3. **Ongoing:** Conduct bi-annual simulated phishing campaigns using a platform such as KnowBe4 or GoPhish; mandatory security-awareness training for all new hires within their first week.

**Residual Risk after controls:** Score reduced to **4** (LOW).

---

## Risk Treatment Plan — 90-Day Roadmap

| Priority | Action | Owner | Deadline |
|---|---|---|---|
| P1 | Enable MFA on all corporate accounts | IT Lead | 14 days |
| P1 | Enforce AWS S3 Block Public Access org-wide | DevOps Lead | 14 days |
| P1 | Deploy DMARC `reject` policy | IT Lead | 30 days |
| P2 | Deploy WAF + enable CloudTrail/GuardDuty | CTO | 30 days |
| P2 | Roll out password manager & SSO | IT Lead | 45 days |
| P2 | Implement EDR on all endpoints + 3-2-1 backup | IT Lead | 60 days |
| P3 | SCA scanning integrated in CI/CD pipeline | DevOps Lead | 60 days |
| P3 | Centralise logging in SIEM | IT Lead | 75 days |
| P3 | First simulated phishing campaign | IT Lead | 90 days |
| P3 | GDPR gap assessment + appoint DPO | CEO / Legal | 90 days |

---

## Next Review

This risk register will be reviewed quarterly. The next scheduled review is **DD/MM/YYYY**. Risk owners are accountable for reporting control implementation status to the CTO at each monthly all-hands meeting.

---

*This document was prepared as part of NimbusTech Solutions' information security governance programme, aligned to ISO 31000:2018 and the NIST Risk Management Framework (SP 800-37 Rev. 2).*

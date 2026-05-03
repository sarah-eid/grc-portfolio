# GRC Portfolio - CS3178 | Spring 2026

**Course:** Governance, Risk & Compliance (CS3178)  
**Student:** Sarah Eid   
**Institution:** Effat Univercity   
**Term:** Spring 2026

---

## Course Overview

This portfolio documents my practical work in Governance, Risk, and Compliance (GRC), focusing on real-world cybersecurity framework selection, incident response, risk assessment, and regulatory compliance. The coursework emphasizes practical decision-making over memorization, simulating real organizational challenges.

### Key Learning Areas
- **Governance:** Decision rights, oversight structures, and performance measurement (COBIT)
- **Risk Management:** Risk identification, assessment, treatment, and register maintenance (ISO 31000, NIST RMF)
- **Compliance:** Regulatory obligations under KSA frameworks (NCA ECC, SAMA CSF, PDPL)
- **Incident Response:** NIST SP 800-61 lifecycle application to real breach scenarios
- **Framework Integration:** Combining NIST CSF, ISO 27001, CIS Controls, and COBIT

---

## 📁 Repository Structure

```
grc-portfolio/
├── README.md                          # This file
├── labs/
│   ├── lab01-frameworks-selection/
│   │   └── lab01.md
│   ├── lab02-ciso-assistant-setup/
│   │   ├── lab02.md
│   │   └── screenshots/
│   └── lab03-ksa-compliance-cycle/
│       └── lab03.md
├── assignments/
│   ├── assignment1-incident-response/
│   │   └── assignment1.md
│   └── assignment2-risk-assessment/
│       └── assignment2.md
├── final-project/
│   └── (to be added)
└── frameworks-cheatsheet.md
```

---

## Labs

### Lab 01: Cybersecurity Frameworks Selection & Incident Stress Test

**Objective:** Select and justify a framework mix for a real organization, then stress-test it with an incident twist.

**Scenario:** Fintech startup with cloud-native architecture, handling PII and payment data

**Framework Mix Selected:**
| Framework | Role |
|-----------|------|
| NIST CSF | Program communication map for leadership |
| ISO 27001 | Management system discipline & audit readiness |
| CIS Controls | Technical control prioritization |
| COBIT | Governance wrapper (decision rights, metrics) |

**Key Insight:** Using only one framework creates gaps between strategy, controls, and accountability. Integration requires a single risk register linking CIS Controls and ISO evidence to NIST CSF outcomes under COBIT oversight.

**Incident Stress Test (Vendor Breach):** Three actionable responses mapped across all four frameworks with evidence requirements.

---

### Lab 02: CISO Assistant Platform Deployment

**Objective:** Deploy and verify the CISO Assistant Community edition locally using Docker.

**Technical Stack:**
- Docker containerization (frontend, backend, database, proxy)
- Local HTTPS deployment (https://localhost:8443/)
- Multi-service orchestration

**Reflection:** Docker enables consistent deployment without manual configuration. Real-world challenges include port conflicts, certificate warnings, and RAM constraints.

---

### Lab 03: KSA Cybersecurity Frameworks & Compliance Cycle

**Objective:** Apply KSA regulatory requirements to a real scenario using CISO Assistant.

**Scenario:** KSA bank launching a mobile banking feature (customer onboarding + transaction access)

**Applied Frameworks:**
- SAMA Cybersecurity Framework (sector-specific for banking)
- NCA Essential Cybersecurity Controls (national baseline)
- PDPL (data privacy overlay for personal data)

**Assessment Output:** 10 requirements assessed across statuses (Compliant / Partially Compliant / Non-Compliant) with evidence notes.

**Key Finding:** The system is partially compliant — leadership and authentication are done, but logging, monitoring, and incident response require work before release.

---

## Assignments

### Assignment 1: Incident Management & Response — MedCore Health Systems

**Scenario:** Ransomware attack with data exfiltration (47 GB) affecting 5 hospitals across Saudi Arabia, 280,000 patients, with backups deliberately wiped.

**Key Deliverables:**

| Question | Focus |
|----------|-------|
| Q1 | Incident classification (ransomware + breach + unauthorized access) — Critical severity justified via CIA triad |
| Q2 | NIST SP 800-61 lifecycle mapped to case facts (6 phases) |
| Q3 | Regulatory notifications: NCA (2 hours), SDAIA (72 hours), SHIC (24 hours) |
| Q4 | Ransom payment briefing — Recommendation: DO NOT PAY (legal, operational, reputational analysis) |
| Q5 | Post-incident report sections + 5 control improvements + risk register update |
| Q6 | GRC pillar failures: Governance (no escalation policy), Risk (no backup validation), Compliance (no network segmentation) |

**Critical Control Improvements Identified:**
- Phishing-resistant MFA + monthly simulations
- Offline immutable backups with weekly restore tests
- Network segmentation (zero-trust architecture)
- 24/7 privileged account monitoring

---

### Assignment 2: Risk Assessment — FinBridge Digital

**Scenario:** Riyadh-based fintech (420 employees, 95k customers) with SAMA, NCA, PDPL, and PCI-DSS obligations. New CISO discovers significant security gaps.

**Risk Assessment Methodology:** Semi-quantitative (NIST SP 800-30 style) — chosen for regulatory demands, board-level clarity, and practical resource constraints.

**Top 5 Risks Documented in Risk Register:**

| Risk ID | Description | Score | Level | Treatment |
|---------|-------------|-------|-------|-----------|
| R-001 | Public S3 buckets with 2,400 real customer records | 25 | Critical | Immediate restriction + automated weekly scans |
| R-002 | Incomplete offboarding (AD accounts active 7-21 days post-departure) | 16 | High | Automated offboarding playbook + quarterly reviews |
| R-003 | AWS root account without MFA | 25 | Critical | Enable MFA immediately + break-glass procedure |
| R-004 | BI vendor (UK) with re-identifiable data, no risk assessment | 15 | High | Vendor assessment + PDPL-compliant DPA + SOC 2 Type II |
| R-005 | 35% of employees have unnecessary admin privileges | 16 | High | Role-based access review + PAM implementation |

**Regulatory Analysis:**
- **SAMA CSF violations:** No MFA on privileged access, no access reviews, missing cloud security controls
- **PDPL implications:** 2,400-record S3 exposure = reportable breach (notification to SDAIA within 72 hours)

**Risk Governance Framework Designed:**
- Weekly top-risk review (CISO)
- Monthly full register review
- Quarterly board reporting
- Critical risk escalation: CEO within 24h → Board within 48h

---

## Frameworks & Regulations Referenced

### International Frameworks
| Framework | Application |
|-----------|-------------|
| NIST CSF | Program structure and maturity communication |
| NIST SP 800-61 | Incident response lifecycle |
| NIST SP 800-30 | Risk assessment methodology |
| ISO 27001 | ISMS, audit readiness, risk treatment |
| ISO 27035 | Incident management |
| ISO 31000 | Risk management principles |
| CIS Controls v8 | Technical control prioritization |
| COBIT 2019 | Governance, decision rights, metrics |

### KSA Regulatory Frameworks
| Framework | Applicability |
|-----------|---------------|
| NCA ECC-1:2018 | National cybersecurity baseline |
| SAMA CSF | Financial sector (banks & fintech) |
| PDPL (Royal Decree M/19) | Personal data protection and breach notification |
| SHIC Guidelines | Health data protection |

### Industry Standards
- PCI-DSS v4.0 (payment processing)
- SOC 2 Type II (vendor assurance)

---

## Tools Used

- **CISO Assistant Community** — Compliance and risk management platform
- **Docker** — Containerized deployment

---

## Key Skills Demonstrated

| Skill Area | Specific Competencies |
|------------|----------------------|
| **Framework Integration** | Combining NIST CSF, ISO 27001, CIS Controls, COBIT for holistic coverage |
| **Incident Response** | Full NIST 800-61 lifecycle application, regulatory notification timelines, ransom decision analysis |
| **Risk Assessment** | Semi-quantitative scoring, risk register creation, treatment planning (mitigate/avoid/transfer/accept) |
| **Regulatory Compliance** | KSA-specific: NCA ECC, SAMA CSF, PDPL, SHIC — with specific clause references |
| **GRC Integration** | Connecting Governance (COBIT), Risk (ISO 31000), and Compliance (regulatory) pillars |
| **Evidence-Based Assurance** | Defining evidence requirements (logs, reports, screenshots, test records) |

---

## Reflection

This course transformed my understanding of cybersecurity from purely technical controls to an integrated GRC discipline. Key takeaways:

1. **No single framework is sufficient** — real organizations need a tailored mix
2. **Incident response is 90% preparation** — MedCore failed because they lacked basic IR plan and backup validation
3. **Risk registers are living documents** — they must be reviewed regularly, not created once and forgotten
4. **Regulatory compliance drives implementation** — SAMA CSF and PDPL create enforceable obligations, not just recommendations
5. **Evidence is everything** — a control isn't compliant unless you can prove it

---

## Academic Integrity Note

This portfolio represents my original work for CS3178. All frameworks, regulations, and case scenarios are either:
- Provided by the course for academic exercise, or
- Publicly available regulatory documents

No confidential or real organizational data is included. Screenshots are from local lab environments only.

---

*Last Updated: Spring 2026*

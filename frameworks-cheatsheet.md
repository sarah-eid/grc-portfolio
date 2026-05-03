# GRC Frameworks & Regulations Cheatsheet

**Course:** CS3178 - Governance, Risk & Compliance  
**Student:** Sarah Eid  
**Last Updated:** Spring 2026

---

## Quick Reference Table

| Framework | Primary Use | Key Focus |
|-----------|-------------|-----------|
| **NIST CSF** | Program communication map | Identify → Protect → Detect → Respond → Recover |
| **NIST SP 800-61** | Incident response lifecycle | Preparation → Detection → Containment → Eradication → Recovery → Post-Incident |
| **NIST SP 800-30** | Risk assessment methodology | Risk scoring (Likelihood × Impact) |
| **ISO 27001** | Management system & audit readiness | ISMS, risk treatment, documentation |
| **ISO 27035** | Incident management | Structured incident handling |
| **ISO 31000** | Risk management principles | Risk framework, process, and evaluation |
| **CIS Controls v8** | Technical control prioritization | Implementation Group (IG1, IG2, IG3) |
| **COBIT 2019** | Governance layer | Decision rights, metrics, oversight |
| **SAMA CSF** | Saudi financial sector | Banking cybersecurity requirements |
| **NCA ECC-1:2018** | Saudi national baseline | Essential cybersecurity controls |
| **PDPL (M/19)** | Saudi data privacy | Personal data protection, breach notification |
| **SHIC Guidelines** | Saudi health data | Healthcare information protection |
| **PCI-DSS v4.0** | Payment security | Cardholder data environment |

---

## International Frameworks

### 1. NIST CSF (Cybersecurity Framework)

**Best for:** Communicating cybersecurity program to leadership and stakeholders

**Core Functions:**
```
┌─────────────┐
│   IDENTIFY  │ ← Asset management, risk assessment, governance
├─────────────┤
│   PROTECT   │ ← Access control, awareness, data security, maintenance
├─────────────┤
│   DETECT    │ ← Monitoring, anomalous activity detection
├─────────────┤
│   RESPOND   │ ← Incident analysis, mitigation, communication
├─────────────┤
│   RECOVER   │ ← Recovery planning, improvements, communication
└─────────────┘
```

**Key Question:** *"How do we talk about our security program?"*

---

### 2. NIST SP 800-61 (Incident Response Lifecycle)

**Best for:** Structured incident handling

**Six Phases:**
| Phase | Key Activities |
|-------|----------------|
| **1. Preparation** | IR policy, team training, tools, simulations |
| **2. Detection & Analysis** | Alert triage, scope assessment, prioritization |
| **3. Containment** | Short-term + long-term containment, evidence preservation |
| **4. Eradication** | Remove malware, close vectors, rebuild systems |
| **5. Recovery** | Restore from clean backups, monitor for recurrence |
| **6. Post-Incident** | Lessons learned, report, control improvements |

**Key Question:** *"What do we do when something happens?"*

---

### 3. NIST SP 800-30 (Risk Assessment)

**Best for:** Structured risk scoring methodology

**Risk Formula:**
```
Risk Score = Likelihood × Impact

Likelihood: 1 (Very Low) → 5 (Very High)
Impact:     1 (Very Low) → 5 (Very High)
Risk Score: 1-25

Levels:
- Critical: 20-25
- High:     12-19
- Medium:   6-11
- Low:      1-5
```

**Key Question:** *"How do we calculate and compare risks?"*

---

### 4. ISO 27001 (Information Security Management System)

**Best for:** Audit readiness and management system discipline

**Core Components:**
- Clause 4: Context of the organization
- Clause 5: Leadership and commitment
- Clause 6: Planning (risk assessment)
- Clause 7: Support (resources, competence, awareness)
- Clause 8: Operation (risk treatment)
- Clause 9: Performance evaluation (monitoring, internal audit)
- Clause 10: Improvement (corrective actions)

**Annex A Controls (selected):**
| Control | Theme |
|---------|-------|
| A.5.15 | Access control |
| A.5.17 | Authentication information |
| A.5.24 | Incident management |
| A.5.30 | Business continuity |
| A.5.34 | Privacy and PII protection |
| A.8.15 | Logging |
| A.8.16 | Monitoring activities |
| A.8.24 | Use of cryptography |

**Key Question:** *"How do we prove we're secure to an auditor?"*

---

### 5. ISO 27035 (Incident Management)

**Best for:** Complementary to NIST 800-61 with ISO alignment

**Five Phases:**
1. Plan and prepare
2. Detection and reporting
3. Assessment and decision
4. Response
5. Lessons learned

**Key Question:** *"How do we align incident response with ISO 27001?"*

---

### 6. ISO 31000 (Risk Management)

**Best for:** High-level risk management principles

**Principles:**
- Integrated
- Structured and comprehensive
- Customized
- Inclusive
- Dynamic
- Best available information
- Human and cultural factors
- Continual improvement

**Framework:**
- Mandate and commitment
- Design of framework
- Continuous improvement
- Monitoring and review

**Process:**
```
Scope → Risk Assessment (ID → Analyze → Evaluate) → Treatment → Record & Report
```

**Key Question:** *"What are the principles of good risk management?"*

---

### 7. CIS Controls v8

**Best for:** Technical implementation prioritization

**Implementation Groups:**
| Group | Organization Size | Focus |
|-------|------------------|-------|
| **IG1** | Small (under 50 employees) | Essential cyber hygiene |
| **IG2** | Medium (enterprise with IT staff) | More sophisticated controls |
| **IG3** | Large (security teams, complex environments) | Advanced, compliance-driven |

**Top 6 Foundational Controls (IG1):**
1. Inventory and Control of Enterprise Assets
2. Inventory and Control of Software Assets
3. Data Protection
4. Secure Configuration of Enterprise Assets
5. Account Management
6. Access Control Management

**Other Key Control Areas:**
| Area | Examples |
|------|----------|
| Account Management | MFA, privileged access, offboarding |
| Secure Configuration | Hardening, baseline images |
| Vulnerability Management | Scanning, patching, vendor risk |
| Logging | Centralized SIEM, retention |
| Data Protection | Encryption, backups, DLP |
| Incident Response | Plan, testing, simulation |
| Backup/Recovery | Immutable backups, restore testing |

**Key Question:** *"What specific technical controls do we implement first?"*

---

### 8. COBIT 2019 (Governance Framework)

**Best for:** Decision rights, ownership, and performance metrics

**Core Components:**
- **EDM (Evaluate, Direct, Monitor):** Board-level governance
- **APO (Align, Plan, Organize):** Strategic alignment
- **BAI (Build, Acquire, Implement):** Solution delivery
- **DSS (Deliver, Service, Support):** Operations
- **MEA (Monitor, Evaluate, Assess):** Performance

**Key Governance Questions:**
- Who decides? (Decision rights)
- Who owns the risk? (Accountability)
- How do we measure success? (Metrics)
- How do we oversee execution? (Monitoring)

**Example Metrics:**
| Metric | Target |
|--------|--------|
| MFA adoption rate | 100% |
| Log ingestion rate | 100% of critical systems |
| Incident detection time (MTTD) | < 1 hour |
| Backup restore test success | > 95% |

**Key Question:** *"Who decides what, and how do we measure it?"*

---

## 🇸🇦 KSA Regulatory Frameworks

### 9. SAMA Cybersecurity Framework

**Applies to:** Licensed financial institutions (banks, fintech, insurance)

**Applicability for FinBridge Digital:**
- Licensed by Saudi Central Bank (SAMA)
- Financial sector obligations above national baseline

**Key Controls (violations identified in Assignments):**
| Clause | Requirement | Our Gap |
|--------|-------------|---------|
| 3.3.5.4e | MFA for privileged access | AWS root account without MFA |
| 3.3.5.4f | Quarterly access reviews | 35% over-privileged users |
| 3.x.x | Cloud security controls | Public S3 buckets |
| 3.x.x | Threat management process | No formal risk register |

**Key Question:** *"What does a bank/fintech need that others don't?"*

---

### 10. NCA ECC-1:2018 (Essential Cybersecurity Controls)

**Applies to:** All KSA government and critical infrastructure entities

**Status:** National baseline (everyone must meet this minimum)

**Key Requirements:**
| Domain | Requirement |
|--------|-------------|
| Governance | Cybersecurity leadership, strategy, policies |
| Risk Management | Risk assessment, treatment, register |
| Access Control | Least privilege, MFA, offboarding |
| Incident Response | IR plan, team, reporting to NCA |
| Business Continuity | BC/DR plans, testing |
| Network Security | Segmentation, firewalls |
| Data Protection | Encryption, backups, classification |

**Breach Reporting:**
- **Critical incidents:** Within 2 hours
- Security incident affecting health sector, critical infrastructure

**Key Question:** *"What's the absolute minimum every KSA entity must do?"*

---

### 11. PDPL (Personal Data Protection Law) — Royal Decree M/19

**Applies to:** Any entity processing personal data of Saudi individuals

**Effective:** March 2023 (full enforcement)

**Key Obligations:**
| Obligation | Requirement |
|------------|-------------|
| Consent | Valid, explicit consent for data collection |
| Purpose limitation | Use data only for stated purpose |
| Data subject rights | Access, correction, deletion |
| Breach notification | SDAIA within 72 hours |
| Subject notification | Affected individuals "without undue delay" |
| Vendor management | Data processing agreements required |
| Records retention | Maintain breach logs |

**Breach Definition:**
> Any breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to, personal data transmitted, stored, or otherwise processed.

**Key Point:** Breach is reportable regardless of whether damage is proven.

**Penalties:**
- Up to 5% of annual revenue for severe violations
- Reputational damage + potential criminal liability

**Key Question:** *"What must we do when personal data is exposed?"*

---

### 12. SHIC Guidelines (Saudi Health Informatics Center)

**Applies to:** Healthcare providers, health data processors

**Applicability for MedCore:**
- Hospital group with 280,000 patient records
- Health sector specific requirements

**Key Controls:**
- Health data classification
- Patient consent management
- Clinical system security
- Health information exchange security

**Key Question:** *"What's specific to healthcare data?"*

---

### 13. PCI-DSS v4.0 (Payment Card Industry)

**Applies to:** Entities handling cardholder data

**Applicability for FinBridge:**
- Recently approved for payment processing
- Will handle card data for mada integration

**Six Goals + 12 Requirements:**
| Goal | Requirements |
|------|--------------|
| Build secure network | 1-2 (firewalls, secure config) |
| Protect cardholder data | 3-4 (encryption, truncation) |
| Maintain vulnerability program | 5-6 (antimalware, secure dev) |
| Implement access control | 7-8 (need-to-know, MFA) |
| Monitor networks | 9-10 (logging, monitoring) |
| Maintain policy | 11-12 (testing, documentation) |

**Key Question:** *"What's required to safely process credit cards?"*

---

## Framework Integration Matrix

| Activity | Primary Framework | Supporting Framework |
|----------|-------------------|----------------------|
| **Program communication** | NIST CSF | COBIT (metrics) |
| **Audit readiness** | ISO 27001 | NCA ECC (KSA specific) |
| **Technical controls** | CIS Controls | ISO 27001 Annex A |
| **Governance** | COBIT | NIST CSF (Govern function) |
| **Incident response** | NIST SP 800-61 | ISO 27035 |
| **Risk assessment** | NIST SP 800-30 | ISO 31000 |
| **KSA compliance** | NCA ECC + SAMA + PDPL | ISO 27001 (mapped) |

---

## Framework Selection Decision Tree

```
Start: What's your primary need?

├─ "How do we talk about security to leadership?"
│   └─ Use: NIST CSF + COBIT (metrics)
│
├─ "We need to pass an audit / get certified"
│   └─ Use: ISO 27001 + relevant regulatory overlay
│
├─ "What technical controls do we implement first?"
│   └─ Use: CIS Controls (IG1 → IG2 → IG3)
│
├─ "Who decides what, and how do we measure it?"
│   └─ Use: COBIT
│
├─ "We're a KSA entity — what's mandatory?"
│   └─ Use: NCA ECC baseline + sector framework (SAMA/SHIC) + PDPL
│
└─ "We need ALL of the above"
    └─ Use: NIST CSF (map) + ISO 27001 (audit) + CIS (tech) + COBIT (governance)
```

---

## Common GRC Terms

| Term | Definition |
|------|------------|
| **Risk Register** | Documented list of identified risks with scores and treatment plans |
| **Residual Risk** | Risk remaining after controls are applied |
| **Risk Appetite** | Amount of risk organization is willing to accept |
| **Control Type** | Preventive (stops), Detective (finds), Corrective (fixes) |
| **MTTD** | Mean Time to Detect (incident detection speed) |
| **MTTR** | Mean Time to Respond/Recover |
| **SOC 2 Type II** | Audit of service organization controls over time |
| **BYOD** | Bring Your Own Device |
| **Shadow IT** | Unapproved systems used without IT knowledge |
| **IAM** | Identity and Access Management |
| **PAM** | Privileged Access Management |
| **SIEM** | Security Information and Event Management |
| **EDR** | Endpoint Detection and Response |
| **WORM** | Write Once, Read Many (immutable storage) |
| **Air-gapped** | Physically isolated from networks |

---

## Helpful Resources

- [NIST CSF 2.0](https://www.nist.gov/cyberframework)
- [NIST SP 800-61 Rev 2](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)
- [ISO 27001:2022](https://www.iso.org/standard/27001)
- [CIS Controls v8](https://www.cisecurity.org/controls/v8)
- [COBIT 2019](https://www.isaca.org/resources/cobit)
- [SAMA CSF](https://www.sama.gov.sa/en-US/Pages/Cybersecurity.aspx)
- [NCA ECC](https://nca.gov.sa/en/Pages/NationalCybersecurityAuthority.aspx)
- [PDPL (SDAIA)](https://sdaia.gov.sa/en/Pages/default.aspx)

---

*Reference document for CS3178 - Governance, Risk & Compliance*  
*Sarah Eid | S22107757 | Spring 2026*

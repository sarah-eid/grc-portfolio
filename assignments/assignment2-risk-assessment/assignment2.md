## Course Title: Governance, risk & compliance Course #: CS 3178

| **CS 3178** | **Governance, Risk & Compliance** | **Assignment 2** | **Spring 2026** |
| ----------- | --------------------------------- | ---------------- | --------------- |
| Name:       | Sarah Eid                         |                  |                 |
| Student ID: | S22107757                         | Section:         | 1               |

**Assignment 2 - Risk Assessment in GRC**

Work mode: Individual  
Total Marks: 10  
Submission: One week from date of issue  

---

**Instructions**

This assignment assesses your ability to conduct and document a structured information security risk assessment within a GRC context. You will analyze a realistic organizational scenario, identify and evaluate risks, and propose a risk treatment plan aligned to recognized frameworks.

1. All six questions are compulsory. Marks are shown per question.  
2. Your risk assessment must reference at least one recognized framework (e.g., ISO 31000, NIST RMF, ISO 27005).  
3. For quantitative questions, show your working — formulae and scoring rationale are assessed, not just the final number.  
4. Where asked to complete the risk register template (Question 3), you must complete all columns for a minimum of five risks.  
5. Professional presentation matters — responses should be clearly structured, use appropriate terminology, and be free of vague generalities.  

---

**Background: FinBridge Digital**

FinBridge Digital is a licensed fintech company headquartered in Riyadh, Saudi Arabia, with 420 employees across three offices (Riyadh, Jeddah, and Dubai). The company offers a mobile-first digital lending platform that processes personal and SME loan applications. FinBridge has been operational for three years and recently received regulatory approval from the Saudi Central Bank (SAMA) to expand its product suite to include payment processing services.

The company's key assets and operations include:

1. A cloud-hosted core lending platform on AWS (Frankfurt region) serving 95,000 active customers  
2. A mobile application available on iOS and Android, handling an average of 4,200 transactions per day  
3. An internal CRM system hosted on-premise in Riyadh, containing KYC (Know Your Customer) data on all customers including national ID numbers, income data, and credit history  
4. A data analytics team that uses a third-party BI platform (SaaS) to process customer behavioral data  
5. API integrations with three Saudi banks, the SIMAH credit bureau, and the Saudi national payment network (mada)  

FinBridge is subject to the following regulatory requirements:

1. SAMA Cybersecurity Framework (CSF) — mandatory for licensed financial institutions  
2. NCA Essential Cybersecurity Controls (ECC-1:2018)  
3. Saudi Personal Data Protection Law (PDPL) — Royal Decree M/19, effective 2023  
4. PCI-DSS v4.0 — applicable following approval for payment processing  

---

**Current Security Situation**

**Finding 1 — Identity and Access Management**  
Approximately 35% of employees have administrative privileges on at least one internal system that their role does not require. The offboarding process for employees lacks a formal checklist — in three recent cases, departed employees' Active Directory accounts remained active for 7 to 21 days after their last working day.

**Finding 2 — Third-Party Risk**  
FinBridge has signed contracts with 14 third-party vendors who have some form of access to internal systems or customer data. Of these, only 4 have provided an up-to-date SOC 2 Type II report or equivalent assurance. The BI platform vendor (Processing Analytics Ltd.) is headquartered in the UK and has access to anonymized but re-identifiable customer behavioral data. No formal vendor risk assessment has been completed for this vendor.

**Finding 3 — Cloud Security**  
A preliminary review of the AWS environment revealed two S3 buckets with public read access that were created during a development sprint six months ago and never locked down. One bucket contains test data that includes a sample of real customer records (approximately 2,400 records) used for load testing. The AWS root account does not have MFA enabled.

**Finding 4 — Incident History**  
In the past 12 months, FinBridge has experienced the following logged events:

1. Two credential stuffing attacks against the mobile application login — both were blocked by rate limiting, but 180 accounts were temporarily locked  
2. One successful phishing attack against a finance department employee — no financial loss occurred, but the attacker had access to internal financial reports for approximately 4 hours before detection  
3. One API misconfiguration incident that briefly exposed internal loan application status data to unauthenticated callers — resolved in 2 hours, but no formal incident report was completed  

**Finding 5 — Governance and Documentation**  
FinBridge has an Information Security Policy that was last reviewed 26 months ago. There is no formal risk register. Business continuity and disaster recovery plans exist as draft documents that have never been tested. The security team consists of Omar and two junior analysts — there is no dedicated compliance officer, and compliance activities are handled informally by the legal team.

---

## **Q1**

Define the scope and objectives of a formal risk assessment for FinBridge Digital. Identify which assets, processes, and departments should be in scope, and explain why. Then identify which risk assessment methodology you would recommend for this organization (qualitative, quantitative, or semi-quantitative) and justify your choice with reference to FinBridge's specific context.

**Answer:**

Scope Definition  

In Scope Assets, Processes, and Departments:

| Category | Items in Scope | Justification |
|----------|--------------|--------------|
| Assets | Cloud-hosted core lending platform (AWS, Frankfurt), Mobile app (iOS/Android), On-premise CRM (KYC data), BI platform (SaaS), API integrations (3 banks, SIMAH, mada) | These systems handle sensitive financial and personal data, so any compromise would directly impact compliance and operations. The S3 buckets with public access are also included since they already represent a confirmed risk. |
| Processes | Identity and Access Management (IAM), Offboarding, Third-party vendor management, Cloud security configuration, Incident response, Business continuity/disaster recovery | Each of Omar’s findings highlights weaknesses in these processes, making them critical to assess. |
| Departments | IT/Security, Finance, HR, Legal, Data Analytics, Development | The risks are not isolated — they span multiple teams. |

Excluded from Scope:  
Physical office security, general HR administrative records (non-KYC), and non-digital operations.

Risk Assessment Methodology Recommendation  

Recommended Approach: Semi-quantitative  

Trade-offs:  
- Less precise than fully quantitative methods  
- More practical and easier to implement  

---

## **Q2**

For each of the five findings documented by Omar Khalid, identify the primary risk(s) it represents. For each risk, identify: (a) the threat source, (b) the vulnerability being exploited, (c) the potential impact on the CIA triad, and (d) an initial likelihood and impact rating on a 1–5 scale with brief justification for each rating.

**Answer:**

**Finding 1 — Identity and Access Management**

- Primary Risk: Unauthorized access due to excessive privileges and delayed offboarding  
- Threat Source: Internal users or external attackers using old credentials  
- Vulnerability: 35% over-privileged users + accounts active 7–21 days after exit  
- CIA Impact:  
  - Confidentiality → data exposure  
  - Integrity → data tampering  
  - Availability → potential system disruption  
- Likelihood: 4 (High) — repeated offboarding failures already observed  
- Impact: 4 (High) — sensitive KYC data involved  

---

**Finding 2 — Third-Party Risk**

- Primary Risk: Vendor-related data breach or misuse  
- Threat Source: Compromised vendor systems or insider misuse  
- Vulnerability: Lack of vendor assessments; BI vendor not evaluated  
- CIA Impact: Confidentiality and integrity risks  
- Likelihood: 3 (Medium) — no incidents yet, but lack of controls  
- Impact: 5 (Very High) — PDPL breach implications  

---

**Finding 3 — Cloud Security**

- Primary Risk: Public exposure of customer data + root account compromise  
- Threat Source: External attackers or public internet access  
- Vulnerability: Public S3 buckets + no MFA on root account  
- CIA Impact:  
  - Confidentiality → exposed data  
  - Availability → possible deletion or manipulation  
- Likelihood: 5 (Very High) — exposure already exists  
- Impact: 5 (Very High) — confirmed sensitive data exposure  

---

**Finding 4 — Incident History**

- Primary Risk: Repeat or escalated cyber incidents  
- Threat Source: External attackers (phishing, credential stuffing)  
- Vulnerability: No structured incident reporting or learning process  
- CIA Impact: All three aspects affected  
- Likelihood: 4 (High) — multiple incidents already occurred  
- Impact: 3 (Medium) — limited damage so far  

---

**Finding 5 — Governance and Documentation**

- Primary Risk: Failure to respond effectively to major incidents  
- Threat Source: Internal weaknesses or external crises  
- Vulnerability: Outdated policies, no risk register, untested BCP/DR  
- CIA Impact: Mainly availability and integrity  
- Likelihood: 3 (Medium)  
- Impact: 5 (Very High) — potential business shutdown  

---

## **Q3**

Using the risk register template provided below, document a minimum of five risks identified from the scenario. Complete all columns. Calculate a risk score using the formula: Risk Score = Likelihood × Impact. Assign a risk level and propose a specific treatment action for each risk.

**Answer:**

| Risk ID | Risk Description | Asset / Process | Threat Source | Likelihood | Impact | Risk Score | Risk Level | Current Controls | Recommended Treatment |
|--------|----------------|----------------|--------------|-----------|--------|------------|------------|------------------|------------------------|
| R-001 | Public exposure of 2,400 real customer records due to publicly accessible S3 buckets | AWS S3 / Cloud security | External users | 5 | 5 | 25 | Critical | None | Restrict access, enable MFA delete, automated scans |
| R-002 | Unauthorized access by former employees due to incomplete offboarding | AD / IAM | Former employees | 4 | 4 | 16 | High | Informal process | Automated offboarding + access reviews |
| R-003 | AWS root account compromise due to missing MFA | AWS IAM | External attackers | 5 | 5 | 25 | Critical | None | Enable MFA + restrict root access |
| R-004 | Third-party data breach via BI vendor | Customer data | Vendor | 3 | 5 | 15 | High | None | Vendor risk assessment + contracts |
| R-005 | Excessive privileged access | Internal systems | Internal misuse | 4 | 4 | 16 | High | None | PAM + role-based access review |

**Scoring Formula:**  
Risk Score = Likelihood × Impact  

---

## **Q4**

FinBridge's CISO must present a risk treatment plan to the board.

**Answer:**

**Risk Treatment Options (ISO 31000):**
- Accept  
- Avoid  
- Transfer  
- Mitigate  

**R-001 (S3 Buckets):**
- Treatment: Mitigate + Avoid  
- Plan: Lock buckets, remove real data, automate checks  
- Residual Risk: Low  

**R-003 (Root Account):**
- Treatment: Mitigate  
- Plan: Enable MFA, restrict access  
- Residual Risk: Low  

**R-002 (Offboarding):**
- Treatment: Mitigate + Transfer  
- Plan: Automated offboarding + cyber insurance  
- Residual Risk: Medium  

---

## **Q5**

Design a risk governance framework and explain regulatory requirements.

**Answer:**

**(a) Framework**

- Board: Oversight and risk appetite approval  
- CISO: Owns risk register  
- Risk Owners: Department-level responsibility  
- Internal Audit: Validation  

**Escalation:**
- Critical → CEO (24h) → Board (48h)  

**Review Frequency:**
- Weekly → top risks  
- Monthly → full register  
- Quarterly → board  
- Annually → reassessment  

---

**(b) Regulatory Requirements**

**SAMA CSF:**
- MFA for privileged access  
- Access reviews required  
- Cloud security controls required  

**PDPL:**
- 72-hour breach notification  
- Notify affected individuals  
- Vendor data agreements  

---

## **Q6**

Analyze PDPL breach scenario.

**Answer:**

**(a) Breach Occurrence:**

Yes — this is a reportable breach. Public access qualifies as unauthorized access even without confirmed exploitation.

**(b) Immediate Actions:**

1. Lock S3 buckets  
2. Preserve logs  
3. Notify SDAIA within 72 hours  
4. Notify affected customers  
5. Remove real data  
6. Document incident  

**(c) Risk Register Update:**

- Likelihood: Reduced after fix  
- Impact: Remains high  
- New controls:
  - Automated S3 scanning  
  - Synthetic data policy  
  - Breach response plan  

---

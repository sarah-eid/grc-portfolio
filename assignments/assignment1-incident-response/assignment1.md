## Course Title: Governance, risk & compliance Course #: CS 3178

| **CS 3178** | **Governance, Risk & Compliance** | **Assignment 1** | **Spring 2026** |
| ----------- | --------------------------------- | ---------------- | --------------- |
| Name:       | Sarah Eid                         |                  |                 |
| Student ID: | S22107757                         | Section:         | 1               |

**Assignment 1 - Incident Management & Response**

Work mode: Individual  
Total Marks: 10  
Submission: One week from date of issue  

---

**Instructions**

- Answer all six questions. Partial credit may be awarded for incomplete but relevant answers.  
- Support your answers with reference to established frameworks where applicable (e.g., NIST SP 800-61, ISO 27035).  
- Where the question asks you to recommend or propose, justify your answer — do not simply list actions.  
- Marks are allocated as shown. Manage your effort accordingly.  
- Plagiarism between submissions will result in disqualification for both parties.  

---

**Background: MedCore Health Systems**

MedCore Health Systems is a mid-sized private hospital group operating across five cities in Saudi Arabia. The organization manages electronic health records (EHR) for approximately 280,000 active patients. MedCore's IT infrastructure includes on-premise servers at each hospital location and a central data center in Riyadh that hosts the EHR system, billing platform, and HR database.  

MedCore is subject to the following regulatory and standards obligations:

- Saudi Arabia National Cybersecurity Authority (NCA) Essential Cybersecurity Controls (ECC-1:2018)  
- Saudi Health Informatics Center (SHIC) health data protection guidelines  
- Internal ISO 27001-aligned Information Security Management System (ISMS)  

---

**The Incident**

**Monday, 07:45 AM — Initial Detection**  
The head nurse at MedCore's Jeddah branch reports that the patient scheduling system is displaying an error and appointment records appear blank. The issue is logged as a routine software glitch.  

**Monday, 09:15 AM — Escalation**  
Multiple branches report similar issues. Investigation reveals:  
- Unauthorized admin account (`sysbackup_admin`) created  
- SQL activity across databases  
- Backup files are empty (0 bytes)  
- 47 GB of outbound data transfer  

**Monday, 10:00 AM — Ransom Note**  
Systems are encrypted and ransom is demanded (12 Bitcoin).  

**Monday, 10:30 AM — Scope Assessment**  
- All five hospitals affected  
- Systems encrypted  
- Attack traced to phishing email  
- Manual operations activated  

---

### **Q1: Incident classification** [2 marks]

**Answer:**

**Incident Type(s):**

This is a multi-category incident involving:  
1. Ransomware / Malware incident – systems encrypted, ransom note left.  
2. Data breach (exfiltration) – 47 GB of patient, billing, and HR data transferred.  
3. Unauthorized access / compromised account – malicious admin account created.  

**Severity Level:** Critical (NIST) or Crisis  

**Justification using CIA Triad:**

- Confidentiality – Sensitive patient data exfiltrated  
- Integrity – Databases corrupted and backups wiped  
- Availability – Systems inaccessible across all hospitals  

**Why severe:**

- Affects all locations  
- Backups destroyed  
- Patient care disrupted  
- Regulatory notification triggered  

---

### **Q2: NIST Incident Response Lifecycle mapping** [2.5 marks]

**Answer:**

1. **Preparation**  
Lacked IR plan, training, monitoring. Should implement EDR, phishing training, defined IR roles.  

2. **Detection & Analysis**  
Misclassified incident. Should correlate reports and escalate faster.  

3. **Containment**  
Isolate data center, block external IP, disable compromised accounts.  

4. **Eradication**  
Remove malware, reset credentials, rebuild systems.  

5. **Recovery**  
Restore from verified backups or reconstruct data. Test systems before reconnecting.  

6. **Post-Incident Activity**  
Produce report, update risk register, improve controls.  

---

### **Q3: Notification obligations** [1.5 marks]

**Answer:**

**Internal notifications (immediate):**
- CEO & CISO  
- Legal  
- PR  
- Hospital directors  
- HR  
- Patients  

**External notifications:**

| Party | Timeframe | Basis |
|------|----------|------|
| NCA | Immediate (≤2 hours) | ECC-1 |
| SDAIA | ≤72 hours | PDPL |
| SHIC | ≤24 hours | Health guidelines |
| Law enforcement | Immediate | Criminal act |
| Patients | ≤72 hours | PDPL |

**NCA notification must include:**
- Organization name  
- Time of discovery  
- Incident description  
- Systems affected  
- Number of individuals  
- Indicators of compromise  
- Actions taken  
- Contact person  

---

### **Q4: Ransom decision briefing** [1.5 marks]

**Answer:**

To: CEO, MedCore Health Systems  
Subject: Ransom Payment Recommendation  

**Risks of paying:**
- Legal issues  
- No guarantee of recovery  
- Encourages future attacks  

**Risks of not paying:**
- Operational disruption  
- Data exposure  
- Regulatory penalties  

**Recommendation: DO NOT PAY**

Focus on recovery, law enforcement engagement, and compliance.  

---

### **Q5: Post-incident report & improvements** [1.5 marks]

**Answer:**

**(a) Report sections:**
- Executive Summary  
- Timeline  
- Root Cause  
- Impact  
- Response Effectiveness  
- Notifications  
- Improvements  
- Lessons Learned  
- Action Plan  

**(b) Control improvements:**

| Failure | Improvement |
|--------|------------|
| Phishing attack | MFA + training |
| Unauthorized account | Monitoring alerts |
| Backup failure | Immutable backups |
| Lateral spread | Network segmentation |
| Misclassification | Incident escalation rules |

**(c) Risk register update:**

| Before | After |
|-------|------|
| Likelihood: Medium | Certain |
| Impact: High | Extreme |
| Risk: High | Critical |

---

### **Q6: GRC failures** [1 mark]

**Answer:**

**Governance:**

| Failure | Solution |
|--------|---------|
| Misclassification | IR policy |
| No coordination | Central SOC |

**Risk Management:**

| Failure | Solution |
|--------|---------|
| Backup failure | Restore testing |
| No ransomware planning | Threat modeling |

**Compliance:**

| Failure | Solution |
|--------|---------|
| Delayed reporting | Compliance tracking |
| No segmentation | Access controls |

---

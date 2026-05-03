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

Read the following case study carefully before answering the questions. All questions are compulsory. Your answers must demonstrate understanding of the incident response lifecycle, reporting obligations, and GRC principles covered in the lecture.

1. Answer all six questions. Partial credit may be awarded for incomplete but relevant answers.  
2. Support your answers with reference to established frameworks where applicable (e.g., NIST SP 800-61, ISO 27035).  
3. Where the question asks you to 'recommend' or 'propose', justify your answer — do not simply list actions.  
4. Marks are allocated as shown. Manage your effort accordingly.  
5. Plagiarism between submissions will result in disqualification for both parties.  

---

**Background: MedCore Health Systems**

MedCore Health Systems is a mid-sized private hospital group operating across five cities in Saudi Arabia. The organization manages electronic health records (EHR) for approximately 280,000 active patients. MedCore's IT infrastructure includes on-premise servers at each hospital location and a central data center in Riyadh that hosts the EHR system, billing platform, and HR database.

MedCore is subject to the following regulatory and standards obligations:

1. Saudi Arabia National Cybersecurity Authority (NCA) Essential Cybersecurity Controls (ECC-1:2018)  
2. Saudi Health Informatics Center (SHIC) health data protection guidelines  
3. Internal ISO 27001-aligned Information Security Management System (ISMS)  

---

**The Incident**

**Monday, 07:45 AM — Initial Detection**  
The head nurse at MedCore's Jeddah branch calls the IT helpdesk to report that the hospital's patient scheduling system is displaying an error and all appointment records for the day appear blank. The helpdesk technician, Fahad, logs the call as a routine software glitch and escalates it to the application support team.

**Monday, 09:15 AM — Escalation**  
Fahad receives three more calls — from the Riyadh branch, the Dammam branch, and the central billing department. All report similar symptoms: systems are accessible but data is missing or corrupted. Fahad escalates to the IT Security Manager, Nora Al-Rashidi.

Nora logs into the central data center monitoring dashboard and immediately notices the following:

1. An unfamiliar administrator account – ‘sysbackup_admin' – was created at 02:14 AM on Sunday night  
2. The account ran a series of SQL commands across the EHR and billing databases between 02:30 AM and 05:45 AM  
3. The central backup server shows all backup jobs as 'completed successfully,' but when Nora checks the backup files, they are empty — 0 bytes  
4. Outbound data transfers of approximately 47 GB were logged to an external IP address between 03:00 AM and 04:30 AM  

**Monday, 10:00 AM — Discovery of Ransom Note**  
A member of the Riyadh IT team finds a text file named 'READ_ME_IMMEDIATELY.txt' on the file server desktop. The file reads:

**Ransom Note**  
Your systems have been compromised. All patient records, billing data, and HR files have been exfiltrated and encrypted. You have 72 hours to pay 12 Bitcoin to the wallet address below or this data will be published publicly. Do not contact law enforcement. Do not attempt recovery — your backups have been wiped. We will know.

**Monday, 10:30 AM — Scope Assessment**  
Nora and her team conduct a rapid preliminary assessment. Their findings are as follows:

1. All five hospital locations are affected — the attack originated from the central Riyadh data center and propagated across the WAN  
2. The EHR system, billing platform, and HR database are all encrypted and inaccessible  
3. The 'sysbackup_admin' account was traced to a phishing email opened by an IT staff member on Thursday evening — the email contained a malicious macro-enabled Excel attachment  
4. There is no evidence that clinical equipment (e.g., imaging systems, lab systems) was affected  
5. Patient care is continuing manually using paper records, but the hospital cannot admit new patients through the normal digital process  

---

## **Q1** [2 marks]

Classify this incident. Identify the incident type(s), assign a severity level, and justify your classification using the CIA triad.

**Answer:**

**Incident Type(s):**

This is a multi-category incident involving:

1. Ransomware / Malware incident – systems encrypted, ransom note left.  
2. Data breach (exfiltration) – 47 GB of patient, billing, and HR data transferred.  
3. Unauthorized access / compromised account – malicious admin account created.  

**Severity Level:** Critical  

**Justification using CIA Triad:**

- Confidentiality – Sensitive health data was exfiltrated  
- Integrity – Databases corrupted and backups wiped  
- Availability – Systems inaccessible across all hospitals  

**Why severe:**

- All five hospitals affected  
- Backups destroyed  
- Patient care disrupted  
- Regulatory notification required  

---

## **Q2** [2.5 marks]

Map this incident to the NIST SP 800-61 Incident Response Lifecycle.

**Answer:**

1. **Preparation**  
Lacked incident response plan, phishing training, monitoring.  

2. **Detection & Analysis**  
Incident misclassified initially. Should correlate reports faster.  

3. **Containment**  
Isolate systems, block IP, disable compromised accounts.  

4. **Eradication**  
Remove malware, reset credentials, rebuild systems.  

5. **Recovery**  
Restore from clean backups, test systems.  

6. **Post-Incident Activity**  
Report incident, update controls, improve monitoring.  

---

## **Q3** [1.5 marks]

Identify notification obligations.

**Answer:**

**Internal:**
- CEO, CISO  
- Legal  
- PR  
- Hospital directors  
- HR  

**External:**

| Party | Timeframe | Basis |
|------|----------|------|
| NCA | Immediate | ECC-1 |
| SDAIA | 72 hours | PDPL |
| SHIC | 24 hours | Guidelines |
| Law enforcement | Immediate | Criminal |
| Patients | ~72 hours | PDPL |

**NCA notification includes:**
- Organization  
- Time  
- Description  
- Systems affected  
- Individuals impacted  
- IoCs  
- Actions taken  
- Contact person  

---

## **Q4** [1.5 marks]

Ransom payment decision.

**Answer:**

**Recommendation: DO NOT PAY**

**Reasons:**
- No guarantee of recovery  
- Encourages attacks  
- Legal concerns  

**Alternative:**
- Restore systems  
- Notify authorities  
- Continue operations manually  

---

## **Q5** [1.5 marks]

Post-incident report.

**Answer:**

**Sections:**
- Executive summary  
- Timeline  
- Root cause  
- Impact  
- Response review  
- Notifications  
- Improvements  
- Lessons learned  
- Action plan  

**Control improvements:**

| Failure | Improvement |
|--------|------------|
| Phishing | Training + MFA |
| Unauthorized account | Monitoring |
| Backup failure | Offline backups |
| Lateral spread | Network segmentation |
| Misclassification | IR procedures |

**Risk update:**

| Before | After |
|-------|------|
| Likelihood: Medium | Certain |
| Impact: High | Extreme |
| Risk: High | Critical |

---

## **Q6** [1 mark]

GRC failures.

**Answer:**

**Governance:**

| Failure | Solution |
|--------|---------|
| Misclassification | IR policy |
| No coordination | Central SOC |

**Risk Management:**

| Failure | Solution |
|--------|---------|
| Backup failure | Testing |
| No planning | Threat modeling |

**Compliance:**

| Failure | Solution |
|--------|---------|
| Delayed reporting | Monitoring |
| No segmentation | Access controls |

---

## Course Title: Governance, risk & compliance Course #: CS 3178

| **CS 3178** | **Governance, Risk & Compliance** | **Lab03** | **Spring 2026** |
| ----------- | --------------------------------- | --------- | --------------- |
| Name:       | Sarah Eid                         |           |                 |
| Student ID: | S22107757                         | Section:  | 1               |

**Lab03 - KSA Cybersecurity Frameworks and Compliance Cycle in CISO Assistant Community**

Work mode: Individual  
Prerequisite: Lab02 completed  
Tool: CISO Assistant Community  

---

**Purpose**

In Lab02, you installed and launched CISO Assistant Community locally. In this lab, you will use the same platform to practice the lecture topic on KSA cybersecurity frameworks and the end-to-end compliance cycle. The goal is not to memorize framework names only, but to organize a practical compliance exercise inside the tool: scope a case, decide which KSA rules apply, create a compliance assessment, update requirement statuses, and attach evidence notes.

---

**Learning outcomes**

- Create a new domain and perimeter in CISO Assistant for a KSA case organization.  
- Translate the lecture idea of baseline + sector + data/privacy overlay into a practical compliance exercise.  
- Create a compliance assessment from an imported framework and assess selected requirements using tool statuses.  
- Record evidence notes that justify why specific KSA frameworks apply to the scenario.  
- Produce a short, organized audit-style summary from the work completed in the platform.  

---

**Scenario used in this lab**

Scenario: A KSA bank is launching a new mobile banking feature for customer onboarding and transaction access. The service processes customer personal data, authentication data, and transaction-related information. Based on the lecture, the student should recognize that this scenario sits on a stack of requirements: a national baseline, a financial-sector regulator, and a data/privacy overlay.  

Before you start: keep CISO Assistant running from Lab02 and open it in your browser at https://localhost:8443/. Use only sample names and placeholder evidence. Do not upload any real personal, banking, or institutional confidential data.

---

**Task 1: log in and verify the local platform**

- Open the browser and go to https://localhost:8443/. If a certificate warning appears, proceed because this is your local lab environment.  
- Log in using the admin account you created in Lab02.  
- Confirm that the system loads correctly before starting the exercise. If the interface does not load, check that Docker is running and that your containers are up.  
- Optional terminal check: run docker compose ps inside the ciso-assistant-community folder.  

---

**Task 2: create a domain for the lab case**

---

**Task 3: create the perimeter for the scenario**

---

**Task 5: import one framework from the library**

---

**Task 6: create the compliance assessment**

---

**Task 7: select at least 10 relevant requirements and assess them**

---

**Task 8: add evidence notes to justify your decisions**

---

**Task 9: build a mini compliance summary inside your work notes**

In this scenario, the system is a banking service in Saudi Arabia, so more than one framework applies. The SAMA Cyber Security Framework is important because it is specific to banks, the NCA Essential Cybersecurity Controls provide the general baseline, and the PDPL applies since the system handles customer personal data. Overall, the system is only partially compliant, because some controls like leadership and authentication are already done, but others such as logging, monitoring, and incident response are still in progress or not implemented yet. This means the system is not fully ready for release. To improve, the organization should work on improving logging and monitoring, finish and test incident response and business continuity plans, and make sure data protection and privacy controls fully meet PDPL requirements.

---

**Summary Table**

| Requirement | Status | Result |
|------------|--------|--------|
| 5.1 Leadership and commitment | Done | Compliant |
| 6.1.1 Risk planning | In progress | Partially compliant |
| A.5.15 Access control | In progress | Partially compliant |
| A.5.17 Authentication information | Done | Compliant |
| A.8.15 Logging | In progress | Partially compliant |
| A.8.16 Monitoring activities | To do | Non compliant |
| A.5.24 Incident management | In progress | Partially compliant |
| A.5.30 Business continuity | To do | Non compliant |
| A.5.34 Privacy and PII protection | In progress | Partially compliant |
| A.8.24 Use of cryptography | To do | Non compliant |

---

**Reflection questions**

Starting with scope and applicability is useful because it helps identify what actually needs to be assessed instead of wasting time on irrelevant controls. It also makes the whole process clearer and more focused. In this case, using only one framework is not enough because the system is a banking service, so it has to follow sector regulations like SAMA, general cybersecurity requirements from NCA ECC, and privacy laws like PDPL. Each one covers a different aspect of security. The easiest evidence to collect is usually written policies or procedures since they already exist in most organizations. On the other hand, the hardest evidence is things like system logs or real monitoring data because they depend on the system being fully implemented. Marking a control as compliant without proper evidence is risky because it may lead to incorrect results and serious issues if a real audit happens.

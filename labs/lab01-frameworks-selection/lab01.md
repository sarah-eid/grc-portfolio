## Course Title: Governance, risk & compliance Course #: CS 3178

| **CS 3178** | **Governance, Risk & Compliance** | **Lab01** | **Spring 2026** |
| ----------- | --------------------------------- | --------- | --------------- |
| Name:       | Sarah Eid                         |           |                 |
| Student ID: | S22107757                         | Section:  | 1               |

**Lab01 - Cybersecurity frameworks selection and incident stress test**

Work mode: team-based activity (3-4 students). Each student submits their own deliverables.

**Description  
**In real organizations, cybersecurity programs rarely use only one framework. Instead, teams combine frameworks for different purposes, for example a program communication map, a management system for audit readiness, a technical control baseline, and a governance layer for decision rights and oversight. In this lab you will act as a small GRC consulting team. You will choose a framework mix for a scenario, then stress-test that choice using an incident twist, and produce a short, realistic plan with evidence expectations. The intent is practical decision-making, not memorizing clauses.

**Frameworks in scope (high-level only)**

- NIST CSF: used to describe the program in a clear structure and communicate maturity and priorities (Identify, Protect, Detect, Respond, Recover).
- ISO/IEC 27001: used to structure an information security management system, risk treatment discipline, and audit evidence.
- CIS Controls: used to prioritize technical implementation and engineering actions.
- COBIT: used for governance, roles, decision rights, performance measurement, and oversight. Consider it the "who decides and how we measure" layer.

**Task 1: choose the framework mix**

Pick a primary mix for your scenario. A common answer is NIST CSF + ISO 27001 + CIS Controls, with COBIT as the governance wrapper. You may choose a different mix if you justify it.

**Deliverable A**: a short selection memo (about 150-200 words) that answers all of the following in plain language:

- which framework is your program "map" for communicating cybersecurity work to leadership
- which framework gives management system discipline and audit readiness
- which framework drives technical control prioritization
- where COBIT fits for governance, for example decision rights, ownership, and oversight metrics
- one sentence describing how these will integrate in practice (not just "we will use them all")

The proposed framework of a cybersecurity program that we are suggesting follows the NIST CSF framework due to its high-level framework of Identify, Protect, Detect, Respond, and Recover, which helps in the communication of the program to the leadership and stakeholders. we are also suggesting the ISO/IEC 27001 framework that follows the implementation of the risk management processes through documentation and audit. CIS Controls also follow the technical implementation of the access control hardening and protection of the backups. we are also suggesting the inclusion of the COBIT framework so that it provides governance by clearly defining the decision and performance metrics. This way, we can easily identify the deficiencies in the technical implementation, audit, and governance.

Student observation (1-2 sentences): what would go wrong if the organization chose only one framework?

If the organization decides to choose one framework, it will lack technical depth, audit, and governance, and this will create a gap between strategy, controls, and accountability.

**Task 2: incident stress test and mapping (3 actions only)**

Step A: pick one scenario (your instructor may assign one to your team)

Scenario A, fintech startup: cloud-native, fast releases, handles customer PII and payment-related data, partner demands assurance soon, weak logging, inconsistent access control.

Scenario B, small clinic: sensitive records, many SaaS tools, audit pressure, phishing exposure, unclear incident response.

Scenario C, university IT: many users and devices, frequent account compromise attempts, limited budget, inconsistent patching, shadow IT.

Step B: after you select your frameworks, your instructor will give one incident twist

Incident 1, ransomware: phished account, credentials reused, disruption, backup uncertainty.

Incident 2, cloud exposure: storage misconfiguration, data exposed, found by external researcher.

Incident 3, vendor breach: SaaS provider compromised, some records leaked, unclear scope.

**Deliverable B:** complete exactly three action rows using this template. _Three rows is a hard limit._

Row template (repeat 3 times)

- What failed (one sentence tied to the incident)
- NIST CSF function (Identify, Protect, Detect, Respond, Recover)
- ISO 27001 theme (choose one): risk process, policy, access control, logging/monitoring, incident management, supplier security, business continuity
- CIS Controls area (broad label): account management, secure configuration, vulnerability management, logging, data protection, incident response, backup/recovery
- Action (one line, specific, implementable)
- Evidence (one item that would prove it is implemented, for example an access review report, a SIEM dashboard screenshot, a backup restore test record, a ticket showing change approval)

Action 1

- What failed: We only checked vendor security once a year instead of monitoring it constantly.
- NIST CSF: Identify
- ISO 27001: Supplier security
- CIS Controls: Vulnerability management
- Action: Start using a vendor risk platform for real-time security alerts.
- Evidence: A vendor report showing a "Critical" status alert.

Action 2

- What failed: We didn't change the vendor's login keys immediately after they were hacked.
- NIST CSF: Protect
- ISO 27001: Access control
- CIS Controls: Account management
- Action: Switch to automated, short-lived API keys instead of permanent passwords.
- Evidence: A system log showing keys rotating automatically.

Action 3

- What failed: We couldn't see what the hackers did because the vendor's logs weren't sent to our system.
- NIST CSF: Detect
- ISO 27001: Logging/monitoring
- CIS Controls: Logging
- Action: Connect all critical vendor logs directly to our SIEM dashboard.
- Evidence: A screenshot of the SIEM showing active vendor log data.

Student observation (2-3 sentences): which of your three actions is most likely to be delayed in a real organization, and why?

The action in (SaaS Log Ingestion) is most likely to be delayed. Many SaaS providers charge extra for "Log Streaming" or API access to logs, and the internal IT team may resist the added cost and technical complexity of integrating different log formats into the company's SIEM.

**Task 3: integration and governance note**

In this task, please write a brief "integration note" (5-6 lines) instead of a full paragraph. Focus on the key points that make integration work in practice:

- Who owns each part of the framework (ownership)?
- What metrics will track progress (metrics)?
- Identify one potential integration issue and how it can be prevented (integration risk).

Ownership: Security leadership will be responsible for the outcomes of the NIST CSF, compliance will oversee the processes of the ISO 27001, engineering will overlookthe implementation of the CIS Controls, and the executives will be in charge of everything through the COBIT decision structures.

Metrics: The important metrics will include the percentage of MFA, the rate at which the logs are ingested, the rate at which the incidents are detected, and the rate at which the backups are restored. Integration risk: The frameworks could be used in isolation, leading to integration risks.

Prevention: The prevention of integration risks will be through the utilization of a single risk register and dashboard that links the CIS controls and the ISO evidence to the outcomes of the NIST CSF and the oversight of the COBIT.

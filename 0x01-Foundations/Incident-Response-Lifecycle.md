# 🚨 Incident Response Lifecycle

## 1. What is Incident Response?
Incident Response (IR) is a structured approach used to manage and handle security incidents in a way that limits damage, reduces recovery time, and preserves evidence.

In a SOC environment, incident response bridges the gap between **detection** and **recovery**, ensuring that threats are handled efficiently and consistently.

---

## 2. Relationship Between SOC and Incident Response
While the SOC focuses on **monitoring and detection**, Incident Response focuses on **action and control**.

- SOC identifies and investigates suspicious activity
- Incident Response executes containment and remediation
- DFIR supports deep forensic investigation when required

Clear separation of responsibilities is critical to avoid confusion during high-pressure incidents.

---

## 3. NIST Incident Response Lifecycle
The most widely adopted IR framework is defined by NIST and consists of six phases.

---

### 🔹 1. Preparation
Preparation determines how effective the response will be.

Activities include:
- Defining incident response policies
- Establishing roles and escalation paths
- Deploying logging and monitoring controls
- Training SOC and IR teams
- Preparing investigation and response tools

Organizations that fail in preparation often fail during real incidents.

---

### 🔹 2. Detection & Analysis
This phase begins when suspicious activity is detected.

Key activities:
- Alert triage and validation
- Severity classification
- Scope identification
- Evidence collection
- Initial root cause assessment

The goal is to determine whether an alert represents a real incident and how serious it is.

---

### 🔹 3. Containment
Containment aims to limit the spread and impact of the incident.

Types of containment:
- **Short-term:** Isolate systems, disable accounts
- **Long-term:** Apply patches, modify firewall rules

Containment decisions must balance security with business continuity.

---

### 🔹 4. Eradication
Eradication removes the root cause of the incident.

Activities include:
- Removing malware or malicious scripts
- Closing exploited vulnerabilities
- Revoking compromised credentials
- Hardening affected systems

Failure to fully eradicate threats can lead to reinfection.

---

### 🔹 5. Recovery
Recovery restores systems to normal operation.

Activities include:
- System restoration
- Monitoring for recurring activity
- Validating system integrity
- Returning services to production

Recovery is not complete until confidence is restored.

---

### 🔹 6. Lessons Learned
This phase improves future defenses.

Activities include:
- Incident documentation
- Root cause analysis
- Detection rule improvements
- Process and control updates

Mature SOCs treat every incident as a learning opportunity.

---

## 4. When to Escalate an Incident
Escalation decisions are based on:
- Severity level
- Business impact
- Data sensitivity
- Regulatory requirements

Not every alert becomes an incident, and not every incident requires full DFIR involvement.

---

## 5. Incident Classification
Common incident categories include:
- Malware infection
- Phishing
- Insider threat
- Account compromise
- Ransomware
- Data exfiltration

Correct classification ensures appropriate response actions.

---

## 6. Evidence Handling Considerations
During incident response:
- Evidence must be preserved
- Actions should be documented
- Logs should be protected from tampering

Poor evidence handling can compromise investigations and legal actions.

---

## 7. Incident Response Mindset
Effective incident responders:
- Stay calm under pressure
- Follow structured processes
- Communicate clearly
- Balance speed with accuracy
- Document every decision

This project applies the incident response lifecycle across multiple realistic scenarios to demonstrate operational readiness.

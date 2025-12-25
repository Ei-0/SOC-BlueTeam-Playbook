# 🛡️ Security Operations Center (SOC) Overview

## 1. What is a SOC?
A Security Operations Center (SOC) is a centralized function responsible for continuously monitoring, detecting, analyzing, and responding to cybersecurity threats across an organization’s infrastructure.

The SOC acts as the first line of defense against cyber attacks by correlating security data from multiple sources, identifying suspicious activity, and initiating incident response actions.

---

## 2. Core Responsibilities of a SOC
The SOC is responsible for the following key functions:

- Continuous security monitoring (24/7)
- Alert triage and prioritization
- Incident detection and investigation
- Incident response and containment
- Threat hunting and proactive analysis
- Security reporting and documentation
- Continuous improvement of detection capabilities

---

## 3. SOC Analyst Roles & Tiers

### 🔹 Tier 1 – SOC Analyst (L1)
**Primary Focus:** Monitoring & Triage

Responsibilities:
- Monitor SIEM dashboards and alerts
- Validate alerts and reduce false positives
- Perform initial investigation
- Escalate confirmed incidents to Tier 2
- Document findings and actions taken

---

### 🔹 Tier 2 – SOC Analyst (L2)
**Primary Focus:** Investigation & Analysis

Responsibilities:
- Deep log analysis and correlation
- Identify attack techniques and scope
- Perform root cause analysis
- Guide containment actions
- Support threat hunting activities

---

### 🔹 Tier 3 – SOC Analyst / DFIR / Threat Hunter (L3)
**Primary Focus:** Advanced Analysis & Strategy

Responsibilities:
- Lead complex investigations
- Digital forensics and incident response (DFIR)
- Develop detection rules and use cases
- Threat hunting and adversary simulation
- Improve SOC processes and tooling

---

## 4. SOC Data Sources
A SOC relies on multiple telemetry sources to build visibility across the environment:

- SIEM platforms (Splunk, Sentinel, QRadar)
- Endpoint Detection & Response (EDR)
- Network logs (Firewall, IDS/IPS, Proxy)
- Identity & access logs (Active Directory, Azure AD)
- Application and database logs
- Email security logs

Effective detection requires correlating events across these sources rather than analyzing logs in isolation.

---

## 5. SOC Alert Lifecycle
A typical SOC alert follows this lifecycle:

1. **Detection** – Suspicious activity is detected by a rule or analytics engine  
2. **Triage** – Analyst validates the alert and determines severity  
3. **Investigation** – Logs and evidence are analyzed to confirm malicious activity  
4. **Response** – Containment, eradication, and recovery actions are executed  
5. **Reporting** – Incident is documented and communicated  
6. **Improvement** – Detection rules and processes are refined

---

## 6. SOC vs Incident Response vs DFIR
While closely related, these functions serve different purposes:

- **SOC:** Continuous monitoring and early detection  
- **Incident Response:** Coordinated actions to contain and remediate incidents  
- **DFIR:** Deep forensic investigation to understand attacker behavior and impact

A mature SOC integrates all three functions seamlessly.

---

## 7. Why SOC Maturity Matters
An effective SOC reduces:
- Time to detect (MTTD)
- Time to respond (MTTR)
- Business impact of cyber incidents

SOC maturity is achieved through skilled analysts, clear processes, quality telemetry, and continuous improvement.

---

## 8. SOC Mindset
A successful SOC analyst does not rely solely on alerts.
They:
- Question assumptions
- Correlate behaviors, not single events
- Think like an attacker
- Document everything clearly

This project simulates that mindset across detection, response, and DFIR scenarios.


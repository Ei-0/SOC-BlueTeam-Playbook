# 🕵️ Threat Hunting

## 1. What is Threat Hunting?
Threat Hunting is a proactive security practice focused on identifying malicious activity that has evaded existing detection controls.

Unlike alert-driven SOC operations, threat hunting assumes that attackers may already be present in the environment without triggering alerts.

---

## 2. Threat Hunting vs Detection
| Detection | Threat Hunting |
|---------|----------------|
| Reactive | Proactive |
| Alert-based | Hypothesis-driven |
| Rule-triggered | Analyst-driven |
| Focuses on known threats | Focuses on unknown or stealthy threats |

Threat hunting complements detection by uncovering gaps and improving security visibility.

---

## 3. Threat Hunting Objectives
The primary objectives of threat hunting include:
- Identifying hidden or advanced threats
- Validating security control effectiveness
- Reducing attacker dwell time
- Improving detection logic
- Enhancing SOC maturity

A successful hunt does not always result in finding malicious activity; validating assumptions is equally valuable.

---

## 4. Hypothesis-Driven Approach
Threat hunting is driven by hypotheses based on:
- MITRE ATT&CK techniques
- Known adversary behaviors
- Environmental risk factors
- Previous incidents
- Threat intelligence

Each hypothesis defines what to hunt for and why.

---

## 5. Data Sources Used for Hunting
Threat hunting relies on high-quality telemetry, including:
- SIEM logs
- Endpoint telemetry (EDR)
- Authentication and identity logs
- Network traffic data
- File access and audit logs

Visibility across multiple data sources is critical.

---

## 6. Threat Hunting Lifecycle
A typical threat hunting cycle includes:
1. Hypothesis creation
2. Data collection
3. Analysis and validation
4. Documentation of findings
5. Detection improvement

Threat hunting is a continuous process, not a one-time activity.

---

## 7. MITRE ATT&CK and Threat Hunting
MITRE ATT&CK provides a structured framework for hunting by:
- Mapping adversary behaviors
- Guiding hypothesis creation
- Identifying detection blind spots
- Standardizing communication

This project uses ATT&CK-driven hypotheses throughout the threat hunting section.

---

## 8. Outcome of Threat Hunting
The results of threat hunting may include:
- Confirmation of malicious activity
- Identification of benign behavior
- Recommendations for new detections
- Tuning of existing rules

Threat hunting strengthens both SOC detection and response capabilities.


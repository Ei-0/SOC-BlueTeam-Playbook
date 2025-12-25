# UC-04 – Data Exfiltration Detection

## 1. Use Case Overview
Data exfiltration refers to the unauthorized transfer of sensitive data outside an organization’s environment.

This use case focuses on detecting abnormal data movement patterns that may indicate insider threats, compromised accounts, or advanced persistent threats (APT).

---

## 2. Threat Scenario
An attacker or malicious insider attempts to exfiltrate data by:

- Uploading files to cloud storage services
- Transferring large volumes of data externally
- Using encrypted channels to evade detection
- Staging data prior to exfiltration

Data exfiltration often occurs after successful access and collection phases.

---

## 3. Relevant Log Sources
Detection requires visibility across network, endpoint, and cloud layers:

- Network Traffic Logs (Firewall, Proxy)
- EDR Telemetry
- File Access Logs
- Cloud Application Logs
- DLP Alerts (if available)

---

## 4. Detection Logic
Indicators of potential data exfiltration include:

- Unusual outbound data volume
- Transfers outside normal business hours
- Data sent to unknown or newly observed destinations
- Repeated uploads to cloud storage services
- Compression or encryption prior to transfer

### Example Logic
- Outbound data volume exceeds baseline
- Destination not previously accessed by the user
- Activity occurs during non-business hours

Baseline behavior is critical for accurate detection.

---

## 5. Alert Context
When reviewing alerts, analysts should assess:

- Type and sensitivity of data transferred
- Destination IP or domain reputation
- User role and expected access
- Historical data transfer patterns
- Whether data staging activity preceded exfiltration

Context distinguishes legitimate business activity from malicious intent.

---

## 6. Common False Positives
Legitimate scenarios may include:

- Large file transfers for business purposes
- Cloud backups or synchronization
- Software updates or patch downloads
- Approved third-party integrations

False positives should be documented and tuned based on business processes.

---

## 7. MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|------|----------|----|
| Exfiltration | Exfiltration Over Web Services | T1567 |
| Collection | Data from Local System | T1005 |

---

## 8. SOC Analyst Response
When data exfiltration is suspected:

1. Validate data transfer legitimacy
2. Identify affected systems and users
3. Block or limit outbound connections if required
4. Preserve evidence for investigation
5. Escalate to incident response and DFIR teams

---

## 9. Outcome
This use case enhances detection of late-stage attack activity and supports early intervention before significant data loss occurs.

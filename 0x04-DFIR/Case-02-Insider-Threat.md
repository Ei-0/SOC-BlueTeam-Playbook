# Case 02 – Insider Threat Investigation

## 📌 Incident Summary
Suspicious activity was identified involving a legitimate internal user accessing sensitive files outside their normal job responsibilities and business hours.

The behavior included abnormal file access patterns and command-line activity, raising concerns of potential data misuse or exfiltration.

Due to the sensitive nature of insider threat investigations, the case required careful evidence handling and controlled response actions.

---

## 🕵️ Detection Source
- SIEM User Behavior Analytics (UBA)
- File Access Audit Logs
- PowerShell and Command-Line Logs

---

## 👤 User Context
- User Type: Internal Employee
- Privilege Level: Standard User
- Department: Non-technical business unit

---

## ⏰ Incident Timeline (High-Level)
- After-hours login detected
- Access to sensitive directories observed
- Unusual file access volume identified
- DFIR investigation initiated

---

## ⚠️ Severity
**High**

---

## 🎯 Initial Impact Assessment
- Unauthorized access to sensitive data
- No confirmed exfiltration at initial stage
- High insider risk due to misuse of legitimate access

# Evidence Collection

## 📂 Collected Evidence
The following evidence sources were preserved for investigation:

- Windows Security Event Logs
- File Access Audit Logs
- PowerShell Operational Logs
- User Authentication Logs
- EDR Telemetry

---

## 🧾 Evidence Handling
- Logs were preserved in read-only format
- Access restricted to DFIR team members
- Chain of custody documented
- No direct interaction with user during early investigation

---

## ⚠️ Considerations
Insider threat investigations require discretion to:
- Avoid alerting the suspect prematurely
- Preserve evidence integrity
- Minimize legal and HR risks

# Logs Analysis

## 🔐 Authentication Activity
- Successful logon detected outside normal business hours
- Login source consistent with internal network
- No evidence of VPN or remote travel

---

## 📁 File Access Analysis
- Multiple sensitive files accessed within short timeframes
- Access patterns inconsistent with user job role
- No business justification identified

---

## 🔧 Command-Line Activity
- PowerShell usage observed
- File enumeration commands executed
- Activity consistent with data discovery and staging

---

## 🧠 Correlation Findings
Correlating authentication, file access, and command-line activity confirms intentional misuse rather than accidental access.

# Forensic Timeline

| Time | Event |
|-----|------|
| 21:42 | User logged in after business hours |
| 21:45 | Sensitive directories accessed |
| 21:51 | PowerShell file enumeration |
| 22:03 | Large number of files opened |
| 22:10 | SIEM UBA alert triggered |

# MITRE ATT&CK Mapping – Case 02 Insider Threat

## 🎯 Overview
This section maps the observed insider threat activities to the MITRE ATT&CK framework to provide structured insight into the attacker’s behavior, intent, and progression.

In insider threat scenarios, ATT&CK mapping helps differentiate between accidental misuse and intentional malicious activity.

---

## 🧭 Attack Behavior Summary
The user leveraged legitimate credentials and access permissions to discover, access, and potentially stage sensitive data.

No malware was involved; instead, the activity relied on trusted system tools and normal authentication mechanisms.

---

## 🧩 MITRE ATT&CK Technique Mapping

| Tactic | Technique | Technique ID | Observed Evidence |
|------|----------|-------------|------------------|
| Initial Access | Valid Accounts | T1078 | Legitimate user account used successfully |
| Discovery | File and Directory Discovery | T1083 | Enumeration of sensitive directories |
| Collection | Data from Local System | T1005 | Access to multiple sensitive files |
| Execution | PowerShell | T1059.001 | PowerShell used for file discovery |
| Defense Evasion | Living off the Land | T1218 | Use of trusted native tools |
| Exfiltration | Data Staging | T1074 | Files accessed in preparation for transfer |

---

## 🔍 Analyst Notes
- The activity aligns with **insider misuse patterns** rather than external compromise.
- Use of legitimate tools and credentials reduced visibility and delayed detection.
- Behavioral anomalies were critical in identifying the threat.

---

## 📈 Detection & Coverage Gaps
- File access monitoring was effective but could be tuned further.
- Additional alerts for abnormal after-hours activity are recommended.
- Data staging detection should be expanded.

---

## 🛠️ Defensive Improvements
- Strengthen User Behavior Analytics (UBA)
- Enforce stricter least privilege access
- Implement periodic access reviews
- Enhance monitoring for data staging locations

---

## ✅ Conclusion
MITRE ATT&CK mapping confirms that the incident followed a typical insider threat pattern relying on legitimate access rather than exploit-based intrusion.

Understanding these behaviors enables more effective detection, response, and prevention of future insider threat incidents.


# Final DFIR Report – Case 02 Insider Threat

## 🧠 Root Cause
The incident was caused by intentional misuse of legitimate access by an internal user to explore and access sensitive data beyond job requirements.

---

## 🛑 Containment Actions
- User access temporarily restricted
- Increased monitoring applied
- No immediate user confrontation initiated

---

## 🧹 Eradication
- Removed unnecessary access permissions
- Cleaned temporary data staging locations
- Reviewed group memberships

---

## 🔄 Recovery
- Access restored based on least privilege
- Continuous monitoring implemented
- Management and HR notified

---

## 📚 Lessons Learned
- Insider threat detection relies on behavior, not malware
- UBA and file auditing are critical
- Regular access reviews reduce risk

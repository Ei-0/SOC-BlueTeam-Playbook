# Case 03 – Ransomware Investigation

## 📌 Incident Summary
A ransomware attack was detected after multiple users reported inaccessible files and ransom notes appearing on shared network drives.

Security telemetry indicated mass file modification activity consistent with ransomware encryption behavior, requiring immediate containment to prevent further spread.

---

## 🕵️ Detection Source
- EDR Alert (Mass File Encryption Behavior)
- SIEM Correlation Alert
- User Reports

---

## 🖥️ Affected Assets
- Multiple user workstations
- File server hosting shared drives

---

## ⏰ Incident Timeline (High-Level)
- Initial endpoint compromise detected
- Lateral movement identified
- File encryption activity observed
- DFIR investigation initiated

---

## ⚠️ Severity
**Critical**

---

## 🎯 Initial Impact Assessment
- Partial business disruption
- Multiple systems impacted
- No confirmed data exfiltration at initial stage

# Attack Path Analysis

## 🔓 Initial Access
The initial compromise likely occurred through a phishing email containing a malicious attachment or link.

---

## 🔁 Lateral Movement
The attacker leveraged compromised credentials to access network shares and move laterally across systems.

---

## 🔐 Encryption Phase
Once sufficient access was achieved, ransomware was executed, encrypting local and network-accessible files.

---

## 🧠 Key Findings
- Credential reuse enabled rapid spread
- Lack of network segmentation increased impact
- Early detection limited full domain compromise

# Forensic Timeline

| Time | Event |
|-----|------|
| 08:32 | Phishing email delivered |
| 08:41 | Initial endpoint compromised |
| 08:55 | Lateral movement to file server |
| 09:02 | Mass file encryption detected |
| 09:05 | Systems isolated |

# MITRE ATT&CK Mapping – Case 03 Ransomware

## 🧭 Attack Behavior Summary
The attacker progressed through multiple ATT&CK stages, from initial access to impact, using common ransomware techniques.

---

## 🧩 MITRE ATT&CK Technique Mapping

| Tactic | Technique | Technique ID | Observed Evidence |
|------|----------|-------------|------------------|
| Initial Access | Phishing | T1566 | Malicious email delivery |
| Execution | Command and Scripting Interpreter | T1059 | Payload execution |
| Credential Access | Credential Dumping | T1003 | Compromised credentials used |
| Lateral Movement | SMB/Windows Admin Shares | T1021.002 | Access to file server |
| Impact | Data Encrypted for Impact | T1486 | Ransomware encryption |

---

## 🛠️ Defensive Improvements
- Strengthen phishing detection
- Enforce MFA
- Improve lateral movement detection
- Harden backup infrastructure

---

## ✅ Conclusion
MITRE mapping confirms a classic ransomware attack chain that can be mitigated through layered defenses and rapid response.

# Final DFIR Report – Case 03 Ransomware

## 🧠 Root Cause
The ransomware incident was caused by successful phishing-based initial access followed by credential misuse and lateral movement.

---

## 🛑 Containment Actions
- Immediate isolation of affected systems
- Network shares disconnected
- Compromised credentials reset

---

## 🧹 Eradication
- Ransomware binaries removed
- Persistence mechanisms eliminated
- Vulnerabilities patched

---

## 🔄 Recovery
- Systems restored from clean backups
- File integrity validated
- Gradual restoration of services

---

## 📚 Lessons Learned
- Phishing remains a primary ransomware vector
- Network segmentation is critical
- Regular backup testing reduces recovery time




# 🧠 Threat Hunting Hypotheses

## Overview
Threat hunting hypotheses are structured assumptions about potential malicious activity that may exist in the environment without triggering existing detection mechanisms.

Each hypothesis is based on adversary behavior, mapped to MITRE ATT&CK, and designed to validate or disprove the presence of a threat.

---

## Hypothesis 01 – Compromised Internal Account Without Alerts

### 🎯 Hypothesis
A legitimate internal user account may be compromised and actively used by an attacker without triggering authentication or brute force alerts.

### 🧩 Rationale
Attackers often obtain valid credentials through phishing or credential leaks, allowing them to bypass traditional authentication-based detections.

### 🔍 What to Hunt For
- Successful logins without prior failed attempts
- Logins from new or rare IP addresses
- Activity outside normal working hours
- Unusual access patterns

### 🎯 MITRE ATT&CK Mapping
- Credential Access – Valid Accounts (T1078)
- Initial Access – Phishing (T1566)

---

## Hypothesis 02 – Stealthy PowerShell Usage

### 🎯 Hypothesis
PowerShell may be used for reconnaissance or execution in a stealthy manner that avoids existing detection rules.

### 🧩 Rationale
Attackers frequently use built-in tools with minimal indicators to blend in with legitimate administrative activity.

### 🔍 What to Hunt For
- PowerShell executions without clear business justification
- Execution outside administrative hours
- Repeated enumeration commands
- PowerShell spawned by unusual parent processes

### 🎯 MITRE ATT&CK Mapping
- Execution – PowerShell (T1059.001)
- Defense Evasion – Obfuscated Files or Information (T1027)

---

## Hypothesis 03 – Data Staging Without Exfiltration

### 🎯 Hypothesis
Sensitive data may be staged internally in preparation for future exfiltration without immediate outbound transfer.

### 🧩 Rationale
Advanced attackers and insiders may collect and stage data over time to avoid detection based on outbound traffic thresholds.

### 🔍 What to Hunt For
- Creation of temporary or hidden directories
- Compression or aggregation of sensitive files
- Access to multiple sensitive files within short periods
- Staging activity in user-controlled locations

### 🎯 MITRE ATT&CK Mapping
- Collection – Data from Local System (T1005)
- Exfiltration – Data Staged (T1074)

---

## Hypothesis 04 – Living-off-the-Land Activity

### 🎯 Hypothesis
An attacker may rely exclusively on trusted native system tools to perform malicious actions, avoiding malware-based detection.

### 🧩 Rationale
Living-off-the-land techniques reduce the likelihood of triggering antivirus or signature-based controls.

### 🔍 What to Hunt For
- Unusual usage of built-in utilities
- Command-line tools used outside normal context
- Tools executed by non-technical users
- Repeated tool usage across multiple hosts

### 🎯 MITRE ATT&CK Mapping
- Defense Evasion – Living off the Land (T1218)
- Execution – Command and Scripting Interpreter (T1059)

---

## Conclusion
These hypotheses guide proactive hunting activities and help identify detection gaps, improve visibility, and reduce attacker dwell time.

Each hypothesis feeds directly into hunting queries and detection improvements.

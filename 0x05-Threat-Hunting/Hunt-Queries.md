# 🔍 Threat Hunting Queries

## Overview
This document contains example hunting queries aligned with the defined threat hunting hypotheses.

The queries are written in a SIEM-agnostic format to demonstrate hunting logic rather than tool-specific syntax.

---

## Hunt 01 – Compromised Internal Account Without Alerts

### 🎯 Objective
Identify potentially compromised accounts using valid credentials without triggering authentication alerts.

### 🔎 Data Sources
- Authentication logs
- Identity provider logs
- VPN logs

### 🧪 Example Query Logic
- Filter successful login events
- Exclude known trusted locations and IP ranges
- Identify logins outside normal business hours
- Group activity by user and source IP
- Highlight new or rare login sources

### 📝 Analyst Notes
Focus on behavioral anomalies rather than single events.  
Cross-reference findings with user roles and travel status.

---

## Hunt 02 – Stealthy PowerShell Usage

### 🎯 Objective
Detect PowerShell activity used for reconnaissance or execution without obvious malicious indicators.

### 🔎 Data Sources
- PowerShell operational logs
- Process creation logs
- EDR telemetry

### 🧪 Example Query Logic
- Identify PowerShell executions
- Exclude known administrative scripts
- Flag executions outside business hours
- Detect unusual parent-child process relationships
- Look for repeated enumeration commands

### 📝 Analyst Notes
PowerShell usage must be evaluated in context.  
Benign administrative activity should be documented and excluded.

---

## Hunt 03 – Data Staging Activity

### 🎯 Objective
Identify internal data staging behavior prior to exfiltration.

### 🔎 Data Sources
- File access logs
- EDR telemetry
- DLP logs

### 🧪 Example Query Logic
- Identify access to multiple sensitive files within short timeframes
- Detect creation of temporary or hidden directories
- Identify compression or archive creation events
- Correlate file access with user role

### 📝 Analyst Notes
Staging activity often precedes exfiltration by days or weeks.  
Look for gradual patterns rather than spikes.

---

## Hunt 04 – Living-off-the-Land Techniques

### 🎯 Objective
Detect misuse of native system tools for malicious purposes.

### 🔎 Data Sources
- Process creation logs
- Command-line logs
- EDR telemetry

### 🧪 Example Query Logic
- Identify executions of native utilities
- Exclude known system or IT usage
- Flag usage by non-technical users
- Detect repeated tool execution across hosts

### 📝 Analyst Notes
Living-off-the-land techniques rely on blending in.  
Behavioral baselining is critical for accurate hunting.

---

## Conclusion
These hunting queries support proactive threat detection by validating hypotheses and uncovering activity that may evade traditional alert-based detection.

Findings from these hunts should feed directly into detection rule improvements.

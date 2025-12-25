# UC-03 – PowerShell Abuse Detection

## 1. Use Case Overview
PowerShell abuse is a common technique used by attackers to execute commands, download payloads, and perform post-exploitation activities while blending in with legitimate administrative behavior.

This use case focuses on detecting suspicious PowerShell execution patterns indicative of malicious activity.

---

## 2. Threat Scenario
An attacker uses PowerShell to:
- Execute encoded or obfuscated commands
- Bypass execution policies
- Download or execute malicious payloads
- Perform reconnaissance or lateral movement

PowerShell is often abused because it is pre-installed and trusted on Windows systems.

---

## 3. Relevant Log Sources
Effective detection requires enhanced logging:

- Windows PowerShell Logs
  - Event ID 4104 – Script Block Logging
  - Event ID 4103 – Module Logging
- Windows Security Logs
  - Event ID 4688 – Process Creation
- EDR Telemetry

---

## 4. Detection Logic
Suspicious PowerShell activity may include:

- EncodedCommand usage
- ExecutionPolicy bypass flags
- Hidden or non-interactive execution
- PowerShell spawning from unusual parent processes
- Network connections initiated by PowerShell

### Example Indicators
- `-EncodedCommand`
- `-ExecutionPolicy Bypass`
- `-NoProfile`
- `-WindowStyle Hidden`

Detection should prioritize **behavioral patterns** rather than single keywords.

---

## 5. Alert Context
When reviewing alerts, analysts should examine:

- Parent process (who launched PowerShell)
- Command-line arguments
- User context
- Time of execution
- Network activity following execution

Context determines whether PowerShell usage is administrative or malicious.

---

## 6. Common False Positives
Legitimate PowerShell usage that may trigger alerts includes:

- IT administrative scripts
- Configuration management tools
- Scheduled maintenance tasks
- Security tooling automation

Known benign scripts should be allowlisted where appropriate.

---

## 7. MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|------|----------|----|
| Execution | PowerShell | T1059.001 |
| Defense Evasion | Obfuscated Files or Information | T1027 |

---

## 8. SOC Analyst Response
Upon detection of suspicious PowerShell activity:

1. Validate command intent and context
2. Identify affected host and user
3. Check for follow-on activity (downloads, persistence)
4. Isolate endpoint if malicious behavior is confirmed
5. Escalate to DFIR if required

---

## 9. Outcome
This use case improves detection of fileless and living-off-the-land attacks that evade traditional malware-based controls.

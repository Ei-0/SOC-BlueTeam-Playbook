# 🎯 MITRE ATT&CK Framework – SOC Perspective

## 1. What is MITRE ATT&CK?
MITRE ATT&CK is a globally recognized knowledge base that documents real-world adversary tactics, techniques, and procedures (TTPs) based on observed cyber attacks.

Rather than focusing on tools or malware names, ATT&CK focuses on **attacker behavior**.

This makes it highly valuable for SOC detection, investigation, and threat hunting.

---

## 2. Why MITRE ATT&CK Matters to a SOC
Traditional security monitoring often focuses on isolated indicators.
MITRE ATT&CK shifts the focus to **how attackers operate**.

For a SOC, ATT&CK helps to:
- Understand attacker objectives
- Detect activity across the attack lifecycle
- Correlate alerts into meaningful attack narratives
- Reduce alert noise by focusing on behaviors

---

## 3. ATT&CK Structure

MITRE ATT&CK is structured into three core components:

### 🔹 Tactics (The "Why")
Tactics represent the attacker’s goal during a specific phase of the attack.

Examples:
- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Lateral Movement
- Exfiltration

---

### 🔹 Techniques (The "How")
Techniques describe **how** an attacker achieves a tactic.

Example:
- Tactic: Execution  
- Technique: PowerShell (T1059.001)

---

### 🔹 Sub-Techniques (The "Details")
Sub-techniques provide additional granularity, describing specific implementations of a technique.

This level of detail allows more precise detection and investigation.

---

## 4. Using MITRE ATT&CK in Detection
SOC detection rules should be mapped to ATT&CK techniques.

Benefits:
- Clear understanding of what behavior is being detected
- Easier gap analysis
- Better detection coverage planning
- Standardized communication across teams

Detection without ATT&CK mapping lacks strategic context.

---

## 5. Using MITRE ATT&CK in Incident Investigation
During investigations, ATT&CK helps analysts:
- Reconstruct the attack path
- Identify what happened before and after detected activity
- Predict attacker next steps
- Guide evidence collection

An alert mapped to ATT&CK is a starting point, not the conclusion.

---

## 6. MITRE ATT&CK and Threat Hunting
Threat hunting is most effective when driven by ATT&CK.

Hunters use ATT&CK to:
- Form hypotheses based on known adversary behavior
- Search for stealthy or missed activity
- Validate assumptions about environment security

ATT&CK turns hunting from guesswork into a structured process.

---

## 7. ATT&CK Coverage vs Alert Volume
A mature SOC prioritizes **coverage** over alert quantity.

Key questions include:
- Which tactics are we blind to?
- Are we detecting only initial access but missing persistence?
- Do alerts tell a story or exist in isolation?

ATT&CK helps SOC teams answer these questions objectively.

---

## 8. MITRE ATT&CK in This Project
Throughout this project:
- Detection use cases are mapped to ATT&CK techniques
- DFIR case studies reference attacker tactics
- Threat hunting hypotheses are ATT&CK-driven
- Reports communicate findings using ATT&CK terminology

This demonstrates an operational SOC mindset aligned with real-world security practices.

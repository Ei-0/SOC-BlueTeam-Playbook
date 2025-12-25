# UC-01 – Brute Force Attack Detection

## 1. Use Case Overview
Brute force attacks attempt to gain unauthorized access by repeatedly trying different passwords against a user account or service.

This use case focuses on detecting abnormal authentication behavior indicative of password guessing or credential stuffing attacks.

---

## 2. Threat Scenario
An attacker attempts to authenticate to a system by generating a high number of failed login attempts within a short time window, potentially followed by a successful login.

This activity may originate from:
- External IP addresses
- Compromised internal systems
- Automated attack tools

---

## 3. Relevant Log Sources
Detection relies on correlating events from multiple sources:

- Windows Security Logs
  - Event ID 4625 – Failed Logon
  - Event ID 4624 – Successful Logon
- VPN Authentication Logs
- Firewall Logs
- Identity Provider Logs (AD / Azure AD)

---

## 4. Detection Logic
The following logic is used to identify brute force activity:

- Multiple failed login attempts
- Same user account or source IP
- Occurring within a defined time window
- Optional successful login after failures

### Example Logic
- ≥ 10 failed login attempts
- Within 5 minutes
- From the same IP address or targeting the same account

---

## 5. Alert Context
When the alert triggers, the SOC analyst should review:

- Targeted user account
- Source IP address and geolocation
- Time of activity
- Authentication method (interactive, remote, VPN)
- Whether a successful login followed the failures

Context is critical to differentiate malicious activity from user error.

---

## 6. Common False Positives
Legitimate activity that may trigger this alert includes:

- Users forgetting passwords
- Automated scripts or services
- Misconfigured applications
- VPN reconnect behavior

False positives should be documented and tuning applied where necessary.

---

## 7. MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|------|----------|----|
| Credential Access | Brute Force | T1110 |

---

## 8. SOC Analyst Response
Upon alert validation, analysts should:

1. Confirm abnormal behavior
2. Identify affected accounts
3. Check for successful authentication
4. Escalate if compromise is suspected
5. Recommend containment actions if required

---

## 9. Outcome
This use case improves early detection of account compromise attempts and reduces the risk of unauthorized access through weak or reused credentials.

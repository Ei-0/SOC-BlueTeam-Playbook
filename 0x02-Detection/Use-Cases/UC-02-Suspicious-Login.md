# UC-02 – Suspicious Login Activity Detection

## 1. Use Case Overview
Suspicious login activity refers to authentication events that deviate from a user’s normal behavior patterns.

This use case focuses on detecting potentially compromised accounts by identifying anomalous login characteristics rather than relying on failed attempts alone.

---

## 2. Threat Scenario
An attacker successfully authenticates using valid credentials obtained through phishing, credential leaks, or brute force attacks.

Indicators of suspicious login activity may include:
- Login from an unusual geographic location
- Access outside normal working hours
- Impossible travel scenarios
- New device or IP address

---

## 3. Relevant Log Sources
This detection relies on identity and access telemetry:

- Windows Security Logs
  - Event ID 4624 – Successful Logon
- Azure AD / Entra ID Sign-in Logs
- VPN Authentication Logs
- Identity Provider Logs
- Endpoint Device Logs

---

## 4. Detection Logic
Suspicious login detection is behavior-based and includes:

- Successful login from a new country or region
- Login outside normal user working hours
- Multiple logins from distant locations within a short time window
- Login from an unmanaged or previously unseen device

### Example Logic
- User logs in from Country A
- Within 30 minutes logs in from Country B
- Distance between locations exceeds realistic travel limits

---

## 5. Alert Context
When reviewing the alert, analysts should evaluate:

- User’s normal login patterns
- Source IP address and geolocation
- Device type and operating system
- Authentication method (VPN, interactive, cloud)
- Any recent password resets or MFA challenges

Contextual validation is essential to avoid unnecessary escalations.

---

## 6. Common False Positives
Legitimate scenarios that may trigger alerts:

- User traveling or working remotely
- VPN or proxy usage
- Mobile network IP changes
- Corporate cloud services using shared IP ranges

False positives should be documented and excluded through tuning.

---

## 7. MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|------|----------|----|
| Credential Access | Valid Accounts | T1078 |

---

## 8. SOC Analyst Response
When a suspicious login is confirmed:

1. Contact the user for verification
2. Review recent account activity
3. Check for additional indicators of compromise
4. Enforce password reset or MFA if required
5. Escalate to incident response if malicious activity is confirmed

---

## 9. Outcome
This use case enhances detection of account compromise scenarios that bypass traditional brute force protections and rely on stolen credentials.

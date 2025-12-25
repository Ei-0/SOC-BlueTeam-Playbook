# 🎣 Phishing Incident Response Playbook

## 1. Purpose
This playbook defines the response process for handling phishing-related security incidents, including credential harvesting, malicious attachments, and malicious links.

The goal is to quickly assess impact, contain potential compromise, and prevent further spread.

---

## 2. Scope
This playbook applies to:
- Email-based phishing attacks
- Credential harvesting campaigns
- Malicious attachments or links
- Business Email Compromise (BEC)

---

## 3. Detection Sources
Phishing incidents may be identified through:
- Email security gateway alerts
- User-reported suspicious emails
- SIEM alerts related to email activity
- Identity alerts following credential use

User reports are often the first indicator and should be treated seriously.

---

## 4. Initial Triage (First 5 Minutes)
Key questions to answer immediately:

- Was the email delivered successfully?
- How many users received the email?
- Did any user click the link or open the attachment?
- Were credentials entered?

### Immediate Actions
- Collect the original email (headers, body, attachments)
- Identify affected users
- Determine phishing type (link, attachment, credential harvesting)

---

## 5. Severity Classification
| Severity | Description |
|-------|------------|
| Low | Phishing email reported, no interaction |
| Medium | User interaction without credential submission |
| High | Credential submission or malware execution |

Severity determines containment urgency.

---

## 6. Containment
Containment actions focus on limiting further exposure:

- Remove the email from all user mailboxes
- Block sender address and domains
- Disable compromised user accounts if credentials were submitted
- Block malicious URLs at email gateway, proxy, and firewall

Time is critical to reduce impact.

---

## 7. Investigation
Analysts should investigate:

- Email headers and sender reputation
- URLs or attachment behavior
- User activity following interaction
- Authentication logs for suspicious access
- Additional emails from the same campaign

Investigation confirms scope and potential compromise.

---

## 8. Eradication
Once containment is complete:

- Reset affected user credentials
- Revoke active sessions and tokens
- Remove malware if attachments were executed
- Clean affected endpoints

Ensure all artifacts are removed before recovery.

---

## 9. Recovery
Restore normal operations:

- Re-enable user accounts after credential reset
- Educate affected users
- Monitor for suspicious login activity
- Validate email security controls

Recovery includes both technical and user-focused actions.

---

## 10. Escalation Criteria
Escalate if:
- Multiple users are compromised
- Privileged accounts are affected
- Data access or exfiltration is suspected
- Incident involves executive impersonation (BEC)

---

## 11. Lessons Learned
After incident closure:
- Update phishing detection rules
- Improve email filtering
- Conduct phishing awareness training
- Document indicators and campaign details

Phishing incidents provide valuable insight into attacker tactics.

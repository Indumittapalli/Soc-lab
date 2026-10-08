# 📝 SOC Incident Report Template

## 1. Incident Information

| Field | Details |
|---|---|
| Incident ID | |
| Alert Type | |
| Severity | |
| Date/Time Detected | |
| Analyst | |
| Affected Host | |
| Affected User | |
| Status | |

---

## 2. Alert Summary

### Alert Description

Describe what triggered the alert.

### Initial Assessment

Explain why the activity was considered suspicious.

---

## 3. Timeline

| Time | Event | Source |
|---|---|---|
| | | |
| | | |
| | | |

Document important events chronologically.

---

## 4. Evidence Collected

### Endpoint Evidence

- Process information
- Windows Event Logs
- Sysmon events
- File information
- User activity

### Network Evidence

- Source IP
- Destination IP
- Ports
- Domains
- URLs
- DNS activity

---

## 5. Indicators of Compromise

| Type | Indicator | Source |
|---|---|---|
| IP Address | | |
| Domain | | |
| URL | | |
| File Hash | | |
| File Name | | |
| Email | | |

---

## 6. Investigation

Document the investigation steps performed.

### Alert Triage

Explain the initial validation of the alert.

### Log Analysis

Describe relevant events discovered during log analysis.

### Endpoint Analysis

Document suspicious processes, files, users, or other endpoint activity.

### Network Analysis

Document relevant network connections, DNS activity, or other traffic.

### Correlation

Explain how different pieces of evidence were correlated.

---

## 7. MITRE ATT&CK Mapping

| Technique | ID | Evidence |
|---|---|---|
| | | |
| | | |

Only map techniques supported by the investigation evidence.

---

## 8. Impact Assessment

Determine:

- Affected systems
- Affected accounts
- Potential compromise
- Data exposure
- Persistence
- Lateral movement
- Business impact

---

## 9. Response Actions

Document actions taken:

- [ ] Alert validated
- [ ] IOC extracted
- [ ] Affected endpoint investigated
- [ ] Suspicious or malicious process contained
- [ ] Account secured
- [ ] Malicious IP/domain blocked
- [ ] Additional systems searched
- [ ] Incident escalated

---

## 10. Findings & Root Cause

Document the key findings from the investigation.

### Findings

Summarize the relevant evidence and investigation results.

### Root Cause

Document the identified or suspected root cause.

If the root cause cannot be confirmed, clearly state that further investigation is required.

---

## 11. Final Disposition

Choose the appropriate classification:

```text
True Positive
False Positive
Benign / Expected Activity
Suspicious - Requires Monitoring
Confirmed Security Incident
```

Document the reasoning behind the final classification.

---

## 12. Lessons Learned & Recommendations

Document improvements identified during the investigation.

### Detection Improvements

- Tune detection rules
- Reduce false positives
- Improve alert context
- Add relevant telemetry

### Security Improvements

- Strengthen authentication controls
- Improve endpoint monitoring
- Update blocking rules
- Review access controls
- Improve logging coverage

### Follow-Up Actions

Document any additional investigation, monitoring, remediation, or security improvements required.

---

## 13. Analyst Notes

Record additional observations, assumptions, limitations, or relevant investigation context.

Avoid including sensitive credentials, secrets, or unnecessary personal information.

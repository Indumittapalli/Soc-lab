# 🛡️ SOC Home Lab — Security Monitoring & Incident Investigation

### Hands-on SOC Analyst Lab | Threat Detection | Alert Triage | IOC Analysis | Threat Hunting | Incident Response

<p align="center">
  <strong>Detect → Triage → Investigate → Correlate → Hunt → Respond → Document</strong>
</p>

---

## 📌 Overview

This repository documents a hands-on Security Operations Center (SOC) home lab focused on security monitoring, alert triage, log analysis, threat detection, IOC investigation, threat hunting, and incident-response workflows.

The project is designed to build practical SOC Analyst skills by investigating common security events across Windows endpoints and network infrastructure in a controlled lab environment.

Rather than focusing only on cybersecurity theory, this lab follows a structured analyst workflow for understanding alerts, validating suspicious activity, collecting evidence, analyzing telemetry, extracting indicators, correlating events, mapping attacker behavior, and documenting findings.

---

# 🎯 Project Objectives

The SOC Home Lab provides practical exposure to:

- Security monitoring and alert triage
- Windows Event Log analysis
- Sysmon telemetry analysis
- Network traffic investigation
- Firewall and network security monitoring
- IOC extraction and investigation
- Phishing investigation
- Brute-force detection
- Suspicious PowerShell activity detection
- Suspicious DNS activity detection
- Port-scanning investigation
- Malware activity investigation
- MITRE ATT&CK technique mapping
- Incident documentation
- Incident response workflows
- Basic threat hunting

---

# 🏗️ Lab Architecture

The lab is designed around an attacker, network security controls, endpoint telemetry, and SOC investigation activities.

```text
                     ┌──────────────────────┐
                     │       Attacker       │
                     │      Kali Linux      │
                     └──────────┬───────────┘
                                │
                          Attack Traffic
                                │
                                ▼
                     ┌──────────────────────┐
                     │       pfSense        │
                     │ Firewall / Network   │
                     │      Monitoring      │
                     └──────────┬───────────┘
                                │
                         Network Activity
                                │
                                ▼
                     ┌──────────────────────┐
                     │   Windows Endpoint   │
                     │                      │
                     │       Sysmon         │
                     │   Windows Event Logs │
                     └──────────┬───────────┘
                                │
                          Security Events
                                │
                                ▼
                     ┌──────────────────────┐
                     │      SOC Analyst     │
                     │                      │
                     │ Alert Triage         │
                     │ Log Analysis         │
                     │ IOC Investigation    │
                     │ Threat Hunting       │
                     │ Incident Response    │
                     └──────────────────────┘

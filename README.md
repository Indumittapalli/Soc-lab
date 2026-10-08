# 🛡️ SOC Home Lab — Security Monitoring & Incident Investigation

### Hands-on SOC Analyst Lab | Threat Detection | Alert Triage | IOC Analysis | Threat Hunting | Incident Response

<p align="center">
  <strong>Detect → Triage → Investigate → Correlate → Hunt → Respond → Document</strong>
</p>

---

# 1. 📌 Overview

This repository documents a hands-on Security Operations Center (SOC) home lab focused on security monitoring, alert triage, log analysis, threat detection, IOC investigation, threat hunting, and incident-response workflows.

The project is designed to develop practical SOC Analyst skills by investigating common security events across Windows endpoints and network infrastructure in a controlled laboratory environment.

The lab follows a structured analyst workflow from initial alert detection through triage, evidence collection, investigation, IOC extraction, event correlation, threat analysis, response, and documentation.

The main focus areas include endpoint monitoring, network security monitoring, Windows Event Log analysis, Sysmon telemetry, suspicious activity investigation, IOC analysis, and incident-response methodology.

---

# 2. 🎯 Project Objectives

The main objectives of this SOC lab are:

- Develop practical SOC monitoring and investigation skills
- Understand security alert triage
- Analyze Windows Event Logs
- Analyze Sysmon endpoint telemetry
- Investigate network activity
- Understand firewall security monitoring
- Identify and investigate Indicators of Compromise (IOCs)
- Investigate phishing activity
- Investigate brute-force attacks
- Investigate suspicious DNS activity
- Investigate suspicious PowerShell activity
- Investigate port-scanning activity
- Investigate potential malware activity
- Correlate security events
- Build investigation timelines
- Apply MITRE ATT&CK techniques
- Perform basic threat hunting
- Understand incident-response workflows
- Document investigation findings
- Practice security incident escalation

---

# 3. 🏗️ Lab Architecture

The SOC lab is designed around an attacker, network security controls, endpoint telemetry, and SOC investigation activities.

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
```

### Core Components

| Component | Purpose |
|---|---|
| Kali Linux | Attack simulation and security testing |
| pfSense | Firewall and network security monitoring |
| Windows | Endpoint investigation environment |
| Windows Event Logs | Authentication and system activity telemetry |
| Sysmon | Detailed endpoint process and activity telemetry |
| SOC Workflow | Alert triage, investigation, correlation, and response |

---

# 4. 🔄 SOC Investigation Workflow

The investigations in this project follow a structured SOC-style workflow.

```text
                    Security Alert
                          │
                          ▼
                   Initial Triage
                          │
                          ▼
                   Validate Alert
                          │
                          ▼
                  Collect Evidence
                          │
                          ▼
                    Analyze Logs
                          │
                          ▼
                    Extract IOCs
                          │
                          ▼
                   Correlate Events
                          │
                          ▼
                Map MITRE ATT&CK
                          │
                          ▼
                  Determine Impact
                          │
                          ▼
               Response / Escalation
                          │
                          ▼
                  Final Disposition
                          │
                          ▼
                   Documentation
```

### Investigation Lifecycle

**Detect → Triage → Investigate → Correlate → Hunt → Respond → Document**

This workflow represents the overall methodology used throughout the repository.

---

# 5. 🧰 Technologies & Tools

## Operating Systems

- Windows
- Kali Linux

## Security Monitoring

- Windows Event Logs
- Sysmon
- pfSense
- Network Traffic Analysis

## Investigation

- Log Analysis
- IOC Analysis
- Timeline Analysis
- Threat Hunting
- MITRE ATT&CK Mapping

## Core SOC Concepts

- Security Monitoring
- Alert Triage
- Incident Investigation
- Evidence Collection
- IOC Extraction
- Incident Response
- Security Documentation

---

# 6. 🚨 Detection & Investigation Use Cases

The repository covers multiple common SOC security events and investigation scenarios.

| Use Case | Investigation Focus |
|---|---|
| 🔐 Brute Force | Repeated authentication failures and suspicious login activity |
| 🦠 Malware | Suspicious processes, files, and endpoint activity |
| 🎣 Phishing | Suspicious emails, URLs, domains, and indicators |
| 🔎 Port Scanning | Network reconnaissance and scanning behavior |
| 🌐 Suspicious DNS | Unusual DNS queries, domains, and possible C2 indicators |
| ⚡ Suspicious PowerShell | Potentially malicious PowerShell execution |

Detailed detection documentation is available in the [`detections/`](./detections/) directory.

---

# 7. 🔐 Brute-Force Investigation

The brute-force investigation focuses on identifying repeated authentication failures and determining whether the activity may indicate credential attacks or potential account compromise.

### Investigation Areas

- Failed authentication attempts
- Source IP addresses
- Target accounts
- Authentication timelines
- Repeated login failures
- Successful authentication following multiple failures
- Potential account compromise
- Related activity around the authentication events

### SOC Investigation Approach

```text
Authentication Alert
        ↓
Review Failed Attempts
        ↓
Identify Source
        ↓
Identify Target Account
        ↓
Build Timeline
        ↓
Check Successful Authentication
        ↓
Correlate Related Activity
        ↓
Assess Risk
        ↓
Document / Escalate
```

📄 [View Brute-Force Detection](./detections/brute-force.md)

📄 [View Brute-Force Investigation](./investigations/brute-force-investigation.md)

---

# 8. 🦠 Malware Investigation

The malware investigation focuses on identifying suspicious endpoint activity and determining whether processes or files may indicate malicious behavior.

### Investigation Areas

- Suspicious processes
- Process execution
- File activity
- Indicators of compromise
- Related network connections
- Suspicious parent-child processes
- Potential persistence
- Related endpoint activity

### SOC Investigation Approach

```text
Suspicious Activity
        ↓
Identify Process / File
        ↓
Review Process Context
        ↓
Analyze Related Events
        ↓
Extract IOCs
        ↓
Check Network Activity
        ↓
Assess Potential Impact
        ↓
Document Findings
```

📄 [View Malware Detection](./detections/malware.md)

📄 [View Malware Investigation](./investigations/malware-investigation.md)

---

# 9. 🎣 Phishing Investigation

The phishing investigation focuses on analyzing potentially malicious emails and identifying associated indicators.

### Investigation Areas

- Sender information
- Suspicious URLs
- Domains
- Attachments
- Email headers
- User interaction
- Suspicious links
- IOC extraction

### Phishing Investigation Workflow

```text
Suspicious Email
       ↓
Analyze Sender
       ↓
Review Email Content
       ↓
Inspect URLs / Domains
       ↓
Analyze Attachments
       ↓
Extract IOCs
       ↓
Correlate Related Activity
       ↓
Assess Risk
       ↓
Document Findings
```

📄 [View Phishing Detection](./detections/phishing.md)

📄 [View Phishing Investigation](./investigations/phishing-investigation.md)

---

# 10. 🔎 Port-Scanning Investigation

The port-scanning investigation focuses on identifying network reconnaissance activity.

### Investigation Areas

- Source IP
- Destination host
- Destination ports
- Number of connection attempts
- Scanning patterns
- Connection frequency
- Potential reconnaissance activity

### Investigation Workflow

```text
Network Activity
       ↓
Identify Source
       ↓
Identify Destination
       ↓
Analyze Destination Ports
       ↓
Review Connection Pattern
       ↓
Determine Scanning Behavior
       ↓
Correlate With Other Activity
       ↓
Assess Risk
       ↓
Document Findings
```

📄 [View Port-Scanning Detection](./detections/port-scanning.md)

📄 [View Port-Scanning Investigation](./investigations/port-scanning-investigation.md)

---

# 11. 🌐 Suspicious DNS Investigation

The suspicious DNS investigation focuses on identifying unusual DNS activity and potential command-and-control indicators.

### Investigation Areas

- Queried domains
- Source hosts
- Query frequency
- Unusual domain patterns
- DNS-related IOCs
- Potential C2 indicators
- Related network activity

### DNS Investigation Workflow

```text
Suspicious DNS Activity
          ↓
Identify Source Host
          ↓
Identify Queried Domain
          ↓
Analyze Query Frequency
          ↓
Review Domain Context
          ↓
Extract DNS IOCs
          ↓
Correlate With Endpoint Activity
          ↓
Assess Potential C2
          ↓
Document Findings
```

📄 [View Suspicious DNS Detection](./detections/suspicious-dns.md)

📄 [View DNS Investigation](./investigations/dns-investigation.md)

---

# 12. ⚡ Suspicious PowerShell Investigation

The PowerShell investigation focuses on identifying potentially malicious PowerShell execution and suspicious process behavior.

### Investigation Areas

- PowerShell command lines
- Parent-child process relationships
- Encoded commands
- Suspicious execution patterns
- User context
- Network connections
- Endpoint activity
- Related process execution

### PowerShell Investigation Workflow

```text
PowerShell Activity
        ↓
Identify Command Line
        ↓
Review Parent Process
        ↓
Analyze Execution Context
        ↓
Check Encoded / Obfuscated Content
        ↓
Review Related Network Activity
        ↓
Extract IOCs
        ↓
Assess Potential Impact
        ↓
Document Findings
```

📄 [View Suspicious PowerShell Detection](./detections/suspicious-powershell.md)

📄 [View PowerShell Investigation](./investigations/powershell-investigation.md)

---

# 13. 🧩 IOC Investigation

Indicators of Compromise are analyzed as part of the investigation workflow.

### Common IOC Types

```text
IP Address
     │
     ├── Domain
     │
     ├── URL
     │
     ├── File Hash
     │
     ├── File Name
     │
     └── Email Address
```

### IOC Investigation Workflow

```text
IOC Identified
      ↓
Validate Indicator
      ↓
Determine Context
      ↓
Correlate With Logs
      ↓
Search Related Activity
      ↓
Assess Threat
      ↓
Document Findings
```

### IOC Investigation Questions

- Where was the IOC observed?
- When was it observed?
- Which system generated the event?
- Which user or process was involved?
- Is the IOC associated with other suspicious activity?
- Does the IOC appear across multiple events?
- What potential impact is associated with the IOC?
- Should the indicator be escalated or blocked?

📄 [View IOC Investigation Resources](./iocs/README.md)

---

# 14. 🧠 SOC Investigation Methodology

The investigations in this project follow a repeatable analyst methodology.

### 1. Identify

Determine what triggered the security alert.

### 2. Triage

Assess the alert severity, context, and potential impact.

### 3. Validate

Determine whether the alert represents expected behavior, suspicious activity, or a potential security incident.

### 4. Investigate

Analyze endpoint, authentication, DNS, network, process, and system activity.

### 5. Correlate

Connect multiple events and indicators to establish an investigation timeline.

### 6. Hunt

Search available telemetry for related or previously unseen suspicious activity.

### 7. Map

Map observed behavior to relevant MITRE ATT&CK techniques when supported by investigation evidence.

### 8. Respond

Determine appropriate containment, remediation, or escalation actions.

### 9. Document

Record evidence, findings, IOCs, impact, response actions, and final disposition.

---

# 15. 🗺️ MITRE ATT&CK

MITRE ATT&CK is used to provide context to observed attacker behavior.

Investigation areas may include:

- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Credential Access
- Discovery
- Command and Control

### Example Investigation Mapping

```text
Security Event
      ↓
Identify Behavior
      ↓
Understand Attack Technique
      ↓
Map to MITRE ATT&CK
      ↓
Record Technique
      ↓
Use Mapping to Support Investigation
```

Techniques are mapped only when supported by the available investigation evidence.

---

# 16. 📝 Incident Documentation

The [`docs/`](./docs/) directory contains documentation resources for recording SOC investigations consistently.

Incident documentation can include:

- Incident information
- Alert summary
- Detection source
- Investigation timeline
- Evidence collected
- Indicators of compromise
- Investigation findings
- MITRE ATT&CK mapping
- Impact assessment
- Response actions
- Escalation details
- Final disposition
- Recommendations
- Lessons learned

A consistent documentation process helps preserve investigation context and supports effective incident handoff and escalation.

📄 [View Documentation Resources](./docs/)

---

# 17. 📸 Screenshots & Visual References

The [`screenshots/`](./screenshots/) directory contains visual references representing different stages of the SOC investigation workflow.

> **Important:** The screenshots in this repository are illustrative/recreated visuals and are not presented as original historical evidence from the previous lab environment.

### SOC Home Lab Architecture

<img src="./screenshots/soc-home-lab-architecture.png" width="850">

### pfSense Firewall Dashboard

<img src="./screenshots/pfsense-firewall-dashboard.png" width="850">

### Windows Event Logs

<img src="./screenshots/windows-event-logs.png" width="850">

### Sysmon Events

<img src="./screenshots/sysmon-events.png" width="850">

### Splunk Brute-Force Detection

<img src="./screenshots/splunk-bruteforce-detection.png" width="850">

### Phishing Email Investigation

<img src="./screenshots/phishing-email-investigation.png" width="850">

### Suspicious DNS Activity

<img src="./screenshots/suspicious-dns-activity.png" width="850">

### Suspicious PowerShell Investigation

<img src="./screenshots/suspicious-powershell.png" width="850">

### IOC Investigation

<img src="./screenshots/ioc-investigation.png" width="850">

📁 [View All Visual References](./screenshots/)

---

# 18. 📊 Analyst Skills Demonstrated

This project demonstrates practical exposure to:

### SOC Operations

- Security Monitoring
- Alert Triage
- Incident Investigation
- Security Alert Validation
- Investigation Documentation
- Incident Escalation
- Incident Response

### Endpoint Security

- Windows Event Log Analysis
- Sysmon Analysis
- Process Investigation
- PowerShell Investigation
- Endpoint Activity Analysis

### Network Security

- Network Traffic Analysis
- Firewall Monitoring
- DNS Investigation
- Port-Scanning Investigation
- Suspicious Network Activity Analysis

### Threat Detection

- Brute-Force Detection
- Malware Investigation
- Phishing Investigation
- Suspicious DNS Detection
- Suspicious PowerShell Detection
- IOC Identification

### Threat Intelligence & Investigation

- IOC Extraction
- IOC Correlation
- Timeline Analysis
- Threat Hunting
- MITRE ATT&CK Mapping

---

# 19. 🗂️ Repository Structure

```text
Soc-lab/
│
├── detections/
│   ├── brute-force.md
│   ├── malware.md
│   ├── phishing.md
│   ├── port-scanning.md
│   ├── suspicious-dns.md
│   └── suspicious-powershell.md
│
├── investigations/
│   ├── brute-force-investigation.md
│   ├── dns-investigation.md
│   ├── malware-investigation.md
│   ├── phishing-investigation.md
│   ├── port-scanning-investigation.md
│   └── powershell-investigation.md
│
├── iocs/
│   └── README.md
│
├── evidence/
│   └── ...
│
├── docs/
│   └── ...
│
├── screenshots/
│   ├── README.md
│   ├── soc-home-lab-architecture.png
│   ├── pfsense-firewall-dashboard.png
│   ├── windows-event-logs.png
│   ├── sysmon-events.png
│   ├── splunk-bruteforce-detection.png
│   ├── phishing-email-investigation.png
│   ├── suspicious-dns-activity.png
│   ├── suspicious-powershell.png
│   ├── ioc-investigation.png
│   └── ...
│
└── README.md
```

---

# 20. 🔍 Investigation Documentation

The repository separates detection content from investigation content so that each security scenario can be approached from both a detection and analyst-investigation perspective.

| Category | Location |
|---|---|
| Detection Rules | [`detections/`](./detections/) |
| Investigations | [`investigations/`](./investigations/) |
| IOC Resources | [`iocs/`](./iocs/) |
| Evidence | [`evidence/`](./evidence/) |
| Documentation | [`docs/`](./docs/) |
| Visual References | [`screenshots/`](./screenshots/) |

### Investigation Categories

- Brute Force
- Malware
- Phishing
- Port Scanning
- Suspicious DNS
- Suspicious PowerShell

Each investigation is structured around identifying suspicious activity, analyzing available evidence, extracting indicators, correlating events, assessing potential impact, and documenting the findings.

---

# 21. 🎓 Learning Outcomes

Through this project, I developed practical understanding of how a SOC analyst approaches security events from initial detection through final documentation.

### Key Learning Areas

- Understanding security alerts
- Performing initial alert triage
- Validating suspicious activity
- Analyzing Windows endpoint telemetry
- Investigating authentication activity
- Reviewing network-related activity
- Identifying suspicious processes
- Investigating PowerShell activity
- Investigating DNS activity
- Investigating network reconnaissance
- Extracting and validating IOCs
- Correlating security events
- Building investigation timelines
- Applying MITRE ATT&CK context
- Performing basic threat hunting
- Determining appropriate response actions
- Documenting investigation findings
- Escalating potential security incidents

---

# 22. 🚀 Future Improvements

Potential future enhancements include:

- Additional detection use cases
- More endpoint telemetry sources
- Expanded threat-hunting scenarios
- Additional MITRE ATT&CK mappings
- Automated IOC enrichment
- Detection rule development
- SIEM integration
- Automated incident-report generation
- Additional network-security investigations
- Expanded incident-response playbooks
- Additional endpoint detection scenarios
- Improved investigation automation

---

# 23. 🎯 Project Purpose

This project was created as a practical cybersecurity portfolio project to demonstrate the ability to approach security events from a SOC Analyst perspective rather than only learning cybersecurity concepts theoretically.

The project emphasizes the complete investigation lifecycle:

```text
Detect
  ↓
Triage
  ↓
Validate
  ↓
Investigate
  ↓
Correlate
  ↓
Hunt
  ↓
Respond
  ↓
Document
```

The goal is to demonstrate practical understanding of how security alerts can be investigated, analyzed, correlated, and documented in a SOC environment.

---

# 24. ⚠️ Disclaimer

This project is intended for educational and defensive security purposes within a controlled laboratory environment.

All testing, attack simulation, and investigation activities should be performed only on systems and networks where appropriate authorization has been obtained.

The screenshots included in this repository are illustrative/recreated visuals and should not be interpreted as original historical evidence from the previous lab environment.

No real-world systems should be tested without proper authorization.

---

# 25. 👤 Author

**Mittapalli Indu**

Cybersecurity | SOC Analyst | Security Operations

GitHub: [github.com/Indumittapalli](https://github.com/Indumittapalli)

---

<p align="center">
  <strong>Cybersecurity • SOC • SIEM • Threat Detection • IOC Analysis • Threat Hunting • Incident Response</strong>
</p>

🛡️ SOC Home Lab

A hands-on **Security Operations Center (SOC) home lab** focused on security monitoring, log analysis, alert triage, threat detection, IOC investigation, threat hunting, and incident-response workflows.

The project is designed to build practical SOC analyst skills by investigating common security events across Windows endpoints and network infrastructure in a controlled lab environment.

 🎯 Project Objectives
The SOC Home Lab provides practical experience with:

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


🏗️ Lab Architecture

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


🧰 Technologies & Tools
Operating Systems
- Windows
- Kali Linux
Security Monitoring
- Windows Event Logs
- Sysmon
- pfSense
- Network traffic analysis
Investigation
- IOC analysis
- Log analysis
- Timeline analysis
- Threat hunting
- MITRE ATT&CK mapping
🚨 Detection Use Cases
The repository contains documented detection scenarios for common SOC alerts.

Detection	Description
🔐 Brute Force	Identification and investigation of repeated authentication failures
🦠 Malware	Investigation of suspicious malware-related activity
🎣 Phishing	Investigation of suspicious emails, URLs, and indicators
🔎 Port Scanning	Identification of network reconnaissance activity
🌐 Suspicious DNS	Investigation of suspicious DNS queries and domains
⚡ Suspicious PowerShell	Investigation of potentially malicious PowerShell execution

Detection documentation is available in the [`detections/`](detections/) directory.

🔍 Investigation Workflows
Each investigation follows a SOC-style workflow:
Alert
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

Investigation documentation is available in the [`investigations/`](investigations/) directory.


🧪 Detection Scenarios
1. Brute-Force Detection
Investigates repeated authentication failures and suspicious login activity.
Focus areas:
- Failed authentication attempts
- Source IP addresses
- Target accounts
- Authentication timelines
- Successful login following multiple failures
- Potential account compromise
2. Malware Detection
Investigates potentially malicious processes, files, and endpoint activity.
Focus areas:
- Suspicious processes
- File activity
- Process execution
- Indicators of compromise
- Related network connections
- Potential persistence
3. Phishing Detection
Investigates potentially malicious emails and associated indicators.
Focus areas:
- Sender information
- Suspicious URLs
- Domains
- Attachments
- Email headers
- User interaction
- IOC extraction
4. Port-Scanning Detection
Investigates network reconnaissance and port-scanning behavior.
Focus areas:
- Source IP
- Destination host
- Destination ports
- Number of connection attempts
- Scanning patterns
- Potential reconnaissance activity
5. Suspicious DNS Detection
Investigates potentially suspicious DNS queries.
Focus areas:
- Queried domains
- Source hosts
- Query frequency
- Unusual domain patterns
- DNS-related IOCs
- Potential command-and-control indicators
6. Suspicious PowerShell Detection
Investigates potentially malicious PowerShell execution.
Focus areas:
- PowerShell command lines
- Parent-child process relationships
- Encoded commands
- Suspicious execution patterns
- User context
- Network connections
- Endpoint activity
🧩 IOC Investigation
The [`iocs/`](iocs/) directory contains IOC-related documentation and investigation resources.


Common IOC types include:
IP Address
Domain
URL
File Hash
File Name
Email Address

IOC investigation workflow:
IOC Identified
      │
      ▼
Validate Indicator
      │
      ▼
Determine Context
      │
      ▼
Correlate With Logs
      │
      ▼
Search Related Activity
      │
      ▼
Assess Threat
      │
      ▼
Document Findings

📝 Incident Response
The [`docs/`](docs/) directory contains an incident-report template designed to document SOC investigations consistently.


The template covers:
- Incident information
- Alert summary
- Investigation timeline
- Evidence collected
- Indicators of compromise
- Investigation findings
- MITRE ATT&CK mapping
- Impact assessment
- Response actions
- Final disposition
- Recommendations
- Lessons learned
🗂️ Repository Structure
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
├── docs/
│   └── incident-report-template.md
│
└── README.md

🧠 SOC Investigation Methodology
The investigations in this project follow a structured analyst workflow:
1. Identify
Determine what triggered the security alert.
2. Triage
Assess the alert's severity, context, and potential impact.
3. Investigate
Analyze endpoint, authentication, DNS, network, and process activity.
4. Correlate
Connect multiple events and indicators to establish an attack timeline.
5. Hunt
Search for related activity across available telemetry.
6. Map
Map observed behavior to relevant MITRE ATT&CK techniques where supported by evidence.
7. Respond
Determine appropriate containment, remediation, or escalation actions.
8. Document
Record evidence, findings, IOCs, impact, and final disposition.


🗺️ MITRE ATT&CK
MITRE ATT&CK techniques are used to provide context to observed attacker behavior.
Example investigation areas include:
Initial Access
Execution
Persistence
Privilege Escalation
Defense Evasion
Credential Access
Discovery
Command and Control

Techniques are mapped only when supported by the investigation evidence.


📊 Analyst Skills Demonstrated
This project demonstrates practical exposure to:
- SOC alert triage
- Security monitoring
- Log analysis
- Windows Event Logs
- Sysmon analysis
- Network security monitoring
- Phishing investigation
- Brute-force investigation
- Malware investigation
- PowerShell investigation
- DNS investigation
- Port-scan investigation
- IOC extraction
- Threat hunting
- Timeline analysis
- MITRE ATT&CK mapping
- Incident response
- Incident documentation
- Security incident escalation
📚 Investigation Documentation
Category	Location
Detection Rules	[`detections/`](detections/)
Investigations	[`investigations/`](investigations/)
IOC Resources	[`iocs/`](iocs/)
Incident Documentation	[`docs/`](docs/)


🎓 Purpose
This project was created as a practical cybersecurity portfolio project to demonstrate the ability to approach security events from a SOC analyst perspective rather than only learning cybersecurity concepts theoretically.
The lab emphasizes:
Detect → Triage → Investigate → Correlate → Hunt → Respond → Document

⚠️ Disclaimer
This project is intended for educational and defensive security purposes within a controlled lab environment.
All testing and investigation activities should be performed only on systems and networks where appropriate authorization has been obtained.
👤 Author
Pranay Kumar
Cyber Security | SOC Analyst | Security Operations
GitHub: Mudimanchi-Pranay

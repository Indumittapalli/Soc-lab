# 🔎 Port Scanning Investigation

## 📌 Incident Summary

A potential network reconnaissance activity was detected involving multiple connection attempts against different ports on a target system.

The investigation focuses on determining whether the activity represents legitimate network discovery or malicious reconnaissance.

---

## 🎯 Investigation Objective

Determine:

- Source IP address
- Target IP address
- Ports scanned
- Scan pattern
- Scan frequency
- Protocol used
- Whether the activity was successful
- Whether follow-up exploitation occurred

---

## 🔎 Investigation Process

### 1. Identify the Source

Determine the system generating the connection attempts.

Review:

- Source IP
- Destination IP
- Timestamp
- Protocol
- Source port
- Destination port

Example:

```text
Source IP:      192.168.1.50
Destination IP: 192.168.1.100
Protocol:       TCP

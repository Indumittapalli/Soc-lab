# 🌐 Suspicious DNS Investigation

## 📌 Incident Summary

Suspicious DNS activity was identified from a network endpoint and investigated to determine whether the activity was associated with malware, command-and-control communication, or other malicious behavior.

---

## 🎯 Investigation Objective

Determine:

- Source endpoint
- Queried domain
- Query frequency
- DNS record type
- Domain reputation
- Query pattern
- Whether the domain is associated with malicious infrastructure
- Whether additional network activity followed the DNS request

---

## 🔎 Investigation Process

### 1. Identify the DNS Request

Review DNS logs and network telemetry for unusual queries.

Important fields include:

- Timestamp
- Source IP
- Requested domain
- Query type
- Response
- Destination DNS server

Example:

```text
Source: 192.168.1.25
Query: suspicious-example.com
Type: A
Response: 203.0.113.50

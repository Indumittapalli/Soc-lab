# 🎣 Phishing Investigation

## 📌 Incident Summary

A suspected phishing email was identified and investigated as a potential attempt to steal credentials, deliver malware, or redirect the user to a malicious website.

---

## 🎯 Investigation Objective

Determine whether the email is malicious and identify:

- Sender information
- Suspicious URLs
- Malicious attachments
- Indicators of compromise (IOCs)
- Intended attack technique
- Potentially affected users or endpoints

---

## 🔎 Investigation Process

### 1. Analyze Email Metadata

Review:

- Sender address
- Recipient
- Subject
- Timestamp
- Reply-To address
- Return-Path
- Received headers

Look for inconsistencies between the displayed sender and the actual sending infrastructure.

---

### 2. Inspect URLs

Extract URLs from the email and investigate:

- Domain reputation
- Domain age
- URL structure
- Redirects
- Suspicious parameters
- Known malicious indicators

Example suspicious characteristics:

```text
http://example-login[.]com/verify
http://secure-account[.]com/login

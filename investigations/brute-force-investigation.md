# 🔐 Brute-Force Attack Investigation

## 📌 Incident Summary

A suspected brute-force authentication attack was detected against a Windows endpoint.

Multiple failed login attempts were observed from the same source within a short period of time.

---

## 🎯 Investigation Objective

Determine whether the authentication failures represent:

- Normal user activity
- A misconfigured application
- Password spraying
- Brute-force activity
- A potentially compromised account

---

## 🔎 Investigation Process

### 1. Identify Authentication Events

Windows Security Event Logs were reviewed for failed authentication attempts.

Relevant Event ID:

```text
4625 - An account failed to log on

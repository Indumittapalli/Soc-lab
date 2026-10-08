# ⚡ Suspicious PowerShell Investigation

## 📌 Incident Summary

Suspicious PowerShell activity was identified on a Windows endpoint and investigated to determine whether PowerShell was being used for legitimate administration or malicious execution.

---

## 🎯 Investigation Objective

Determine:

- Which user executed PowerShell
- Which process launched PowerShell
- What command was executed
- Whether the command was encoded or obfuscated
- Whether PowerShell downloaded or executed external content
- Whether additional suspicious processes were created
- Whether network connections were established

---

## 🔎 Investigation Process

### 1. Identify PowerShell Execution

Review Windows and Sysmon telemetry for PowerShell activity.

Important information includes:

- Username
- Timestamp
- Process ID
- Parent process
- Command line
- Execution path
- Destination IP/domain

---

### 2. Analyze the Parent Process

Investigate which process launched PowerShell.

Examples:

```text
winword.exe
    └── powershell.exe

excel.exe
    └── powershell.exe

outlook.exe
    └── powershell.exe

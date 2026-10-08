# Suspicious PowerShell Detection

## Objective

Detect potentially malicious PowerShell activity that may indicate
command execution, reconnaissance, persistence, or other post-exploitation
behavior.

## Data Sources

- Windows PowerShell logs
- Windows Event Logs
- Sysmon telemetry

## Detection Indicators

Look for PowerShell execution involving:

- `powershell.exe`
- `pwsh.exe`
- Encoded commands
- Obfuscated commands
- `-EncodedCommand`
- `-ExecutionPolicy Bypass`
- `-WindowStyle Hidden`
- Download or execution of remote content
- PowerShell spawned by unusual parent processes

## Relevant Windows Events

- **Event ID 4104** — PowerShell Script Block Logging
- **Event ID 4688** — Process Creation
- **Sysmon Event ID 1** — Process Creation

## Investigation Workflow

1. Identify the PowerShell process.
2. Review the command line.
3. Identify the parent process.
4. Determine the user account involved.
5. Check whether encoded or obfuscated commands were used.
6. Investigate referenced files, URLs, IP addresses, or domains.
7. Review related processes and network connections.
8. Extract relevant IOCs.
9. Map the activity to MITRE ATT&CK.
10. Document the investigation and response.

## Example Detection Logic

```text
Process = powershell.exe
AND
(CommandLine contains suspicious execution indicators)

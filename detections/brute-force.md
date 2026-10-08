# Brute-Force Login Detection

## Objective

Detect repeated failed authentication attempts that may indicate a
brute-force or password-guessing attack against a Windows endpoint.

## Data Sources

- Windows Security Event Logs
- Authentication events
- Sysmon telemetry where applicable

## Detection Logic

Look for multiple failed authentication attempts from the same source
within a short time window.

Relevant Windows Event ID:

- **4625** — An account failed to log on

Example investigation indicators:

- Multiple 4625 events
- Same source IP repeatedly attempting authentication
- Multiple usernames targeted from one source
- Successful login following repeated failures
- Unusual authentication times

## Investigation Workflow

1. Identify the affected account.
2. Identify the source IP address or hostname.
3. Review the frequency and time range of failed attempts.
4. Check whether a successful authentication occurred afterward.
5. Determine whether the source is internal or external.
6. Review related endpoint and network activity.
7. Extract relevant indicators of compromise.
8. Map the activity to the appropriate MITRE ATT&CK technique.
9. Document findings and recommended response actions.

## Example Detection Query

```text
Event ID = 4625
AND
Multiple failures from the same source
within a defined time window

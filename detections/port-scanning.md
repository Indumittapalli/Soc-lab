# Port Scanning Detection

## Objective

Detect network reconnaissance activity in which a host scans multiple
ports or services to identify accessible systems and potential attack
surfaces.

## Data Sources

- Firewall logs
- Network traffic logs
- IDS/IPS alerts
- Wireshark packet captures
- Sysmon network telemetry where available

## Detection Indicators

Look for:

- Multiple connection attempts to different ports
- Multiple destination ports contacted in a short period
- Sequential or systematic port probing
- Connection attempts to closed or filtered ports
- One source contacting many hosts
- Unusual internal reconnaissance activity

## Common Scanning Patterns

### Vertical Scan

One source scans multiple ports on a single destination.

### Horizontal Scan

One source attempts the same port across multiple destinations.

### Network Sweep

One source attempts to discover active hosts across a network range.

## Investigation Workflow

1. Identify the scanning source IP.
2. Identify the targeted destination IP or subnet.
3. Determine the number of ports contacted.
4. Review the time window of the activity.
5. Identify whether the source is internal or external.
6. Check whether connections were successful.
7. Review related firewall and IDS/IPS events.
8. Investigate the source host for additional suspicious activity.
9. Extract relevant IP addresses and ports.
10. Map the activity to MITRE ATT&CK.

## Example Detection Logic

```text
Same source IP
AND
Multiple destination ports
AND
High connection frequency
within a short time window

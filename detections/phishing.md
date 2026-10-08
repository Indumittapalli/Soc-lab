# Phishing Detection and Investigation

## Objective

Detect and investigate phishing activity that may attempt to trick users
into revealing credentials, opening malicious attachments, or accessing
malicious links.

## Data Sources

- Email security logs
- Mail gateway logs
- Windows Event Logs
- DNS logs
- Proxy or web logs
- Endpoint telemetry

## Detection Indicators

Look for:

- Suspicious sender addresses
- Spoofed or lookalike domains
- Unexpected attachments
- Suspicious URLs
- Credential-harvesting pages
- URL redirects
- Newly registered or suspicious domains
- Emails creating urgency or unusual requests
- Malicious file types or macros

## Common Phishing Techniques

### Malicious Link

An email contains a link that redirects the user to a malicious or
credential-harvesting website.

### Malicious Attachment

An attacker sends an attachment designed to execute malicious code
or exploit the recipient.

### Credential Phishing

A fake login page is used to capture usernames, passwords, or other
authentication information.

## Investigation Workflow

1. Identify the sender and recipient.
2. Review the sender address and domain.
3. Inspect URLs and attachments safely.
4. Extract domains, URLs, IP addresses, and file hashes.
5. Check whether the recipient opened the email or attachment.
6. Review endpoint activity following the interaction.
7. Review DNS and network connections.
8. Determine whether credentials may have been exposed.
9. Identify other recipients who received the same message.
10. Document findings and recommended response actions.

## IOC Extraction

Potential indicators include:

- Sender email address
- Sender domain
- Destination URL
- IP address
- File hash
- Attachment filename
- Malicious domain

## Analyst Response

If confirmed as malicious:

- Remove or quarantine the phishing email.
- Block malicious domains and URLs where appropriate.
- Isolate affected endpoints if compromise is suspected.
- Reset compromised credentials.
- Revoke active sessions when required.
- Search for the same indicators across the environment.
- Report and document the incident.

## MITRE ATT&CK

**T1566 — Phishing**

Related techniques may include:

- **T1566.001 — Spearphishing Attachment**
- **T1566.002 — Spearphishing Link**

## Investigation Status

Detection logic and investigation workflow documented.

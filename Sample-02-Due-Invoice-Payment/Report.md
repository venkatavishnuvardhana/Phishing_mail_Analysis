# Phishing Email Investigation Report

## Incident Summary

| Field | Value |
|------|------|
| Incident Type | Phishing Email |
| Analysis Date | July 2026 |
| Severity | High |
| Status | Confirmed Malicious |
| Analyst | A. Venkata Vishnu Vardhan |

---

# Executive Summary

A phishing email was received pretending to be a legitimate payment confirmation from a business partner. The attacker attempted to convince the recipient to open an attached ISO image named **quotation.iso**.

The attachment contained a malicious executable designed to infect the victim's system.

Static and dynamic analysis confirmed that the attachment is malicious.

---

# Investigation Methodology

The investigation followed the standard SOC phishing investigation workflow:

1. Email Review
2. Email Header Analysis
3. Attachment Analysis
4. VirusTotal Analysis
5. Dynamic Analysis (ANY.RUN)
6. IOC Extraction
7. Risk Assessment
8. Recommendations

---

# Email Analysis

## Sender

Paolo Reggiani <Paolo.Reggiani@moss.it>

## Recipient

wpx@protonmail.com

## Subject

FW: Due Invoice Payment - protonmail.com - Wire Transfer Document

## Social Engineering Indicators

- Payment urgency
- Business impersonation
- Requests immediate confirmation
- Uses professional language
- Malicious attachment included

---

# Header Analysis

The email headers were inspected to verify sender authenticity.

Items reviewed:

- Return-Path
- Received Headers
- SPF
- DKIM
- DMARC
- Message-ID

The header information showed authentication failures and suspicious routing, indicating the email should not be trusted.

---

# Attachment Analysis

Attachment Name

```
quotation.iso
```

Type

```
ISO Image
```

Purpose

The ISO image contained a Windows executable that launches malware when opened.

---

# VirusTotal Analysis

The attachment hash was searched in VirusTotal.

Results

- Multiple antivirus vendors detected the file.
- Classified as Trojan/Backdoor.
- High confidence malicious.

Evidence collected:

- Detection ratio
- File hashes
- File metadata
- File history

---

# Dynamic Analysis (ANY.RUN)

The attachment was executed inside the ANY.RUN sandbox.

Observed Behavior

- Process creation
- File extraction
- Dropped files
- Malware execution
- Network activity

The sandbox confirmed malicious behavior after execution.

---

# Indicators of Compromise

## Email

- Subject:
  - FW: Due Invoice Payment - protonmail.com - Wire Transfer Document

- Sender
  - Paolo.Reggiani@moss.it

- Attachment
  - quotation.iso

---

## File Hashes

MD5

```
6aef1df78e8ea4a50a0c604b4caee5ba
```

SHA1

```
3fe45f8cd20cd7c63e55e3918dac1d3a0d7fb05a
```

SHA256

```
75fdb848eac332b4ca7d88f497e7ba7ebbb9a798d825b28cf1f87b9d7149e87f
```

---

# Risk Assessment

| Category | Rating |
|----------|---------|
| Likelihood | High |
| Impact | High |
| Overall Risk | Critical |

---

# MITRE ATT&CK Mapping

| Technique | Description |
|-----------|-------------|
| T1566.001 | Phishing Attachment |
| T1204 | User Execution |
| T1105 | Ingress Tool Transfer |

---

# Recommendations

- Block the sender email address.
- Block the attachment hash.
- Quarantine infected endpoints.
- Educate users about phishing emails.
- Monitor for related Indicators of Compromise.
- Scan endpoints using EDR or antivirus.
- Implement email attachment filtering.
- Block ISO attachments where appropriate.

---

# Conclusion

The investigation confirmed that the email is a phishing campaign delivering malware through a malicious ISO attachment.

Both VirusTotal and ANY.RUN verified the attachment as malicious. The email should be considered a confirmed phishing attempt, and appropriate containment and detection measures should be implemented.

---

# Tools Used

- Thunderbird
- Sublime Text
- VirusTotal
- ANY.RUN
- Linux
- GitHub

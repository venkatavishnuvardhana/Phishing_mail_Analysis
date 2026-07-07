# Phishing Email Analysis

> A practical SOC analyst project demonstrating manual and automated phishing email analysis, IOC extraction, malware investigation, and incident reporting.

---

##  Project Objective

This repository demonstrates how Security Operations Center (SOC) analysts investigate phishing emails from initial detection to final incident response.

The objective is to:

- Analyze suspicious emails
- Investigate headers
- Analyze attachments
- Examine URLs
- Extract Indicators of Compromise (IOCs)
- Map attacker techniques to MITRE ATT&CK
- Produce an incident report

---


---

##  Tools Used

| Category | Tools |
|-----------|-------|
| Header Analysis | MXToolbox, Google Header Analyzer |
| Malware Analysis | ANY.RUN, Hybrid Analysis |
| URL Analysis | VirusTotal, URLScan.io |
| Threat Intelligence | ThreatFox, AbuseIPDB |
| Network Analysis | Wireshark, tcpdump |
| Endpoint Detection | Wazuh, Sysmon |
| Detection Rules | Sigma, YARA |

---

##  What You'll Learn

- Phishing Email Investigation
- Email Header Analysis
- Attachment Analysis
- Malicious URL Investigation
- IOC Extraction
- Malware Analysis
- MITRE ATT&CK Mapping
- SOC Incident Response

---

##  Analysis Stages

### Stage 1 – Email Collection

Collect:

- Original Email (.eml)
- Attachments
- URLs
- Email Headers

---

### Stage 2 – Initial Triage

Verify:

- Sender
- Subject
- Urgency
- Grammar
- Attachment
- URL

---

### Stage 3 – Header Analysis

Investigate:

- SPF
- DKIM
- DMARC
- Return-Path
- Reply-To
- Received Chain

---

### Stage 4 – URL Analysis

Check:

- Domain Reputation
- WHOIS
- DNS
- SSL Certificate
- Redirects

---

### Stage 5 – Attachment Analysis

Analyze:

- File Hash
- Metadata
- Macros
- Embedded URLs
- File Type

---

### Stage 6 – Malware Analysis

Perform:

- Static Analysis
- Dynamic Analysis
- Network Traffic Analysis
- Persistence Analysis

---

### Stage 7 – IOC Extraction

Extract:

- IP Addresses
- Domains
- URLs
- Hashes
- Registry Keys

---

### Stage 8 – Detection & Response

- MITRE ATT&CK Mapping
- Wazuh Detection
- Sigma Rules
- YARA Rules
- Incident Report

---

##  Sample Cases

| Case | Description |
|------|-------------|
| Case 01 | Malicious PDF Attachment |
| Case 02 | Fake Microsoft Login Page |
| Case 03 | ZIP File Malware Delivery |
| Case 04 | HTML Smuggling |
| Case 05 | Invoice Phishing |

---

##  Skills Demonstrated

- SOC Investigation
- Malware Analysis
- Threat Hunting
- IOC Extraction
- Network Analysis
- Incident Response
- Threat Intelligence

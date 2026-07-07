#  Project Objective

This repository demonstrates how a Security Operations Center (SOC) analyst performs a complete phishing email investigation from initial detection to final incident reporting.

The objective is not only to determine whether an email is malicious, but also to understand the attacker's techniques, identify Indicators of Compromise (IOCs), assess business risk, and recommend defensive actions.

---

#  Investigation Methodology

The investigation follows the same workflow commonly used by SOC analysts during phishing investigations.

## 1️ Email Header Analysis

**Purpose**

Verify the legitimacy of the sender and identify spoofing attempts.

**What is analyzed**

- From Address
- Reply-To Address
- Return-Path
- Sender IP Address
- Received Headers
- SPF
- DKIM
- DMARC
- Message-ID

**What we identify**

- Sender spoofing
- Authentication failures
- Mail server path
- Real sending infrastructure
- Suspicious mail routing

---

## 2️ Email Content Analysis

**Purpose**

Understand the attacker's social engineering strategy.

**What is analyzed**

- Subject line
- Email body
- Branding
- Language
- Urgency
- Psychological manipulation
- Embedded buttons
- Requests made to the victim

**What we identify**

- Brand impersonation
- Fear or urgency tactics
- Credential harvesting attempts
- Financial fraud
- Business Email Compromise indicators

---

## 3️ URL Analysis

**Purpose**

Determine whether embedded links redirect victims to malicious websites.

**What is analyzed**

- Embedded URLs
- Redirect chain
- Landing page
- Domain reputation
- WHOIS information
- SSL Certificate
- URLScan
- VirusTotal
- PhishTank

**What we identify**

- Credential phishing pages
- URL shorteners
- Malicious domains
- Newly registered domains
- Suspicious redirects

---
## 4️ Attachment Analysis (If Present)

**Purpose**

Determine whether the attachment contains malware or malicious content.

**What is analyzed**

- File extension
- File hash
- Static analysis
- Dynamic analysis
- Office macros
- JavaScript
- PDF objects

**What we identify**

- Malware
- Droppers
- Loaders
- Remote Access Trojans (RATs)
- Malicious scripts

---

## 5️ IOC Extraction

**Purpose**

Collect all Indicators of Compromise for future detection and response.

**Collected IOCs**

- IP Addresses
- Domains
- URLs
- Email Addresses
- File Hashes
- File Names
- Message IDs

**Usage**

These indicators can be imported into SIEM, EDR, IDS, firewall, or threat intelligence platforms.

---

## 6️ MITRE ATT&CK Mapping

**Purpose**

Map attacker behavior to the MITRE ATT&CK framework.

**Examples**

- T1566 – Phishing
- T1566.002 – Spearphishing Link
- T1036 – Masquerading
- T1204 – User Execution
- T1078 – Valid Accounts

This helps security teams understand attacker techniques and improve detection coverage.

---

## 7️ Incident Report

**Purpose**

Produce a professional investigation report.

The report includes:

- Executive Summary
- Header Analysis
- Content Analysis
- URL Analysis
- IOC Summary
- MITRE ATT&CK Mapping
- Risk Assessment
- Final Verdict
- Recommended Defensive Actions

---

#  Project Outcome

At the end of each investigation, the analyst is able to:

- Determine whether the email is legitimate or malicious.
- Identify the attacker's objective.
- Understand how the phishing attack works.
- Extract Indicators of Compromise (IOCs).
- Map the attack to MITRE ATT&CK.
- Produce a professional incident report suitable for SOC documentation.

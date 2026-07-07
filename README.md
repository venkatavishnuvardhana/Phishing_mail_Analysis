Phishing Email Analysis
Overview

This repository demonstrates how phishing emails are analyzed from the perspective of a Security Operations Center (SOC) analyst.

The objective is to determine whether an email is malicious, identify Indicators of Compromise (IOCs), understand attacker techniques, analyze attachments or URLs, and produce an incident report.

The repository combines both manual investigation and automated malware analysis to simulate a real-world SOC workflow.

What is a Phishing Email?

A phishing email is a malicious email designed to trick a user into performing an action such as:

Opening a malicious attachment
Clicking a malicious URL
Entering credentials
Installing malware
Sending sensitive information

Common phishing goals include:

Credential theft
Malware delivery
Initial Access
Business Email Compromise (BEC)
Financial Fraud
Phishing Email Analysis Stages
Stage 1 – Email Collection

Receive the suspicious email.

Sources

User Report
Secure Email Gateway
Microsoft Defender
Gmail
Exchange
SOC Alert

Evidence Collected

Original Email (.eml)
Headers
Attachments
URLs
Stage 2 – Initial Triage

Determine whether the email is suspicious.

Check

Sender
Subject
Attachment
URL
Urgency
Grammar
Brand impersonation

Decision

Benign
Suspicious
Malicious
Stage 3 – Header Analysis

Analyze email headers.

Investigate

From
Reply-To
Return-Path
SPF
DKIM
DMARC
Message-ID
Received chain

Goal

Determine if sender identity was spoofed.

Stage 4 – URL Analysis

Analyze embedded URLs.

Check

Domain Reputation
IP Address
WHOIS
DNS
HTTPS Certificate
URL Redirections
Stage 5 – Attachment Analysis

Analyze every attachment.

Possible Types

PDF
DOCM
XLSM
ZIP
ISO
EXE
LNK

Determine

Hashes
Metadata
Macros
Embedded URLs
Droppers
Stage 6 – Malware Analysis

If attachment is malicious

Perform

Static Analysis

File Hash
Strings
PE Information
Imports
Entropy

Dynamic Analysis

Process Creation
Network Traffic
Registry Changes
Dropped Files
Persistence
Stage 7 – IOC Extraction

Extract

IP Addresses
Domains
URLs
File Hashes
Registry Keys
Mutexes
File Names
Stage 8 – Detection

Map findings.

Examples

MITRE ATT&CK

T1566.001

Phishing Attachment

T1566.002

Phishing Link

T1204

User Execution

T1059

Command Execution

Stage 9 – Containment

SOC actions

Block sender
Block domain
Block URL
Block hash
Isolate endpoint
Reset credentials
Stage 10 – Reporting

Produce final report

Include

Timeline
Root Cause
Malware Family
IOCs
MITRE Mapping
Recommendations
Manual vs Automated Phishing Analysis
Manual Analysis	Automated Analysis
Human Investigation	Sandbox Analysis
Email Header Review	VirusTotal
URL Inspection	ANY.RUN
Attachment Inspection	Joe Sandbox
IOC Extraction	Hybrid Analysis
MITRE Mapping	CAPE Sandbox
Report Writing	Automated IOC Extraction
Analyst Decision	YARA Detection
Tools Used
Email Analysis
Thunderbird
Outlook
Gmail
Header Analysis
MXToolbox
Google Header Analyzer
URL Analysis
VirusTotal
URLScan
WHOIS
AbuseIPDB
Cisco Talos
Attachment Analysis
7-Zip
pdfid
oledump.py
olevba
pefile
Malware Analysis
ANY.RUN
Hybrid Analysis
CAPE Sandbox
Procmon
Process Explorer
Network Analysis
Wireshark
tcpdump
IOC Intelligence
VirusTotal
ThreatFox
MalwareBazaar
AlienVault OTX
Detection
Wazuh
Sysmon
Sigma Rules
YARA

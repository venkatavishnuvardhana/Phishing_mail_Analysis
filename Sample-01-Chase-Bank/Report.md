# Incident Report

## Executive Summary

A phishing email impersonating Chase Bank was analyzed.

The email falsely claimed the recipient's bank account had been temporarily suspended because of unusual activity.

The objective was to convince the victim to click a malicious URL and enter banking credentials into a fraudulent website.

---

# Header Analysis

## Observations

From:
alerts@chase.com

Reply-To:
kellyellin426@proton.me

Return-Path:
kellyellin426@proton.me

Sender IP:
185.70.40.140

SPF:
PASS

DKIM:
None

DMARC:
PASS (Policy=None)

---

## Analysis

Although SPF passed, it only verifies that ProtonMail is authorized to send email for the ProtonMail domain.

The visible sender claims to be Chase Bank, while the Reply-To and Return-Path point to a ProtonMail account.

This mismatch is a strong phishing indicator.

DKIM is not present, meaning there is no cryptographic signature verifying message integrity.

DMARC policy is set to "none", meaning emails failing authentication are not rejected.

---

# Email Content Analysis

The email creates urgency by claiming the victim's bank account has been blocked.

It instructs the user to immediately click a button labelled "Reactivate Your Account".

Psychological techniques used include:

- Fear
- Urgency
- Brand impersonation
- Account suspension

No legitimate banking verification process is described.

---

# Attacker Objective

The attacker attempts to steal:

- Online banking username
- Password
- Account credentials
- Personal information
- Financial information

The victim is redirected to a fake login page designed to harvest credentials.

---

# URL Analysis

The embedded URL uses:

dsgo.to

This shortened URL hides the final destination from the victim.

URLScan confirms the domain redirects.

VirusTotal reports the URL as malicious/suspicious.

PhishTank also classifies the URL as phishing.

---

# Indicators of Compromise

Sender IP:
185.70.40.140

Reply-To:
kellyellin426@proton.me

Return-Path:
kellyellin426@proton.me

Brand:
Chase Bank

Subject:
Your Bank Account has been blocked due to unusual activities

---

# Risk Assessment

Likelihood:
High

Impact:
High

Overall Risk:
Critical

---

# Verdict

This email is confirmed as a phishing attack.

The attacker impersonates Chase Bank and attempts to steal online banking credentials by redirecting victims to a credential harvesting website.

---

# Recommended Actions

- Block sender IP
- Block Reply-To address
- Block malicious URL
- Add IOC to SIEM
- Warn affected users
- Reset passwords if compromised
- Monitor authentication logs

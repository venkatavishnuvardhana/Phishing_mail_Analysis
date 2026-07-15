
# Indicators of Compromise (IOCs)

## Email Indicators

| Indicator | Value |
|-----------|-------|
| Subject | FW: Due Invoice Payment - protonmail.com - Wire Transfer Document |
| Sender | Paolo Reggiani <Paolo.Reggiani@moss.it> |
| Recipient | wpx@protonmail.com |
| Return Path | <Paolo.Reggiani@moss.it> |

---

## Attachment

| Indicator | Value |
|-----------|-------|
| File Name | quotation.iso |
| File Type | ISO Image |
| Size | 112 KB |

---

## File Hashes

| Hash | Value |
|------|-------|
| MD5 | 6aef1df78e8ea4a50a0c604b4caee5ba |
| SHA1 | 3fe45f8cd20cd7c63e55e3918dac1d3a0d7fb05a |
| SHA256 | 75fdb848eac332b4ca7d88f497e7ba7ebbb9a798d825b28cf1f87b9d7149e87f |

---

## Malware Detection

- Multiple antivirus engines detected the attachment as malicious.
- Malware was delivered through an ISO image containing a Windows executable.

---

## Recommended Actions

- Block the sender.
- Block the attachment hash.
- Quarantine affected systems.
- Scan endpoints for related malware.
- Educate users about malicious ISO attachments.

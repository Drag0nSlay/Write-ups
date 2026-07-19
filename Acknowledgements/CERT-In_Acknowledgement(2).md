# Case Study: Responsible Disclosure of Student PII & Financial Data Exposure

## Executive Summary
This case study documents the discovery, risk assessment, and successful remediation of a high-severity data exposure found on a prominent public educational institution's domain. The vulnerability exposed sensitive Personally Identifiable Information (PII) and banking credentials of approximately 377 students to the public internet without authentication. 

The issue was responsibly reported to the **Indian Computer Emergency Response Team (CERT-In)**, triaged under reference **CERTIn-76782826**, and has been completely remediated.

---

## Timeline
* **Discovery Date:** July 2026
* **Report Submitted (CERT-In):** July 2026
* **Triage & Registration:** July 2026 (Case Ref: CERTIn-76782826)
* **Remediation & Takedown:** July 2026 (Verified 404/403 Status)

---

## 🔍 Vulnerability Analysis & Discovery Method
The exposure was identified during a passive reconnaissance phase using targeted Open Source Intelligence (OSINT) and Advanced Google Dorking strings aimed at indexing audits.

### Discovery Pattern (Genericized)
```text
site:[redacted_target_domain] filetype:pdf inurl:accounts
```

### Affected Component

**Target Domain:** [REDACTED].[REDACTED].in

**Exposed Path:** https://www.[redacted].[redacted_domain]/accounts/refundlist2015/[redacted].pdf

### 🚨 Data Impact Assessment
The unauthenticated directory contained an active database dump/export in PDF format. A manual audit of the file structure revealed the exposure of:

**1. Full Identity Data:** Legal names, Roll numbers, Father Names and Ranks of ~377 enrolled students.

**2. Contact Tracing:** Active mobile/contact configurations.

**3. Critical Financial Vectors:** Plaintext listing of Bank Names, Individual Account Numbers, and IFSC codes.

### Attack Vector & Risk Scenario
Had this data been scraped by malicious threat actors, it could have been weaponized for:

- **Highly Targeted Social Engineering / Vishing:** Attackers posing as university account officials using exact refund details to drain accounts.

- **Financial Fraud & Identity Theft:** Using the leaked PII and banking coordinates to initiate unauthorized mandates or phishing campaigns.

### 🛡️ Remediation & Verification
Upon receiving the formal proof-of-concept, CERT-In coordinated with the institution's network administrators to enforce immediate containment.

#### Current Security Posture (Verified)
**Direct File Access:** Returns `404 Not Found` (Asset successfully expunged).

**Directory Traversal Route:** Returns `403 Forbidden` (Server-side indexing disabled).

🧾 Evidence & Acknowledgments
*All sensitive infrastructure endpoints and PII have been strictly redacted to maintain disclosure integrity.*

1. Reported Mail
2. Redacted Proof of Exposure
3. CERT-In Triage Confirmation

> Disclaimer: This repository is maintained strictly for educational and portfolio purposes. No identifying logs, live endpoints, or active user data have been or will be published.

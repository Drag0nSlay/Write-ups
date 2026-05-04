# Critical Security Risk – Exposed ADB Service (Port 5555)

![Poster](Images/Gemini_Generated_Image_1jfsm51jfsm51jfs.png)

## 🧾 Overview
A critical security exposure was identified involving an Android device with an open Android Debug Bridge (ADB) service accessible over the public internet. The service was exposed on TCP port 5555 without authentication.

---

## 🎯 Vulnerability Details
- **Type:** Misconfiguration / Unauthorized Remote Access  
- **Service:** Android Debug Bridge (ADB)  
- **Port:** 5555 (TCP)  
- **Exposure:** Publicly accessible via internet  

---

## ⚠️ Risk Impact
The exposed ADB service allows unauthorized users to:
- Gain remote shell access to the device
- Install or uninstall applications
- Access sensitive data
- Execute arbitrary commands
- Deploy malware or spyware

This creates a **high-risk scenario**, potentially leading to full device compromise.

---

## 🔍 Discovery Methodology
The exposed service was identified through passive reconnaissance using publicly available search engines for internet-connected devices.

- The device was indexed due to an open ADB port
- No authentication mechanism was observed

> Note: No active exploitation or interaction with the target system was performed.


## 📸 Evidence (Sanitized)

> Screenshots have been partially redacted to prevent misuse.

- HKCERT acknowledgement (sensitive details blurred)
- Shodan exposure preview (IP masked)

## 🔗 Public Disclosure
A summarized version of this finding was shared publicly:
[LinkedIn Post](https://www.linkedin.com/posts/aman-kothari-995944274_cybersecurity-responsibledisclosure-hkcert-activity-7341294233657425920-LhO7?utm_source=share&utm_medium=member_android&rcm=ACoAAEMPEIEBkP_6DK_YORdL0VqmbRIov8tHmHI)

---

## 🛡️ Responsible Disclosure
The issue was responsibly reported to **HKCERT (Hong Kong Computer Emergency Response Team Coordination Centre)**.

- The report was submitted in good faith
- No data was accessed, modified, or exfiltrated
- The report was acknowledged by HKCERT

---

## ✅ Mitigation Recommendations
To prevent such exposures, the following measures are recommended:
- Disable ADB over network when not in use
- Restrict access to trusted IP addresses only
- Use secure authentication mechanisms
- Keep device firmware updated
- Implement firewall rules to block public access

---

## 🏁 Conclusion
Exposed ADB services on public networks present a critical security risk due to the lack of authentication and high privilege access. Proper configuration and access control are essential to prevent unauthorized access and potential compromise.

---

## 🙌 Acknowledgement
This issue was responsibly disclosed to HKCERT (**Hong Kong Computer Emergency Response Team**), and acknowledgement was received from their team.

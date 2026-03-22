# 🧠 Advanced Phone OSINT Dorks

### 1. Multi-format brute correlation
People leak numbers in weird formats. Catch them all:
```bash
("9xxxxxxxxx" OR "9xxxx xxxxx" OR "9xxxx-xxxxx" OR "+919xxxxxxxxx")
```
👉 This is your base payload. Combine it with everything below.

### 2. Resume / Job portal leaks
```bash
("9xxxxxxxxx") ("resume" OR "cv" OR "curriculum vitae")
("9xxxxxxxxx") ("gmail.com" OR "yahoo.com")
filetype:pdf ("9xxxxxxxxx") ("resume" OR "contact")
```
💡 Freshers often expose full identity + email + address

### 3. Govt / institutional exposure (India-focused)
```bash
("9xxxxxxxxx") ("gov.in" OR "nic.in")
site:gov.in "9xxxxxxxxx"
site:ac.in "9xxxxxxxxx"
```
👉 Tenders, RTI docs, school lists, staff directories

### 4. Marketplace & classifieds footprint
```bash
("9xxxxxxxxx") ("OLX" OR "Quikr" OR "listing")
("9xxxxxxxxx") ("sell" OR "price" OR "urgent")
```
💡 Reveals behavior patterns + sometimes location clues

### 5. Directory indexing leaks (goldmine)
```bash
intitle:"index of" "9xxxxxxxxx"
intitle:"index of" ("contact" OR "users") "9xxxxxxxxx"
```
👉 Open directories = accidental data dumps

### 6. Breach + paste correlation
```bash
("9xxxxxxxxx") ("password" OR "pass" OR "pwd")
("9xxxxxxxxx") ("database" OR "dump" OR "leak")
site:pastebin.com "9xxxxxxxxx"
site:anonfiles.com "9xxxxxxxxx"
```
⚠️ Often partial but useful for pivoting

### 7. Username / identity pivoting
```bash
("9xxxxxxxxx") ("username" OR "user" OR "id")
("9xxxxxxxxx") ("@gmail.com" OR "@outlook.com")
```
👉 Connect number → email → username → social accounts

### 8. Social media deep indexing
```bash
site:facebook.com "9xxxxxxxxx" "lives in"
site:instagram.com "9xxxxxxxxx"
site:twitter.com "9xxxxxxxxx"
```
💡 Old cached data sometimes survives deletion

### 9. Behavioral inference dorks
```bash
("9xxxxxxxxx") ("OTP" OR "verification code")
("9xxxxxxxxx") ("booking" OR "order" OR "invoice")
```
👉 Reveals services used (food apps, travel, fintech)

### 10. Sensitive exposure hunting
```bash
("9xxxxxxxxx") ("patient" OR "hospital" OR "report")
("9xxxxxxxxx") ("aadhaar" OR "pan card")
```
⚠️ Rare but critical findings

### 11. Subdomain + internal leaks
```bash
site:*.in "9xxxxxxxxx"
site:*.com "9xxxxxxxxx" "contact"
```
👉 Helps find forgotten subdomains or internal portals

### 12. Smart chaining (real power)
Combine everything:
```bash
("9xxxxxxxxx" OR "+919xxxxxxxxx") ("resume" OR "gmail.com" OR "address" OR "Delhi") filetype:pdf
```
👉 This is where OSINT becomes *surgical*

## Tools + Platform Pivoting
**After dorks, pivot into:**
- **Truecaller** → Name tagging patterns
- **WhatsApp** → DP + status intel
- **Telegram** → Username mapping
- **Maltego** → Graph-based correlation

### Other Tactics
1. 🧵 **Pivot chaining:** number → email → username → GitHub → leaks
2. 🧪 **Time-based search:** filter old results (pre-account deletion)
3. 🧬 **Pattern reuse:** same number across resumes + classifieds
4. 🕳️ **Cache digging:** deleted pages via cached copies
5. 🔄 **Cross-format fuzzing: try partial numbers:**
   `"9xxxx" "xxxxx"`

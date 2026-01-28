# How I Hacked my College Attendance System - Not for Marks, but for Respect

2023 - the year I took admission into college.
Like most freshers, I was curious, observant, and already deep into cybersecurity. One day, a friend (Hacker K) casually said:
> Yaha ek Attendance System (eSIM) hai... usko hack krna hai.

That sentence planted a **wishlist** in my mind.
Not ego. Not marks. Not for Attendance. Just Curiosity 
> By the way in my college for 1st year students 79.99% attendance is mandatory.

At that time, I didn't even know what system - but I knew one thing:

**If a system exists, it can be broken.**

## The First Reality Check
I started finding Vulnerabilities - a lot of them
But none were **directly exploitable**

### From OSINT:
```bash
*.servergi.com:8077/ISI/login*
Registrant, Admin, Biling, Tech Name: Agarwal, Vineet
Street: <Redacted for Privacy>
City: -
State: U.P.
Postal Code: 2010xx
Country: IN
Phone: +9199xxxxxxxx
Email: <some-email@gmail.com>
<alternate-mail@rediffmail.com>

4 person who have access:-
1. Admin1
2. Admin2
3. Admin3
4. Admin4
```

> Note - All the Information above is Reacted for Privacy (including names who have access of admin panel)

### Testssl.sh
```bash
No engine or GOST support via engine with your /data/data/com.termux/files/usr/bin/openssl

 Start 2025-06-28 08:35:33        -->> 115.246.x.x:8077 (*.servergi.com) <<--

 rDNS (115.246.x.x):  --
 Service detected:       HTTP


 Testing vulnerabilities 

 Heartbleed (CVE-2014-0160)                not vulnerable (OK), no heartbeat extension
 CCS (CVE-2014-0224)                       not vulnerable (OK)
 Ticketbleed (CVE-2016-9244), experiment.  not vulnerable (OK), no session ticket extension
 ROBOT                                     not vulnerable (OK)
 Secure Renegotiation (RFC 5746)           supported (OK)
 Secure Client-Initiated Renegotiation     not vulnerable (OK)
 CRIME, TLS (CVE-2012-4929)                not vulnerable (OK)
 BREACH (CVE-2013-3587)                    potentially NOT ok, "gzip" HTTP compression detected. - only supplied "/SI*/login" tested
                                           Can be ignored for static pages or if no secrets in the page
 POODLE, SSL (CVE-2014-3566)               VULNERABLE (NOT ok), uses SSLv3+CBC (check TLS_FALLBACK_SCSV mitigation below)
 TLS_FALLBACK_SCSV (RFC 7507)              No fallback possible (OK), no protocol below TLS 1.2 offered
 SWEET32 (CVE-2016-2183, CVE-2016-6329)    VULNERABLE, uses 64 bit block ciphers
 FREAK (CVE-2015-0204)                     not vulnerable (OK)
 DROWN (CVE-2016-0800, CVE-2016-0703)      not vulnerable on this host and port (OK)
                                           make sure you don't use this certificate elsewhere with SSLv2 enabled services
                                           https://search.censys.io/search?resource=hosts&virtual_hosts=INCLUDE&q=902867650880C6D7103702F590D3727D84A7D8BBF9910F4EBFC8C86304DB3BD2
 LOGJAM (CVE-2015-4000), experimental      VULNERABLE (NOT ok): common prime: RFC2409/Oakley Group 2 (1024 bits),
                                           but no DH EXPORT ciphers
 BEAST (CVE-2011-3389)                     SSL3: DES-CBC3-SHA 
                                           VULNERABLE -- but also supports higher protocols  TLSv1.2 (likely mitigated)
 LUCKY13 (CVE-2013-0169), experimental     potentially VULNERABLE, uses cipher block chaining (CBC) ciphers with TLS. Check patches
 RC4 (CVE-2013-2566, CVE-2015-2808)        VULNERABLE (NOT ok): RC4-SHA RC4-MD5 


 Done 2025-06-28 08:36:41 [0080s] -->> 115.246.x.x:8077 (*.servergi.com) <<--
```

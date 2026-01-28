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
![PoC](PoC/Picsart_26-01-27_23-52-24-869.jpg)

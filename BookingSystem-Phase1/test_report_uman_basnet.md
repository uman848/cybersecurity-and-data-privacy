# 1️⃣ Introduction

## Tester(s)
- **Name:** Uman Basnet

## Purpose
Identify vulnerabilities and weaknesses in the **registration page** of the Booking System (Phase 1).

## Scope
- **Tested:** Registration page, form inputs, database storage, HTTP communication, OWASP ZAP scan  
- **Excluded:** Login, reservations, admin features, session management  

## Test Approach
Gray‑box testing

## Test Environment & Dates
- **Start:** *[11 feb 2026]* 
- **End:** *[11 feb 2026]*  
- **Environment:**  
  - macOS  
  - Docker Desktop  
  - PostgreSQL (Docker)  
  - Chrome 
  - OWASP ZAP 2.16.1  

## Assumptions & Constraints
- Only registration page tested  
- System intentionally vulnerable  
- No HTTPS available  

---

# 2️⃣ Executive Summary

## Short Summary
The registration page contains several high‑risk vulnerabilities, including plain‑text password storage, missing validation, and missing security headers.

## Overall Risk Level
🟥 **High**

## Top 5 Immediate Actions
1. Hash passwords (bcrypt/Argon2)  
2. Add server‑side input validation  
3. Enable HTTPS  
4. Add security headers (CSP, X‑Frame‑Options, X‑Content‑Type‑Options)  
5. Add CSRF protection  

---

# 3️⃣ Severity Scale & Definitions

| Severity | Description | Recommended Action |
|---------|-------------|--------------------|
| 🔴 High | Serious vulnerability | Fix immediately |
| 🟠 Medium | Significant issue | Fix ASAP |
| 🟡 Low | Minor weakness | Fix soon |
| 🔵 Info | No direct risk | Fix in maintenance |

---

# 4️⃣ Findings

| ID | Severity | Finding | Description | Evidence / Proof |
|----|----------|---------|-------------|------------------|
| **F‑01** | 🔴 High | Plain‑text password storage | Passwords stored in cleartext in DB | `SELECT * FROM booking_users;` shows readable passwords |
| **F‑02** | 🔴 High | Missing input validation | SQLi, XSS, long strings accepted | `' OR '1'='1`, `<script>alert(1)</script>` |
| **F‑03** | 🟠 Medium | No HTTPS | Data sent over HTTP | Browser shows `http://localhost:8001` |
| **F‑04** | 🟠 Medium | Missing security headers | CSP, X‑Frame‑Options, X‑Content‑Type‑Options missing | ZAP alerts |
| **F‑05** | 🟠 Medium | No CSRF protection | Forms lack anti‑CSRF tokens | ZAP alert: Absence of Anti‑CSRF Tokens |
   ## Screen shot
   <img width="579" height="378" alt="Screenshot 2026-02-12 at 18 18 03" src="https://github.com/user-attachments/assets/ca775db5-abd0-4de3-90cf-ca5b3fef6523" /><img width="862" height="789" alt="Screenshot 2026-02-12 at 18 19 06" src="https://github.com/user-attachments/assets/678a4e84-02d1-464e-925c-58f8bf2392c0" />
   

   <img width="563" height="373" alt="Screenshot 2026-02-18 at 21 23 16" src="https://github.com/user-attachments/assets/e5870fd0-bbdc-41a1-ba52-672bf581e741" />




# 1️⃣ Phase 1 – Part 2

## Tester(s)
- **Name:** Uman Basnet

## Purpose
Re-test the updated Booking System (Phase 1 → Part 2) to verify whether the vulnerabilities identified in Part 1 were fixed.

## Scope
- **Tested:** Registration page, form inputs, database storage, HTTP communication, OWASP ZAP Round 2  
- **Excluded:** Login, reservations, admin features, session management  

## Test Approach
Gray‑box testing

## Test Environment & Dates
- **Date:** *18 Feb 2026*  
- **Environment:**  
  - macOS  
  - Docker Desktop  
  - PostgreSQL (Docker)  
  - Chrome  
  - OWASP ZAP  

## Assumptions & Constraints
- Only registration page re-tested  
- System intentionally vulnerable  
- No HTTPS available  

---

# 2️⃣ Executive Summary

## Short Summary
The updated application (Part 2) was tested to verify whether the issues from Part 1 were fixed.  
All five major vulnerabilities remain unfixed.

## Overall Fix Status
🟥 **0 / 5 Issues Fixed**

## Findings Status Overview
1. Plain‑text password storage → **Not Fixed**  
2. Missing input validation (SQLi/XSS) → **Not Fixed**  
3. No HTTPS → **Not Fixed**  
4. Missing security headers → **Not Fixed**  
5. No CSRF protection → **Not Fixed**  

---

# 3️⃣ Verification of Findings (Part 2)

## **F‑01: Plain‑text Password Storage**
- **Status:** Not Fixed  
- Passwords still stored in readable form in `booking_users` table  
- Verified using:  
  ```
  SELECT * FROM booking_users;
  ```

## **F‑02: Missing Input Validation (SQLi/XSS)**
- **Status:** Not Fixed  
- SQL injection payloads still accepted  
- XSS payloads still executed  

## **F‑03: No HTTPS**
- **Status:** Not Fixed  
- Application still runs on `http://localhost:8002`  

## **F‑04: Missing Security Headers**
- **Status:** Not Fixed  
- ZAP Round 2 shows missing CSP, X‑Frame‑Options, X‑Content‑Type‑Options  

## **F‑05: No CSRF Protection**
- **Status:** Not Fixed  
- Forms still lack anti‑CSRF tokens  
- ZAP Round 2 confirms absence of CSRF protection  

---

screenshot
<img width="563" height="373" alt="Screenshot 2026-02-18 at 21 23 16" src="https://github.com/user-attachments/assets/55452ad9-c6d3-40b9-8fc0-5c8de82a0752" />


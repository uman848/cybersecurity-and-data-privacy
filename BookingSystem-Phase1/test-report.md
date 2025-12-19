# Phase 1 Test Report

## 1. Introduction
**Tester:** Uman Basnet  
**Purpose:** Identify vulnerabilities in the Booking System registration and authentication flows.  
**Scope:** Registration page, input validation, session handling, error messages, database storage.  
**Environment:**  
- macOS Ventura  
- Docker Desktop (web app + PostgreSQL)  
- Browsers: Chrome, Firefox  
- Dates: 2025‑12‑18 to 2025‑12‑19  

---

## 2. Executive Summary
Testing revealed multiple vulnerabilities including SQL injection, weak password enforcement, and missing CSRF protection. These flaws pose a high risk to system integrity and user data privacy.  

**Overall Risk Level:** 🔴 High  

**Top 5 Immediate Actions:**
1. Implement parameterized queries to prevent SQL injection.  
2. Enforce strong password policies.  
3. Add CSRF tokens to registration forms.  
4. Regenerate session IDs after login.  
5. Configure security headers (CSP, HSTS, X‑Frame‑Options).  

---

## 3. Severity Scale
| Severity | Description | Action |
|----------|-------------|--------|
| 🔴 High  | Leads to full system compromise or data breach | Immediate fix |
| 🟠 Medium| Significant issue requiring conditions/user interaction | Fix ASAP |
| 🟡 Low   | Minor issue or weakness | Fix soon |
| 🔵 Info  | No direct risk, useful for hardening | Monitor |

---

## 4. Findings
| ID   | Severity | Finding                  | Description | Evidence |
|------|----------|--------------------------|-------------|----------|
| F‑01 | 🔴 High  | SQL Injection            | Input field allows `' OR '1'='1` injection | sqlmap log |
| F‑02 | 🟠 Medium| Session Fixation         | Session ID unchanged after login | Burp capture |
| F‑03 | 🟡 Low   | Weak Password Policy     | Accepts trivial passwords | Screenshot |
| F‑04 | 🔵 Info  | Missing Security Headers | No CSP, HSTS, X‑Frame‑Options | ZAP scan |
| F‑05 | 🟠 Medium| CSRF Vulnerability       | Registration form lacks CSRF token | Burp/ZAP evidence |

---

## 5. Conclusion
Phase 1 testing shows critical vulnerabilities that must be addressed before moving to Phase 2. Immediate remediation is required to ensure compliance with GDPR and Privacy by Design principles.

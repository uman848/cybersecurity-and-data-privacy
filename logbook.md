# Logbook

## Phase 1 – Booking System Security Testing
**Date:** 2025‑12‑19  
**Tester:** Uman Basnet  

### Activities
- Set up Docker environment with Booking System and PostgreSQL.
- Conducted manual testing of registration and login flows.
- Ran OWASP ZAP baseline scan against http://localhost:8000.
- Documented vulnerabilities in `test-report.md` and `zap_report_round1.md`.

### Findings
- SQL injection vulnerability in registration input.
- Missing CSRF protection on forms.
- Weak password policy accepted trivial values.
- Security headers (CSP, HSTS, X‑Frame‑Options) not configured.

### Reflections
- Environment setup was straightforward with Docker.
- ZAP scan confirmed manual findings, reinforcing the importance of automated tools.
- Next phase will focus on remediation and retesting.

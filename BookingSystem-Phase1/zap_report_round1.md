# OWASP ZAP Report – Round 1

**Target:** http://localhost:8000  
**Date:** 2025‑12‑19  
**Tool:** OWASP ZAP baseline scan  

---

## Alerts

| ID   | Severity | Issue                  | Description | Evidence |
|------|----------|------------------------|-------------|----------|
| Z‑01 | 🔴 High  | SQL Injection          | Input vulnerable to injection | ZAP log |
| Z‑02 | 🟠 Medium| Missing CSRF Token     | Form requests accepted without CSRF protection | Request replay |
| Z‑03 | 🟡 Low   | Weak Password Policy   | Password field accepts trivial values | Screenshot |
| Z‑04 | 🔵 Info  | Missing Security Headers | CSP, HSTS not configured | ZAP scan |

---

## Commands Used
```bash
zap-baseline.py -t http://localhost:8000 -r zap_report_round1.html -J zap_report.json
zap-cli report -o zap_report_round1.md -f markdown

# 1️⃣ Introduction

**Tester(s):**  
- Name:  UMAN BASNET

**Purpose:**  
- Checking if the system can be broken or misused
- Making sure user data is protected(GDPR).
- Ensuring the registration works correctly and securely.
- Finding anything that could let attackers bypass rules, injectcode or steal data

**Scope:**  
- Tested components: 
 user registration page, 
 input valiadation,
 registration logic and error handling,
 database storage of new users,
 basic security check related to registration,
- Exclusions: Login functionality, User roles (admin/reserver) after registration ,resource booking or reservation feartures, Administrator action ,performance testing, Full GDPR compliance audit
- Test approach: Gray-box (some interal knowledge available,including database access, but no source code.)

**Test environment & dates:**  
- Start:  02 march 2026
- End: 02 march 2025 
- Test environment details (MACOS, runtime, docker, browsers, VS code, zap):

**Assumptions & constraints:**  
- Acess, functionality, test-data, local-environment
- Time,scope , no-code, local-only

---

# 2️⃣ Executive Summary

**Short summary (1-2 sentences):**  
The registration feature contain several critical weakness, including missing input validation, incorrect age check and improper role handling. these issues allow attackers to create invalid accounts, underage accounts, and even administrator account.


**Overall risk level:** **critical**

**Top 5 immediate actions:**  
1.  fix age validation logic
2.  enforce strong input invalidation for all fields
3.  implement strict password policy and hashing.
4.  prevent unauthorixed role assignment
5.  validate and sanitize all user inputs (email, name,date of birht).

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration | Input field allows `' OR '1'='1` injection | Screenshot or sqlmap result |
| F-02 | 🟠 Medium | Session fixation | Session ID remains unchanged after login | Burp log or response headers |
| F-03 | 🟡 Low | Weak password policy | Accepts passwords like "12345" | Screenshot of registration success |

---


---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).
- i have attached zap report in seperate file.

  SCREENSHOT OF SQL injection

  <img width="629" height="422" alt="Screenshot 2026-03-02 at 23 31 22" src="https://github.com/user-attachments/assets/c86c43ec-7108-4888-b30e-fba0c915e8b8" />

  


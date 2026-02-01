# Logbook – Cybersecurity and Data Privacy Spring 2026
Author: Uman Basnet  
GitHub Repo: https://github.com/uman848/cybersecurity-and-data-privacy/edit/main/logbook.md

---

## Week 1
### Date: 2026-01-25
**Topic:** Course introduction, Git setup, and cybersecurity basics  
**What I learned:**  
- Understood course structure and assignment workflow  
- Set up GitHub repository for submitting tasks  
- Reviewed fundamental cybersecurity concepts (CIA triad, malware types, security tools)

**Tasks completed:**  
- Created GitHub repository  
- Created logbook following the required template  
- Submitted repo link for assignment

**Next steps:**  
- Begin working on Week 2 exercises  
- Continue adding entries to the logbook after each session

## Week 2
   ✅ Completed Labs
## 🧪 SQL Injection
1. SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
Reflection:  
I learned how attackers can change a SQL query by adding their own input. This allowed me to see information that was supposed to be hidden. The hardest part was finding which input field was vulnerable. This lab showed why websites must always check and clean user input.

2. SQL injection vulnerability allowing login bypass
Reflection:  
This lab taught me how SQL injection can break the login system. By adding a special input to the username, I could skip the password check and log in as the administrator. The difficult part was dealing with the CSRF token and matching the session. Once I understood that, the attack worked easily.

 ##**Authentication**
3. Username enumeration via different responses
Reflection:  
I learned that websites can accidentally reveal valid usernames if their error messages are different. By testing different usernames, I could see which ones existed. The challenge was noticing the small differences in the responses. This showed why login errors should always look the same.

4. 2FA simple bypass
Reflection:  
This lab showed how weak two‑factor authentication can be bypassed. By understanding how the 2FA step worked, I was able to skip it and log in. The hardest part was figuring out where the system failed. This taught me that 2FA must be implemented carefully to be secure.

##**Access Control**
5. Unprotected admin functionality
Reflection:  
I learned that some admin pages can be accessed without any checks. By going directly to the admin URL, I could use admin features without logging in. The challenge was finding the admin page. This showed why access control must always be checked on the server.

6. Unprotected admin functionality with unpredictable URL
Reflection:  
This lab taught me that even if an admin URL looks random, it still needs proper access control. I found the hidden URL and accessed admin features without permission. The hardest part was locating the correct path. This showed that security should not rely on “hidden” URLs.

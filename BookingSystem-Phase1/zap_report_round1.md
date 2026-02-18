[zap report 1.md.txt](https://github.com/user-attachments/files/25394929/zap.report.1.md.txt)
  ZAP by Checkmarx Scanning Report   

ZAP by Checkmarx Scanning Report
================================

Generated with [![The ZAP logo](2026-02-11-ZAP-Report%20part1-/zap32x32.png)ZAP](https://zaproxy.org) on Wed 11 Feb 2026, at 19:13:37

ZAP Version: 2.16.1

ZAP by [Checkmarx](https://checkmarx.com/)

Contents
--------

1.  [About This Report](#about-this-report)
    1.  [Report Parameters](#report-parameters)
*   [Summaries](#summaries)
    1.  [Alert Counts by Risk and Confidence](#risk-confidence-counts)
    2.  [Alert Counts by Site and Risk](#site-risk-counts)
    3.  [Alert Counts by Alert Type](#alert-type-counts)
*   [Alerts](#alerts)
    1.  [Risk\=Medium, Confidence\=High (1)](#alerts--risk-2-confidence-3)
    2.  [Risk\=Medium, Confidence\=Medium (1)](#alerts--risk-2-confidence-2)
    3.  [Risk\=Medium, Confidence\=Low (1)](#alerts--risk-2-confidence-1)
    4.  [Risk\=Low, Confidence\=High (1)](#alerts--risk-1-confidence-3)
    5.  [Risk\=Low, Confidence\=Medium (2)](#alerts--risk-1-confidence-2)
*   [Appendix](#appendix)
    1.  [Alert Types](#alert-types)

About This Report
-----------------

### Report Parameters

#### Contexts

No contexts were selected, so all contexts were included by default.

#### Sites

The following sites were included:

*   http://localhost:8001

(If no sites were selected, all sites were included by default.)

An included site must also be within one of the included contexts for its data to be included in the report.

#### Risk levels

Included: High, Medium, Low, Informational

Excluded: None

#### Confidence levels

Included: User Confirmed, High, Medium, Low

Excluded: User Confirmed, High, Medium, Low, False Positive

Summaries
---------

### Alert Counts by Risk and Confidence

This table shows the number of alerts for each level of risk and confidence included in the report.

(The percentages in brackets represent the count as a percentage of the total number of alerts included in the report, rounded to one decimal place.)

   

Confidence

User Confirmed

High

Medium

Low

Total

Risk

High

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

Medium

0  
(0.0%)

1  
(16.7%)

1  
(16.7%)

1  
(16.7%)

3  
(50.0%)

Low

0  
(0.0%)

1  
(16.7%)

2  
(33.3%)

0  
(0.0%)

3  
(50.0%)

Informational

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

0  
(0.0%)

Total

0  
(0.0%)

2  
(33.3%)

3  
(50.0%)

1  
(16.7%)

6  
(100%)

### Alert Counts by Site and Risk

This table shows, for each site for which one or more alerts were raised, the number of alerts raised at each risk level.

Alerts with a confidence level of "False Positive" have been excluded from these counts.

(The numbers in brackets are the number of alerts raised for the site at or above that risk level.)

  

Risk

High  
(= High)

Medium  
(>= Medium)

Low  
(>= Low)

Informational  
(>= Informational)

Site

http://localhost:8001

0  
(0)

3  
(3)

3  
(6)

0  
(6)

### Alert Counts by Alert Type

This table shows the number of alerts of each alert type, together with the alert type's risk level.

(The percentages in brackets represent each count as a percentage, rounded to one decimal place, of the total number of alerts included in this report.)

Alert type

Risk

Count

[Absence of Anti-CSRF Tokens](#alert-type-0)

Medium

1  
(16.7%)

[Content Security Policy (CSP) Header Not Set](#alert-type-1)

Medium

3  
(50.0%)

[Missing Anti-clickjacking Header](#alert-type-2)

Medium

3  
(50.0%)

[Application Error Disclosure](#alert-type-3)

Low

1  
(16.7%)

[X-Content-Type-Options Header Missing](#alert-type-4)

Low

6  
(100.0%)

[ZAP is Out of Date](#alert-type-5)

Low

1  
(16.7%)

Total

6

Alerts
------

1.  ### Risk\=Medium, Confidence\=High (1)
    
    1.  #### http://localhost:8001 (1)
        
        1.  ##### [Content Security Policy (CSP) Header Not Set](#alert-type-1) (1)
            
            1.  GET http://localhost:8001
                
                Alert tags
                
                *   [OWASP\_2021\_A05](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)
                *   POLICY\_QA\_STD =
                *   POLICY\_PENTEST =
                *   [SYSTEMIC](https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic)
                *   [CWE-693](https://cwe.mitre.org/data/definitions/693.html)
                *   [OWASP\_2017\_A06](https://owasp.org/www-project-top-ten/2017/A6_2017-Security_Misconfiguration.html)
                
                Alert description
                
                Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.
                
                Request
                
                Request line and header section (228 bytes)
                
                    GET http://localhost:8001 HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                
                Request body (0 bytes)
                
                Response
                
                Status line and header section (141 bytes)
                
                    HTTP/1.1 200 OK
                    content-type: text/html; charset=UTF-8
                    vary: Accept-Encoding
                    content-length: 3341
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                
                Response body (3341 bytes)
                
                    <!DOCTYPE html>
                    <html lang="en">
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <title>Booking System</title>
                        <link href="/static/tailwind.css" rel="stylesheet">
                    </head>
                    <body class="flex flex-col min-h-screen bg-gray-100 text-gray-900">
                        <!-- Header -->
                        <div class="container mx-auto p-4 mt-4 text-center">
                            <div class="flex flex-col md:flex-row justify-between space-y-6 md:space-y-0 md:space-x-6 max-w-5xl mx-auto">
                                <!-- Left box -->
                                <div class="bg-white shadow-md rounded-lg p-6 w-full md:w-2/3">
                                    <h1 class="text-2xl font-bold mb-4">Welcome to the Booking system</h1>
                                    <p class="mb-4">Please choose one of the options below:</p>
                                    <div id="action-links" class="flex justify-between space-x-4">
                                        <a id="add-resource" href="/resources" class="inline-block bg-gray-400 text-white py-2 px-4 rounded w-1/2 cursor-not-allowed pointer-events-none">Add a new resource</a>
                                        <a id="add-reservation" href="/reservation" class="inline-block bg-gray-400 text-white py-2 px-4 rounded w-1/2 cursor-not-allowed pointer-events-none">Add a new reservation</a>
                                    </div>
                                </div>
                    
                                <!-- Right box -->
                                <div id="userBox" class="bg-white shadow-md rounded-lg p-6 w-full md:w-1/3">
                                    <h2 class="text-xl font-bold mb-4">You are not logged in</h2>
                                    <p class="mb-4">You must first log in or register.</p>
                                    <div id="action-links" class="flex justify-between space-x-4 mt-4">
                                        <a href="/login" class="inline-block bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 w-1/2 cursor-not-allowed pointer-events-none">Login</a>
                                        <a href="/register" class="inline-block bg-gray-500 text-white py-2 px-4 rounded hover:bg-gray-600 w-1/2">Register</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <main class="flex-grow">
                        <!-- Reservations -->
                        <div class="container mx-auto p-4 text-center">
                            <div class="bg-white shadow-md rounded-lg p-6 mb-6 max-w-5xl mx-auto">
                                <h1 class="text-2xl font-bold mb-4">Booked resources</h1>
                                <div class="overflow-x-auto">
                                    <table class="min-w-full bg-white border border-gray-300">
                                        <thead id="reservationTableHead" class="bg-gray-200">
                                            <tr>
                                                <th class="py-2 px-4 border-b">Resource name</th>
                                                <th class="py-2 px-4 border-b">Reservation start</th>
                                                <th class="py-2 px-4 border-b">Reservation end</th>
                                                <!--<th id="reserverHead" class="py-2 px-4 border-b">Reserver</th>-->
                                            </tr>
                                        </thead>
                                        <tbody id="reservationTable">
                                            <!-- Dynamic table rows injected here -->
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                        </main>
                        <!-- Footer -->
                        <div id="footer-placeholder"></div>
                        <script src="/static/footer.js"></script>
                        <script src="/static/index.js"></script>
                    </body>
                    </html>
                
                Solution
                
                Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header.
                
2.  ### Risk\=Medium, Confidence\=Medium (1)
    
    1.  #### http://localhost:8001 (1)
        
        1.  ##### [Missing Anti-clickjacking Header](#alert-type-2) (1)
            
            1.  GET http://localhost:8001
                
                Alert tags
                
                *   [OWASP\_2021\_A05](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)
                *   POLICY\_QA\_STD =
                *   POLICY\_PENTEST =
                *   [CWE-1021](https://cwe.mitre.org/data/definitions/1021.html)
                *   [SYSTEMIC](https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic)
                *   [WSTG-v42-CLNT-09](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/11-Client-side_Testing/09-Testing_for_Clickjacking)
                *   [OWASP\_2017\_A06](https://owasp.org/www-project-top-ten/2017/A6_2017-Security_Misconfiguration.html)
                
                Alert description
                
                The response does not protect against 'ClickJacking' attacks. It should include either Content-Security-Policy with 'frame-ancestors' directive or X-Frame-Options.
                
                Request
                
                Request line and header section (228 bytes)
                
                    GET http://localhost:8001 HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                
                Request body (0 bytes)
                
                Response
                
                Status line and header section (141 bytes)
                
                    HTTP/1.1 200 OK
                    content-type: text/html; charset=UTF-8
                    vary: Accept-Encoding
                    content-length: 3341
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                
                Response body (3341 bytes)
                
                    <!DOCTYPE html>
                    <html lang="en">
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <title>Booking System</title>
                        <link href="/static/tailwind.css" rel="stylesheet">
                    </head>
                    <body class="flex flex-col min-h-screen bg-gray-100 text-gray-900">
                        <!-- Header -->
                        <div class="container mx-auto p-4 mt-4 text-center">
                            <div class="flex flex-col md:flex-row justify-between space-y-6 md:space-y-0 md:space-x-6 max-w-5xl mx-auto">
                                <!-- Left box -->
                                <div class="bg-white shadow-md rounded-lg p-6 w-full md:w-2/3">
                                    <h1 class="text-2xl font-bold mb-4">Welcome to the Booking system</h1>
                                    <p class="mb-4">Please choose one of the options below:</p>
                                    <div id="action-links" class="flex justify-between space-x-4">
                                        <a id="add-resource" href="/resources" class="inline-block bg-gray-400 text-white py-2 px-4 rounded w-1/2 cursor-not-allowed pointer-events-none">Add a new resource</a>
                                        <a id="add-reservation" href="/reservation" class="inline-block bg-gray-400 text-white py-2 px-4 rounded w-1/2 cursor-not-allowed pointer-events-none">Add a new reservation</a>
                                    </div>
                                </div>
                    
                                <!-- Right box -->
                                <div id="userBox" class="bg-white shadow-md rounded-lg p-6 w-full md:w-1/3">
                                    <h2 class="text-xl font-bold mb-4">You are not logged in</h2>
                                    <p class="mb-4">You must first log in or register.</p>
                                    <div id="action-links" class="flex justify-between space-x-4 mt-4">
                                        <a href="/login" class="inline-block bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 w-1/2 cursor-not-allowed pointer-events-none">Login</a>
                                        <a href="/register" class="inline-block bg-gray-500 text-white py-2 px-4 rounded hover:bg-gray-600 w-1/2">Register</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <main class="flex-grow">
                        <!-- Reservations -->
                        <div class="container mx-auto p-4 text-center">
                            <div class="bg-white shadow-md rounded-lg p-6 mb-6 max-w-5xl mx-auto">
                                <h1 class="text-2xl font-bold mb-4">Booked resources</h1>
                                <div class="overflow-x-auto">
                                    <table class="min-w-full bg-white border border-gray-300">
                                        <thead id="reservationTableHead" class="bg-gray-200">
                                            <tr>
                                                <th class="py-2 px-4 border-b">Resource name</th>
                                                <th class="py-2 px-4 border-b">Reservation start</th>
                                                <th class="py-2 px-4 border-b">Reservation end</th>
                                                <!--<th id="reserverHead" class="py-2 px-4 border-b">Reserver</th>-->
                                            </tr>
                                        </thead>
                                        <tbody id="reservationTable">
                                            <!-- Dynamic table rows injected here -->
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                        </main>
                        <!-- Footer -->
                        <div id="footer-placeholder"></div>
                        <script src="/static/footer.js"></script>
                        <script src="/static/index.js"></script>
                    </body>
                    </html>
                
                Parameter
                
                    x-frame-options
                
                Solution
                
                Modern Web browsers support the Content-Security-Policy and X-Frame-Options HTTP headers. Ensure one of them is set on all web pages returned by your site/app.
                
                If you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive.
                
3.  ### Risk\=Medium, Confidence\=Low (1)
    
    1.  #### http://localhost:8001 (1)
        
        1.  ##### [Absence of Anti-CSRF Tokens](#alert-type-0) (1)
            
            1.  GET http://localhost:8001/register
                
                Alert tags
                
                *   [OWASP\_2021\_A01](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
                *   POLICY\_QA\_STD =
                *   POLICY\_PENTEST =
                *   [SYSTEMIC](https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic)
                *   [WSTG-v42-SESS-05](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/06-Session_Management_Testing/05-Testing_for_Cross_Site_Request_Forgery)
                *   [OWASP\_2017\_A05](https://owasp.org/www-project-top-ten/2017/A5_2017-Broken_Access_Control.html)
                *   [CWE-352](https://cwe.mitre.org/data/definitions/352.html)
                *   POLICY\_DEV\_STD =
                
                Alert description
                
                No Anti-CSRF tokens were found in a HTML submission form.
                
                A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.
                
                CSRF attacks are effective in a number of situations, including:
                
                \* The victim has an active session on the target site.
                
                \* The victim is authenticated via HTTP auth on the target site.
                
                \* The victim is on the same local network as the target site.
                
                CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.
                
                Other info
                
                No known Anti-CSRF token \[anticsrf, CSRFToken, \_\_RequestVerificationToken, csrfmiddlewaretoken, authenticity\_token, OWASP\_CSRFTOKEN, anoncsrf, csrf\_token, \_csrf, \_csrfSecret, \_\_csrf\_magic, CSRF, \_token, \_csrf\_token, \_csrfToken\] was found in the following HTML form: \[Form 1: "birthdate" "password" "username" \].
                
                Request
                
                Request line and header section (269 bytes)
                
                    GET http://localhost:8001/register HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                    referer: http://localhost:8001
                
                Request body (0 bytes)
                
                Response
                
                Status line and header section (141 bytes)
                
                    HTTP/1.1 200 OK
                    content-type: text/html; charset=UTF-8
                    vary: Accept-Encoding
                    content-length: 3026
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                
                Response body (3026 bytes)
                
                    <!DOCTYPE html>
                    <html lang="en">
                    
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <title>User Registration</title>
                        <link href="/static/tailwind.css" rel="stylesheet"> <!-- Link to Tailwind CSS -->
                    </head>
                    
                    <body class="flex flex-col min-h-screen bg-gray-100 text-gray-900">
                      <main class="flex-grow">
                        <div class="container mx-auto p-4">
                            <div class="bg-white shadow-md rounded-lg p-6 mt-6 max-w-lg mx-auto">
                                <h1 class="text-2xl font-bold mb-4 text-center">Register</h1>
                                <form action="/register" method="POST">
                                    <div class="mb-4">
                                        <label for="username" class="block text-sm font-medium text-gray-700 font-bold">Email</label>
                                        <input type="email" id="username" name="username" placeholder="Enter your email" required class="mt-1 block w-full px-3 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                                    </div>
                                    <div class="mb-4">
                                        <label for="password" class="block text-sm font-medium text-gray-700 font-bold">Password</label>
                                        <input type="password" id="password" name="password" placeholder="Create a password" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                                    </div>
                                    <div class="mb-4">
                                        <label for="birthdate" class="block text-sm font-medium text-gray-700 font-bold">Birthdate</label>
                                        <input type="date" id="birthdate" name="birthdate" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                                    </div>
                                    <div class="mb-4">
                                        <label for="role" class="block text-sm font-medium text-gray-700 font-bold">Role</label>
                                        <select id="role" name="role" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                                            <option value="reserver">Reserver</option>
                                            <option value="administrator">Administrator</option>
                                        </select>
                                    </div>
                                    <div class="flex justify-between space-x-4">
                                        <button type="submit" class="inline-block bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 w-1/2">Register</button>
                                        <a href="/" class="inline-block bg-gray-500 text-white py-2 px-4 rounded hover:bg-gray-600 w-1/2 text-center">Cancel</a>
                                    </div>
                                </form>
                            </div>
                        </div>
                      </main>
                      <div id="footer-placeholder"></div>
                      <script src="/static/footer.js"></script>
                    </body>
                    
                    </html>
                
                Evidence
                
                    <form action="/register" method="POST">
                
                Solution
                
                Phase: Architecture and Design
                
                Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.
                
                For example, use anti-CSRF packages such as the OWASP CSRFGuard.
                
                Phase: Implementation
                
                Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.
                
                Phase: Architecture and Design
                
                Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).
                
                Note that this can be bypassed using XSS.
                
                Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.
                
                Note that this can be bypassed using XSS.
                
                Use the ESAPI Session Management control.
                
                This control includes a component for CSRF.
                
                Do not use the GET method for any request that triggers a state change.
                
                Phase: Implementation
                
                Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.
                
4.  ### Risk\=Low, Confidence\=High (1)
    
    1.  #### http://localhost:8001 (1)
        
        1.  ##### [ZAP is Out of Date](#alert-type-5) (1)
            
            1.  GET http://localhost:8001/login
                
                Alert tags
                
                *   [CWE-1104](https://cwe.mitre.org/data/definitions/1104.html)
                
                Alert description
                
                The version of ZAP you are using to test your app is out of date and is no longer being updated.
                
                The risk level is set based on how out of date your ZAP version is.
                
                Other info
                
                The latest version of ZAP is 2.17.0
                
                Request
                
                Request line and header section (266 bytes)
                
                    GET http://localhost:8001/login HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                    referer: http://localhost:8001
                
                Request body (0 bytes)
                
                Response
                
                Status line and header section (147 bytes)
                
                    HTTP/1.1 404 Not Found
                    content-type: text/plain; charset=UTF-8
                    vary: Accept-Encoding
                    content-length: 13
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                
                Response body (13 bytes)
                
                    404 Not Found
                
                Solution
                
                Download the latest version of ZAP from https://www.zaproxy.org/download/ and install it.
                
5.  ### Risk\=Low, Confidence\=Medium (2)
    
    1.  #### http://localhost:8001 (2)
        
        1.  ##### [Application Error Disclosure](#alert-type-3) (1)
            
            1.  POST http://localhost:8001/register
                
                Alert tags
                
                *   [WSTG-v42-ERRH-02](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/08-Testing_for_Error_Handling/02-Testing_for_Stack_Traces)
                *   [WSTG-v42-ERRH-01](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/08-Testing_for_Error_Handling/01-Testing_For_Improper_Error_Handling)
                *   [OWASP\_2021\_A05](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)
                *   POLICY\_QA\_STD =
                *   POLICY\_PENTEST =
                *   [CWE-550](https://cwe.mitre.org/data/definitions/550.html)
                *   [OWASP\_2017\_A06](https://owasp.org/www-project-top-ten/2017/A6_2017-Security_Misconfiguration.html)
                
                Alert description
                
                This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.
                
                Request
                
                Request line and header section (348 bytes)
                
                    POST http://localhost:8001/register HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                    content-type: application/x-www-form-urlencoded
                    referer: http://localhost:8001/register
                    content-length: 83
                
                Request body (83 bytes)
                
                    username=foo-bar%40example.com&password=ZAP&birthdate=2026-02-11&role=administrator
                
                Response
                
                Status line and header section (159 bytes)
                
                    HTTP/1.1 500 Internal Server Error
                    content-type: text/plain; charset=UTF-8
                    vary: Accept-Encoding
                    content-length: 25
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                
                Response body (25 bytes)
                
                    Error during registration
                
                Evidence
                
                    HTTP/1.1 500 Internal Server Error
                
                Solution
                
                Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.
                
        2.  ##### [X-Content-Type-Options Header Missing](#alert-type-4) (1)
            
            1.  GET http://localhost:8001/static/index.js
                
                Alert tags
                
                *   [CWE-693](https://cwe.mitre.org/data/definitions/693.html)
                *   [OWASP\_2021\_A05](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/)
                *   [OWASP\_2017\_A06](https://owasp.org/www-project-top-ten/2017/A6_2017-Security_Misconfiguration.html)
                *   POLICY\_QA\_STD =
                *   POLICY\_PENTEST =
                *   [SYSTEMIC](https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic)
                
                Alert description
                
                The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.
                
                Other info
                
                This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
                
                At "High" threshold this scan rule will not alert on client or server error responses.
                
                Request
                
                Request line and header section (276 bytes)
                
                    GET http://localhost:8001/static/index.js HTTP/1.1
                    host: localhost:8001
                    user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
                    pragma: no-cache
                    cache-control: no-cache
                    referer: http://localhost:8001
                
                Request body (0 bytes)
                
                Response
                
                Status line and header section (145 bytes)
                
                    HTTP/1.1 200 OK
                    content-type: text/javascript; charset=utf-8
                    vary: Accept-Encoding
                    date: Wed, 11 Feb 2026 17:09:34 GMT
                    content-length: 41
                
                Response body (41 bytes)
                
                    async function init() {
                        }
                    
                    init();
                
                Parameter
                
                    x-content-type-options
                
                Solution
                
                Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
                
                If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.
                

Appendix
--------

### Alert Types

This section contains additional information on the types of alerts in the report.

1.  #### Absence of Anti-CSRF Tokens
    
    Source
    
    raised by a passive scanner ([Absence of Anti-CSRF Tokens](https://www.zaproxy.org/docs/alerts/10202/))
    
    CWE ID
    
    [352](https://cwe.mitre.org/data/definitions/352.html)
    
    WASC ID
    
    9
    
    Reference
    
    1.  [https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site\_Request\_Forgery\_Prevention\_Cheat\_Sheet.html](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)
    2.  [https://cwe.mitre.org/data/definitions/352.html](https://cwe.mitre.org/data/definitions/352.html)
    
2.  #### Content Security Policy (CSP) Header Not Set
    
    Source
    
    raised by a passive scanner ([Content Security Policy (CSP) Header Not Set](https://www.zaproxy.org/docs/alerts/10038/))
    
    CWE ID
    
    [693](https://cwe.mitre.org/data/definitions/693.html)
    
    WASC ID
    
    15
    
    Reference
    
    1.  [https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP)
    2.  [https://cheatsheetseries.owasp.org/cheatsheets/Content\_Security\_Policy\_Cheat\_Sheet.html](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
    3.  [https://www.w3.org/TR/CSP/](https://www.w3.org/TR/CSP/)
    4.  [https://w3c.github.io/webappsec-csp/](https://w3c.github.io/webappsec-csp/)
    5.  [https://web.dev/articles/csp](https://web.dev/articles/csp)
    6.  [https://caniuse.com/#feat=contentsecuritypolicy](https://caniuse.com/#feat=contentsecuritypolicy)
    7.  [https://content-security-policy.com/](https://content-security-policy.com/)
    
3.  #### Missing Anti-clickjacking Header
    
    Source
    
    raised by a passive scanner ([Anti-clickjacking Header](https://www.zaproxy.org/docs/alerts/10020/))
    
    CWE ID
    
    [1021](https://cwe.mitre.org/data/definitions/1021.html)
    
    WASC ID
    
    15
    
    Reference
    
    1.  [https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options)
    
4.  #### Application Error Disclosure
    
    Source
    
    raised by a passive scanner ([Application Error Disclosure](https://www.zaproxy.org/docs/alerts/90022/))
    
    CWE ID
    
    [550](https://cwe.mitre.org/data/definitions/550.html)
    
    WASC ID
    
    13
    
5.  #### X-Content-Type-Options Header Missing
    
    Source
    
    raised by a passive scanner ([X-Content-Type-Options Header Missing](https://www.zaproxy.org/docs/alerts/10021/))
    
    CWE ID
    
    [693](https://cwe.mitre.org/data/definitions/693.html)
    
    WASC ID
    
    15
    
    Reference
    
    1.  [https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85)](https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85))
    2.  [https://owasp.org/www-community/Security\_Headers](https://owasp.org/www-community/Security_Headers)
    
6.  #### ZAP is Out of Date
    
    Source
    
    raised by a passive scanner ([ZAP is Out of Date](https://www.zaproxy.org/docs/alerts/10116/))
    
    CWE ID
    
    [1104](https://cwe.mitre.org/data/definitions/1104.html)
    
    WASC ID
    
    45
    
    Reference
    
    1.  [https://www.zaproxy.org/download/](https://www.zaproxy.org/download/)

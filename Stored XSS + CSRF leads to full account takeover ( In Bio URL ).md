# Stored XSS + CSRF leads to full account takeover ( In Bio URL )

## Affected URL
http://social.barracks.army/profile.php

## Vulnerability Type
Others

## Description
I would like to report a critical security vulnerability discovered in the Profile URL section of your web application. This issue allows an attacker to execute a stored cross-site scripting (XSS) attack and exploit Cross-Site Request Forgery (CSRF) to achieve full account takeover, putting user data and system security at risk.

## Impact
Full Account Takeover

## Steps To Reproduce
1. Login into domain http://social.barracks.army/
2. Go to edit profile and enter following payload in profile URL section &quot;&gt;&lt;/img&gt;&lt;script&gt;alert(document.cookie)&lt;/script&gt;
3. Now intercept the request in burp suite -> Right click on it -> "Engagement Tools" -> Generate CSRF POC
4. Save that file as ANYNAME.html and host it on any website.

Now when victim will open this file and click on submit ( or we can create POC with autosubmit too), his bio will updated with our XSS payload and attacker will get victim's cookie ( via webhook )

( Remote JAVASCRIPT EXECUTION )

## Remediation
Input Validation and Sanitization: CSRF Protection: Content Security Policy (CSP): Regular Security Testing: Security Awareness Training:

## CVSS
9.3

## Username
Null_traiger

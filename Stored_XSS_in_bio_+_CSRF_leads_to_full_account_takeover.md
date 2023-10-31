# Stored XSS in bio + CSRF leads to full account takeover

## Affected URL
http://social.barracks.army/profile.php

## Vulnerability Type
Others

## Description
The identified vulnerability is a combination of Stored Cross-Site Scripting (XSS) and Cross-Site Request Forgery (CSRF) affecting the user profiles within [Application Name/URL]. This vulnerability allows an attacker to execute malicious scripts within a victim user's session, potentially leading to a full account takeover.

## Impact
Full account takeover

## Steps To Reproduce
1. Login into domain http://social.barracks.army/
2. Go to edit profile and enter following payload in bio section &quot;&gt;&lt;script&gt;alert(document.cookie)&lt;/script&gt;
3. Now intercept the request in burp suite -> Right click on it -> "Engagement Tools" -> Generate CSRF POC
4. Save that file as ANYNAME.html and host it on any website.

Now when victim will open this file and click on submit ( or we can create POC with autosubmit too), his bio will updated with our XSS payload and attacker will get victim's cookie ( via webhook )

( Remote JAVASCRIPT EXECUTION )

## Remediation
Input Validation and Escaping: CSRF Protection:

## CVSS
9.3

## Username
Null_traiger

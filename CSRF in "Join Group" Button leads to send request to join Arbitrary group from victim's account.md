# CSRF in "Join Group" Button leads to send request to join Arbitrary group from victim's account

## Affected URL
http://social.barracks.army/all_groups.php

## Vulnerability Type
Cross-Site Request Forgery

## Description
Here, If a normal user want to join any group, he/she has to send a request to join that group.

Now for sending request, user needs to click on "Join Group" button from Page "all_groups.php" which has no CSRF protection So, Attacker can forcefully send request to join any group from victim's account

## Impact
Attacker can forcefully send request to join any group from victim's account also victim may feel trust issue towards website because he did not send any request to join group

## Steps To Reproduce
1. Login into your account at http://social.barracks.army/
2. Go to "All Groups" and there will be some group and you need to send request to join any group.
3. Click on "Join Group" button to send reuest.
4. Intercept that request in proxy like burp suite -> Right click on it -> "Engagement Tools" -> Generate CSRF POC
5. Save that file as ANYNAME.html and host it on any website.
6. Now when victim will open this file and click on submit ( or we can create POC with autosubmit too), the request will generate to join that group from victim's account

## Remediation
Implement CSRF protection in all POST request

## CVSS
4.6

## Username
Null_traiger

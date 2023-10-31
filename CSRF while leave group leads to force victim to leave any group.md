# CSRF while leave group leads to force victim to leave any group

## Affected URL
http://social.barracks.army/leave_group.php

## Vulnerability Type
Cross-Site Request Forgery

## Description
if you want to leave the group, you need to send a post request and you need to click on "leave group" That post request is vulnerable to CSRF

## Impact
Attacker force victim to leave any group

## Steps To Reproduce
CSRF while leave group leads to force victim to leave any group

## Steps to Reproduce:
1. Login into your account at http://social.barracks.army/
2. Go to "my_groups.php" and you will see groups in which , you are member
3. Now if you want to leave the group, you need to send a post request and you need to click on "leave group"
4. That post request has no csrf protection so you can force any victim to leave the group
5. Click on "leave group" in my_groups.php -> intercept the request in burp suite -> Right click on it -> "Engagement Tools" -> Generate CSRF POC
6. Save that file as ANYNAME.html and host it on any website.
7. Now when victim will open this file and click on submit ( or we can create POC with autosubmit too), so this request will force victim to leave group

## Remediation
Add CSRF token

## CVSS
3.5

## Username
Null_traiger

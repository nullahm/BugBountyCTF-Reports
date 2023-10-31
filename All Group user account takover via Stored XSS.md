# All Group user account takover via Stored XSS

## Affected URL
https://social.barracks.army/post_detail.php?post_id=7fc3d225-f786-4ac8-8c72-d29b80797ce2

## Vulnerability Type
Cross-Site Scripting

## Description
content= FILED is vulnerable to xss

## Impact
Ato of all users via stord xss , Cookie steling run javascript

## Steps To Reproduce
Create post with this payload : <script>alert(document.cookie)</script>

## Remediation
Add client side fielter

## CVSS
8.5

## Username
Null_traiger 2

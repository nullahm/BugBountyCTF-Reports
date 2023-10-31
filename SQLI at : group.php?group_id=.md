# SQLI at : https://social.barracks.army/group.php?group_id=

## Affected URL
https://social.barracks.army/group.php?group_id=

## Vulnerability Type
SQL Injection

## Description
SQL injection (SQLi) is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. This can allow an attacker to view data that they are not normally able to retrieve. This might include data that belongs to other users, or any other data that the application can access. In many cases, an attacker can modify or delete this data, causing persistent changes to the application's content or behavior.

## Impact
A successful SQL injection attack can result in unauthorized access to sensitive data, such as:
```
Passwords.
Credit card details.
Personal user information.
```
SQL injection attacks have been used in many high-profile data breaches over the years. These have caused reputational damage and regulatory fines. In some cases, an attacker can obtain a persistent backdoor into an organization's systems, leading to a long-term compromise that can go unnoticed for an extended period.

## Steps To Reproduce
1. login to account
2. go to this group URL : https://social.barracks.army/group.php?group_id=f4f3561a9eb2b83e2b96b715c287ae81
3. I applied SLEEP command to prove SQLI here is the POC : \<REDACTED\>

## Remediation
You can prevent most instances of SQL injection using parameterized queries instead of string concatenation within the query. These parameterized queries are also know as "prepared statements".

reference : https://portswigger.net/web-security/sql-injection#how-to-prevent-sql-injection

## CVSS
9.9

## Username
pratikpanchal

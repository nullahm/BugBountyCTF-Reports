# Database Sensitive Information Disclosure in "/docker-compose.yml"

## Affected URL
https://social.barracks.army/docker-compose.yml

## Vulnerability Type
Sensitive Data Exposure

## Description
Sensitive Information Disclosure (also known as Sensitive Data Exposure) happens when an application does not adequately protect sensitive information that may wind up being disclosed to parties that are not supposed to have access to it.

## Impact
The scale of impact from a Sensitive Information Disclosure event is limited only by the type of sensitive information disclosed and a malicious actor’s ability to leverage it.

For example, the fallout could be as minor as a local pathname being disclosed in a stack trace, allowing a malicious actor to improve their knowledge of the target’s implementation details, right through to a full-blown data leak involving millions of customers’ confidential data.

## Steps To Reproduce
GO to this direct URL : https://social.barracks.army/docker-compose.yml

- You will find database credentials there.
- MYSQL_ROOT_PASSWORD=\<REDACTED\> - MYSQL_DATABASE=\<REDACTED\> - MYSQL_USER=\<REDACTED\> - MYSQL_PASSWORD=\<REDACTED\>
- DONE

## Remediation
Do the following, at a minimum, and consult the references:

- Classify data processed, stored or transmitted by an application. Identify which data is sensitive according to privacy laws, regulatory requirements, or business needs.
- Apply controls as per the classification.
- Don’t store sensitive data unnecessarily. Discard it as soon as possible or use PCI DSS compliant tokenization or even truncation. Data that is not retained cannot be stolen.
- Make sure to encrypt all sensitive data at rest.
- Ensure up-to-date and strong standard algorithms, protocols, and keys are in place; use proper key management.
- Encrypt all data in transit with secure protocols such as TLS with perfect forward secrecy (PFS) ciphers, cipher prioritization by the server, and secure parameters. Enforce encryption using directives like HTTP Strict Transport Security (HSTS).
- Disable caching for response that contain sensitive data.
- Store passwords using strong adaptive and salted hashing functions with a work factor (delay factor), such as Argon2, scrypt, bcrypt or PBKDF2.
- Verify independently the effectiveness of configuration and settings.

## CVSS
6.3

## Username
pratikpanchal

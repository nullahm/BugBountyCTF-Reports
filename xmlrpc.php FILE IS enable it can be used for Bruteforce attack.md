# xmlrpc.php FILE IS enable it can be used for Bruteforce attack

## Affected URL
http://shop.barracks.army/xmlrpc.php

## Vulnerability Type
Others

## Description
The website http://shop.barracks.army/ has the xmlrpc.php file enabled and could thus be potentially used for such an attack against other victim hosts. WordPress that has xmlrpc.php enabled for pingbacks, trackbacks, etc.

## Impact
This method is also used for brute force attacks to steal the admin credentials and other important credentials

## Steps To Reproduce
1. go to http://shop.barracks.army/wp-json/wp/v2/users/ here we can find 2 users : dev dev and root
2. now go to http://shop.barracks.army/xmlrpc.php and intercept the request
3. send it to the intruder and change request method to post and put this `<methodCall> <methodName>wp.getUsersBlogs</methodName> <params> <param><value>dev dev</value></param> <param><value>pass</value></param> </params> </methodCall>`
4. here we can see that we have username and with xmlrpc we can do the no rate limit to get users password.

## Remediation
Disable the xmlrpc.php

## CVSS
6.5

## Username
test

# xss

## Affected URL
http://social.barracks.army/group.php?group_id=g1h2i3j4-k5l6-7890-g1h2-i3j4k5l67890

## Vulnerability Type
Cross-Site Scripting

## Description
go to the http://social.barracks.army/group.php?group_id=g1h2i3j4-k5l6-7890-g1h2-i3j4k5l67890 and in the content parameter type paylaod <image/src/onerror=prompt(document.cookie)> and it shows you cookie of user.

## Impact
cookie

## Steps To Reproduce
go to the http://social.barracks.army/group.php?group_id=g1h2i3j4-k5l6-7890-g1h2-i3j4k5l67890 and in the content parameter type paylaod `<image/src/onerror=prompt(document.cookie)>` and it shows you cookie of user.

## Remediation
block user input for special charactors and html tags

## CVSS
5

## Username
rakesh

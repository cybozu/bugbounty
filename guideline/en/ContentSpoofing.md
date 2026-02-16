Content Spoofing
====

## Vulnerability Overview
Content Spoofing is an attack where an attacker presents malicious content to users as if it were legitimate. Attackers use this technique to guide users to fake web sites or alter information.

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
A process will be identified as a vulnerability if the process allows content spoofing to cause breaches of confidentiality, integrity, or availability. 

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
The following cases are not identified as a vulnerability:
* An attacker exploiting text formatting or HTML e-mail to present a fake URL.
* An attacker exploiting a link to present a fake file name or extension.
* An attacker altering an organization name to pretend to belong to a different organization.
* An attacker injecting characters included in URL paths or parameters to display on an error or search screen.

Our products have the risk that some features might be exploited for content spoofing attacks. However, we intentionally make such features available because they are critical to the value of the products.  
If there is a case where content spoofing can lead to a severer attack, such as cross-site scripting, then the case will be identified as a vulnerability.

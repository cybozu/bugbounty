Cross Site Request Forgery(CSRF)
====

## Vulnerability Overview
Cross-Site Request Forgery (CSRF) is an attack that forces an end user to execute unwanted actions on a web application in which they are currently authenticated. CSRF attacks specifically target state changing requests. As the attacker has no way to see the response to the forged request, no data is stolen during these attacks. With a little help from social engineering (such as sending a link via email or chat), an attacker may trick the users of a web application into executing actions of the attacker's choosing. If the victim is a normal user, a successful CSRF attack can force the user to perform state changing requests like transferring funds, changing their email address, and so forth. If the victim has administrative permissions, CSRF can compromise the entire web application.

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
Processes that involve data modifications require protection against CSRF.

### Examples of APIs That Need Protection Against CSRF
* User login
* APIs for changing data on servers and user authentication

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
The following processes involve updating data on servers. However, since the damage from the attack can be difficult to predict, we do not identify these processes as vulnerability.

* Logout process
* APIs that modify data as a side effect of GET (example: marking notifications as read)
* APIs for modifying data to maintain UI state (example: opening and closing processes for folders) * Excludes settings related to access permissions

## References
The description of the "Vulnerability Overview" section is an excerpt from the following source:

[Cross-Site Request Forgery (CSRF)](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF))

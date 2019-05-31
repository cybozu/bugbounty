Sensitive Data Exposure
====

## Overview
This document summarizes information that is treated as vulnerability when a possible information leak may occur due to product specifications/defects.

## Is This Identified as a Vulnerability?
Yes.  
We identify cases in which authentication information and similar information are leaked as vulnerabilities. Cases in which other types of information are leaked will not be considered vulnerabilities.

### Information That Is Similar to Authentication Information
The following types of information are included:

* Information from which the presence of an account can be deduced
URL information that was only sent to specific persons (example: a URL that was sent to a user for a password reset, etc.)
* CSRF tokens (excluding cases in which users can use their own privileges to get a CSRF token for logged-in users)

## Points That Need Protection Against This Vulnerability (Scope)
Cases in which the following information may be potentially leaked due to product specifications or defects outputting the information to logs, e-mail headers, or HTTP headers will be handled as vulnerabilities:  

* Authentication information and similar information

In addition, cases in which processing related error messages (stack traces, etc.) are displayed on screens shall be similarly handled as vulnerabilities.

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
Cases in which the following information is leaked shall not be handled as a vulnerability as the information itself has been determined to not lead to an attack directly: However, this does not necessarily hold true to cases in which the specific attack method is clear.

* Local IP addresses in a data center
* Server banner information or information to software in use
* Unauthorized or unimplemented HTTP methods

### Sending Confidential Information by E-mail
For e-mail encryption, the two points of consideration are as follows:

1. Encrypting message bodies
2 Encrypting e-mail transmission routes

#### Encrypting message bodies

Comparison of implementation cases for other cloud services and other such services reveals that encrypting message bodies of system e-mails has not been widely used. As of 2016, we have no plans for implementing this encryption. Therefore, we do not identify non-encrypted cases as vulnerabilities.

#### Encrypting e-mail transmission routes

We are considering this as a known issue and are planning to handle the issue. However, we cannot force all customers to enable encryption for communication, and such a specification change is not possible. Therefore, we do not identify the fact that transmission routes are not encrypted as a vulnerability.

## References

* [OWASP Top 10 for 2013 A6 - Sensitive Data Exposure](http://owasptop10.googlecode.com/files/OWASP%20Top%2010%20-%202013.pdf)
* [Disclosed Information from Error Messages](https://www.ipa.go.jp/security/awareness/vendor/programmingv1/b09_03.html)

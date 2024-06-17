Leakage of Sensitive Information
====

## Overview
This document summarizes the types of information leakage which should be handled as vulnerabilities. The document is common and not limited to the case relating to product specifications/defects.

## Is This Identified as a Vulnerability?
Yes. We identify cases in which authentication information and similar information are leaked as vulnerabilities.
Cases in which other types of information are leaked will not be identified as vulnerabilities.

## Points That Need Protection Against This Vulnerability (Scope)
If product specifications or defects may cause the outside leakage of the following information written in logs, e-mail headers, or HTTP headers, such cases will be handled as vulnerabilities:


* Authentication information and similar information

Information that is similar to authentication information includes the following:
* Information from which the presence of an account can be deduced
* URL information that is sent to only specific persons (example: a URL that was sent to a user for a password reset, etc.)
* CSRF tokens (excluding cases in which users can use their own privileges to get a CSRF token for logged-in users)

In addition, in the case of processing related error messages (stack traces, etc.) displayed on screens, cases that we consider as confidential information shall be similarly handled as vulnerabilities.

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
Cases in which the following information is leaked shall not be handled as a vulnerability as the information itself has been determined to not lead to an attack directly:
However, this does not necessarily hold true to cases in which the specific attack method is clear.

* Local IP addresses in a data center
* Server banner information or information to software in use
* Unauthorized or unimplemented HTTP methods

### Sending Confidential Information by E-mail
For e-mail encryption, the two points of consideration are as follows:

1. Encrypting message bodies
2. Encrypting e-mail transmission routes

#### Encrypting message bodies
Comparison of implementation cases for other cloud services and other such services reveals that encrypting message bodies of system e-mails has not been widely used. We therefore have no plans for implementing this encryption. (as of 2019)  
Therefore, we do not identify non-encrypted cases as vulnerabilities.

#### Encrypting e-mail transmission routes
We have acknowledged this as a known issue.  
However, we cannot force all customers to enable encryption for communication, and such a specification change is not possible. Therefore, we do not identify the fact that transmission routes are not encrypted as a vulnerability.

### Regarding Vulnerabilities of Web Sites
Criteria to identify a vulnerability differ between Web Sites and products. 
Therefore, even if the administrator's user name or email address is leaked on the "Web Sites" in the following URL, we do not identified the leakage as a vulnerability.   
[https://cybozu.co.jp/en/company/products/bug-bounty/#web-site](https://cybozu.co.jp/en/company/products/bug-bounty/#web-site)

## References

* [OWASP Top Ten 2017 | A3:2017-Sensitive Data Exposure](https://owasp.org/www-project-top-ten/2017/A3_2017-Sensitive_Data_Exposure)

X-Frame-Options:SAMEORIGIN Output Defects
====
## Vulnerability Overview
If the X-Frame-Options: SAMEORIGIN response header is not provided for an API response, the response may be exploited by clickjacking.  
This document provides the identification policy for the X-Frame-Options: SAMEORIGIN output in API responses.

### What Is Clickjacking
> Some websites provide login functions that can only be used by logged-in users. If such functions can be used only with mouse operation, users may be forced to execute unintended functions by browsing and operating a crafted external site. Such a problem is called a "clickjacking vulnerability," and an attack that exploits the problem is called a "clickjacking attack".

(This is an abridged translation of some parts of the document at: https://www.ipa.go.jp/security/vuln/websecurity/clickjacking.html)

## Is This Identified as a Vulnerability?
Yes

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
### Regarding Vulnerabilities of Web Pages
Criteria to identify a vulnerability differ between Web pages and products.  
Therefore, even if `X-Frame-Options: SAMEORIGIN` is not provided for a response header on Web pages listed in the "Web Sites" of the following URL, we do not identified the leakage as a vulnerability.  
[https://cybozu.co.jp/products/bug-bounty/](https://cybozu.co.jp/products/bug-bounty/)

## Points That Need Protection Against This Vulnerability (Scope)
Processes in which clickjacking may lead to breaches of confidentiality, integrity, and availability.  
However, this does not apply to processes that are expected to have no impact.

## References
[Clickjacking](https://www.owasp.org/index.php/Clickjacking)  
[X-Frame-Options Response Header](https://developer.mozilla.org/ja/docs/Web/HTTP/X-Frame-Options)  

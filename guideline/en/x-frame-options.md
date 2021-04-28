X-Frame-Options:SAMEORIGIN Output Defects
====
## Vulnerability Overview
If the X-Frame-Options: SAMEORIGIN response header is not provided for an API response, the response may be exploited by clickjacking.  
This document provides the identification policy for the X-Frame-Options: SAMEORIGIN output in API responses.

### What Is Clickjacking
> Clickjacking is an attack technique that tricks users into clicking contents on a web page different from what the users perceives they are clicking on. Clicking on a seemingly innocuous web page from a malicious site may result in revealing user privacy information or forcing users to register information without their awareness.

(This is an abridged translation of some parts of the document at: https://www.ipa.go.jp/files/000026479.pdf)

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
Processes in which clickjacking may lead to breaches of confidentiality, integrity, and availability.  
However, this does not apply to processes that are expected to have no impact.
## References
[Clickjacking](https://www.owasp.org/index.php/Clickjacking)  
[X-Frame-Options Response Header](https://developer.mozilla.org/ja/docs/Web/HTTP/X-Frame-Options)  
[IPA Technical Watch: Reports on Clickjacking (Tricking Users into Disclosing Sensitive Information Without Their Awareness)](https://www.ipa.go.jp/about/technicalwatch/20130326.html)

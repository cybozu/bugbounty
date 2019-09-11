X-Frame-Options:SAMEORIGIN Output Defects
====
## Vulnerability Overview
If `X-Frame-Options: SAMEORIGIN` is not provided for a response header, the response may be exploited by clickjacking.  
This article describes the policy whether or not to identify a case regarding `X-Frame-Options: SAMEORIGIN` output in an API response.

### What Is Clickjacking
> Clickjacking is an attack technique that tricks users into clicking contents on a Web page different from what the users perceives they are clicking on. Clicking on a seemingly innocuous Web page from a malicious site may result in revealing user privacy information or forcing users to register information without their awareness.

(This is an abridged translation of some parts of the document at: https://www.ipa.go.jp/files/000026479.pdf)

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
Processes in which clickjacking may lead to breaches of confidentiality, integrity, or availability.  
However, this does not apply to processes that are expected to have no impact.

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
### Regarding Vulnerabilities of Web Pages
Criteria to identify a vulnerability differ between Web pages and products.  
Therefore, even if `X-Frame-Options: SAMEORIGIN` is not provided for a response header on Web pages listed in the "Home page" of the following URL, we do not identified the leakage as a vulnerability.  
[https://cybozu.co.jp/products/bug-bounty/](https://cybozu.co.jp/products/bug-bounty/)

## References
[Clickjacking](https://www.owasp.org/index.php/Clickjacking)  
[X-Frame-Options Response Header](https://developer.mozilla.org/ja/docs/Web/HTTP/X-Frame-Options)  
[IPA Technical Watch: Reports on Clickjacking (Tricking Users into Disclosing Sensitive Information Without Their Awareness)](https://www.ipa.go.jp/about/technicalwatch/20130326.html)

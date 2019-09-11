Open Redirect
===

## Vulnerability Overview
Open redirect is a vulnerability that causes a redirection to an unintended URL by specifying an arbitrary URL as a redirection target.  
This vulnerability enables attackers to redirect users to illegitimate Web sites by spoofing URLs of trusted Web sites.

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
If a URL that is not intended by our products can be specified as a redirection target after processing user's input, the case is identified as a vulnerability. 

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
Open redirect caused by rewriting a part of request header is not identified as a vulnerability.

## References
[How to make a legitimate redirection which can be trusted (1 of 3): "New security rule" in HTML5 format (4)](https://www.atmarkit.co.jp/ait/articles/1406/20/news007.html)

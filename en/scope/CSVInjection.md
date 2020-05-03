CSV Injection
====

## Vulnerability Overview

CSV Injection, also known as Formula Injection, occurs when websites embed untrusted input inside CSV files.  

When a spreadsheet program such as Microsoft Excel or LibreOffice Calc is used to open a CSV, any cells starting with ‘=’ will be interpreted by the software as a formula. Maliciously crafted formulas can be used for three key attacks:  

* Hijacking the user’s computer by exploiting vulnerabilities in the spreadsheet software, such as CVE-2014-3524
* Hijacking the user’s computer by exploiting the user’s tendency to ignore security warnings in spreadsheets that they downloaded from their own website  
* Exfiltrating contents from the spreadsheet, or other open spreadsheets.  

## Is This Identified as a Vulnerability?
No

## Reason This Is Not Identified as a Vulnerability
CSV Injection is not handled as a vulnerability for the Bug Bounty Program. The reasons are as follows.

* To prevent this vulnerability from manifesting, CSV data output from products must be modified. Specifically, if the entry of a cell begins with a symbol: '=', '+', or '-', the entry will have an additional single quotation mark (') at the beginning. However, in that case, CSV data cannot begin with a single quotation mark. We determined this solution to be unacceptable because the minus (-) sign in particular is frequently used.

* We asked Microsoft about Excel specifications and got the answer below:

> Microsoft determines this case is not a vulnerability because the reported behavior occurs only when macros are enabled by users. For more information on Microsoft's definition of vulnerabilities and their immutable laws of security, also see the following web site.
>
> [Definition of a "Security Vulnerability"](http://technet.microsoft.com/ja-jp/library/gg983510.aspx)  
> [Ten Immutable Laws of Security](https://technet.microsoft.com/ja-jp/library/gg983506.aspx#E1)  

## References

The description of the "Vulnerability Overview" section is an excerpt from the following source:

[CSV Injection](https://owasp.org/www-community/attacks/CSV_Injection)

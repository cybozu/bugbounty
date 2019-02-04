CSV Excel Macro Injection(CEMI)
====

## Vulnerability Overview

Many web applications allow users to download template files for settings such as user preferences.　 Many users may also choose to open CSV files in Excel, Libre Office, or Open Office. If web applications do not verify the contents of CSV files properly, entries in cells of the files may be executed as macros.  

CSV Excel Macro Injection is an attack technique that abuses the trust of users. "The trust of users" mentioned here refers to the following:  

1. Users trust sites in which contents are stored.
2. Users assume that their downloaded files are simple CSV files and that the files do not contain any functions or macros.

Therefore, users seldom heed warnings from Excel about possible malicious functions in downloaded files.

## Is This Identified as a Vulnerability?
No

## Reason This Is Not Identified as a Vulnerability

Cybozu has confirmed that some of such cases in other companies have been fixed.

> 90131 CSV Excel Macro Injection Vulnerability in export customer tickets Zendesk rewarded psychomantis with a $100 bounty for CSV Excel Macro Injection Vulnerability in export customer tickets. Zendesk resolved CSV Excel Macro Injection Vulnerability in export customer tickets that was submitted by psychomantis.  
> [CSV Excel Macro Injection Vulnerability in export customer tickets](https://hackerone.com/reports/90131)

To prevent this vulnerability from manifesting, CSV data output from products must be modified. Specifically, if the entry of a cell begins with a symbol: '=', '+', or '-', the entry will have an additional single quotation mark (') at the beginning. However, in that case, CSV data cannot begin with a single quotation mark. We determined this solution to be unacceptable because the minus (-) sign in particular is frequently used.

We asked Microsoft about Excel specifications and got the answer below:

> Microsoft determines this case is not a vulnerability because the reported behavior occurs only when macros are enabled by users. For more information on Microsoft's definition of vulnerabilities and their immutable laws of security, also see the following web site.
>
> [Definition of a "Security Vulnerability"](http://technet.microsoft.com/ja-jp/library/gg983510.aspx)
> [Ten Immutable Laws of Security](https://technet.microsoft.com/ja-jp/library/gg983506.aspx#E1)

In light of this, we have conclusively decided not to treat the CSV Excel Macro Injection issue as vulnerability.

## References

The description of the "Vulnerability Overview" section is an excerpt from the following source:

[CSV Excel Macro Injection](https://www.owasp.org/index.php/CSV_Excel_Macro_Injection)

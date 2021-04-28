PDF FormCalc Attack
====

## Vulnerability Overview

"PDF FormCalc Attack" is an attack technique that uses FormCalc, which is the operation language that was developed by Adobe. It was disclosed by Alexander Inführ at APPSEC EU 2015.  
[https://2015.appsec.eu/wp-content/uploads/2015/09/owasp-appseceu2015-infuhr.pdf](https://2015.appsec.eu/wp-content/uploads/2015/09/owasp-appseceu2015-infuhr.pdf)  
The key point of the attack is that using FormCalc can provide the ability to issue requests at the origin where PDF files were uploaded.  

By exploiting the ability, attackers can send requests with a victim's cookies or CSRF protection tokens, which means that by using the privileges of a victim viewing a malicious site, attackers can execute any code on a specific product.  

Users that meet any of the following conditions may be affected by the attack:

1. Using applications with a function for uploading PDF files  
2. Have Adobe PDF Reader Plugin enabled on Microsoft Internet Explorer or Mozilla Firefox

The issue in which send cross-origin requests can be sent (CVE-2014-8453) has been fixed by Adobe.  
Nevertheless, in Adobe's opinion, sending requests within the same origin is not regarded as vulnerability.  

> From our perspective, website owners must realize that PDF is active content, and serving user-uploaded/malicious PDFs from a non-throwaway domain is effectively an XSS (just like hosting an arbitrary/malicious HTML).

## Is This Identified as a Vulnerability?
No

## Reason This Is Not Identified as a Vulnerability
For this issue, storing user content in a Sandbox Domain can reduce some degree of risk.   
We recognize that many companies offering notable services, including Google, have implemented the above solution.  
On the other hand, a specification of Cybozu products is that user uploaded content is stored in the same origin as the one running the programs.  
For this specification to be amended, incompatible specifications must be modified. Such modification will cause a great burden on users.  
Customers using the on-premise version in particular will encounter difficulties in configuring a different origin for storing user content.  
In conclusion, given that the reproduced conditions are limited (meaning that using third party products is the prerequisite of the attack), we developed our own policy to handle this case as a restriction.  

You can find information about restrictions on the following web page:  
* [cybozu.com Restrictions](https://www.cybozu.com/jp/service/restrictions.html)  
* [Understanding Usage of Adobe Acrobat Reader Plugin (2016/11/11)](https://cs.cybozu.co.jp/2016/006288.html)  

When you are using Microsoft Internet Explorer or Mozilla Firefox, we recommended that you disable the Acrobat Reader Plugin if it is enabled. For checking and configuring your settings, see the following web pages:  

* [Manage add-ons in Internet Explorer 11](https://support.microsoft.com/ja-jp/help/17447/windows-internet-explorer-11-manage-add-ons)  
* [Use plugins to play audio, video, games and more](https://support.mozilla.org/ja/kb/use-plugins-play-audio-video-games)

## References
* [JVNTA#94087669 Stealing Information with Crafted PDF Files](https://jvn.jp/ta/JVNTA94087669/)
* [Hack Patch!-PDF Special Features (for FormCalc)](https://shhnjk.blogspot.jp/2016/10/pdfformcalc.html)  
* [InsertScript-Multiple PDF Vulnerabilities - Text and Pictures on Steroids](http://insert-script.blogspot.jp/2014/12/multiple-pdf-vulnerabilites-text-and.html)

## Trademarks of Other Companies:
All company names, system names, and product names appearing in this document are registered trademarks or trademarks of their respective holders.  
Trademark symbols, '™' and '®', are not indicated in this document.  

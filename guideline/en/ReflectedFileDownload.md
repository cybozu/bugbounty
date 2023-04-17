Reflected File Download
====

## Vulnerability Overview
Reflected File Download (RFD) is an attack technique that was presented by Oren Hafif at Black Hat Europe 2014. [https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector.pdf](https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector.pdf)

RFD allows the attacker to execute commands on the OS level of the victim's client computer.  
In an RFD attack, the attacker prepares a malicious link and then directs a user on a trusted domain to the malicious link for downloading a malicious file.  
When the victim opens the downloaded file from the trusted domain, OS commands (or scripts) that were prepared by the attacker are executed on the victim's computer.  

Oren Hafif says that there are three requirements for a successful RFD attack:  

1. Reflected – Some user input is being "reflected" to the response content. (This is used to inject shell commands.)
2. Filename – The URL of the vulnerable site or API is permissive, and accepts additional input. (This is often the case, and is used by attackers to set the extension of the file to an executable extension.)
3. Download – The content of the response is downloaded as a file via the Web browser. (The browser then sets the filename by adding '(2)' to the name.)

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
The points that meet all RFD requirements described in the "Vulnerability Overview" section are identified as RFD vulnerability.  
However, RFD vulnerabilities in which file names and extensions can be tampered with during download will not be added to the bug bounty program hereafter.  
In this case, the information may be publicly published with the assumption that the vulnerability will not be fixed.  
Even in circumstances where extensions and file names can be overwritten, since the direct impact does not increase, we have assessed that the impact will be of low significance.  
For Cybozu product users, a feature of our products is the ability to upload any files.  
For non-Cybozu product users, some method is required for uploading a specific file through phishing and other techniques.  
In addition, RFD vulnerabilities that can overwrite the contents of a file during download will be identified as new vulnerabilities.  

Certain cases may be handled as similar cases of a vulnerability. For example, different processes that use the same logic expose a vulnerability in several places.  

For more information, see ["Cybozu Bug Bounty Program Rulebook"](https://github.com/cybozu/bugbounty/blob/master/rulebook/en/rulebook.md).  

## References

The description of requirements for a successful RFD attack is an excerpt from the following source:
* [Reflected File Download a New Web Attack Vector](https://www.blackhat.com/docs/eu-14/materials/eu-14-Hafif-Reflected-File-Download-A-New-Web-Attack-Vector-wp.pdf)

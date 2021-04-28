# Cross Site Port Attack (XSPA)

## Vulnerability Overview
Cross site port attack (XSPA) is a technique that attackers send a forgery request to exploit a vulnerable Web application for a springboard attack.  
Their attacking targets vary such as external Internet connection servers, internal network devices, and servers themselves where Web applications are running.  
Attackers can identify the availability (such as port status and banner information) of the target by analyzing its response.  

## Is This Identified as a Vulnerability?
No

## Reason This Is Not Identified as a Vulnerability
XSPA using an error message displayed by the Cybozu product/service is not identified as a vulnerability. This is because "any host", "IP address", or "port number" can be specified in features so that displayed error messages with the features help users resolve their misconfiguration. The elapsed time to display and the contents of error messages will vary depending on the status of connection targets, and this is a expected behavior based on specifications.

## References
[XSPA : Cross Site Port Attack - INDIATRIKS](http://indiatriks.blogspot.com/2012/07/xspa-cross-site-port-attack.html)

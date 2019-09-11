# Denial of Service (Dos) Requiring a Large Amount of Data or Requests

## Vulnerability Overview
Attackers generate an excess load on network devices or servers running products or exploit vulnerabilities on the devices or servers, in order to cause the products to fail or slow down.

## Is This Identified as a Vulnerability?
No

## Prohibitions
It is prohibited to send a large amount of data or requests to a verification environment for the purpose of discovering vulnerabilities.
If a penetration tester interferes with our environments, we may take measures such as blocking their access to the environments without any prior warning.

## Supplementary Information
### Denial of Service (Dos) Not Requiring a Large Amount of Data or Requests
A behavior that does not require a large amount of data or requests and also can compromise the availability of Cloud Services may be identified as a vulnerability.
Specific Cloud Services are listed on the following page as applicable Products and Services:  
https://cybozu.co.jp/products/bug-bounty/en/

The following behaviors are not identified as a vulnerability because the impact is expected to be minor:
* The impact is limited to packaged products.
* There is no impact on other domains.

These are not applied when the vulnerability can be exploited not only for DoS attacks but also for causing other damage, such as buffer overflow, on target components.

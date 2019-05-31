Denial of Service (DoS)
====

## Vulnerability Overview
Attackers generate an excess load on network devices or servers running products or exploit vulnerabilities on the devices or servers in order to cause the products to fail or slow down.

## Is This Identified as a Vulnerability?
Yes

## Points That Need Protection Against This Vulnerability (Scope)
Behaviors that can compromise the availability of Cloud Services.  
Specific Cloud Services are listed on the following page as applicable Products and Services:  
https://cybozu.co.jp/products/bug-bounty/en/

## Exceptions (Cases Where This Is Not Identified as a Vulnerability)
The following behaviors are not identified as a vulnerability because the impact is expected to be minor:
* The impact is limited to packaged products.
* There is no impact on other domains.

These are not applied when the vulnerability can be exploited not only for DoS attacks but also for causing other damage, such as buffer overflow, on target components.

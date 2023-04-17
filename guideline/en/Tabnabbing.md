Tabnabbing
====

## Vulnerability Overview
"Tabnabbing" is a phishing technique that was announced by Aza Raskin in 2010.  
[http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/](http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/)

The Tabnabbing attack technique uses scripts to rewrite a page on an inactive tab to a malicious page (example: a fake page that looks like a real service login screen). When a user goes to the tab, the malicious page steals confidential information (example: login information). If one or both of the following conditions are met, the attack is successful.

- A link with the `target="_blank"` attribute specified exists in an attacked site
- The `window.open()` description exists in an attacked site

## Is This Identified as a Vulnerability?
No

## Reason This Is Not Identified as a Vulnerability

We have adopted the policy of not identifying "Tabnabbing" attacks as a vulnerability due to the following reasons:

- Solutions that use `rel="noopener"` and other attributes are not supported by some browsers, so not all browsers can be fully protected against the attack.
[http://caniuse.com/#feat=rel-noopener](http://caniuse.com/#feat=rel-noopener)
- Since there are a huge number of links in existing products, modifying all links would be very difficult.
- We have determined that the impact of the attack is limited and the risk is acceptable.

For reference, Google indicates a policy of excluding this case (phishing by navigating browser tabs) from rewards.
[https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs](https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs)

## References

* [Tabnabbing: A New Type of Phishing Attack](http://www.azarask.in/blog/post/a-new-type-of-phishing-attack/)
* [Phishing by navigating browser tabs](https://bughunters.google.com/learn/invalid-reports/web-platform/navigation/5825028803002368/phishing-by-navigating-browser-tabs)

## Copyrights and Trademarks of Other Companies

All company names, system names, and product names appearing in this document are registered trademarks or trademarks of their respective holders.  
Trademark symbols, '™' and '®', are not indicated in this document

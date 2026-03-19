# Base Guidelines

## About the Base Guidelines

The Base Guidelines outline the basic quality standards for vulnerability reports submitted to Cybozu’s Bug Bounty Program.
In the event of a conflict between the Base Guidelines and guidelines on other pages covering specific vulnerability types, the Base Guidelines take precedence.

Vulnerability reports deemed by Cybozu to fall into one of the categories below are ineligible for vulnerability identification, regardless of risk level. 

### 1. Reports from which risk cannot be appropriately identified

Examples:

- Speculative reports about theoretical vulnerabilities without PoC code or reproduction steps
- Reports with general descriptions of common attack methods without product-specific operational steps (e.g. specific screen or button actions)
- Reports on issues which are deemed to have no substantial impact on system safety
- Reports with unclear procedures that make it difficult to verify the vulnerability

### 2. Reports about deviations from security best practices that do not present an imminent risk

Examples:

- Reports simply identifying the possibility of brute force attacks on passwords or tokens
- Reports about missing security headers (e.g., `Content-Security-Policy`, `X-Frame-Options`)
- Reports about missing “Secure” attributes in non-essential cookies
- Reports about domains that have not set up SPF, DMARC, and DKIM

### 3. Reports that require improbable actions or scenarios relative to the claimed risk

Examples of improbable actions or scenarios:

- The attacker sharing the victim's device or account
- The victim intentionally disabling the browser's security settings
- The victim executing JavaScript or arbitrary scripts using developer tools or similar tools
- The victim intentionally performing operations outside normal use

### 4. Reports about risks accepted as part of the product specifications

Copyright (C) Cybozu, Inc

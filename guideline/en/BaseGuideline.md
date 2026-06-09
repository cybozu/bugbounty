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

### 5. Reports without an attached PoC-video that meets the requirements below

A vulnerability report submitted to our Bug Bounty Program must not only include a text description of the procedure for reproducing the vulnerability, but also a video (hereafter referred to as a “PoC-video”) showing the actual vulnerability being reproduced.
If a report is submitted without a PoC-video attachment that meets the requirements below, the report will be deemed ineligible.

#### 5.1 Video specifications
- Format: .mp4 or .webm
- Language: The display language of the testing environment (OS, browser) and services must be set to “Japanese” or “English”

#### 5.2 Video content
- The video must be one, continuous series of footage that has not been cut, trimmed, sped up, or edited to blur certain areas of the footage (including passwords, etc.) with pixelation
- The video must clearly show the browser address bar (URL bar) at all times
- The footage must be contained within a single video and must show the entire vulnerability reproduction process, starting from the login screen or initial state and ending with a successful attack and real harm

#### 5.3 Other important information
- The PoC-video must be uploaded directly to the attachment field in the report submission form. Uploading the video to an external service, such as a video sharing service, file transfer service, or cloud storage service, and pasting the video link into the body text of the submission form is strictly prohibited
- If the PoC-video shows evidence of being generated, altered or tampered with using AI or other means, the report will be deemed ineligible
- If a report is submitted through our report form with a video file but without a text description of the reproduction procedure, the report will be deemed ineligible. Make sure to include both text instructions and a PoC-video in the same submission

Copyright (C) Cybozu, Inc

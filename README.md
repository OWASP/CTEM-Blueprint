OWASP CTEM Top 10
Continuous Threat Exposure Patterns in Modern Applications
Version 0.1 – Draft (Incubator)

Executive Summary
The OWASP CTEM Top 10 identifies the most common and impactful continuous exposure patterns observed in modern applications, particularly in Retail, Banking, and FinTech ecosystems where automated attacks, fraud, and abuse are persistent.
Unlike traditional vulnerability lists, the CTEM Top 10 focuses on validated exploitability and continuous exposure, not theoretical weaknesses.
The goal is to help organizations:
    • Continuously measure real-world exposure
    • Validate whether security controls actually work
    • Detect regression and exposure drift
    • Prioritize risk based on exploitability, not CVSS alone
This document complements existing OWASP projects such as the OWASP Top 10 and OWASP API Security Top 10 by operationalizing exposure through continuous validation.

Methodology
The CTEM Top 10 is derived from:
    • Continuous Threat Exposure Management (CTEM) principles
    • Observed attack and abuse patterns in real-world environments
    • Mapping to OWASP Top 10 and API Security Top 10
    • Exposure validation through adversary emulation
    • Industry observations across Retail, Banking, and FinTech platforms
Each category represents a continuous exposure pattern, not a single vulnerability.

CTEM-01: Broken Authentication & Account Takeover Exposure
Mapped OWASP: A2 – Broken Authentication
Description
Authentication controls fail under realistic attacker behaviour, enabling account takeover through credential stuffing, token replay, and session misuse.
Common Attack Patterns
    • Account Takeover (ATO)
    • Credential stuffing
    • Automated password brute force
    • Session/token replay
Why This Exposure Persists
    • Token lifecycle weaknesses
    • Refresh tokens not invalidated
    • Authentication validated only periodically
    • Lack of automation detection
Continuous Validation
    • Token replay simulation
    • Credential stuffing emulation
    • Session fixation and hijack testing
    • Authentication abuse under automated behaviour

CTEM-02: Broken Authorization / IDOR Exposure
Mapped OWASP: A5 – Broken Access Control
Description
Authorization controls fail across object or tenant boundaries, allowing horizontal or vertical privilege escalation.
Continuous Validation
    • Cross-user access testing
    • IDOR emulation
    • Token scope abuse validation

CTEM-03: Excessive Attack Surface Exposure
Mapped OWASP: A5, A9
Description
Unused, undocumented, or legacy endpoints remain exposed and exploitable.
Continuous Validation
    • Endpoint discovery
    • Shadow API detection
    • Exposure drift monitoring

CTEM-04: Security Control Bypass After Change
Mapped OWASP: A5, A8
Description
Security controls degrade or fail after deployments, configuration changes, or refactoring.
Continuous Validation
    • Replay of validated attack paths in CI/CD
    • Control effectiveness verification

CTEM-05: Automation & Bot Abuse Exposure
Mapped OWASP: A2, A4
Description
Applications fail to detect and mitigate automated abuse, including credential stuffing, scraping, and fraud automation.
Common Attack Patterns
    • Credential stuffing
    • Web scraping
    • Inventory hoarding / scalping
    • Card cracking / carding
Continuous Validation
    • Automated login abuse simulation
    • Scraping behavior emulation
    • Fraud automation pattern testing

CTEM-06: API Trust Boundary Exposure
Mapped OWASP: API1, API2, API5
Description
Implicit trust between APIs or services allows lateral movement and privilege escalation.
Continuous Validation
    • Cross-service authorization testing
    • Token scope misuse validation

CTEM-07: Business Logic Abuse Exposure
Mapped OWASP: A4 – Insecure Design
Description
Application logic can be abused through workflow manipulation not detected by vulnerability scanners.
Continuous Validation
    • Abuse-case simulation
    • Sequence and workflow manipulation testing

CTEM-08: Third-Party & Supply Chain Exposure
Mapped OWASP: A6, A8
Description
Exposure arises from dependencies, SDKs, payment processors, or external integrations.
Continuous Validation
    • Attack chain validation
    • Exploitability assessment beyond CVSS

CTEM-09: Detection & Response Validation Gaps
Mapped OWASP: A9 – Logging & Monitoring Failures
Description
Attacks succeed without triggering detection, alerting, or response.
Continuous Validation
    • Attack-with-visibility testing
    • Alert accuracy and latency validation

CTEM-10: Exposure Drift
Mapped OWASP: All
Description
Previously remediated exposure reappears due to code, configuration, or environmental drift.
Continuous Validation
    • Continuous replay of known attack paths
    • Regression exposure detection
    • Exposure trend tracking

Automation & Fraud Exposure Coverage
The CTEM Top 10 addresses continuous exposure related to:
    • Account Takeover (ATO)
    • Credential stuffing
    • Web scraping
    • Inventory scalping and hoarding
    • Card cracking and carding
    • Automated fraud workflows
These are treated as validated exposure scenarios, not standalone fraud categories.

Defensive Capability Validation (Automation-Aware)
CTEM evaluates whether defensive mechanisms effectively mitigate automated abuse, including:
    • Continuous verification of client authenticity
    • Detection of automated behavior
    • Real-time mitigation effectiveness
    • Increased attack cost mechanisms
    • Behavioral anomaly detection
Evaluation is functional and vendor-neutral.

Role of AI / LLM (Bounded Use)
LLMs may assist with:
    • Threat hypothesis generation
    • Exposure reasoning
    • Security signal summarisation
    • Developer remediation guidance
LLMs do not:
    • Execute attacks
    • Make enforcement decisions
    • Automatically remediate vulnerabilities
Human validation remains required.

# Introduction to CTEM

**Status:** Q1 foundation draft · **Audience:** application, API, mobile, cloud, and AI security practitioners

## Background

Security reviews, automated vulnerability scans, and penetration tests provide valuable observations but often represent a single moment in time. Exposure is dynamic: routes and identities change, services gain access, new code introduces assumptions, and compensating controls can regress. The same technical weakness can carry different operational consequences depending on business importance, actual reachability, and control effectiveness.

**Continuous Threat Exposure Management (CTEM)** is the practice of using repeatable context gathering, discovery, validation, prioritization, and action to reduce meaningful exposure over time. This Blueprint offers a vendor-neutral approach focused on software and digitally delivered services.

## Intended outcomes

- Know **which services, data, processes, and boundaries** are being assessed.
- Translate security observations into **testable exposure hypotheses**.
- Evaluate findings and controls through **authorized, non-destructive validation**.
- Make transparent **risk-treatment decisions**, including confidence and unknowns.
- Verify that a change **reduced exposure** and repeat assessments when conditions change.
- Support consistent communication between engineering, security and business owners.

CTEM is **not** a replacement for asset inventory, secure design, SAST, DAST, SCA, pen testing, incident response, or risk management. It connects their outputs into a recurring operational feedback loop.

## Conceptual example: a retail checkout flow

A release exposes an unexpected API route that writes to a cart. Discovery flags the change. During validation, the team examines the documented route, authorization expectations, current edge policy, and permitted test evidence in staging. The findings are recorded with confidence and limitations; the business and technical owners select treatment, implement it, and repeat a scoped regression check. A suspected weakness becomes a documented, actionable exposure decision.

Equivalent concepts apply to cross-account banking APIs, mobile-to-backend token handling, and an AI assistant that can invoke privileged tools.

## Technology domains

**Web:** login, session handling, browser workflows and business logic.

**API:** object/function authorization, token boundaries, version inventory and data exposure.

**Mobile:** client/API trust boundaries, deep links, token storage and platform integrity controls.

**AI/LLM:** prompts and retrieved content, data access, tool permissions, agent workflows and monitoring.

Shared infrastructure, edge controls, dependencies, identity, CI/CD and logging form the broader context. See [scope](scope.md).

## The method

This Q1 framework uses **Scope → Discover → Validate → Prioritize → Mobilize**, with continuous reassessment. See [framework](ctem-framework.md) and [lifecycle](ctem-5-phase-lifecycle.md).

## Evidence and ethical use

Validation must be specifically approved. Results should include the subject, time, environment, test preconditions, observations, expected controls, uncertainty and responsible owner. AI-generated summaries require human corroboration. No live testing of third-party systems is authorized by this project.

## Related work

The Blueprint operationalizes existing OWASP risk categories and security testing guidance rather than replacing them. It is a working draft open to review, not a Foundation-approved normative standard.

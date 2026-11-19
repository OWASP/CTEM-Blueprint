# CTEM Blueprint — Scope and Boundaries

**Status:** Q1 draft · Applicable to **web, API, mobile, and AI/LLM-enabled** application systems.

## Scope statement

The Blueprint provides **methodology, evidence expectations, conceptual architecture and governance** for continuous application-oriented exposure management. It is not a penetration-testing authorization, turnkey bot mitigation platform, compliance certification, or substitute for OWASP domain-specific projects.

## Included environments

| Domain | Representative surfaces | Candidate exposure questions |
|---|---|---|
| Web | Login, session handling, payment/cart flows, browser routes | Are authorization and abuse controls effective after change? |
| API | Public/internal APIs, identity and tenant boundaries, versions | Are access checks enforced on each object/function? |
| Mobile | Apps, platform services, API calls, token/session lifecycle | Can client assumptions lead to backend exposure? |
| AI/LLM | Assistants, retrieval, prompts, models, tools and agents | Can untrusted content affect privileges or sensitive data? |
| Shared | Edge/CDN/WAF, load balancers, CI/CD, logging, IAM, dependencies | Are controls consistent across deployments and environments? |

## Included work

- Service context, ownership, dependencies and criticality.
- Candidate exposure discovery through approved sources.
- Threat hypotheses and *scoped, authorized* validation.
- Evidence recording, decision tracking, remediation verification and drift monitoring.
- High-level CI/CD and edge protection integration concepts.
- Domain mapping to existing OWASP resources, in future quarters.
- Human-reviewed assistance from AI/LLM tools.

## Excluded work in Q1

- Final CTEM Top 10 category selection, ranking or risk statistics.
- Production-grade edge/client fingerprinting or anti-bot enforcement.
- Detailed attack or adversary-emulation playbooks.
- Automated exploit chains, unsupervised testing, credential stuffing or card testing on real services.
- A mandatory universal numerical risk formula.
- Working Jenkins/GitLab/GitHub testing pipelines or deployed dashboards.
- Vendor-specific purchasing guidance, endorsements or proprietary implementations.
- Unapproved testing or publication of private security data.

These may be considered as scoped, safe future contributions only where appropriate.

## Authorization requirements

Before any validation activity, the assessment owner must agree:

1. **In-scope assets and accounts**, with authoritative approval.
2. **Permitted test types, time and volume**, plus relevant change/incident controls.
3. **Prohibited actions** and stop conditions.
4. **Data protection measures**, retention and reporting contacts.
5. **Who can accept risk and verify closure**.

For Q1 diagrams and examples, use fictitious assets and synthetic data only.

## Framework success criteria

Documentation is usable if a reader can identify scope, evidence requirements, decision owners, the repeatable phases, and the difference between a potential finding and validated exposure.

Q1 completion does **not** require live traffic inspection, production agent deployment, a completed Top 10, or test automation. See [Q1 checklist](q1-completion-checklist.md).

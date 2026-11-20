# OWASP CTEM Blueprint

**Continuous Threat Exposure Management for Web, API, Mobile, and AI/LLM Security**

> **Status:** Quarter 1 foundation documentation — working draft pending leader/community review. This is not a published CTEM standard, certified test suite, or endorsement of any product.

The **OWASP CTEM Blueprint** is an open, vendor-neutral methodology for continuously identifying, validating, prioritizing and reducing security exposure. It focuses on whether real conditions and security controls create meaningful exposure in a defined business context—not merely on the number of scanner findings.

## Who is it for?

AppSec, API and mobile security teams, AI security practitioners, cloud security engineers, defenders, development teams, and business risk owners.

## Why does it exist?

An alert can indicate a possible weakness without showing that it can cause harm in the assessed environment. Conversely, weaknesses in authorization, workflows, identity, third-party services, or security configuration can combine into an exploitable path. Security posture can change after every release. CTEM connects discovery to scoped evidence, actionable decisions, and verification after change.

## The Q1 lifecycle

**Scope → Discover → Validate → Prioritize → Mobilize → reassess**

1. **Scope:** agree what matters, who owns it and where tests are authorized.
2. **Discover:** collect potential exposure hypotheses, dependencies and control gaps.
3. **Validate:** safely assess evidence and the effectiveness of relevant controls.
4. **Prioritize:** decide treatment order based on impact, evidence, urgency and uncertainty.
5. **Mobilize:** assign remediation, mitigation or acceptance; then retest and feed back.

This is the Blueprint’s proposed Q1 order. Emergency containment can occur at any phase; tests do not have to prove exploitability before urgent defensive action.

## Quarter 1 documentation index

| Topic | Document |
|---|---|
| Overview and intended users | [Introduction](docs/introduction.md) |
| Concepts, responsibilities and evidence | [CTEM framework](docs/ctem-framework.md) |
| Phase-by-phase guidance | [Five-phase lifecycle](docs/ctem-5-phase-lifecycle.md) |
| Web, API, Mobile and AI boundaries | [Scope](docs/scope.md) |
| Human-supervised AI assistance | [Responsible AI use](docs/responsible-ai-use.md) |
| Vocabulary | [Glossary](docs/glossary.md) |
| System-level conceptual interactions | [CTEM reference architecture](architecture/ctem-reference-architecture.md) |
| CI/CD integration concept | [CI/CD architecture](architecture/ctem-ci-cd-architecture.md) |
| Quarterly plan | [Roadmap](ROADMAP.md) |
| Collaboration rules (proposed for adoption) | [Governance](GOVERNANCE.md) |
| Contribution process | [Contributing](CONTRIBUTING.md) |
| Conduct and reporting | [Code of Conduct](CODE_OF_CONDUCT.md) |

[Q1 acceptance and review checklist](docs/q1-completion-checklist.md) · [Q1 planning meeting notes](meetings/2026-10-10-q1-planning.md)

## Relationship to other OWASP projects

This Blueprint complements the [OWASP Top 10](https://owasp.org/www-project-top-ten/), [API Security](https://owasp.org/www-project-api-security/), [Mobile Application Security](https://owasp.org/www-project-mobile-app-security/), [GenAI Security](https://genai.owasp.org/), and [Automated Threats to Web Applications](https://owasp.org/www-project-automated-threats-to-web-applications/). These sources identify risk areas, testing guidance, or abuse patterns. The Blueprint proposes a repeatable method for validating and managing actual exposure, not a competing taxonomy.

**Q1 is documentation-only:** proposals for a CTEM Top 10, executable playbooks, edge mitigation tools, dashboards, and working CI/CD integrations are **later-quarter deliverables**. Existing repository material in those folders may be exploratory placeholders, not shipped capabilities.

## Safety and accountability

Tests require written authorization, defined scope, synthetic accounts/data where practical, bounded traffic, stop conditions and reviewable evidence. A finding is not necessarily an exploitable exposure, and a failed test does not prove safety. LLM output may assist a reviewer but is not evidence by itself.

## Contributing and licensing

Contributions are welcome from everyone; OWASP project leadership has separate membership obligations. See [CONTRIBUTING.md](CONTRIBUTING.md), [GOVERNANCE.md](GOVERNANCE.md), [SECURITY.md](SECURITY.md), and the [OWASP Code of Conduct](https://owasp.org/www-policy/operational/code-of-conduct/).

Source code: [Apache License 2.0](LICENSE). Original documentation: [CC BY-SA 4.0](LICENSE-DOCS.md), subject to separately identified third-party licenses.

**Project milestones and approval status must be verified on the official project page and through the repository review process.**

# OWASP CTEM Blueprint — Framework

**Version:** 0.1 Q1 working draft · **Status:** Proposed, subject to project-leader/community review

## Purpose

Establish a repeatable, practical process for evaluating **what is exposed, why it matters, whether controls work, and how exposure changes over time** across web, API, mobile and AI/LLM systems. This is a methodology, not a certification or vulnerability scoring standard.

## Principles

1. **Business context before severity.** Define affected services, owners, data, identities and expected harm.
2. **Discovery is a hypothesis.** A scanner hit or intelligence report alone does not prove exposure or exploitability.
3. **Authorized validation.** Use approved environments, test identities, non-destructive checks, documented limits and stop conditions.
4. **Controls matter.** Observe whether preventive, detective and response controls function for the defined scenario.
5. **Confidence is explicit.** Differentiate confirmed observations, partially supported findings, unverified hypotheses and unknown conditions.
6. **Decisions are accountable.** A named risk/technical owner approves remediation, mitigation, exception or escalation.
7. **Feedback is continuous.** Repeat relevant assessment after releases, changes, new findings or deteriorating controls.
8. **Open and vendor-neutral.** Open examples and interchangeable inputs; no proprietary service required.

## Five phases

| Phase | Questions | Minimum outcome |
|---|---|---|
| **1. Scope** | What assets and processes matter? Which tests are authorized? | Service/asset inventory, criticality, boundaries, owners and safeguards |
| **2. Discover** | Which weaknesses, exposures, control gaps or attack paths may apply? | Candidate hypotheses linked to assets and risk sources |
| **3. Validate** | What is observed and how effective are the controls? | Evidence, environment and time, test limits, confidence and outcome |
| **4. Prioritize** | What harm is plausible, how urgent is action and what remains unknown? | Decision rationale, treatment order, risk owner and due date |
| **5. Mobilize** | Who will change what, when will controls be retested? | Fix/mitigate/accept/escalate record, tracking and reassessment trigger |

The order is this **Blueprint's proposed adaptation**. Immediate containment and preliminary triage can take place before formal validation when justified by risk.

See [the detailed lifecycle](ctem-5-phase-lifecycle.md).

## Minimum exposure record

A reusable exposure record should contain:

| Field | Explanation |
|---|---|
| Identifier | Stable finding or hypothesis ID |
| Service and scope | Asset, owner, environment and authorization reference |
| Observation | What was discovered, with source and timestamp |
| Hypothesis | How the condition could cause a specific adverse outcome |
| Validation method | Approved procedure, bounds and expected behavior |
| Evidence | Redacted observations, control signals and links to controlled evidence |
| Validation status | Confirmed / partially supported / unconfirmed / not tested |
| Impact and context | Potential business and user consequences |
| Confidence and unknowns | Limitations, alternate explanations and missing evidence |
| Treatment and approver | Decision, accountable owner, timeframe and rationale |
| Retest result | Post-change outcome and next assessment trigger |

Do not publish credentials, customer information, vulnerabilities in third-party applications, or sensitive exploit details in public examples.

## Domain application

- **Web:** Validate access, session and workflow boundaries.
- **API:** Validate object- and function-level authorization and service trust assumptions.
- **Mobile:** Assess device-to-API trust, token handling and managed application boundaries.
- **AI/LLM:** Assess how retrieved data, prompts, tools and model outputs affect permissions and confidentiality.

The same evidence model applies, but authorization and observability vary by domain.

## Technology touchpoints

Asset inventory, threat intelligence, logs, app testing, WAF/CDN/edge telemetry, identity services, CI/CD evidence and tickets may supply inputs. No individual tool is required. A control's presence or a response status alone is not sufficient proof of effectiveness.

## Risk decisions

Q1 **does not define a numerical exposure score**. Later work may propose a transparent, reviewable model using impact, demonstrated exploitability, reachability, existing controls, and confidence. No single number should substitute for a human decision on urgent threats.

## Safety, AI, and review

AI may draft hypotheses or summarize redacted evidence, but it must not independently execute tests, approve mitigations, or set production enforcement. Follow [responsible AI use](responsible-ai-use.md). Reviewer acknowledgement is required before project documentation becomes official release guidance.

## Deliverable boundary

Q1 is **foundation documentation**. The CTEM Top 10, runnable playbooks, production-ready edge tools, executable CI/CD security gates and dashboards are later-quarter scope. [Roadmap](../ROADMAP.md).

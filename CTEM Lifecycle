# OWASP CTEM Blueprint: Five-Phase Lifecycle

| Field | Value |
| --- | --- |
| Version | 0.1 working draft |
| Quarter | Quarter 1 — Foundation |
| Document type | Lifecycle guidance |
| Status | Proposed for project review; not approved project policy |
| Intended repository path | `docs/ctem-5-phase-lifecycle.md` |
| Basis | OWASP CTEM Blueprint Quarter 1 Project Guidelines, version 0.1 Draft |

## 1. Purpose and Audience

This document describes the five-phase Continuous Threat Exposure Management (CTEM) lifecycle for the OWASP CTEM Blueprint project.

The lifecycle helps organizations identify potential exposures, assess their practical significance, decide what needs attention, and coordinate actions whose effectiveness can be verified. Its intended outcome is sustained reduction of meaningful security exposure, rather than an increase in findings or closed tickets.

The intended audience includes security practitioners, application and service owners, engineering teams, risk owners, and contributors developing the Blueprint's foundation documentation.

This is a Quarter 1 foundation document. It explains the lifecycle and its decision points without prescribing specific products, testing procedures, or implementation technologies.

## 2. Scope and Q1 Boundaries

### 2.1 Applicable systems and processes

The lifecycle applies to the areas identified in the Q1 guideline:

- Web applications and APIs.
- Mobile applications and their supporting services.
- AI/LLM-enabled systems and their connected components.
- Security controls, including edge protection and API gateways.
- CI/CD pipelines.
- Telemetry and monitoring systems.
- Remediation workflows and governance processes.

Q1 defines one shared lifecycle applicable across these areas. It does not require a separate detailed methodology for every technology domain. Each organization selects a bounded assessment scope appropriate to its business context and authorization.

### 2.2 Outside this document

This document does not define:

- A final CTEM Top 10 or comprehensive mappings to OWASP lists.
- Detailed validation playbooks or attack instructions.
- A numerical exposure scoring model.
- CI/CD automation templates.
- Dashboard, policy, or telemetry schemas.
- Tooling or reference implementations.
- A complete framework or version 1.0 release.

These remain later-quarter work as established by the Q1 guideline.

### 2.3 Relationship to other foundation documents

The framework document explains the conceptual model and principles. The scope document defines project boundaries. This lifecycle document explains how work moves between phases. Architecture documents describe component interactions, while the glossary maintains shared terminology.

The related documents are listed in Section 14. References to planned files do not imply that those files have already been completed.

## 3. Essential Terminology

| Term | Meaning in this document |
| --- | --- |
| Exposure | A condition or combination of conditions that could permit harm to an in-scope business service, asset, or process. Exposures can involve vulnerabilities, misconfigurations, permissions, workflows, dependencies, or ineffective controls. |
| Finding | A recorded observation or hypothesis about a potential exposure. A finding is not automatically a confirmed exposure. |
| Exposure path | A plausible sequence of access, conditions, or interactions through which an adverse outcome could occur. |
| Validation | Authorized assessment of whether a finding is practically meaningful and whether relevant controls behave as expected, with explicit evidence and limitations. |
| Evidence | Information supporting an observation, assessment outcome, or decision within a stated scope and time. |
| Remediation | A change intended to remove the cause of an exposure. |
| Mitigation | A measure intended to reduce likelihood or impact without necessarily removing the underlying cause. |
| Risk acceptance | An authorized, documented decision to retain a specified residual risk for a defined period, subject to review. |
| Retest | A scoped reassessment after an action to determine whether the intended exposure reduction occurred. |
| Regression validation | Reassessment intended to detect the reintroduction of a previously addressed exposure or failure of a relevant control. |

These definitions provide a working baseline and should remain consistent with the project glossary as it is developed.

## 4. Lifecycle Overview

The Q1 guideline defines the following order:

**Scope → Discover → Validate → Prioritize → Mobilize**

The phases describe connected activities rather than a rigid, one-way sequence. Different findings can occupy different phases at the same time, and new evidence can require a return to an earlier phase.

### 4.1 Why validation precedes formal prioritization here

This document follows Section 9 of the Q1 guideline. Discovery includes preliminary triage to select suitable validation candidates. Validation then gathers evidence about practical exposure and control effectiveness. Prioritization uses that evidence, business context, urgency, and remaining uncertainty to determine action.

Preliminary triage allocates assessment effort; formal prioritization determines the action order. This does not mean every finding must undergo active testing before it can receive attention.

Findings that cannot safely or feasibly be validated remain eligible for prioritization with their uncertainty explicitly recorded. Urgent containment and incident response must not wait for completion of every phase.

If the project changes the phase order, the guideline, framework, lifecycle, and architecture descriptions should be updated together.

### 4.2 Principal phase outputs

| Phase | Principal output |
| --- | --- |
| Scope | An agreed assessment boundary, business context, accountable owners, and constraints. |
| Discover | Candidate exposures with sources, affected scope, uncertainty, and preliminary triage. |
| Validate | Assessment outcomes with supporting evidence, observed control behavior, and limitations. |
| Prioritize | An ordered action set with business rationale, urgency, and decision ownership. |
| Mobilize | Coordinated actions, verification results, and documented residual-risk dispositions. |

Continuous operation combines recurring reviews with reassessment triggered by material changes. It does not require uninterrupted active testing.

## 5. Roles and Decision Authority

The roles below belong to the organization applying CTEM. They are distinct from the project-maintainer and contributor roles described in project governance.

| Role | Main responsibility |
| --- | --- |
| Business or service owner | Provides business context, agrees service boundaries, and owns the service's operational outcomes. |
| CTEM coordinator | Coordinates the lifecycle, maintains traceability between findings and actions, and ensures unresolved decisions reach the appropriate owner. |
| Validation practitioner | Performs authorized assessment, protects evidence, reports limitations, and stops or escalates when safety boundaries are reached. |
| Remediation owner | Coordinates corrective or mitigating changes and supplies the information needed for verification. |
| Authorized risk approver | Makes risk-acceptance decisions within the organization's delegated authority and sets review conditions. |

One person may hold several roles where appropriate, but decision authority should remain explicit. Where the organization requires independent review or separation of duties, those requirements continue to apply.

The organization identifies who may authorize testing, approve production changes, and accept residual risk. The service owner may perform some of these functions only where that authority has been delegated. Neither a project contributor nor an AI system gains such authority by participating in this lifecycle.

## 6. Phase 1 — Scope

### Purpose

Define the business services, systems, components, and controls to be assessed, together with the boundaries and conditions under which assessment may occur.

### Inputs

- Business objectives and service criticality.
- Available asset, application, API, dependency, and ownership information.
- Relevant data sensitivity and operational constraints.
- Prior findings, incidents, accepted risks, and significant changes.
- Applicable organizational obligations and testing permissions.

### High-level activities

- Select a manageable service or exposure boundary.
- Identify relevant components, dependencies, users, trust relationships, and controls.
- Record business impact considerations and accountable owners.
- State exclusions, third-party boundaries, and known visibility gaps.
- Establish authorization requirements, permitted environments, and safety constraints.
- Agree recurring review expectations and events that would require rescoping.

Assessment scope is not itself permission to test every component within it. Specific methods and environments remain subject to the authorization requirements in Section 11.

### Accountable role

The business or service owner agrees the business boundary. The CTEM coordinator documents the scope and confirms that the necessary operational authorities are identified.

### Outputs

An agreed scope description covering the service, relevant components, owners, business context, exclusions, visibility gaps, authorization boundaries, and reassessment triggers.

### Exit and return criteria

Discovery can proceed when the boundary is sufficiently clear and the intended discovery activities are authorized. Missing ownership, unclear permissions, or material scope uncertainty should be resolved or explicitly escalated before affected activities proceed.

Return to Scope when a material change alters the service boundary, ownership, dependencies, business impact, or assessment authority.

## 7. Phase 2 — Discover

### Purpose

Identify candidate exposures within the agreed scope and gather enough context to support assessment and risk decisions.

### Inputs

- The agreed scope and applicable authorization constraints.
- Available inventories, design information, configuration observations, security findings, and relevant telemetry.
- Previous validation outcomes and unresolved evidence gaps.

### High-level activities

- Identify relevant exposed interfaces, access paths, configuration weaknesses, permission concerns, and possible control failures.
- Consider findings affecting business workflows and combinations of conditions, not only individually reported vulnerabilities.
- Correlate related observations and distinguish duplicates from separate affected contexts.
- Associate findings with services, owners, sources, and observation dates.
- Record uncertainty and visibility limitations.
- Perform preliminary triage to select assessment effort according to potential impact, credible exposure paths, available evidence, and validation safety.

Discovery does not establish that every candidate is exploitable. Likewise, a lack of findings does not demonstrate complete coverage or absence of exposure.

### Accountable role

The CTEM coordinator owns the discovery handoff and involves the relevant service and technical owners.

### Outputs

A traceable set of candidate exposures with affected scope, source information, known context, uncertainty, preliminary triage rationale, and proposed next action.

### Exit and return criteria

A candidate may move to Validate when it has sufficient context for an authorized assessment. If assessment is unsafe, unavailable, or disproportionate, preserve the finding and its uncertainty for prioritization rather than silently discarding it.

Return to Scope when discovery identifies material components or dependencies outside the agreed boundary. Return for further discovery when assessment needs additional context.

## 8. Phase 3 — Validate

### Purpose

Assess whether a candidate exposure is practically meaningful in the stated context and whether relevant controls prevent, detect, or limit the adverse outcome.

### Inputs

- Candidate findings and preliminary triage results.
- Business and technical context.
- Documented authorization, permitted methods, approved environments, and stop conditions.
- Relevant control expectations and available evidence.

### High-level activities

- Select an assessment method proportionate to the question and operational risk.
- Use documentary review, configuration inspection, existing observations, or controlled testing as appropriate.
- Compare expected control behavior with observed behavior.
- Assess the relevant exposure path and potential consequence within the authorized boundary.
- Record results, conditions, evidence, uncertainty, and limitations.
- Stop and escalate when authorization or safety conditions are no longer satisfied.

Documentary or non-intrusive assessment is appropriate where active testing is unsuitable. Its conclusions must remain limited to what the evidence actually supports.

### Accountable role

The validation practitioner owns the assessment quality and safety. The relevant organizational authority approves the assessment conditions; the CTEM coordinator ensures the result reaches decision-makers.

### Outputs

An evidence-supported assessment outcome, using distinctions such as:

| Outcome | Interpretation |
| --- | --- |
| Confirmed | Evidence supports the exposure or control weakness within the assessed context. |
| Not reproduced under stated conditions | The assessment did not demonstrate the suspected behavior in the tested conditions. This does not establish safety under all conditions. |
| Inconclusive | The available evidence is insufficient to support a reliable conclusion. |
| Not tested | Assessment was not performed; the reason and remaining uncertainty are recorded. |

A suspected false positive should be dismissed only with a documented rationale and appropriate review. A failed attempt to reproduce an issue alone is not proof that the original finding was false.

### Exit and return criteria

Move to Prioritize when the result or an explicit evidence limitation can inform a decision. Inconclusive and untested findings can still require urgent action.

Return to Discover when further context is necessary, or to Scope when assessment reveals a material boundary or authorization issue.

## 9. Phase 4 — Prioritize

### Purpose

Determine which exposures require action, in what order, and with what urgency, using business context and the best available evidence.

### Inputs

- Findings, validation outcomes, and unresolved uncertainty.
- Business impact and service criticality.
- Exposure paths, relevant threat context, and control effectiveness.
- Dependencies, operational constraints, and existing risk decisions.

### High-level activities

- Consider likelihood, impact, exploitability evidence, and business context together.
- Consider exposure reachability, affected privileges or sensitive information, and demonstrated control behavior.
- Preserve the distinction between confidence in a finding and the potential severity of its consequences.
- Identify urgent containment needs, corrective actions, evidence-gathering needs, and decisions requiring risk approval.
- Assign action ownership and an organization-defined target or review point.
- Record the decision rationale and any dependencies or exceptions.

No numerical scoring formula or universal response deadline is required in Q1. Organizations should use qualitative decisions consistent with their established risk and response practices. Low confidence must not automatically be treated as low risk.

### Accountable role

The business or service owner owns the business priority decision with security input coordinated by the CTEM coordinator. Risk acceptance is reserved for an authorized risk approver.

### Outputs

An ordered action set that states the rationale, urgency, action owner, intended next step, review or target date, and any unresolved uncertainty.

### Exit and return criteria

Move to Mobilize when action ownership and the intended response are clear. Disagreement, missing ownership, and blocked decisions should be escalated rather than treated as completed prioritization.

Return to Discover or Validate when additional evidence could materially change the decision, without delaying urgent protective action unnecessarily.

## 10. Phase 5 — Mobilize

### Purpose

Coordinate the people, approvals, and changes needed to reduce exposure, and verify whether the intended outcome was achieved.

### Inputs

- Prioritized actions and their rationale.
- Assigned owners, target dates, and operational dependencies.
- Applicable change-management and approval requirements.
- Validation evidence and the conditions needed for meaningful retesting.

### High-level activities

- Agree feasible remediation or mitigation with the responsible teams.
- Obtain required change approvals and coordinate dependencies.
- Track blocked work, missed review points, and unresolved ownership.
- Carry out approved changes through the organization's established processes.
- Retest the relevant exposure and assess any limitations of the result.
- Identify appropriate regression-validation needs without prescribing automation.
- Document residual risk and the final or continuing disposition.
- Feed lessons and material changes back into the lifecycle.

### Accountable role

The remediation owner is accountable for coordinating action. The CTEM coordinator tracks progress and verification. Relevant service and risk authorities approve residual-risk decisions within their delegated authority.

### Outputs and dispositions

| Disposition | Required interpretation |
| --- | --- |
| Verified remediation | Evidence supports that the identified cause or exposure has been addressed within the reassessed scope. |
| Verified mitigation | Evidence supports the intended reduction in exposure; remaining risk and the underlying condition remain visible where applicable. |
| Risk accepted | An authorized approver records the residual risk, rationale, scope, expiry or review date, and conditions requiring earlier reconsideration. This is not remediation. |
| Deferred or blocked | Work remains outstanding with an owner, reason, escalation path, and review point. Deferral is not implicit risk acceptance. |

### Exit and return criteria

An action is not verified merely because a ticket is closed, a configuration was changed, or a team reports completion. Verification must address the original exposure and relevant control behavior under stated conditions.

Failed retests return the finding for further action and, where needed, renewed validation or prioritization. Accepted risks and temporary mitigations remain subject to review. Significant service or boundary changes return to Scope.

Completion of an individual action does not end the CTEM lifecycle.

## 11. Cross-Cutting Safeguards

### 11.1 Authorization and validation safety

Before any validation activity, establish:

- Documented authority from the appropriate organizational owner.
- Agreed targets, accounts or data where relevant, methods, environments, and time constraints.
- Applicable permissions for third-party systems and shared infrastructure.
- Protection of production availability, sensitive data, and other users.
- Named operational contacts, stop conditions, and escalation arrangements.

Being publicly reachable does not make a system authorized for testing. Human involvement does not, by itself, establish permission or safety.

Prefer approved test environments and synthetic data when they can answer the assessment question. Where production assessment is necessary, require specific approval and proportionate safeguards. If safe assessment is not possible, record the limitation and use other evidence or an explicit risk decision.

### 11.2 Evidence quality and handling

Evidence should be sufficient to explain the finding, decision, or verification result. At a minimum, describe:

- The affected service or scope.
- The source and observation date.
- Relevant assessment conditions.
- The observed result and supporting evidence reference.
- Limitations and uncertainty.
- The responsible assessor or reviewer.

These are documentation expectations, not a required data schema.

Collect only what is necessary. Protect operational evidence according to organizational access, retention, privacy, and handling requirements. Avoid unnecessary secrets, credentials, personal data, or customer content in findings.

Use sanitized or clearly fictional examples in public project contributions. Keep sensitive operational evidence out of public issues, pull requests, and documentation.

Evidence can become stale after relevant changes. Decisions and retests should consider whether prior observations still describe the current environment.

### 11.3 Responsible AI assistance

AI/LLM-enabled systems being assessed are part of project scope. AI used to assist the CTEM process is a separate concern.

Consistent with the Q1 guideline, AI may assist with documentation, hypothesis generation, signal summarization, exposure reasoning, and remediation explanations. These outputs remain unverified suggestions until a responsible person reviews them against available evidence.

AI assistance must not:

- Execute attacks or perform unauthorized testing.
- Make autonomous enforcement or production-remediation decisions.
- Generate uncontrolled exploit automation.
- Approve risk acceptance or replace human review.
- Convert an unsupported hypothesis into a claimed validation result.

Operational information must not be submitted to an AI service without the organization's authorization for that data and service. Apply the same evidence-handling and access requirements used elsewhere in the lifecycle.

### 11.4 Urgent exposure and incident escalation

A credible urgent exposure may require immediate protective action. Evidence of an active incident should be routed to the organization's incident-response process.

CTEM does not replace incident response, and the lifecycle must not delay containment. Record the decision and reconcile scope, findings, and follow-up work once the immediate situation permits.

## 12. Continuous Feedback and Reassessment

Organizations should define a review cadence appropriate to service criticality, rate of change, and operational constraints. This document does not prescribe a universal interval.

Reassessment should also respond to events such as:

- Material application, API, mobile, or AI-enabled service changes.
- Changes to identities, permissions, dependencies, or security controls.
- Newly observed exposure paths or relevant threat information.
- Failed retests or recurring findings.
- Incidents or meaningful changes in control telemetry.
- Expiry of risk acceptance or review of a temporary mitigation.
- Changes in business impact, ownership, or assessment authority.

| Trigger | Typical lifecycle response |
| --- | --- |
| Material boundary, ownership, or authority change | Revisit Scope. |
| Newly observed surface or suspected weakness | Revisit Discover within the agreed scope. |
| Relevant new evidence or changed control behavior | Revisit Validate and update Prioritize as needed. |
| Failed retest | Continue corrective work in Mobilize and reassess evidence or priority where necessary. |
| Expiring acceptance or temporary mitigation | Revisit the risk decision and relevant Prioritize/Mobilize activities. |

Feedback should preserve traceability between the original finding, subsequent evidence, decisions, actions, and verification. Repeated findings should prompt review of contributing process or control weaknesses, not only repeated closure of individual tickets.

## 13. Illustrative Walkthrough

The following example is fictional and is not a validation playbook.

1. **Scope:** A team selects a customer-service API and its access controls. They identify the service owner, business impact, approved test environment, permitted assessment boundaries, and synthetic records.
2. **Discover:** An authorized review identifies a possible access-control weakness. The team records the affected function, source, uncertainty, and preliminary triage rationale.
3. **Validate:** A controlled assessment in the approved environment confirms access to a synthetic record that the test identity should not be able to access. The assessor records the result and limitations; no customer records are used.
4. **Prioritize:** The service owner and security team consider the confirmed behavior, potential business impact, and control context. They assign an action owner and an appropriate target date without relying on a Q1 scoring formula.
5. **Mobilize:** The responsible team implements an approved correction. A scoped retest verifies the expected access-control behavior under the reassessed conditions. The team records the evidence and identifies relevant future changes that should trigger regression validation.

If the retest fails, the finding remains outstanding. If testing cannot be performed safely, the team records that limitation and makes a risk-informed decision rather than declaring the service safe.

## 14. Related Documents and Source

### Primary source

`OWASP_CTEM_Blueprint_Quarter_1_Project_Guidelines.pdf`, version 0.1 Draft:

- Sections 3 and 8: Q1 boundaries and project coverage.
- Section 9: the five lifecycle phases and their order.
- Section 10: responsible AI/LLM usage.
- Sections 11 and 12: architecture and project governance.
- Sections 15–19: acceptance, completion, and later-quarter handover.

### Planned repository references

- `docs/introduction.md`
- `docs/ctem-framework.md`
- `docs/scope.md`
- `docs/responsible-ai-use.md`
- `docs/glossary.md`
- `docs/quarter-1-project-guidelines.md`
- `architecture/ctem-reference-architecture.md`
- `architecture/ctem-ci-cd-architecture.md`
- `GOVERNANCE.md`

Convert these references to relative links when the files are available in the repository. The operational detail in this draft is proposed clarification of the Q1 foundation, not a claim that the source guideline already specifies every requirement above.

## 15. Q1 Review and Acceptance Checklist

- [ ] The phase names and order match the agreed project guideline.
- [ ] The distinction between preliminary triage and formal prioritization is clear.
- [ ] Every phase defines its purpose, inputs, activities, accountable role, outputs, and exit/return criteria.
- [ ] Operational roles are distinct from project governance roles.
- [ ] Validation requires appropriate authorization and explicit safety boundaries.
- [ ] Evidence quality, handling, limitations, and uncertainty are addressed.
- [ ] Untested or inconclusive findings are not automatically treated as low risk.
- [ ] Prioritization considers business context without requiring a numerical scoring model.
- [ ] Mobilization includes action ownership and evidence-backed verification.
- [ ] Remediation, mitigation, risk acceptance, and deferral are distinguished.
- [ ] Scheduled and event-driven feedback are explained.
- [ ] Urgent containment and incident response are not blocked by phase order.
- [ ] AI assistance remains bounded and human-reviewed.
- [ ] The guidance applies across the Q1 scope without promising detailed domain playbooks.
- [ ] Terminology and document boundaries are consistent with the other foundation documents.
- [ ] No later-quarter mappings, schemas, automation, or tooling are required by this document.
- [ ] Project maintainers have reviewed the draft before it is represented as accepted guidance.

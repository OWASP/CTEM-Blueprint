# OWASP CTEM Blueprint — Governance Guide

| Field | Value |
| --- | --- |
| Document version | 0.1 working draft |
| Status | Proposed for project review; not approved project policy |
| Scope | Quarter 1 foundation work and contributions to `quarter1-poc` |
| Created by | `Sathish Kishore` |
| Review date | 2026-11-06 |
| Reviewed repository | [OWASP/CTEM-Blueprint](https://github.com/OWASP/CTEM-Blueprint) |
| Reviewed branch | `quarter1-poc` |
| Reviewed by | `Arief Mohammed` |
| Reviewed commit | [`0f795b031058e82b4e4256cefd608dc333de027a`](https://github.com/OWASP/CTEM-Blueprint/tree/0f795b031058e82b4e4256cefd608dc333de027a) |
| Intended repository location | Root `GOVERNANCE.md`, replacing the current outline only after review |

> **Draft notice:** This guide builds on the branch's existing maintainer-led, consensus-oriented governance. Approval counts, decision procedures, branch workflow, and other operational details below are proposed additions unless explicitly identified as existing repository statements or external OWASP policy. They become project rules only through recorded adoption. Existing OWASP policies remain applicable independently of this draft.

## 1. Purpose and Authority

This guide defines how contributors and maintainers develop, review, accept, and maintain the CTEM Blueprint's Quarter 1 foundation documentation.

The objectives are to:

- Keep work within the agreed quarterly scope.
- Make ownership, reviews, and decisions traceable.
- Maintain accurate, practical, vendor-neutral, and responsibly written guidance.
- Enable community participation without implying that every contribution is accepted guidance.
- Distinguish project governance from the operational authority of organizations using the Blueprint.

The project is a collaborative documentation initiative. A merge, draft document, or repository location does not constitute Foundation endorsement, certification, production-readiness assurance, or authorization to test a system.

Project decisions remain subject to applicable OWASP Foundation policies. Maintainers cannot authorize exceptions to those policies where the Foundation or Project Committee reserves that authority.

### 1.1 Existing baseline

The reviewed branch already states that:

- Maintainers review and approve changes.
- Contributors submit material through a feature-branch and pull-request process.
- Reviewers assess accuracy, clarity, and CTEM alignment.
- Discussion should seek consensus where possible.
- Human review is required for AI-assisted work.

This guide makes that baseline more specific; it does not identify or appoint project leaders by inference from commit history.

## 2. Q1 Scope and Document Authority

### 2.1 Foundation work

The Q1 guideline supplied separately for this project defines a documentation foundation: project introduction, scope, framework and lifecycle, governance and contribution guidance, responsible-AI principles, glossary, roadmap, and conceptual reference and CI/CD architectures.

The guideline is not present in the reviewed branch. Before accepting Q1 completion, maintainers should add or link the agreed version and record its status.

The existence of directories for later work does not expand Q1 acceptance criteria. Final Top 10 content, comprehensive mappings, detailed validation playbooks, numerical scoring models, schemas, dashboards, automation templates, tooling, and a complete v1.0 framework remain outside this foundation milestone unless an explicit scope decision changes that boundary.

Contributors may propose later-quarter work in issues. Such work should be labelled and kept separate from the Q1 completion decision.

### 2.2 Authority and status

Use the following order when resolving documentation conflicts:

1. Applicable OWASP policies and legal obligations.
2. Explicitly adopted project governance and recorded project decisions.
3. The agreed quarterly guideline and acceptance criteria.
4. Reviewed documentation accepted for that scope.
5. Proposals, examples, placeholders, and unreviewed drafts.

A filename, merge, or detailed treatment does not by itself establish approval. Acceptance should be recorded in a pull request or decision issue, identifying the approver and reviewed version.

Use clear document states:

| State | Meaning |
| --- | --- |
| Proposed | Submitted for discussion; not authoritative guidance. |
| In review | Being assessed; material questions may remain open. |
| Accepted for Q1 | Approved as foundation guidance within the stated scope and limitations. |
| Deferred | Retained for a later milestone; not required for Q1 completion. |
| Superseded | Replaced by an identified decision or document. |

Accepted foundation guidance may still carry a project-wide draft version. Content acceptance and release publication are separate decisions.

### 2.3 Canonical documents

Maintain one authoritative location for each topic. Supporting files should link to it rather than maintain competing copies.

In particular, the root file `CTEM Lifecycle` and `docs/ctem-5-phase-lifecycle.md` contain different phase sequences at the reviewed commit. Maintainers must decide the intended sequence and consolidate the material into an agreed canonical path. This governance draft does not choose the technical sequence on the team's behalf.

## 3. Roles and Accountability

| Role | Responsibilities | Authority boundaries |
| --- | --- | --- |
| Recognized project leader | Maintains direction, coordinates with OWASP, confirms scope and governance decisions, and oversees continuity. | Acts within Foundation policy; cannot independently grant Foundation exceptions or endorsement. |
| Maintainer | Triages contributions, reviews and merges approved work, maintains consistency, and coordinates document acceptance. | Repository permissions and decision responsibilities must be explicitly assigned. |
| Reviewer | Assesses factual accuracy, methodology, safety, clarity, and relevant domain content. | A review does not grant merge or release authority unless separately assigned. |
| Contributor | Proposes improvements, supplies sources and appropriate rights, addresses feedback, and follows conduct and safety requirements. | Authorship does not confer acceptance, merge authority, or authority over another organization's systems. |
| Release coordinator | Assembles an approved snapshot, checks status and references, and prepares release notes or handover material. | This is an assigned responsibility, not an independent governing body; publication requires authorized approval. |

Small teams may combine roles. The approval and conflict-of-interest requirements still apply.

### 3.1 Role register and continuity

Maintain a public role register with each confirmed role-holder's public handle or approved contact, responsibilities, and applicable review or merge authority. Do not publish personal contact information without consent.

Project leaders should confirm appointments and permission changes in a recorded decision. Contributors may volunteer or be nominated for maintenance responsibilities based on sustained participation and relevant expertise. Repository access should be limited to what the role requires.

For ordinary succession or role changes, record the reason, outgoing responsibilities, handover, and replacement or interim owner. Give the affected person an opportunity to respond where appropriate. Urgent access containment and conduct cases may require restricted handling.

The published OWASP Project Policy sets leadership eligibility and composition requirements, including membership and a two-to-five-leader range. Confirm the project's recognized leadership arrangements with OWASP rather than treating repository access as proof of appointment.

## 4. Contributions and Pull Requests

### 4.1 Proposed workflow for this branch

The following workflow is proposed specifically for the Q1 proof-of-concept branch:

1. Open an issue or describe the proposed change in a focused pull request.
2. Identify whether the work belongs to Q1 or a later milestone.
3. Create a feature branch based on `quarter1-poc`; external contributors may use a fork.
4. Make a focused change, keeping unrelated corrections separate where practical.
5. Submit a pull request targeting `quarter1-poc` once maintainers confirm it as the Q1 integration branch.
6. Address review feedback and obtain the required approval.
7. An authorized maintainer merges the reviewed revision.

Until the branch target is confirmed, contributors should ask maintainers rather than assume that `quarter1`, `quarter1-poc`, or the default branch is the accepted destination.

The observed default branch is `master`. This guide does not rename it, authorize a release into it, or imply that `main` exists as the intended target.

### 4.2 Pull-request information

A substantive pull request should include:

- The problem or proposal and its related issue, if any.
- The affected documents and intended quarter.
- A concise summary and supporting references.
- Known limitations, unresolved questions, or conflicts with other documents.
- Confirmation that examples are authorized for publication and appropriately sanitized.
- A note about material AI assistance, where used, and the human verification performed.
- Any changes to scope, terminology, policy, or acceptance criteria.

Do not describe a scaffold, illustrative example, or untested approach as an implemented or validated capability.

### 4.3 Proposed review requirements

| Change | Required review before acceptance |
| --- | --- |
| Routine documentation or correction | At least one non-author maintainer approval of the current substantive revision. |
| Methodology, architecture, or security-sensitive guidance | Non-author maintainer approval plus relevant technical review; the same reviewer may satisfy both roles if qualified. |
| Governance, Q1 scope, canonical lifecycle, or release-status change | Non-author maintainer approval and explicit project-leader acceptance of the decision; one appropriately authorized non-author may fulfil both responsibilities. |
| License or Foundation-policy exception | Appropriate project review and any approval reserved to OWASP or the Project Committee. A project pull request alone cannot grant the exception. |

An author must not provide the sole approval of their own substantive work. Material changes after approval require renewed review of the affected content.

Reviewers should check correctness, evidence, consistency, scope, safe publication, licensing, broken references, and clear status labels. Where documentation describes a conceptual design, reviewers must not imply that a runtime test occurred.

There is no guaranteed response or resolution time in this guide. If an independent reviewer is unavailable, defer acceptance or request help; do not silently waive the review rule.

## 5. Decisions, Consensus, and Conflicts

Seek consensus through focused issue or pull-request discussion. Record material objections and address them with evidence and reference to scope.

For significant decisions, record:

- The question and available options.
- The affected documents and constraints.
- The decision and rationale.
- Reviewers, authorized approver, and relevant conflicts of interest.
- Follow-up actions, unresolved limitations, and conditions for reconsideration.

An existing issue or pull request is sufficient; Q1 does not require a separate decision-management system.

If consensus is not reached, maintainers summarize the unresolved points and request a decision from the recognized project leadership. Keep the current accepted baseline, or label the affected content unresolved, until the decision is recorded. Silence is not approval.

If project leadership itself cannot resolve the matter, seek assistance through OWASP's appropriate project-governance channels. Do not invent a voting threshold or override Foundation leadership-selection rules.

Anyone with a material commercial, employment, authorship, or personal conflict should disclose it and step aside from sole decision-making on the affected matter. A contributor's employer or sponsorship does not buy approval or control of project direction.

A contributor may request reconsideration by identifying new evidence, a scope conflict, or an unmet review requirement. Seek a different reviewer where feasible. Conduct complaints follow Section 9, not public technical debate.

## 6. Branch Controls and Change Traceability

Preserve issue, review, and commit history so that accepted decisions can be reconstructed. Do not use destructive history changes to conceal objections or retract published information without a traceable explanation.

Proposed controls, subject to authorized repository-administrator configuration, are:

- Pull-request review for accepted work.
- Independent approval for substantive changes.
- Renewed approval after material updates.
- Resolution of material review objections before merging.
- Restrictions on force-pushes and branch deletion for integration and publication branches.

These are recommendations, not claims about enabled GitHub enforcement. At review time, the public metadata reported `quarter1-poc` as unprotected and returned no applicable rulesets. Repository settings may change after this review.

The example under `ci-cd/github-actions/` is not an active repository workflow. Do not treat an illustrative validation file or an absent status check as an operational quality gate.

### 6.1 Urgent corrections

For accidentally exposed sensitive information or immediately harmful published guidance, an authorized maintainer may take the minimum necessary containment action before ordinary review. Notify project leadership through an appropriate restricted route and obtain independent follow-up review promptly.

Keep the public record sanitized. Never repeat exposed credentials or private evidence in an issue to explain the incident. Containment does not authorize unrelated policy changes or imply that sensitive information has disappeared from all copies or history.

## 7. Q1 Acceptance, Handover, and Releases

### 7.1 Q1 acceptance checklist

Project leadership and maintainers should explicitly record completion only when:

- [ ] The agreed Q1 guideline is available and its authority is clear.
- [ ] Foundation documents have identifiable owners and reviewed content, not just filenames.
- [ ] The Blueprint/Top 10 relationship and current project status are consistent.
- [ ] The competing lifecycle sequences are resolved and one canonical document is identified.
- [ ] Scope, framework, lifecycle, glossary, governance, and responsible-AI guidance are consistent.
- [ ] Conceptual architecture is distinguished from implemented automation or tooling.
- [ ] Public examples are sanitized, references are usable, and factual claims are supportable.
- [ ] Contribution, conduct, and private security-reporting routes are usable and accurately described.
- [ ] Licensing and contribution-attestation requirements have been confirmed with the appropriate authority.
- [ ] Remaining limitations and later-quarter work are recorded without being represented as completed.
- [ ] The acceptance decision identifies the reviewed commit or pull request and its approver.

This checklist does not add later-quarter tooling, playbooks, mappings, schemas, or scoring implementations to Q1.

### 7.2 Handover

A Q1 handover should identify the accepted snapshot, completed foundation documents, unresolved questions, known limitations, document owners, and deferred work. Distinguish recommendations for future quarters from approved commitments.

### 7.3 Release wording

Publication requires an explicit decision identifying the version or milestone, source commit, scope, limitations, and responsible approver. An authorized maintainer performs the publication after that decision.

Use draft and unreleased labels consistently until a release is actually approved and published. A file named `version-1.0.md` is not evidence that version 1.0 has shipped.

The branch's annual release cadence is expressed as a suggested aim, not a guaranteed schedule. This guide does not impose a release date or convert quarter completion into a v1.0 release.

Before merging Q1 work into the stable/default branch, confirm the destination and record the promotion decision. GitHub publication and project acceptance do not establish separate Foundation endorsement.

## 8. Safety, Evidence, and Responsible AI

### 8.1 Project approval is not testing authorization

Acceptance of documentation never authorizes a contributor or reader to test third-party systems. Examples and guidance should describe explicit scope, permission, operational safety, and relevant limitations.

Keep Q1 guidance foundational. Do not add uncontrolled testing instructions or operational validation playbooks under the label of governance.

### 8.2 Evidence and public content

Minimize collected information and publish only what is necessary and authorized. Do not include credentials, tokens, session cookies, sensitive infrastructure details, personal data, customer material, or confidential vulnerability evidence in public contributions.

Use sanitized or clearly fictional examples. Keep operational evidence in an appropriately controlled system outside the public documentation repository. Human review should verify both the substantive claim and whether its supporting material may be published.

### 8.3 AI-assisted contributions

AI may assist with drafting, summarization, hypotheses, and explanation within the project's responsible-AI boundaries. A human contributor remains accountable for sources, correctness, privacy, licensing, and safe publication.

Do not use AI assistance to:

- Execute attacks or unauthorized testing.
- Make autonomous enforcement or production-remediation decisions.
- Generate uncontrolled exploit automation.
- Accept risk or replace required human review.
- Present generated hypotheses as observed validation results.

Do not submit confidential or operational data to an AI service without the applicable organizational authorization. Material AI assistance should be disclosed in the contribution so reviewers can focus their verification; an AI output is not itself evidence.

## 9. Conduct and Reporting

Participants must follow the project's Code of Conduct and the applicable [OWASP Code of Conduct](https://policy.owasp.org/operational/code-of-conduct).

Maintain respectful, professional, evidence-led discussion. Harassment, discrimination, threats, retaliation, personal attacks, and deliberate disruption are unacceptable.

Maintainers may moderate project spaces within their assigned authority. Foundation-level sanctions, leadership removal, and formal complaint handling remain subject to OWASP's policies and designated authorities.

Formal conduct complaints can be submitted through the route in the [OWASP Whistleblower & Anti-Retaliation Policy](https://policy.owasp.org/operational/whistleblower.html), which currently identifies **compliance@owasp.org**. This is a conduct-reporting route, not the project's vulnerability-disclosure address.

Handle complaints on a need-to-know basis and follow Foundation policy. Do not promise absolute confidentiality or publish allegation details in project issues. If a complaint involves a project maintainer, use the Foundation route rather than require disclosure to the person concerned.

## 10. Private Security Reporting

Security defects, exposed secrets, and confidential vulnerability reports must not be submitted through ordinary public issues or pull requests.

At the time of review, `SECURITY.md` asks for private reporting but provides no concrete maintainer contact, and GitHub private vulnerability reporting is disabled. Do not tell contributors that a working private-report form exists until it has been enabled and verified.

Before adopting this guide, maintainers should:

1. Select and verify a private reporting channel accessible to the designated responders.
2. Name the responsible role and backup without exposing private personal details.
3. Update `SECURITY.md` with that route and accurately describe its availability.
4. Ensure the reporting guidance is discoverable from the default/public entry point.
5. Define triage, coordination, and advisory responsibilities without promising unapproved deadlines.

Until a private route is published, ask through a non-sensitive contact request where to send a report. Do not attach confidential details to that request. General OWASP support may help establish contact, but should not be described as a dedicated CTEM vulnerability intake unless confirmed.

## 11. Licensing, Attribution, and Neutrality

### 11.1 Current license and policy question

The reviewed repository contains the **Apache License 2.0 (`Apache-2.0`)**. This guide does not replace that license, relicense existing material, or represent a different documentation license as already adopted.

The published [OWASP Project Policy](https://policy.owasp.org/operational/projects) specifies documentation licensing requirements and reserves approval of departures to the Project Committee. Because this project is documentation-focused and currently uses Apache-2.0, leadership should confirm the applicable interpretation and any approved exception with OWASP, then record the outcome.

Do not assume either compliance or noncompliance solely from this draft. Any license change requires authorized review of rights and existing contributions; it cannot be accomplished merely by editing this guide.

### 11.2 Contributions and attribution

Contributors must have the right to submit their work, preserve relevant attribution, and identify externally sourced material and license restrictions.

The published Project Policy requires a Developer Certificate of Origin (DCO) process unless a qualifying existing contribution agreement provides an applicable exemption. No repository-specific DCO or CLA procedure was found in the reviewed branch. Maintainers should document the applicable process in `CONTRIBUTING.md` and establish how attestations are checked. Do not claim that sign-off enforcement is already configured.

Do not copy third-party standards or copyrighted material beyond what their terms permit. Prefer clear summaries and source references where redistribution rights are uncertain.

### 11.3 Commercial interests

Keep project guidance vendor-neutral. Commercial affiliations and relevant sponsorship should be disclosed where they may influence a contribution. Examples must not imply product endorsement or give a sponsor control over conclusions.

Contracts, sponsorship arrangements, donations, and other financial activities must follow OWASP's Foundation processes. Project contributors and maintainers must not bind the Foundation or collect project funds through unauthorized arrangements.

## 12. Adoption and Amendment

To adopt this guide, recognized project leadership and maintainers should review it through a pull request, resolve the adoption blockers below, and explicitly record the accepted version, effective date, and responsible roles.

Thereafter, amendments follow the same contribution and review process. Identify affected documents and distinguish substantive policy changes from editorial corrections. Preserve the decision rationale and superseded version in repository history.

Where a proposed rule cannot be implemented with the current team or repository permissions, record a specific alternative for approval. Do not silently label the rule enforced.

### 12.1 Decisions required before adoption

| Decision | Recommended responsible role | Required outcome |
| --- | --- | --- |
| Confirm leaders, maintainers, and contact routes | Recognized project leadership | Published role/authority register; no assumptions based on authorship. |
| Confirm Q1 source and contribution target | Leadership and maintainers | Agreed guideline location and confirmation whether `quarter1-poc` is the integration branch. |
| Accept review and decision rules | Leadership and maintainers | Recorded approval of the proposed requirements in Sections 4–6. |
| Resolve lifecycle conflict | Technical reviewers and maintainers, with leader acceptance | One documented sequence and canonical lifecycle path. |
| Reconcile project and release labels | Leadership and release coordinator | Consistent Blueprint/Top 10 relationship and draft/unreleased wording. |
| Establish private security reporting | Designated security-reporting maintainer | Verified channel and updated, discoverable `SECURITY.md`. |
| Confirm documentation license and contribution attestation | Leadership with OWASP/Project Committee as applicable | Recorded policy interpretation or approval; accurate licensing and DCO/CLA instructions. |
| Confirm governance adoption | Recognized project leadership | Accepted version, effective date, and responsible role register. |

## Appendix A — Review Observations

These observations describe the inspected snapshot and public repository settings on the review date. They are not additional claims of approved policy.

- The existing `GOVERNANCE.md` is a short outline describing maintainer approval, reviewer responsibilities, and consensus.
- Root `CTEM Lifecycle` is a detailed proposal explicitly marked as not approved project policy; `docs/ctem-5-phase-lifecycle.md` is a separate scaffold with a different phase order.
- The Q1 guideline previously supplied for the project is absent from the reviewed branch.
- The README describes a CTEM Top 10 v0.1 draft, while other documents describe the broader Blueprint.
- `releases/version-1.0.md` uses completed-release language, while `CHANGELOG.md` says unreleased and public tags/releases were empty at review time.
- The default branch is `master`. The `quarter1-poc` branch was reported as unprotected, and no applicable rulesets were returned by the public API.
- No `.github/` workflows, issue/PR templates, `CODEOWNERS`, or maintainer roster were found in the inspected tree.
- The CI/CD example referring to `main` is outside `.github/workflows` and is not an active quality gate.
- GitHub private vulnerability reporting was disabled, despite the branch's general private-reporting instruction.
- The repository license is Apache-2.0; no repository-specific DCO or CLA process was found.

## Appendix B — Source References

### Pinned repository material

The following links identify the reviewed commit rather than a moving branch:

- [Repository snapshot](https://github.com/OWASP/CTEM-Blueprint/tree/0f795b031058e82b4e4256cefd608dc333de027a)
- [Existing governance outline](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/GOVERNANCE.md)
- [Contribution guidance](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/CONTRIBUTING.md) and [review process](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/community/review-process.md)
- [Root lifecycle proposal](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/CTEM%20Lifecycle) and [canonical-path lifecycle scaffold](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/docs/ctem-5-phase-lifecycle.md)
- [Scope](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/docs/scope.md) and [responsible AI](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/docs/responsible-ai-use.md)
- [Security guidance](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/SECURITY.md) and [project Code of Conduct](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/CODE_OF_CONDUCT.md)
- [Annual release-cadence proposal](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/community/annual-release-cadence.md), [v1.0 text](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/releases/version-1.0.md), and [changelog](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/CHANGELOG.md)
- [Apache-2.0 license](https://github.com/OWASP/CTEM-Blueprint/blob/0f795b031058e82b4e4256cefd608dc333de027a/LICENSE)

### Additional project input

- `OWASP_CTEM_Blueprint_Quarter_1_Project_Guidelines.pdf`, version 0.1 Draft, previously supplied by the project contributor and reviewed in full. It is contextual input, not a file verified in the target branch or proof of recorded project adoption.

### External policies and live settings

- [OWASP Project Policy](https://policy.owasp.org/operational/projects)
- [OWASP Code of Conduct](https://policy.owasp.org/operational/code-of-conduct)
- [OWASP Whistleblower & Anti-Retaliation Policy](https://policy.owasp.org/operational/whistleblower.html)
- [Repository metadata](https://api.github.com/repos/OWASP/CTEM-Blueprint), [target-branch metadata](https://api.github.com/repos/OWASP/CTEM-Blueprint/branches/quarter1-poc), and [applicable rulesets](https://api.github.com/repos/OWASP/CTEM-Blueprint/rulesets?includes_parents=true)
- [Private vulnerability-reporting status](https://api.github.com/repos/OWASP/CTEM-Blueprint/private-vulnerability-reporting)

External policies and live repository settings may change. Verify them again when adopting this document. No repository files, permissions, branch settings, or releases were changed by this review.

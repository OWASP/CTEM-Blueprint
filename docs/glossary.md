# CTEM Glossary

**Status:** Q1 working terminology. These definitions support consistency across the Blueprint; they do not replace authoritative OWASP or standards-body definitions.

| Term | Working definition |
|---|---|
| **Asset** | A service, system, interface, identity, data store or process that has security and business relevance. |
| **Business criticality** | Importance of an asset/process to business operations, customer trust, safety or obligations. |
| **Attack surface** | Interfaces, permissions, dependencies and paths through which a threat could interact with a system. |
| **Exposure** | A condition or combination of conditions that may enable meaningful harm in a particular context. |
| **Finding** | An observed indicator or hypothesis requiring further context or evaluation. |
| **Exposure hypothesis** | A testable claim about conditions, plausible threat behavior and adverse outcome. |
| **Exposure path** | An ordered set of circumstances or interactions connecting threat capability to an outcome. |
| **Validation** | Authorized, bounded evaluation of evidence and relevant control behavior for a specific hypothesis. |
| **Validated exposure** | An exposure supported by evidence sufficient to substantiate the defined hypothesis within stated limitations. |
| **Unverified hypothesis** | Potential exposure for which confirming evidence has not been gathered or is insufficient. |
| **Compensating control** | Alternate preventive, detective or mitigating measure reducing risk when a primary control is absent or weak. |
| **Control effectiveness** | Demonstrated behavior of a security measure against defined expected outcomes and conditions. |
| **Reachability** | Whether a relevant actor or path can interact with an exposed interface under given conditions. |
| **Likelihood** | Judgement of how plausible an event is in its context, not interchangeable with a raw scanner score. |
| **Impact** | Plausible consequences to users, assets, data or business services. |
| **Confidence** | Strength of evidence and certainty supporting an assessment or decision. |
| **Residual risk** | Risk remaining after treatment or compensating controls are considered. |
| **Remediation** | Change aimed at eliminating the underlying cause of an exposure. |
| **Mitigation** | Change aimed at reducing likelihood or impact without necessarily removing its cause. |
| **Risk acceptance** | Time-bounded, documented retention of residual risk approved by an accountable authority. |
| **Retest** | Reassessment after a change to verify expected exposure reduction. |
| **Regression** | Reintroduction of a previously addressed weakness or loss of a previously effective control. |
| **Exposure drift** | Change in effective exposure due to configuration, architecture, code, permissions or threat context. |
| **CI/CD** | Continuous integration and continuous delivery/deployment processes supporting software changes. |
| **Edge control** | Protective or observational controls operating at a CDN, WAF, gateway, proxy or load balancer. |
| **LLM** | Large language model used within an application or as an assistive analytic component. |
| **AI agent** | AI-enabled workflow able to perform or request actions using tools or connected services. |
| **Human-in-the-loop** | A qualified individual reviews and authorizes defined decisions or actions. |
| **CTEM** | Continuous Threat Exposure Management: recurring context, discovery, validation, prioritization and mobilization activities to reduce significant exposure. |

## Status labels

- **Confirmed:** Evidence supports the stated hypothesis *within an explicitly documented scope*.
- **Partially supported:** Some evidence exists but key steps or assumptions remain uncertain.
- **Unconfirmed:** Available evidence does not substantiate the hypothesis; this does not prove safety.
- **Not tested:** No approved validation performed.
- **Mitigated / remediated / accepted:** Treatment disposition; each requires owner, rationale, and reassessment date or trigger.

## Usage

Use the full term on first appearance. Avoid calling a scan result “exploitable” without evidence. Record uncertainty rather than forcing a categorical decision.

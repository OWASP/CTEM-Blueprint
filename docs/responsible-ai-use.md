# Responsible AI and LLM Use in CTEM

**Status:** Quarter 1 draft · Applies both to **AI as a security assessment target** and **AI as an analyst assistant**.

## Distinguish two use cases

1. **Security of AI/LLM applications:** include assistants, agents, retrieval components, model APIs, tool integrations, permissions, data handling and monitoring within the CTEM scope.
2. **AI-assisted CTEM work:** use approved assistants to draft hypotheses, summarize sanitized signals, organize evidence or suggest remediation and regression tests.

These uses should not be conflated. A system that summarizes security logs is not evidence that the underlying web/API/mobile/AI exposure was actually validated.

## Acceptable assisted tasks

- Propose possible threat hypotheses from an approved, sanitized architecture description.
- Translate public OWASP risk categories into candidate validation questions.
- Summarize redacted observations, distinguishing facts from inference.
- Help explain suggested remediations and human-owned verification steps.
- Suggest coverage gaps for human review.

## Requirements and guardrails

**Human accountability:** A designated reviewer approves scope, testing, exposure status, mitigation and CI/CD release decisions. The model must not make binding decisions alone.

**Authorization:** Do not let AI agents run scans, access systems, call production tools, create tickets with live changes, or invoke security controls without separately approved safeguards and explicit authorization.

**Data minimization:** Never paste secrets, access tokens, customer records, confidential architecture or sensitive logs into unapproved AI services. Use synthetic/redacted evidence and access-controlled services.

**Untrusted input:** Treat external pages, logs, model outputs, retrieved documents and user-supplied prompts as untrusted content. Prompt injection can attempt to change an analyst's instructions, leak data or trigger tools.

**Reproducibility:** Preserve the source observation, timestamp, tested boundary, assumptions, model version where relevant, and human validation. Disclose when substantive assistance was AI-generated.

**Bias and error:** Models may fabricate exploit paths, overstate severity or overlook controls. Corroborate against actual evidence and seek independent review when uncertainty is high.

**Safe output:** Do not provide unauthorized exploit instructions, personal data, credentials, stealth evasion instructions or unsupervised production changes as part of published examples.

**Auditability:** Retain appropriate redacted provenance and a clear human decision trail. Apply organization's retention and privacy policies.

## Example (fictional)

Given a synthetic service inventory, an assistant suggests that a customer order API could lack object-level authorization. The analyst marks this an **unverified hypothesis**. An approved staging test with separate synthetic users is then run by qualified staff. The exposure record includes test evidence, limitations, independent review, and treatment owner. The assistant may help draft the report but cannot mark the result confirmed.

## Q1 versus later work

Q1 documents safe principles; it does not ship AI-enabled autonomous test agents, prompt-attack playbooks, production tool integrations or a scoring model. Later work may add public sample policies and reviewed procedures.

## References

- [OWASP GenAI Security](https://genai.owasp.org/)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)

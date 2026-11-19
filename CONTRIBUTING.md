# Contributing to OWASP CTEM Blueprint

We welcome contributions from all community members, including those who are not OWASP members. OWASP project leadership has separate membership and recognition requirements.

## Before contributing

- Read [README](README.md), [scope](docs/scope.md), [roadmap](ROADMAP.md), [governance](GOVERNANCE.md), and [Code of Conduct](CODE_OF_CONDUCT.md).
- For Q1, focus on **foundation documentation**. Top 10 details and executable tooling belong to later quarters unless a documented exception is approved.
- Search existing issues and open a proposal before substantial changes.
- Keep examples vendor-neutral, safe, accurate, and suitable for public use.

## Pull request workflow

1. Fork or branch from the agreed target branch and identify a single reviewable issue or improvement.
2. Make focused Markdown/source changes and verify relative links, terminology and scope.
3. Attribute outside content correctly; do not include non-permitted third-party text, screenshots, client secrets, personal data or private findings.
4. Sign every commit according to the **Developer Certificate of Origin (DCO)**, using `git commit -s` or the corresponding sign-off option.
5. Open a PR explaining **what changed**, **why**, **Q1 acceptance criterion**, **references**, **security/data implications**, and **validation performed**.
6. Address reviewer feedback; maintainers determine acceptance according to the adopted governance and OWASP requirements.

## DCO sign-off

Include this line in the commit message:

```text
Signed-off-by: Your Name <your-email@example.com>
```

The DCO text is at https://developercertificate.org/. Signing off certifies the contribution is yours or you have permission to contribute it under the repository license; it is not a guarantee that content is accurate.

## Editorial standards

- Distinguish **observations, hypotheses, and validated exposure**.
- Name expected controls, authority, environment and uncertainty where relevant.
- Use readable Markdown headings, internal links and accessible diagrams.
- Align the lifecycle with the canonical [five-phase document](docs/ctem-5-phase-lifecycle.md).
- Use existing OWASP resources as references and explain how CTEM complements them.
- Avoid saying a tool or defense is effective without reproducible evidence.
- Keep AI-generated text human-reviewed and cite the original underlying sources.

## Safe testing and disclosure

Do not run assessments against systems without explicit authorization. Use synthetic data and controlled environments for examples. Report sensitive vulnerabilities privately following [SECURITY.md](SECURITY.md), not in public issues.

## Project decisions

Proposed operational and approval arrangements are documented in [GOVERNANCE.md](GOVERNANCE.md). They become binding project rules only when adopted by the recognized project leadership and subject to OWASP Foundation policy.

# Security and Privacy Posture

Meridian's public posture is built around controlled intake operations, human oversight, data minimization, and evidence-based review. This document is a concise public summary for buyers, partners, reviewers, and maintainers.

## Scope

This posture applies to Meridian public repositories and public-facing intake documentation. Production implementation details, client-specific configurations, secrets, transcripts, recordings, and sensitive operating procedures are intentionally excluded from public repositories.

## Security Principles

- **Least privilege:** Access should be limited to the people, services, and environments that need it.
- **Separation of environments:** Development, staging, and production should use separate configuration, credentials, and data boundaries.
- **No secrets in source control:** Secrets, tokens, private keys, webhook credentials, passwords, and production configuration must be managed outside Git.
- **Reviewable change management:** Material changes should be made through pull requests, documented validation, and reviewer sign-off.
- **Audit-friendly operations:** Intake workflows should preserve enough non-sensitive operational evidence to support QA, escalation review, and performance reporting.

## Privacy Principles

- **Data minimization:** Collect only the information needed to recover, qualify, route, or review an intake request.
- **Synthetic public examples:** Public examples must use fictional names, fictional contact details, and synthetic scenarios.
- **Need-to-know access:** Sensitive intake records should be available only to authorized operators and reviewers.
- **Purpose limitation:** Intake data should be used for approved intake, routing, QA, reporting, and operational improvement purposes.
- **Retention awareness:** Retention expectations should be defined per implementation and aligned with client, legal, and operational requirements.

## Regulated-Domain Boundaries

Meridian systems must not provide legal advice, medical advice, diagnosis, treatment recommendations, triage, or final professional judgment. Workflows should identify when a conversation must be routed to a qualified human reviewer.

## Public Repository Rules

Do not commit:

- Client, caller, patient, lead, matter, appointment, transcript, recording, voicemail, or SMS data.
- API keys, OAuth tokens, webhook secrets, private keys, passwords, or production credentials.
- Privileged material, regulated professional notes, vendor contracts, or confidential commercial terms.
- Internal incident details or implementation specifics that would increase operational risk.

## Control Areas

| Area | Public baseline |
| --- | --- |
| Access control | Protected branches, least-privilege collaborator access, and review-based changes. |
| Secrets | No secrets in Git; use secure secret stores and environment-specific configuration. |
| Documentation | Public artifacts should be procurement-friendly, non-sensitive, and current. |
| Intake boundaries | Approved scripts and escalation rules should prevent regulated professional advice. |
| Evidence | Logs, routing records, QA notes, and reporting definitions should be inspectable without exposing public data. |
| Vendors | Vendor integrations should be documented privately when details are sensitive. |

## Review Cadence

- **Monthly:** Review public issues, documentation gaps, and buyer questions.
- **Quarterly:** Review privacy language, repository standards, and roadmap progress.
- **Annually:** Reassess public posture against operating model, market expectations, and implementation maturity.

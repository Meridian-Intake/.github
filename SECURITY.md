# Security Policy

Meridian treats intake infrastructure as sensitive operational software. Public repositories must never contain secrets, credentials, client records, transcripts, protected health information, privileged material, or confidential operational details.

## Reporting a Vulnerability

If you believe you have found a vulnerability or sensitive exposure, do not create a public issue. Contact Meridian through the website or business email listed in the organization profile and include a non-sensitive summary of the concern.

Please include:

- A concise description of the issue.
- The affected repository, document, or workflow.
- Steps to reproduce when safe to share.
- Potential impact.
- Your preferred contact method.

## Security Baseline

Meridian repositories should follow these defaults:

- Protected default branches.
- Pull-request reviews before merge.
- Least-privilege repository access.
- Secret scanning and dependency alerts where applicable.
- Environment-specific configuration outside source control.
- No production credentials or sensitive data in Git history.
- Audit-friendly documentation for operational changes.

## Data Handling Boundaries

Do not commit or request:

- Client, patient, caller, lead, matter, or appointment records.
- Call transcripts, SMS conversations, voicemails, or recordings.
- Legal, medical, or regulated professional notes.
- API keys, OAuth tokens, webhook secrets, private keys, or passwords.
- Vendor contracts or internal commercial terms.

Use synthetic examples when examples are needed.

# Repository Standards

These standards define the baseline expected across Meridian repositories.

## Required Community Files

- `README.md` or organization profile overview.
- `CONTRIBUTING.md` for contribution and review expectations.
- `SECURITY.md` for vulnerability and data-handling guidance.
- `SUPPORT.md` for appropriate contact paths.
- Pull request template with privacy and validation checks.
- Issue templates that prevent accidental sensitive disclosures.

## Branch and Review Controls

- Protect the default branch.
- Require pull requests for changes to protected branches.
- Require at least one review for material changes.
- Use status checks for runnable code repositories.
- Keep administrator bypasses limited and auditable.

## Secrets and Sensitive Data

Repositories must not contain:

- Secrets, tokens, passwords, private keys, or production credentials.
- Client, caller, patient, lead, matter, appointment, transcript, recording, or message data.
- Privileged legal or regulated professional content.
- Confidential vendor, pricing, or internal operating details.

Use synthetic examples and environment-variable placeholders.

## Documentation Requirements

- Explain purpose, scope, and audience.
- Separate current capability from planned capability.
- Include operational boundaries and escalation assumptions.
- Keep public documentation procurement-friendly and non-sensitive.
- Update documentation when workflows, controls, or ownership changes.

## Release and Change Management

- Use small, reviewable pull requests.
- Document validation performed.
- Identify privacy, security, and operational risks.
- Keep changelogs or release notes for major public artifact updates.
- Review public content on a regular cadence.

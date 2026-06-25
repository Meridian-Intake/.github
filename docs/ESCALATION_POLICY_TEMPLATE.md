# Escalation Policy Template

This template defines when an intake workflow should hand off to a human reviewer, client team, licensed professional, or emergency/urgent pathway.

## Escalation Owners

| Role | Owner | Coverage | Backup |
| --- | --- | --- | --- |
| Workflow owner | TBD | Business-hours workflow questions | TBD |
| Intake operator | TBD | Conversation monitoring and routing | TBD |
| QA reviewer | TBD | QA sampling and remediation | TBD |
| Regulated reviewer | TBD | Legal, medical, clinical, or other professional questions | TBD |
| Security/privacy contact | TBD | Sensitive data or security concerns | TBD |

## Escalation Triggers

Escalate when a conversation includes:

- Legal advice requests, legal conclusions, or matter-specific professional judgment.
- Medical advice requests, symptoms, diagnosis questions, treatment recommendations, or triage needs.
- Urgent safety, emergency, self-harm, threat, or abuse indicators.
- Complaints, disputes, refund demands, or reputational risks.
- Sensitive personal information beyond approved collection fields.
- Caller confusion, consent concerns, opt-out requests, or repeated failed contact attempts.
- Workflow uncertainty, missing routing rules, or incomplete evidence.

## Escalation Severity

| Severity | Description | Expected action |
| --- | --- | --- |
| Low | Non-urgent routing or clarification issue. | Route to workflow owner or intake operator. |
| Medium | Potential quality, privacy, or boundary issue without immediate harm. | Route to QA reviewer and document remediation. |
| High | Potential regulated advice, safety issue, sensitive exposure, or client-impacting error. | Pause workflow if needed and notify designated reviewer. |
| Critical | Emergency, security incident, or serious privacy exposure. | Follow emergency/security procedure and notify leadership. |

## Escalation Record

Each escalation should record:

- Timestamp.
- Synthetic or internal review ID.
- Trigger category.
- Severity.
- Owner assigned.
- Action taken.
- Follow-up due date.
- Resolution status.

## Review Cadence

- Review open escalations weekly during active pilots.
- Review escalation patterns monthly for production workflows.
- Convert recurring escalation causes into workflow updates, script changes, or training items.

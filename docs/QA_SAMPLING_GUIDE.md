# QA Sampling Guide

This guide defines a practical quality-assurance process for controlled intake workflows.

## QA Objectives

QA should verify that intake workflows are safe, bounded, reviewable, and operationally useful. The review should focus on approved language, routing accuracy, data minimization, regulated-domain boundaries, and evidence completeness.

## Recommended Sampling

| Workflow stage | Suggested sample | Purpose |
| --- | --- | --- |
| Pilot | 20% to 100% of eligible conversations | Catch boundary, routing, and evidence issues before scaling. |
| Early production | 10% to 20% weekly | Verify workflow stability and operator consistency. |
| Mature production | 5% to 10% monthly | Monitor drift and identify improvement opportunities. |
| High-risk workflow | Risk-based sample plus targeted review | Increase review for regulated, sensitive, or ambiguous workflows. |

## QA Criteria

- Approved opening and follow-up language was used.
- Qualification questions matched the approved workflow.
- No legal, medical, clinical, or regulated professional advice was provided.
- Sensitive data collection was minimized.
- Routing and escalation rules were followed.
- Caller opt-out, no-response, or consent signals were respected.
- Required timestamps, summary, routing outcome, and QA fields were captured.
- Any issue was assigned an owner and remediation action.

## QA Outcomes

| Outcome | Definition | Required follow-up |
| --- | --- | --- |
| Pass | Meets approved workflow and evidence requirements. | No immediate follow-up. |
| Monitor | Minor issue or dependency that does not block workflow. | Track trend and review next cycle. |
| Remediate | Incorrect routing, script drift, missing evidence, or training gap. | Assign owner and due date. |
| Escalate | Potential safety, privacy, security, or regulated-boundary issue. | Notify designated reviewer and follow escalation policy. |

## Monthly QA Review Questions

1. Which issue categories appeared most often?
2. Did any boundary exceptions occur?
3. Were routing rules clear enough for operators and automation?
4. Were required evidence fields complete?
5. Which scripts, templates, or escalation rules should be updated?
6. What should be reviewed again next cycle?

# Synthetic Intake Review and QA Examples

The examples below are fictional and designed to demonstrate review structure. They do not contain real client, caller, patient, matter, transcript, or operational data.

## Sample Intake Review

| Field | Synthetic example |
| --- | --- |
| Review ID | SYN-INTAKE-2026-001 |
| Vertical | Dental implant practice |
| Inbound event | Missed call after business hours |
| Follow-up channel | Approved SMS response |
| First response | 3 minutes after missed call |
| Caller intent | Requested consultation for implant options |
| Qualification status | Qualified for coordinator follow-up |
| Routing outcome | Routed to treatment coordinator queue |
| Escalation needed | No clinical or urgent-care escalation identified |
| Boundary check | No diagnosis, treatment recommendation, or clinical advice provided |
| Evidence captured | Timestamp, approved message ID, qualification fields, routing record, QA status |

## Synthetic Conversation Summary

A fictional caller contacted a dental practice after hours about implant consultation availability. The approved follow-up acknowledged the missed call, asked whether the caller wanted help scheduling a consultation, and collected preferred contact timing. The workflow avoided diagnosis, treatment recommendations, pricing guarantees, and urgent-care triage. The conversation was routed to a treatment coordinator for next-business-day follow-up.

## QA Review Example

| QA criterion | Result | Notes |
| --- | --- | --- |
| Approved opening used | Pass | Used the approved missed-call acknowledgment. |
| Sensitive data minimized | Pass | Collected only appointment intent and preferred callback window. |
| Regulated boundary respected | Pass | No clinical recommendation or diagnosis. |
| Routing rule followed | Pass | Sent to treatment coordinator queue. |
| Evidence complete | Pass | Timestamps, message ID, summary, and route were recorded. |
| Follow-up risk | Monitor | Confirm callback completion in next review cycle. |

## QA Scoring Rubric

| Score | Meaning | Action |
| --- | --- | --- |
| Pass | Workflow followed approved script, boundaries, and routing rules. | No immediate action. |
| Monitor | Minor issue or follow-up dependency requires review. | Track in QA log and review next cycle. |
| Remediate | Incorrect routing, missing evidence, or unclear boundary language. | Update workflow, coach operator, or revise script. |
| Escalate | Potential privacy, safety, legal, medical, or security concern. | Notify designated reviewer and follow incident process. |

## Public Example Requirements

Public synthetic examples must:

- Use fictional names, contact details, organizations, and scenarios.
- Avoid real transcripts, recordings, screenshots, message IDs, or phone numbers.
- Avoid advice, diagnosis, triage, or regulated professional judgment.
- Demonstrate controls, routing, evidence, and reviewability.

# Launch Readiness Checklist

Use this checklist before launching a Meridian intake workflow. This template is intended for controlled, reviewable deployments and should be adapted for each implementation.

## 1. Scope and Ownership

- [ ] Business goal is documented.
- [ ] In-scope channels are documented.
- [ ] Out-of-scope channels and requests are documented.
- [ ] Workflow owner is assigned.
- [ ] Human escalation owner is assigned.
- [ ] QA reviewer is assigned.

## 2. Approved Workflow

- [ ] Missed-call or inbound-event trigger is defined.
- [ ] Approved opening message is documented.
- [ ] Qualification questions are approved.
- [ ] Routing rules are documented.
- [ ] Escalation rules are documented.
- [ ] Stop, opt-out, and no-response behavior is documented.

## 3. Privacy and Data Minimization

- [ ] Required data fields are documented.
- [ ] Optional data fields are documented.
- [ ] Prohibited data fields are documented.
- [ ] Public examples use synthetic data only.
- [ ] Retention expectations are documented.
- [ ] Access is limited to authorized users.

## 4. Regulated Boundary Review

- [ ] Workflow avoids legal advice, medical advice, diagnosis, treatment recommendations, triage, and regulated professional judgment.
- [ ] Sensitive or ambiguous conversations route to a human reviewer.
- [ ] Vertical-specific boundary language has been reviewed.
- [ ] Emergency, urgent, or high-risk requests have a documented escalation path.

## 5. Technical and Operational Readiness

- [ ] Environment variables are configured outside source control.
- [ ] Required integrations are tested in the correct environment.
- [ ] Logging and routing evidence are enabled.
- [ ] Failure and retry behavior is understood.
- [ ] Monitoring or review cadence is assigned.
- [ ] Rollback or pause procedure is documented.

## 6. Reporting and QA

- [ ] Core metrics are defined.
- [ ] QA sampling cadence is defined.
- [ ] Review dashboard or report location is documented.
- [ ] Launch success criteria are documented.
- [ ] First post-launch review date is scheduled.

## Launch Decision

| Decision | Criteria |
| --- | --- |
| Launch | All required controls are complete and owners are assigned. |
| Launch with monitoring | Low-risk gaps are documented with owners and dates. |
| Do not launch | Privacy, safety, regulated-boundary, routing, or evidence gaps remain unresolved. |

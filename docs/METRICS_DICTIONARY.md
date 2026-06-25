# Metrics Dictionary and Synthetic Reporting Examples

This document defines core Meridian intake metrics and provides a synthetic reporting example. Metrics should be interpreted with context and should not be used to imply legal, medical, clinical, or other regulated outcomes.

## Core Metrics

| Metric | Definition | Example calculation | Notes |
| --- | --- | --- | --- |
| Missed-call recovery rate | Share of missed calls that receive an approved follow-up. | Recovered missed calls / eligible missed calls | Exclude test calls and out-of-scope channels. |
| First-response time | Time from eligible inbound event to approved first response. | Response timestamp - event timestamp | Report median and percentile values, not only average. |
| Qualification completion rate | Share of recovered conversations with required qualification fields completed. | Completed qualifications / recovered conversations | Required fields vary by workflow. |
| Escalation rate | Share of conversations routed to a human or specialist review path. | Escalations / recovered conversations | Higher rates may be appropriate in regulated contexts. |
| Booked opportunity rate | Share of qualified opportunities that become scheduled or accepted next steps. | Booked opportunities / qualified opportunities | Define booking consistently per vertical. |
| QA pass rate | Share of sampled conversations that pass QA criteria. | Passing QA samples / total QA samples | Include sample size and sampling method. |
| Intake leakage reduction | Estimated reduction in missed or mishandled inbound demand. | Baseline leakage - current leakage | Requires a documented baseline. |
| Boundary exception rate | Share of sampled conversations with potential regulated-boundary issues. | Boundary exceptions / QA samples | Any high-risk exception should trigger review. |
| Evidence completeness rate | Share of reviewed events with required timestamps, route, outcome, and QA fields. | Complete records / reviewed records | Supports auditability and operational review. |

## Synthetic Monthly Report

| Metric | Synthetic value | Trend | Interpretation |
| --- | --- | --- | --- |
| Eligible missed calls | 120 | +8% | Higher inbound volume during campaign period. |
| Missed-call recovery rate | 94% | +5 pts | Most eligible missed calls received approved follow-up. |
| Median first-response time | 2m 40s | -35s | Faster response after trigger tuning. |
| Qualification completion rate | 71% | +4 pts | More conversations collected required routing fields. |
| Escalation rate | 18% | +2 pts | Increase driven by better boundary detection. |
| Booked opportunity rate | 29% | +3 pts | Requires client confirmation of completed bookings. |
| QA pass rate | 96% | +1 pt | Sample passed script, boundary, and evidence checks. |
| Evidence completeness rate | 98% | +2 pts | Missing fields reduced after QA feedback. |

## Reporting Rules

- Always define numerator, denominator, and exclusions.
- Separate operational metrics from business outcomes.
- Include sample size for QA and review-based metrics.
- Use medians or percentiles for response-time metrics where possible.
- Flag workflow, staffing, campaign, seasonality, or channel changes that affect comparability.
- Use synthetic data in public examples.

## Dashboard Sections

A production dashboard should separate:

1. Inbound volume and missed-call events.
2. Recovery and first-response performance.
3. Qualification and routing outcomes.
4. Escalations and boundary exceptions.
5. QA sampling and evidence completeness.
6. Opportunity and booking outcomes where client-confirmed data is available.

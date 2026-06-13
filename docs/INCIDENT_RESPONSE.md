# Incident Response Model

## Purpose

This document defines a lightweight incident response model for OaaS.

The goal is not to create a heavy enterprise process, but to make incidents understandable, assignable and reviewable.

---

## Incident lifecycle

```text
Detect
  ↓
Triage
  ↓
Contain
  ↓
Restore / workaround
  ↓
Communicate
  ↓
Record evidence
  ↓
Review and improve
```

---

## Incident classification

| Level | Description | Example response |
| --- | --- | --- |
| Low | Minor issue, limited impact | Record and fix during normal operations |
| Medium | Service degradation or repeated issue | Assign owner, communicate, track follow-up |
| High | Service outage or business-impacting failure | Immediate coordination, escalation and post-incident review |
| Critical | Major service, security or continuity impact | Formal escalation, evidence capture and management review |

---

## Minimum incident evidence

Every meaningful incident should record:

- date and time
- detected by
- affected service
- user/business impact
- suspected cause
- actions taken
- recovery or workaround
- owner
- follow-up actions
- whether documentation/runbooks need updating

---

## Public/private boundary

Public examples must not include:

- real customer names
- real users
- real IP addresses
- real system identifiers
- real secrets
- screenshots containing sensitive information
- production logs

Real incident evidence belongs in a private operational annex.

# Operating Model

## Purpose

This document defines how the service is operated in a repeatable and transferable way.

The operating model answers:

- who owns the service
- how work is received
- how incidents are handled
- how changes are controlled
- how recovery is verified
- how service evidence is reviewed

---

## Operating principles

| Principle | Meaning |
| --- | --- |
| Ownership is explicit | Every service area has a named owner or role |
| Changes are controlled | Changes require scope, impact, rollback and evidence |
| Incidents are recorded | Incidents produce a summary, impact view and follow-up actions |
| Recovery is tested | Backup existence is not enough; restore must be verified |
| Evidence is reusable | Operational evidence should support review, audit and handover |
| Public/private boundary is respected | Real customer data and environment details stay private |

---

## Operational cadence

| Cadence | Activity |
| --- | --- |
| Daily / as needed | Incident handling and operational checks |
| Weekly | Open issues, risks and change queue review |
| Monthly | Service review, evidence review and improvement actions |
| Quarterly | Recovery test review and responsibility review |
| Before major change | Change risk, rollback and approval check |

---

## Operating flow

```text
Request / event / incident
        ↓
Classify scope and urgency
        ↓
Assign owner
        ↓
Execute runbook or change process
        ↓
Record evidence
        ↓
Review outcome
        ↓
Update documentation if needed
```

---

## Definition of done

Operational work is done only when:

- the action is completed
- the impact is understood
- evidence is recorded
- follow-up actions are visible
- documentation is updated if needed
- ownership is clear

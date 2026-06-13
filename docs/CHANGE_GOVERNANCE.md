# Change Governance

## Purpose

This document defines how operational changes are scoped, reviewed, executed and evidenced.

The goal is to prevent uncontrolled changes and make service impact visible before execution.

---

## Change classes

| Class | Description | Example |
| --- | --- | --- |
| Class 1 | Low-risk documentation or configuration note | Runbook clarification |
| Class 2 | Operational change with limited blast radius | Monitoring threshold adjustment |
| Class 3 | Service-impacting or recovery-related change | Backup process change |
| Class 4 | High-risk security, availability or customer-impacting change | Identity, access, network or production change |

---

## Minimum change fields

A change should define:

- change title
- requester
- owner
- scope
- affected service
- risk class
- impact assessment
- rollback plan
- validation plan
- approval requirement
- evidence location

---

## Change flow

```text
Propose change
  ↓
Define scope and owner
  ↓
Classify risk
  ↓
Assess blast radius
  ↓
Define rollback
  ↓
Approve if needed
  ↓
Execute
  ↓
Validate
  ↓
Record evidence
  ↓
Review if impact occurred
```

---

## Key rule

A change is not ready if rollback, validation or ownership is missing.

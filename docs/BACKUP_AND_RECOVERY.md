# Backup and Recovery Model

## Purpose

This document defines how backup and recovery thinking is handled in the OaaS model.

The key principle is simple:

> Backup existence is not enough. Recovery must be testable and evidenced.

---

## Recovery maturity levels

| Level | Description |
| --- | --- |
| Level 0 | No known backup or recovery process |
| Level 1 | Backup exists, but restore is untested |
| Level 2 | Restore process is documented |
| Level 3 | Restore has been tested and evidenced |
| Level 4 | Restore is periodically tested and reviewed |

---

## Minimum recovery evidence

A recovery test should record:

- service or component tested
- backup source
- restore target
- restore owner
- date and time
- test result
- issues found
- time to restore
- follow-up actions
- evidence location

---

## Recovery questions

Before claiming operational readiness, answer:

```text
What must be recoverable?
Where is the backup?
Who can restore it?
Has restore been tested?
How long did it take?
What evidence exists?
What failed during the test?
What must be improved?
```

---

## Public/private boundary

Public examples must use synthetic service names and fake evidence.

Real backup locations, system names, credentials, storage paths and recovery evidence belong in a private operational annex.

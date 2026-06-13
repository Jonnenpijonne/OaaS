# Service Catalog

## Purpose

This document is a compatibility entry for validation flows that expect a service catalog document.

The primary OaaS service listing model is maintained in:

- `docs/SERVICE_INDEX.md`

---

## Catalog meaning in OaaS

In this repository, the service catalog is a simple operational index. It explains:

- what service or operational area exists
- why it exists
- who owns it
- what is included
- what is excluded
- what review or recovery material supports it

---

## Minimum service entry

| Field | Description |
| --- | --- |
| Service name | Name of the service or operational area |
| Purpose | Why the service exists |
| Service owner | Accountable role |
| Technical owner | Technical responsibility |
| Included scope | What is covered |
| Excluded scope | What is not covered |
| Criticality | Low, Medium, High or Critical |
| Runbook reference | Operational instructions |
| Recovery reference | Restore or rollback model |
| Review reference | Service review material |

---

## Key rule

If a service is important enough to operate, it is important enough to define clearly.

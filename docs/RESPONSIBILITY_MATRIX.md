# Responsibility Matrix

## Purpose

This document defines ownership and responsibility boundaries for an Operations as a Service model.

The goal is to remove ambiguity around who owns what.

---

## Responsibility roles

| Role | Responsibility |
| --- | --- |
| Service owner | Owns the service scope, priorities and service review |
| Technical owner | Owns technical implementation, runbooks and recovery model |
| Operations owner | Owns daily operational process and incident coordination |
| Change owner | Owns planned changes, impact assessment and rollback plan |
| Evidence owner | Ensures service evidence is recorded and reviewable |
| Customer / stakeholder | Confirms business impact, acceptance and priorities |

---

## RACI-style matrix

| Activity | Service owner | Technical owner | Operations owner | Change owner | Evidence owner |
| --- | --- | --- | --- | --- | --- |
| Define service scope | A | C | C | C | C |
| Maintain runbooks | C | A/R | R | C | C |
| Handle incidents | C | R | A/R | C | C |
| Approve changes | A | C | C | R | C |
| Execute changes | C | R | C | A/R | C |
| Verify rollback | C | A/R | C | R | C |
| Record evidence | C | C | R | R | A/R |
| Review service maturity | A/R | R | R | C | R |

Legend:

- A = Accountable
- R = Responsible
- C = Consulted

---

## Key rule

If ownership is unclear, the work is not operationally ready.

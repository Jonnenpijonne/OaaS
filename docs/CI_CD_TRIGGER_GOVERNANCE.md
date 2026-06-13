# CI/CD Trigger Governance Note

## Purpose

This note documents a small but important governance-oriented change made in this fork.

The upstream OaaS/Oparaca project is a complex Java/Maven, serverless and platform-oriented codebase. In this fork, additional public-safe operations and governance documentation was added for portfolio and learning purposes.

During that work, the existing GitHub Actions workflows were reviewed from a risk and change-management perspective.

---

## Observation

The repository contained automation workflows that were originally designed for the full platform codebase:

- Java/Maven build workflow
- platform/container build workflow
- function container build workflow

The Java/Maven workflow was configured to run on every push to `main`, and the platform workflow was configured to run broadly across branches. This meant that documentation-only changes could still trigger heavy platform-level automation.

For a complex platform repository, this creates unnecessary operational noise and can blur the boundary between low-risk documentation work and higher-risk platform build activity.

---

## Change made

The workflow configuration was adjusted using a risk-based approach:

1. The Maven workflow was scoped to Java/Maven-related paths only.
2. The Maven workflow was updated to use JDK 21 to better align with the broader platform workflow.
3. The heavy platform workflow was changed to manual-only execution using `workflow_dispatch`.
4. Documentation, evidence and template changes were intentionally kept from triggering platform-level automation.

---

## Rationale

This was not done to remove automation as a principle.

It was done to apply automation more deliberately.

Documentation-only changes should not trigger heavy platform build processes unless those processes are directly relevant to the change. Platform-level automation has a larger blast radius and should be triggered intentionally, especially in a forked research/platform codebase.

The change reflects a governance-first CI/CD principle:

> CI/CD is not only automation. It is also a control surface.

A pipeline that is too broadly triggered can become operational noise or risk. A well-scoped pipeline supports stability, traceability and controlled change.

---

## Risk-based change-management framing

The change separates low-risk and higher-risk work:

| Change type | Expected automation |
| --- | --- |
| Documentation update | No Maven/platform build required |
| Governance template update | No Maven/platform build required |
| Java/Maven source change | Maven CI should run |
| Platform/container change | Manual or explicitly scoped workflow |
| Function code change | Function container workflow may run |

This reduces unnecessary build activity and makes workflow execution more meaningful.

---

## Audit and traceability value

A manual platform workflow creates a clearer operational signal:

- the workflow is triggered intentionally
- the actor is visible in GitHub Actions
- the execution time is recorded
- the action is distinguishable from routine documentation changes

This makes platform-level automation more reviewable and easier to reason about.

---

## Portfolio learning value

This fork is not presented as an original implementation of the OaaS/Oparaca platform.

The value of this change is in the governance decision:

- identifying automation scope risk
- separating documentation changes from platform changes
- reducing unnecessary CI/CD blast radius
- using manual execution for higher-risk workflow activity
- treating GitHub Actions as part of operational control, not only as a build mechanism

---

## Summary

This change demonstrates risk-based CI/CD trigger governance in a real repository context.

The key lesson is:

> Automate what should be repeatable, but control what has a high operational blast radius.

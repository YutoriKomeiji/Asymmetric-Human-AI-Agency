# Responsibility Pathways

Safety-LCA defines responsibility as a **structural flow**, not a moral concept.

Responsibility must be:
- Explicit
- Traceable
- Interruptible
- Human-terminating

If responsibility cannot be traced to a human decision point,  
the system is already unsafe — regardless of model quality or intent.

---

## The Core Problem: Responsibility Collapse

Most AI-related incidents are not caused by model errors.

They are caused by **responsibility collapse**, where:

- AI outputs are treated as decisions
- Human confirmation becomes implicit
- Authority shifts silently through convenience
- No one can clearly answer “who decided this?”

This collapse happens gradually, not maliciously.

Safety-LCA is designed to **make responsibility visible again**.

---

## Responsibility Is Not Shared

In Safety-LCA, responsibility is never:
- Shared
- Diffused
- Delegated
- Inherited by the system

Responsibility always belongs to a **specific human at a specific moment**.

AI may participate in reasoning, but never in responsibility.

---

## The Responsibility Pathway Model

Every action in a Safety-LCA system must pass through a defined pathway:

AI Output
 ↓
Human Interpretation
 ↓ 
Explicit Decision
 ↓ 
Human Confirmation
 ↓ 
Irreversible Action

If any step is skipped, merged, or automated,
the pathway is broken.

Broken pathways produce **ghost decisions** —
actions with no accountable owner.

---

## Explicit Responsibility Points (ERPs)

Safety-LCA requires explicit responsibility points:

- Decision to accept AI output
- Decision to ignore AI output
- Decision to override AI output
- Decision to commit irreversible actions

These points must be:
- Visible in the workflow
- Logged by design
- Impossible to bypass accidentally

---

## Responsibility ≠ Approval

Clicking “OK” is not responsibility.

Responsibility requires:
- Awareness
- Intent
- Opportunity to refuse
- Clear consequences

UX that hides responsibility is a **safety bug**, not a usability feature.

---

## Failure Modes of Responsibility Pathways

Common failure patterns include:

- Auto-commit after AI suggestion
- Default acceptance of AI output
- Batch approvals without review
- Silent escalation of permissions
- “Human-in-the-loop” in name only

Safety-LCA treats these as **architectural failures**.

---

## Design Requirement

A system is Safety-LCA compliant only if:

> At any point, a human can point to a specific action and say:
> “This was my decision — and I could have chosen otherwise.”

If that statement is not true,
responsibility has already been lost.

---

## Relation to Asymmetric Human–AI Agency

Responsibility pathways are the **mechanical implementation** of asymmetric agency.

Agency defines *who may decide*.  
Pathways define *how that decision flows*.

Without explicit pathways,
asymmetry collapses into illusion.

---

## Summary

- Responsibility must flow only through humans
- AI outputs never carry responsibility
- Workflow design is the primary safety surface
- Invisible responsibility is already failure
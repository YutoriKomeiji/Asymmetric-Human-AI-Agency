# Design Patterns for Safety-LCA

This document defines **design patterns** that enforce asymmetric human–AI agency at the architecture level.

These patterns are not UX tips or policies.
They are structural mechanisms that prevent responsibility collapse.

---

## Pattern 1: Explicit Decision Gate

**Problem:**  
AI outputs are silently treated as decisions.

**Solution:**  
Insert an explicit human decision step between AI output and action.

**Rule:**
- No AI output may trigger an irreversible action
- A human must explicitly choose to accept, reject, or defer

**Implementation examples:**
- Mandatory confirmation dialog
- Signed approval step
- Recorded decision checkpoint

---

## Pattern 2: Responsibility Anchor

**Problem:**  
Decisions occur, but ownership is unclear.

**Solution:**  
Every irreversible action must be anchored to a specific human identity and moment.

**Rule:**
- Decision owner must be explicit
- Time and context must be logged
- Responsibility cannot be inherited or transferred implicitly

**Design constraint:**
> If you cannot name the human, the action must not execute.

---

## Pattern 3: Irreversibility Barrier

**Problem:**  
Automation drifts into irreversible domains.

**Solution:**  
Create hard boundaries around irreversible actions.

**Rule:**
- Irreversible actions require human confirmation
- Automation may prepare, but never cross the boundary

**Examples:**
- Deployments
- External communications
- Financial actions
- Record mutations

---

## Pattern 4: Separation of Suggestion and Execution

**Problem:**  
AI suggestions blend into execution paths.

**Solution:**  
Physically and logically separate suggestion flows from execution flows.

**Rule:**
- AI outputs live in read-only channels
- Execution requires a separate human action

**Result:**  
Prevents “AI already did it” ambiguity.

---

## Pattern 5: Visibility of Decision Moments

**Problem:**  
Humans lose awareness of when they are deciding.

**Solution:**  
Make decision moments visible, explicit, and interruptive.

**Rule:**
- Decision points must feel like decisions
- No silent defaults
- No pre-checked confirmations

**Design goal:**  
Humans should *feel* responsibility, not just hold it.

---

## Pattern 6: Autonomy Budget

**Problem:**  
Autonomy increases gradually without intent.

**Solution:**  
Define and enforce a maximum autonomy level per system.

**Rule:**
- Autonomy increases require explicit design change
- Temporary automation must expire by default
- Drift is treated as a bug

---

## Pattern 7: Failure Visibility Pattern

**Problem:**  
Responsibility failures are discovered too late.

**Solution:**  
Design systems to surface broken pathways early.

**Examples:**
- Missing decision owner warnings
- Skipped confirmation alerts
- Responsibility chain validation

---

## Summary

These patterns convert **ethics into architecture**.

If these patterns cannot be implemented,
the system is not ready for safe AI integration.
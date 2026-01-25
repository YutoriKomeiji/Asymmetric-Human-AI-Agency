# Failure Modes in Safety-LCA

Safety-LCA defines failure not as model error, but as **structural breakdown of responsibility and agency**.

This document enumerates the primary failure modes that occur when responsibility pathways are weakened, bypassed, or erased.

These failures are architectural, not behavioral.

---

## 1. Responsibility Collapse

**Definition:**  
A state where actions occur without a clearly identifiable human decision owner.

**Typical causes:**
- Implicit acceptance of AI outputs
- Missing confirmation steps
- UI auto-commit patterns
- Process shortcuts under time pressure

**Result:**  
No one can answer: *“Who decided this?”*

---

## 2. Authority Leakage

**Definition:**  
Decision authority shifts from humans to AI systems through workflow convenience rather than explicit delegation.

**Signals:**
- AI outputs treated as defaults
- “AI already decided” language
- Humans acting as approvers, not deciders

**Result:**  
AI becomes a de facto actor without formal authority.

---

## 3. Silent Autonomy Drift

**Definition:**  
Gradual increase of system autonomy without explicit design intent or governance decision.

**How it happens:**
- Automation added incrementally
- Steps merged for efficiency
- Human confirmation removed “temporarily”

**Result:**  
The system evolves into something no one explicitly designed.

---

## 4. Ghost Decisions

**Definition:**  
Actions that occur with no accountable human owner, produced by broken responsibility pathways.

**Characteristics:**
- Cannot be traced to a human decision
- Explained as “system behavior”
- Justified post-hoc

Ghost decisions are the **signature failure** of unsafe AI systems.

---

## 5. UI-Induced Failures

**Definition:**  
Responsibility breakdown caused by interface or tooling design, not intent.

**Examples:**
- Auto-filled confirmations
- One-click irreversible actions
- Hidden decision boundaries
- Collapsed multi-step flows

**Result:**  
Humans lose awareness of when they are deciding.

---

## Design Implication

If a system allows these failure modes to occur,  
it is **structurally unsafe** — regardless of model quality, policy, or intent.

Safety-LCA treats these as **design bugs**, not user errors.
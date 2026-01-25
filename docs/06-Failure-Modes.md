# Failure Modes in Safety-LCA Systems

This document defines the canonical failure modes that occur
when Safety-LCA constraints are violated.

These are **architectural failures**, not user errors.

---

## 1. Responsibility Collapse

### Description
Responsibility becomes unclear, diffused, or absent.

### Symptoms
- No single human can answer “who decided”
- Decisions appear to have happened automatically
- Post-hoc rationalization replaces accountability

### Root Causes
- Missing explicit responsibility points
- Implicit acceptance of AI output
- Workflow convenience overriding decision boundaries

### Detection
- Decision logs lack human identity
- Decision timestamps are missing
- Confirmation steps are skipped

### Severity
Critical (system-level safety failure)

---

## 2. Ghost Decisions

### Description
Actions occur without an accountable decision owner.

### Symptoms
- “The system decided”
- “It just happened”
- “AI did it”

### Root Causes
- Merged pathway steps
- Automated confirmation
- Silent defaults
- Background execution

### Detection
- Action executed without ERP
- No explicit confirmation recorded
- Decision boundary crossed by automation

### Severity
Critical (unrecoverable accountability loss)

---

## 3. Authority Leakage

### Description
AI gains de facto authority without explicit delegation.

### Symptoms
- AI output treated as final
- Human role becomes rubber-stamp
- Confirmation becomes habitual or automatic

### Root Causes
- UX minimizing friction
- Over-optimization for speed
- Trust accumulation without design limits

### Detection
- Confirmation time drops to near-zero
- Rejection rate approaches zero
- Human intervention disappears

### Severity
High (pre-collapse state)

---

## 4. Autonomy Drift

### Description
System autonomy increases unintentionally over time.

### Symptoms
- Gradual removal of confirmation steps
- Batch execution added “temporarily”
- Emergency shortcuts become permanent

### Root Causes
- No explicit autonomy ceiling
- Temporary automation without expiration
- Operational pressure

### Detection
- Change logs show shrinking human involvement
- Exceptions become defaults
- Automation scope expands silently

### Severity
High (latent catastrophic risk)

---

## 5. Silent Execution

### Description
Irreversible actions occur without perceptible decision moments.

### Symptoms
- No interruptive UI
- No felt moment of responsibility
- Actions happen in background

### Root Causes
- Async execution
- Auto-apply patterns
- Invisible confirmations

### Detection
- Humans cannot recall decision moment
- Logs exist but humans don’t remember acting

### Severity
Critical (ethical failure)

---

## 6. Responsibility Inheritance Fallacy

### Description
Responsibility is assumed to transfer automatically.

### Symptoms
- “The team decided”
- “The process approved it”
- “The policy allows it”

### Root Causes
- Role-based instead of person-based responsibility
- Missing decision ownership binding
- Organizational abstraction

### Detection
- No individual named in decision log
- Responsibility assigned to group or system

### Severity
High (organizational safety failure)

---

## 7. Model Blame Displacement

### Description
Failures are attributed to the model instead of the system design.

### Symptoms
- “The model hallucinated”
- “AI made a mistake”
- Retraining used as solution

### Root Causes
- Lack of responsibility pathway awareness
- Model-centric thinking
- Architecture ignored

### Detection
- Fixes focus on prompts or models only
- No workflow changes after incidents

### Severity
Medium → High (prevents learning)

---

## Safety-LCA Rule of Failure

> If a failure can occur without a human explicitly deciding,
> the architecture is broken.

---

## Final Note

These failures are **predictable**.  
They are **repeatable**.  
They are **designable away**.

Safety-LCA exists to make them impossible by construction.
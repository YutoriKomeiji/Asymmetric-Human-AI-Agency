# Asymmetric-Human-AI-Agency
A design principle and reference architecture for AI systems where decision authority is intentionally asymmetric: humans retain final agency, AI remains a bounded, non-sovereign actor. Focused on safety, responsibility pathways, and prevention of silent autonomy drift.
What this is
Asymmetric Human–AI Agency (AHAA) is a design principle and reference architecture for AI systems in which decision authority is intentionally asymmetric:
humans retain final agency, while AI remains a bounded, non-sovereign actor.
This repository defines how to prevent silent autonomy drift while still enabling powerful AI-assisted work, by structurally separating capability from authority.
Why this exists
Most AI failures are not caused by model errors alone, but by agency misalignment:
AI outputs are treated as decisions, not suggestions
Responsibility pathways are implicit or missing
Autonomy increases silently through workflow design
Humans lose effective veto power without noticing
This project addresses that failure mode at the architectural level, not through policy or ethics statements.
Core principle
Capability may be delegated.
Authority must not be.
AI can propose, simulate, summarize, generate, and optimize —
but only humans can commit, decide, and bear responsibility.
This asymmetry is not a limitation.
It is a safety mechanism.
What “Asymmetric” means here
Humans are sovereign agents
AI is a bounded tool with no final authority
Responsibility flows only through human decision points
All irreversible actions require explicit human confirmation
AI outputs are never treated as facts by default
What this repository contains
Design principles for asymmetric agency systems
Reference architectures (Safety-LCA, responsibility pathways)
Failure mode taxonomy (autonomy drift, authority leakage)
Practical design patterns for real systems
Documentation-first safety engineering approach
This is not a model, SDK, or product.
It is a design substrate for safe human–AI systems.
Who this is for
AI system architects
Safety & governance engineers
Product designers of AI-enabled workflows
Researchers in alignment, HCI, and socio-technical systems
Organizations deploying AI in high-stakes contexts
Philosophy
We do not aim to make AI more human.
We aim to make humans remain human in the presence of powerful AI.
License
This work is licensed under CC BY-NC 4.0.
Commercial use requires explicit permission.

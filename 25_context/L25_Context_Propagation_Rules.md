<!--
CANONICAL: TRUE
LAYER: L25
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L25 — Context Propagation (How Context Moves, Evolves & Constrains Action)
Defines how contextual information is carried forward, transformed, inherited, constrained, or terminated across the Sovereign Substrate. Context determines how actions are interpreted, which rules apply, and how meaning persists across event sequences.

## 25.0 Purpose
L25 establishes the canonical rules for:
- How context is attached to events, actors, objects, and processes  
- How context flows through causal chains and provenance  
- How context shapes what actions are valid, safe, or permitted  
- How context influences ADT/MAIAi decision-making  
- How context is transformed or terminated  
- How context enters and exits a domain or federated boundary  

Context propagation prevents ambiguity, ensures deterministic interpretation, and enables situation-aware governance.

## 25.1 Scope
Context applies to:
- Human, ADT, MAIAi, and system actors  
- All events and state transitions  
- All provenance and lineage objects  
- All temporal, spatial, jurisdictional, and policy domains  
- All permissions, capabilities, and accountability relationships  
- All AI/ADT reasoning, predictions, and autonomous actions  
- All cross-substrate, federated, or inter-jurisdictional interactions  

Every canonical action is interpreted inside a context window.

## 25.2 Core Principles
1. **Context is mandatory** — no event may be interpreted without contextual framing.  
2. **Context is inherited** — child events receive context from parents unless redefined.  
3. **Context is layered** — multiple contexts may apply simultaneously.  
4. **Context is deterministic** — identical sequences yield identical context propagation.  
5. **Context is bounded** — every context has a domain of validity.  
6. **Context is auditable** — provenance and audits must reflect context flow.  
7. **Context constrains action** — permissions, capabilities, and accountability depend on context.

## 25.3 Context Object Model
A canonical context record must contain:

### Context Identity
- Context ID  
- Origin event or state  
- Context type  

### Context Content
- Declarative parameters  
- Effective scope  
- Propagation mode  

### Anchoring
- Timestamp (L14)  
- Causal parents (L15)  
- Provenance references (L18)

### Cryptographic Attributes
- Context hash  
- Issuer signatures  
- Optional multi-signature approval  

## 25.4 Types of Context
- Temporal  
- Spatial / Domain  
- Intent  
- Policy / Regulatory  
- Risk  
- Capability  
- AI / ADT  
- Custody / Control  

## 25.5 Context Propagation Rules
- **Inheritance** — flows forward by default  
- **Extension** — accumulates parameters  
- **Restriction** — narrows allowable actions  
- **Override** — permitted only with capability and permission  
- **Termination** — explicit or condition-based  
- **Cross-boundary propagation** — filtered or transformed  
- **AI/ADT propagation** — mandatory internal and external attachment  

Failure to propagate context invalidates the action.

## 25.6 Context Validation Rules
Before execution, the substrate validates:
1. Completeness  
2. Correctness  
3. Continuity  
4. Alignment with identity, capability, permission  
5. Freshness  
6. Safety  
7. Cross-context consistency  

Invalid context blocks execution.

## 25.7 Context Transformation
Context may change via:
- Actor-driven modification  
- System-driven evolution  
- Event-driven triggers  

All transformations must be authenticated, recorded, and traceable.

## 25.8 Context Merging & Branching
- **Merging** requires compatibility and explicit resolution  
- **Branching** preserves traceable divergence  

## 25.9 Observability & Reporting
The substrate must expose:
- Context lineage graphs  
- Parameter evolution timelines  
- Cross-boundary transformation logs  
- AI/ADT context reports  
- Conflict detection tools  

## 25.10 Interaction With Other Layers
L11–L24 collectively ensure context authenticity, determinism, legality, auditability, accountability, and enforcement.

## 25.11 Invariants
1. CONTEXT_REQUIRED  
2. CONTEXT_INHERITED  
3. CONTEXT_TRACEABLE  
4. CONTEXT_DETERMINISTIC  
5. CONTEXT_SAFE  
6. CONTEXT_BOUND  
7. CONTEXT_AWARE_AGENTS  

## 25.12 Real-World Capability Enabled by Context Propagation

Context propagation enables **policy-, jurisdiction-, and risk-aware automation at scale**.

It allows:
- The same action to be evaluated differently based on jurisdiction, time, or risk without rewriting logic.
- AI and automated systems to operate safely across domains while respecting legal and operational boundaries.
- Governments and enterprises to enforce situational rules (e.g., emergency powers, sanctions, compliance windows) deterministically.
- Federated systems to interoperate without leaking sensitive policy or intent.
- Auditors and courts to reconstruct *why* an action was permitted, not just *that* it occurred.

Context becomes **a first-class control surface**, replacing implicit assumptions with enforceable, machine-verifiable meaning.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

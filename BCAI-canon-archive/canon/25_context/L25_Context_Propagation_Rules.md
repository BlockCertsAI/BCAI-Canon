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
3. **Context is layered** — multiple contexts (temporal, spatial, policy, jurisdictional) may apply simultaneously.  
4. **Context is deterministic** — identical sequences yield identical context propagation.  
5. **Context is bounded** — every context has a domain of validity.  
6. **Context is auditable** — provenance (L18) and auditability (L19) must reflect contextual flows.  
7. **Context constrains action** — permissions, capabilities, and accountability depend on context (L22–L24).  

## 25.3 Context Object Model
A canonical context record must contain:

### Context Identity
- Context ID  
- Origin event or state  
- Type (temporal, spatial, jurisdictional, operational, intent, policy, risk, environmental)

### Context Content
- Declarative parameters (rules, constraints, metadata)  
- Effective range (event scope, object scope, domain scope)  
- Propagation mode (inherit, restrict, override, terminate)

### Anchoring
- Timestamp (L14)  
- Causal parents (L15)  
- Provenance references (L18)

### Cryptographic Attributes
- Context hash  
- Signatures of context issuers  
- Optional multi-signature for policy-level contexts  

## 25.4 Types of Context

### 25.4.1 Temporal Context
Defines time windows, deadlines, validity periods, ordering constraints.

### 25.4.2 Spatial or Domain Context
Defines jurisdiction, domain boundary, substrate partition.

### 25.4.3 Intent Context
Describes actor purpose, workflow goal, or objective of the action.

### 25.4.4 Policy/Regulatory Context
Defines rules, obligations, governance requirements.

### 25.4.5 Risk Context
Defines operational risk, threat level, special handling requirements.

### 25.4.6 Capability Context
Defines constraints on what actions are possible or safe (links to L23).

### 25.4.7 AI/ADT Context
Defines:
- Observed state  
- Active policy windows  
- Autonomy boundaries  
- Required oversight  

### 25.4.8 Custody/Control Context
Defines:
- Current custodian  
- Allowed transformations  
- Handoff history  

## 25.5 Context Propagation Rules
Context propagation must obey the following:

### 25.5.1 Inheritance
Child events inherit context from parent events unless explicitly modified or terminated.

### 25.5.2 Extension
Context may accumulate additional parameters as actions progress.

### 25.5.3 Restriction
Context may become more restrictive as risks or obligations increase.

### 25.5.4 Override
Authorized actors may replace inherited context if:
- They hold capability (L23)  
- They hold permission (L22)  
- Override stays within legal and policy bounds  

### 25.5.5 Termination
Context ceases when:
- It reaches end-of-life  
- Domain boundaries change  
- It is explicitly terminated  
- The triggering conditions are satisfied  

### 25.5.6 Cross-Boundary Propagation
When crossing a domain or jurisdiction:
- Only approved context types may propagate  
- Sensitive context must be redacted or transformed  
- Zero-knowledge context proofs may substitute for raw content  

### 25.5.7 AI/ADT Propagation Rules
AI and ADT must:
- Maintain internal contextual awareness  
- Propagate context across reasoning steps  
- Attach context to all autonomous actions  
- Never operate “context-free”  

Failure to propagate context invalidates the action.

## 25.6 Context Validation Rules
Before executing an action, the substrate validates:

1. **Context completeness** — required context types are present.  
2. **Context correctness** — parameters match current environment.  
3. **Context continuity** — no broken inheritance chain.  
4. **Context alignment** — matches actor identity, capability, and permission.  
5. **Context freshness** — no expired or outdated context.  
6. **Context safety** — context does not violate governance or risk constraints.  
7. **Cross-context compatibility** — no contradictions between overlapping contexts.  

Actions without valid context must be rejected.

## 25.7 Context Transformation
Context may transform under:

### Actor-driven transformation  
Authorized modifications by human, ADT, MAIAi, or governance actors.

### System-driven transformation  
Context changes automatically based on:
- Time evolution  
- Domain transitions  
- Policy updates  
- Risk detection  

### Event-driven transformation  
Certain events trigger context extension or restriction.

All transformations must be:
- Authenticated  
- Recorded  
- Traceable  

## 25.8 Context Merging & Branching

### Merging
When two event streams converge, context must merge if:
- Both are compatible  
- No contradictions exist  
- Shared context is clearly defined  

### Branching
When an event produces multiple future event paths:
- Each child inherits context  
- Each may diverge as needed  
- Divergence must remain traceable  

## 25.9 Observability & Reporting
The substrate must expose:
- Context lineage  
- Context parameter history  
- Cross-boundary transformation logs  
- AI/ADT context decision reports  
- Multi-context conflict detectors  

Auditors must reconstruct:
- Why context was present  
- How it evolved  
- Whether propagation followed rules  
- Which context influenced AI/ADT actions  

## 25.10 Interaction With Other Layers
- L11 ensures context authenticity (signatures, hashes).  
- L12 ensures deterministic reconstruction of context flows.  
- L13 ensures context respects object mutability.  
- L14 defines time-based context rules.  
- L15 ensures causal correctness of context inheritance.  
- L16 ensures context is preserved or compensated in undo sequences.  
- L17 ensures context integrity after recovery.  
- L18 binds context to provenance.  
- L19 ensures context is auditable.  
- L20 attaches attestations to context changes.  
- L21 handles context during handoffs.  
- L22 ensures permissions align with context.  
- L23 ensures actor capability is context-appropriate.  
- L24 ensures accountability maps to context windows.

## 25.11 Invariants
1. CONTEXT_REQUIRED — no event may execute without context.  
2. CONTEXT_INHERITED — context flows forward unless explicitly changed.  
3. CONTEXT_TRACEABLE — all contextual changes must appear in provenance.  
4. CONTEXT_DETERMINISTIC — identical inputs → identical context state.  
5. CONTEXT_SAFE — context cannot bypass governance or risk controls.  
6. CONTEXT_BOUND — each context must have a valid domain of effect.  
7. CONTEXT_AWARE_AGENTS — ADT/MAIAi must operate within active context.  

## 25.12 Informative Guidance
Context should be minimal but sufficient for unambiguous interpretation.  
Context drift should be monitored, especially for AI/ADT autonomy.  
Contexts governing risk, jurisdiction, or policy should be restricted from untrusted propagation.  
Federated contexts should use privacy-preserving forms.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

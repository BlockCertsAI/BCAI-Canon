<!--
CANONICAL: TRUE
LAYER: L44
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L44 — State Transition Rules (Legal, Safe & Canonical Mutation of Substrate State)
Defines the complete rule system governing how state transitions are allowed to occur within the Sovereign Substrate. Unlike L33 (Transition Model), which defines *structure*, L44 defines the *rules* that constrain, validate, and enforce legal state mutation.

The State Transition Rules answer:  
**“Under what rules may the substrate change its state — and how are illegal transitions prevented?”**

---

## 44.0 Purpose
L44 establishes:
- The legal boundaries for all state transitions  
- Which transitions are valid, invalid, or conditionally valid  
- How validation and verification constraints apply during mutation  
- How causality, provenance, and temporal rules regulate state changes  
- How governance, constraints, and enforcement modify or override transitions  
- How state consistency survives consensus, finality, and recovery  

State transitions are the engine of the substrate.  
L44 ensures that *only safe, deterministic, and lawful transitions* become part of canonical truth.

---

## 44.1 Scope
Applies to:
- All transitions (L33)  
- All state objects (L32)  
- All transitions proposed by humans, agents, governance, or federated domains  
- All identity-driven actions  
- All provenance updates (L18)  
- All authorization paths (L42)  
- All constraint bindings (L31)  
- All consensus/finality operations (L34–L35)  
- Undo/rollback (L16) and recovery (L38)  

State transitions are the *boundary* between potential and actual reality.

---

## 44.2 Core Principles
1. **State must only change through legal transitions.**  
2. **All transitions must be deterministic.**  
3. **All transitions must be authenticated and authorized.**  
4. **All transitions must respect causality and temporal order.**  
5. **All transitions must satisfy constraints (L31).**  
6. **All transitions must be validated (L27) and verified (L28).**  
7. **All transitions must be provenance-complete.**  
8. **No transition may violate governance rules.**  
9. **No transition may introduce forked or ambiguous state.**  
10. **Finalized transitions become immutable.**  

---

## 44.3 Transition Rule Object Model
Each transition must be evaluated against a canonical Transition Rule Object:

### Inputs
- Actor identity & authentication (L41)  
- Authorization and capabilities (L42–L23)  
- State snapshot (L32)  
- Transition specification (L33)  
- Provenance references (L18)  
- Constraint context (L31)  
- Governance overlays (L29)  

### Outputs
- Transition decision (VALID / INVALID / CONDITIONAL / ESCALATE)  
- Resulting state delta  
- Required post-transition enforcement (L40)  
- Evidence bundle (validation + verification)  
- Provenance update instructions  

### Anchoring
- Transition hash  
- Causal anchors (L37)  
- Timestamp  
- Policy version  

No transition lacking a complete rule object may proceed.

---

## 44.4 Legal State Transition Requirements

### 44.4.1 Authentication Requirement
Every transition must:
- Originate from an authenticated identity  
- Include authentication proofs  
- Pass key ownership verification  

Unauthenticated transitions → **HARD BLOCK**.

---

### 44.4.2 Authorization Requirement
The actor must:
- Possess the required permission(s)  
- Possess the required capability(ies)  
- Have valid delegations (if any)  
- Not exceed safety ceilings  

Unauthorized transitions → **BLOCK & REVOKE**.

---

### 44.4.3 Causality Requirement (L37)
Transitions must:
- Reference valid parents  
- Establish legal cause–effect chains  
- Avoid causal cycles  
- Maintain dependency correctness  

Causal violations → **INVALID TRANSITION**.

---

### 44.4.4 Temporal Requirement (L14)
Transitions must comply with:
- Legal timestamp windows  
- Ordering requirements  
- Domain-specific time rules  

Temporal violations → **INVALID OR OUT-OF-WINDOW**.

---

### 44.4.5 Provenance Requirement (L18)
Transitions must:
- Append valid lineage  
- Maintain custody chain integrity  
- Include transformation metadata  

Missing provenance → **NONCANONICAL → REJECT**.

---

### 44.4.6 Constraint Requirement (L31)
Transitions must:
- Respect hard constraints  
- Respect soft constraints where applicable  
- Avoid safety violations  
- Stay within risk bounds  

Constraint violations → **ABORT & ESCALATE**.

---

### 44.4.7 Structural Consistency Requirement
Transitions must:
- Produce legal state deltas  
- Preserve schema integrity  
- Avoid incomplete or malformed objects  

Structural violations → **INVALID**.

---

### 44.4.8 Governance Requirement (L29)
Transitions must:
- Follow active governance policies  
- Respect emergency directives  
- Respect domain-level overrides  
- Submit to governance enforcement  

Governance violations → **ESCALATION**.

---

### 44.4.9 Verification Requirement (L28)
Transitions must be:
- Signature-verified  
- Hash-verified  
- Proof-complete  

Verification failures → **REJECTION**.

---

### 44.4.10 Validation Requirement (L27, L39)
Transitions must undergo:
- Pre-transition validation  
- Pre-commit validation  
- Commit-stage validation  
- Replay validation  

Validation failures → **FAIL**.

---

## 44.5 State Delta Rules

### 44.5.1 Frozen State Protection
Once finalized, state cannot be:
- Modified  
- Replaced  
- Overwritten  

Only forward evolution permitted.

---

### 44.5.2 Delta Minimality
Transitions must:
- Modify only what is allowed  
- Avoid unintended side effects  
- Declare all modifications explicitly  

---

### 44.5.3 Delta Determinism
Given:
- Same prior state  
- Same context  
- Same transition  

The resulting delta must always be identical.

---

### 44.5.4 Delta Safety
Deltas must:
- Maintain substrate invariants  
- Not reduce security posture  
- Not break data integrity  

---

## 44.6 Transition Ordering Rules

### 44.6.1 Causal Ordering
Effects follow causes.

### 44.6.2 Temporal Ordering
Earlier timestamps precede later.

### 44.6.3 Governance Ordering
Governance directives override other transitions.

### 44.6.4 Deterministic Ordering
Conflicts resolved deterministically (L12).

---

## 44.7 Illegal Transition Conditions
A transition is illegal if:
- Actor unauthenticated  
- Actor unauthorized  
- Delegation invalid  
- Provenance incomplete  
- Constraint violated  
- Governance override violated  
- Structural integrity broken  
- Causality or temporal rules broken  
- Any verification or validation step fails  

Illegal transitions → **BLOCKED + LOGGED + ENFORCED (L40)**.

---

## 44.8 Transition Enforcement (Integration With L40)
Enforcement may:
- BLOCK transition  
- QUARANTINE transition  
- REVOKE capability  
- ESCALATE to governance  
- INITIATE recovery if severe  

Enforcement ensures illegal transitions cannot propagate.

---

## 44.9 Transition Behavior for Agents (L26)
Agents must:
- Propose deterministic transitions  
- Provide reasoning traces  
- Respect constraint ceilings  
- Operate strictly within authorization  

Agents may NOT:
- Speculate unauthorized deltas  
- Produce multi-path or ambiguous proposals  
- Mutate state without explicit governance or capability  

---

## 44.10 Transition Behavior During Recovery (L38)
During recovery:
- Illegal transitions purged  
- Partial transitions removed  
- Transitions replayed deterministically  
- Governance may override or invalidate transitions  
- State reconstituted from canonical provenance  

Recovery must restore legal transitions only.

---

## 44.11 Transition Behavior in Federation
Cross-domain transitions must:
- Pass identity verification  
- Pass provenance verification  
- Pass finality verification  
- Align with local governance  

Federated illegal transitions → **QUARANTINE**.

---

## 44.12 Observability & Reporting
System must expose:
- Transition logs  
- Failure logs  
- Causal dependency maps  
- Validation & verification evidence  
- Provenance updates  
- Governance intervention logs  
- Constraint violations  

Auditors must understand:
- Why a transition occurred  
- Why it was accepted or rejected  
- How it modified state  

---

## 44.13 Interaction With Other Layers
- **L11** — cryptographic security of transitions.  
- **L12** — deterministic transition outcomes.  
- **L13** — mutability restrictions.  
- **L14** — temporal correctness.  
- **L15/L37** — causal correctness.  
- **L16/L38** — rollback and recovery enforcement.  
- **L17** — restore transitions correctly.  
- **L18** — provenance integrity.  
- **L19** — transition auditability.  
- **L20** — attestations verifying transition truth.  
- **L21** — custody implications of mutation.  
- **L22–L24** — permissions, capabilities, accountability.  
- **L25** — context-bound transition legality.  
- **L26** — agent constraints.  
- **L27–L28** — validation and verification.  
- **L29** — governance priority rules.  
- **L30–L31** — delegation and constraints.  
- **L32–L33** — state and transition structure.  
- **L34–L36** — consensus, finality, fork prevention.  
- **L39** — validation model persistence.  
- **L40** — enforcement of transition legality.  
- **L41–L42** — authentication & authorization clarity.  
- **L43** — identity persistence  

---

## 44.14 Invariants
1. STATE_CHANGE_LAWFUL — no unlawful transition may modify state.  
2. STATE_CHANGE_DETERMINISTIC — transitions yield one reproducible outcome.  
3. STATE_CHANGE_AUTHORIZED — only permitted actors may mutate.  
4. STATE_CHANGE_VERIFIABLE — every mutation must have evidence.  
5. STATE_CHANGE_TRACEABLE — provenance must record lineage.  
6. STATE_CHANGE_SAFE — constraints override permissions.  
7. STATE_CHANGE_FINAL — finalized transitions immutable.  

---

## 44.15 Informative Guidance
State transitions are the heart of system safety.  
If state transition failures increase, governance or constraint policy should tighten.  
Agents should model transitions conservatively, avoiding ambiguous behaviors.  
Federated transitions must be treated as high risk and validated deeply.  
Recovery should never restore illegal transitions — only lawful ones.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

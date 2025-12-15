<!--
CANONICAL: TRUE
LAYER: L33
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L33 — Transition Model (How Canonical State Moves, Evolves & Becomes New Truth)
Defines the complete rules governing how the Sovereign Substrate moves from one canonical state to the next — including requirements, constraints, sequencing, validation, verification, provenance anchoring, governance integration, and agent participation.

The Transition Model answers the question:  
**“How does the system change — safely, lawfully, and deterministically?”**

## 33.0 Purpose
L33 establishes:
- How transitions are defined, structured, and represented  
- How actors initiate and complete transitions  
- How transitions interact with identity, state, provenance, context, and governance  
- How ADT/MAIAi may propose or execute transitions  
- How transitions are validated (L27) and verified (L28)  
- How transitions maintain safety and ordering  
- How transitions survive undo (L16) and recovery (L17)  

Transitions are the *engine of change* in the Sovereign Substrate.

## 33.1 Scope
The Transition Model applies to:
- Identity transitions  
- Object and data transitions  
- State transitions (L32)  
- Permission/capability/accountability transitions (L22–L24)  
- Context transitions (L25)  
- Custody transitions (L21)  
- Delegation transitions (L30)  
- Governance-induced transitions (L29)  
- ADT/MAIAi agent transitions  
- Cross-domain and federated transitions  

No actor or domain may bypass transition rules.

## 33.2 Core Principles
1. **Transitions must be intentional** — no implicit or silent changes.  
2. **Transitions must be deterministic** — same inputs → same new canonical state (L12).  
3. **Transitions must be authenticated** — identity and signatures are mandatory.  
4. **Transitions must be legal** — allowed by mutability rules (L13).  
5. **Transitions must be ordered** — time-first (L14), cause-first (L15).  
6. **Transitions must be safe** — evaluated against constraints (L26, L31).  
7. **Transitions must be provable** — with evidence bundles (L28).  
8. **Transitions must be final when canonical** — cannot be rewritten retroactively.  

## 33.3 Transition Object Model
Each transition must include:

### Actor
- Initiator identity  
- Delegation rights (if applicable, L30)  
- Required permissions/capabilities (L22–L23)  

### Transition Intent
- Operation type  
- Target object or state  
- Expected outcome  
- Context dependencies (L25)  
- Preconditions  

### Transition Mechanics
- Input state  
- Proposed state delta  
- Required proofs  
- Constraint evaluation results  

### Cryptographic Binding
- Transition hash  
- Actor signature  
- Optional multisig for Critical transitions  

### Anchoring
- Timestamp and temporal ordering  
- Causal parent  
- Provenance insertion (L18)  
- Governance references (if triggered)  

## 33.4 Types of Transitions

### 33.4.1 Creation Transitions
Establish new objects, identities, or agents:  
- Bind origin data  
- Generate initial lineage  
- Create canonical “first state”  

### 33.4.2 Mutation Transitions
Modify existing state:  
- Apply legal state transformations  
- Preserve prior state immutability  
- Update lineage and hashes  

### 33.4.3 Activation / Deactivation
Toggle state, capabilities, permissions, or systems:  
- Activate contexts  
- Suspend roles or domains  
- Enable or disable agents  

### 33.4.4 Custody Transitions (L21)
Transfer control, ownership, or operational authority:  
- Require full chain-of-custody tracking  
- Require explicit authenticated handoffs  

### 33.4.5 Delegation Transitions (L30)
Grant or revoke delegated authority:  
- Update responsibility and capability chains  
- Bind delegation provenance  

### 33.4.6 Governance Transitions (L29)
Apply governance-induced changes:  
- Override or impose rules  
- Modify policy or system-level parameters  

### 33.4.7 Agent Transitions (ADT/MAIAi)
Adjust agent internal state or autonomy:  
- Capability ceilings  
- Constraint layers  
- Mode switching  

### 33.4.8 Federated Transitions
Synchronize or translate transitions across substrate boundaries:  
- Require cross-domain proofs  
- Record federated provenance markers  

## 33.5 Transition Lifecycle

### 33.5.1 Initiation
Actor forms transition intent and attaches required proofs.

### 33.5.2 Pre-Validation (Safety Check)
System checks:
- Constraints (L26, L31)  
- Permissions/capabilities (L22, L23)  
- Context windows (L25)  
- Governance boundaries (L29)  

If failed → transition is blocked.

### 33.5.3 Validation (L27)
Logical, structural, legal correctness.

### 33.5.4 Verification (L28)
Cryptographic and truth-checking:
- Signatures  
- Hashes  
- Causal and temporal consistency  
- Provenance continuity  

### 33.5.5 Execution
Apply the state delta to produce new provisional state.

### 33.5.6 Canonicalization
Transition becomes canonical only if:
- All validations succeed  
- All verifications succeed  
- Governance boundaries permit  
- Provenance insertion succeeds  
- No higher-order constraints are violated  

### 33.5.7 Finalization
Transition is now permanent and non-rewriteable.

## 33.6 Forbidden Transitions
The system must reject:
- Any transition without identity or signatures  
- Any transition violating mutability (L13)  
- Retroactive or backdated transitions  
- Causal impossibilities or loops  
- Temporal order violations (L14)  
- Missing or broken provenance  
- Authority impersonation  
- ADT/MAIAi transitions exceeding autonomy  
- Delegations that violate governance  

## 33.7 Transition Ordering Rules

### 33.7.1 Temporal Order (L14)
All transitions must obey:
- Time windows  
- Expiration conditions  
- Clock monotonicity  

### 33.7.2 Causal Order (L15)
Transition must:
- Reference valid parents  
- Maintain DAG structure  
- Avoid cycles  

### 33.7.3 Cross-Domain Ordering
Federated transitions must:
- Provide synchronization proofs  
- Map causality across boundaries  
- Preserve ordering semantics  

## 33.8 Agent (ADT/MAIAi) Transition Rules

### 33.8.1 Proposal Limits
Agents may propose transitions only when:
- Within capability bounds (L23)  
- Within permission ceilings (L22)  
- Constraints allow (L26)  
- Governance permits  

### 33.8.2 Execution Limits
Agents may execute transitions only when:
- Supervision conditions are satisfied  
- Risk thresholds are not exceeded  
- Required attestations are produced  

### 33.8.3 Escalation
Agents must escalate instead of guessing when:
- Preconditions unclear  
- Constraint ambiguity exists  
- High-risk transition detected  

## 33.9 Transition Behavior in Undo (L16) & Recovery (L17)

### Undo
- Reverts to prior canonical state  
- Must maintain lineage  
- Must verify cryptographic continuity  

### Recovery
- Reconstructs the canonical transition sequence  
- Eliminates noncanonical forks  
- Replays only verified transitions  

## 33.10 Observability & Reporting
The substrate must expose:
- Transition logs  
- Transition lineage graphs  
- Diff tools (before/after state)  
- Governance-induced transitions  
- AI/ADT transition traces  
- Anomaly and violation reports  

Auditors must reconstruct:
- Why transitions occurred  
- How they were validated  
- Whether governance was followed  
- Whether actors behaved within constraints  

## 33.11 Interaction With Other Layers
- **L11** — provides cryptographic primitives for transitions.  
- **L12** — ensures deterministic transition evaluation.  
- **L13** — governs legality of state changes.  
- **L14** — provides temporal ordering rules.  
- **L15** — provides causal ordering rules.  
- **L16** — defines undo behavior.  
- **L17** — defines recovery behavior.  
- **L18** — ties transitions into provenance.  
- **L19** — audits transitions.  
- **L20** — provides attestations for transitions.  
- **L21** — governs custody transitions.  
- **L22** — permissions required for transitions.  
- **L23** — capabilities required.  
- **L24** — accountability for transition outcomes.  
- **L25** — context propagation into transitions.  
- **L26** — agent constraint compliance.  
- **L27** — transition validation.  
- **L28** — transition verification.  
- **L29** — governance influence on transitions.  
- **L30** — delegation transitions.  
- **L31** — constraints governing transitions.  
- **L32** — how transitions create new state.  

## 33.12 Invariants
1. TRANSITION_AUTHENTIC — must be signed, verified, and traceable.  
2. TRANSITION_ORDERED — must follow temporal and causal rules.  
3. TRANSITION_SAFE — must satisfy all constraints.  
4. TRANSITION_PROVENANCED — must enter canonical lineage.  
5. TRANSITION_NONREVISION — cannot be rewritten once canonical.  
6. TRANSITION_CONTEXTUAL — context must be applied at evaluation time.  
7. TRANSITION_DETERMINISTIC — must produce deterministic results.  

## 33.13 Informative Guidance
Treat transitions as atomic, verifiable units of change.  
AI/ADT transitions require heightened scrutiny.  
Federated transitions must avoid state drift.  
Transition storms (rapid bursts) should trigger risk checks.  
Canonicalization should remain conservative and safety-focused.  

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

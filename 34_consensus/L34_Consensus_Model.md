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
- Permission, capability, and accountability transitions (L22–L24)  
- Context transitions (L25)  
- Custody transitions (L21)  
- Delegation transitions (L30)  
- Governance-induced transitions (L29)  
- ADT/MAIAi agent transitions  
- Cross-domain and federated transitions  

No actor or domain may bypass transition rules.

## 33.2 Core Principles
1. **Transitions must be intentional** — no implicit or silent changes.  
2. **Transitions must be deterministic** — same inputs produce the same canonical state (L12).  
3. **Transitions must be authenticated** — identity and signatures are mandatory.  
4. **Transitions must be legal** — allowed by mutability rules (L13).  
5. **Transitions must be ordered** — temporal first (L14), causal first (L15).  
6. **Transitions must be safe** — evaluated against constraints (L26, L31).  
7. **Transitions must be provable** — via cryptographic evidence (L28).  
8. **Transitions are final when canonical** — no retroactive revision.  

## 33.3 Transition Object Model
Each transition must include:

### Actor
- Initiator identity  
- Delegation authority if applicable (L30)  
- Required permissions and capabilities (L22–L23)  

### Transition Intent
- Operation type  
- Target object or state  
- Expected outcome  
- Context dependencies (L25)  
- Preconditions  

### Transition Mechanics
- Input (prior) state  
- Proposed state delta  
- Required proofs  
- Constraint evaluation results  

### Cryptographic Binding
- Transition hash  
- Actor signature  
- Optional multi-signature for Critical transitions  

### Anchoring
- Timestamp and temporal ordering  
- Causal parent reference  
- Provenance insertion (L18)  
- Governance references when applicable  

## 33.4 Types of Transitions

### 33.4.1 Creation Transitions
Establish new objects, identities, or agents:
- Bind origin data  
- Generate initial lineage  
- Create first canonical state  

### 33.4.2 Mutation Transitions
Modify existing state:
- Apply lawful transformations  
- Preserve historical immutability  
- Update lineage and hashes  

### 33.4.3 Activation / Deactivation
Toggle state or authority:
- Activate contexts or domains  
- Suspend roles, permissions, or agents  

### 33.4.4 Custody Transitions (L21)
Transfer control or ownership:
- Require authenticated handoff  
- Preserve full chain-of-custody  

### 33.4.5 Delegation Transitions (L30)
Grant or revoke delegated authority:
- Update capability and responsibility chains  
- Bind delegation provenance  

### 33.4.6 Governance Transitions (L29)
Apply governance-directed changes:
- Override rules  
- Enforce policy or system parameters  

### 33.4.7 Agent Transitions (ADT/MAIAi)
Adjust agent state or autonomy:
- Capability ceilings  
- Constraint layers  
- Execution modes  

### 33.4.8 Federated Transitions
Cross-substrate synchronization:
- Require federated proofs  
- Record cross-domain provenance markers  

## 33.5 Transition Lifecycle

### 33.5.1 Initiation
Actor declares intent and attaches required proofs.

### 33.5.2 Pre-Validation (Safety Gate)
System evaluates:
- Constraints (L26, L31)  
- Permissions and capabilities (L22–L23)  
- Context windows (L25)  
- Governance boundaries (L29)  

Failure blocks the transition.

### 33.5.3 Validation (L27)
Structural, logical, and legal correctness.

### 33.5.4 Verification (L28)
Cryptographic truth checks:
- Signatures  
- Hash integrity  
- Temporal and causal alignment  
- Provenance continuity  

### 33.5.5 Execution
Apply the state delta to produce a provisional new state.

### 33.5.6 Canonicalization
Transition becomes canonical only if:
- All validations succeed  
- All verifications succeed  
- Governance permits  
- Provenance insertion succeeds  
- No higher-order constraints are violated  

### 33.5.7 Finalization
Canonical transition becomes permanent and non-rewriteable.

## 33.6 Forbidden Transitions
The substrate must reject:
- Unsigned or unauthenticated transitions  
- Mutability violations (L13)  
- Retroactive or backdated transitions  
- Causal loops or impossibilities  
- Temporal violations (L14)  
- Broken provenance chains  
- Authority impersonation  
- Agent actions exceeding autonomy  
- Governance-violating delegations  

## 33.7 Transition Ordering Rules

### 33.7.1 Temporal Ordering (L14)
Transitions must respect:
- Validity windows  
- Expiration rules  
- Monotonic clocks  

### 33.7.2 Causal Ordering (L15)
Transitions must:
- Reference valid parents  
- Preserve DAG structure  
- Avoid cycles  

### 33.7.3 Cross-Domain Ordering
Federated transitions must:
- Provide synchronization proofs  
- Preserve ordering semantics across domains  

## 33.8 Agent (ADT/MAIAi) Transition Rules

### 33.8.1 Proposal Limits
Agents may propose transitions only when:
- Within capability bounds (L23)  
- Within permission ceilings (L22)  
- Constraints permit (L26)  
- Governance allows  

### 33.8.2 Execution Limits
Agents may execute transitions only when:
- Supervision conditions are met  
- Risk thresholds are not exceeded  
- Required attestations are produced  

### 33.8.3 Escalation
Agents must escalate rather than guess when:
- Preconditions are unclear  
- Constraint ambiguity exists  
- High-risk transitions are detected  

## 33.9 Transition Behavior in Undo (L16) & Recovery (L17)

### Undo
- Reverts to the prior canonical state  
- Preserves lineage  
- Verifies cryptographic continuity  

### Recovery
- Reconstructs verified transition sequences  
- Eliminates noncanonical forks  
- Replays only validated transitions  

## 33.10 Observability & Reporting
The substrate must expose:
- Transition logs  
- Transition lineage graphs  
- Before/after state diffs  
- Governance-induced transition views  
- AI/ADT transition traces  
- Anomaly and violation reports  

Auditors must reconstruct:
- Why transitions occurred  
- How they were validated  
- Whether governance was followed  
- Whether actors remained within constraints  

## 33.11 Interaction With Other Layers
- **L11** — cryptographic primitives  
- **L12** — deterministic evaluation  
- **L13** — mutability legality  
- **L14** — temporal ordering  
- **L15** — causal ordering  
- **L16** — undo handling  
- **L17** — recovery handling  
- **L18** — provenance anchoring  
- **L19** — auditing  
- **L20** — attestations  
- **L21** — custody transitions  
- **L22** — permissions  
- **L23** — capabilities  
- **L24** — accountability  
- **L25** — context propagation  
- **L26** — agent constraints  
- **L27** — validation  
- **L28** — verification  
- **L29** — governance  
- **L30** — delegation  
- **L31** — constraints  
- **L32** — state creation  

## 33.12 Invariants
1. TRANSITION_AUTHENTIC — signed, verified, traceable.  
2. TRANSITION_ORDERED — temporal and causal compliance.  
3. TRANSITION_SAFE — all constraints satisfied.  
4. TRANSITION_PROVENANCED — enters canonical lineage.  
5. TRANSITION_FINAL — non-rewriteable once canonical.  
6. TRANSITION_CONTEXTUAL — evaluated within context.  
7. TRANSITION_DETERMINISTIC — identical input yields identical outcome.  

## 33.13 Informative Guidance
Treat transitions as atomic, verifiable units of change.  
AI/ADT transitions require heightened scrutiny.  
Federated transitions must avoid state drift.  
Transition storms should trigger risk analysis.  
Canonicalization should remain conservative and safety-first.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

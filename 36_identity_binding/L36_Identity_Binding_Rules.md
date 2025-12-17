<!--
CANONICAL: TRUE
LAYER: L36
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L36 — Fork Prevention Model (How the Substrate Avoids Divergent Truth & Ensures a Single Canonical Reality)
Defines the mechanisms that prevent the Sovereign Substrate from diverging into inconsistent branches of truth. Fork prevention ensures that **one and only one canonical history** can exist, eliminating split-brain states, race conditions, ambiguous transitions, and competing versions of reality.

Fork Prevention answers the question:  
**“How does the system guarantee that truth never diverges?”**

## 36.0 Purpose
L36 establishes:
- The architectural rules that make forks structurally impossible  
- How ordering, validation, verification, and constraints eliminate divergence  
- How governance ensures conflict resolution without forking  
- How ADT/MAIAi must behave to avoid creating divergent state proposals  
- How temporal, causal, and provenance rules maintain a single global truth  
- How federated domains avoid incompatible truth branches  

Fork Prevention is the substrate’s shield against chaos, ambiguity, and split truth.

## 36.1 Scope
Applies to:
- All transitions (L33)  
- State evolution (L32)  
- Consensus and finality formation (L34–L35)  
- Provenance lineage (L18)  
- Governance-induced updates (L29)  
- Delegated authority (L30)  
- AI/ADT proposals (L26)  
- Cross-domain or federated truth mapping  
- Undo/Recovery mechanisms (L16–L17)  

Fork prevention is substrate-wide and cannot be overridden.

## 36.2 Core Principles
1. **Single Canonical History** — only one global truth may exist at any time.  
2. **Deterministic Ordering** — events ordered identically everywhere prevent divergence.  
3. **Identity-Rooted Consensus** — PoA eliminates anonymous competition that causes forks.  
4. **Constraint Enforcement** — unsafe or conflicting transitions cannot enter canonical flow.  
5. **Governance Supremacy** — governance resolves conflicts, preventing parallel truths.  
6. **Strict Provenance** — lineage must form a single DAG with no branching contradictions.  
7. **No Competing Proposals** — transitions must obey ordering windows and constraints.  
8. **No Probabilistic Finality** — deterministic rules eliminate race-condition forks.  

## 36.3 Fork Object Model
A “fork risk” is tracked as a structured object containing:

### Inputs
- Conflicting transitions  
- Conflicting provenance parents  
- Conflicting temporal anchors  
- Competing governance directives  
- Agent-generated divergent proposals  

### Outputs
- Fork classification (TEMPORARY / INVALID / CRITICAL)  
- Required remediation action  
- Governance escalation flag  
- Diagnostic evidence  

### Anchoring
- Timestamp  
- Causal references  
- Provenance references  

No unhandled fork object may persist.

## 36.4 Structural Fork Prevention Mechanisms

### 36.4.1 Deterministic Identity Layer
Because identities are verified (L01, L22–L24):
- No anonymous proposals  
- No Sybil-induced conflicts  
- No probabilistic block competition  

### 36.4.2 Deterministic Ordering (L14–L15)
Every transition is:
- Time-ordered  
- Cause-ordered  
- Context-ordered  
- Constraint-ordered  

Identical ordering eliminates divergent branches.

### 36.4.3 Serialized Provenance (L18)
Provenance enforces:
- Single-parent lineage where required  
- DAG structure with no cycles  
- Immutable historical record  

### 36.4.4 Single-Truth Consensus Engine (L34)
Consensus is:
- Not a vote  
- Not probabilistic  
- Not competitive  

It is deterministic, identity-rooted, and rule-driven.

### 36.4.5 Finality Rules (L35)
Once a transition is final:
- No alternative path may override it  
- No conflicting transition may be accepted  
- No ambiguous state may persist  

### 36.4.6 Mutability Restrictions (L13)
State cannot be rewritten; only forward append is permitted.

## 36.5 Fork Prevention Workflow

### 36.5.1 Pre-Transition Fork Check
Before execution:
- Confirm no conflicting transitions are pending  
- Confirm identical parent state across nodes  
- Confirm no causal disagreement  

### 36.5.2 Validation Conflict Detection (L27)
Detect:
- Competing mutations of the same object  
- Invalidated predecessor state  
- Simultaneous transitions requiring exclusive authority  

If conflict → BLOCK.

### 36.5.3 Verification Conflict Detection (L28)
Detect:
- Mismatched signatures  
- Divergent hashes  
- Missing lineage parents  
- Impossible time markers  

If conflict → REJECT.

### 36.5.4 Governance Conflict Detection (L29)
Governance resolves:
- Authority conflicts  
- Domain conflicts  
- Jurisdiction conflicts  

Resolution is singular — never parallel.

### 36.5.5 Constraint-Level Fork Prevention (L31)
If competing transitions could diverge:
- Hard-stop constraints trigger  
- Higher-order constraints block execution  
- Governance intervention required  

### 36.5.6 Provenance Merge Protection
No merge is permitted between:
- Divergent state chains  
- Conflicting histories  
- Unsigned or unverifiable branches  

The substrate maintains one global DAG, never multiple trees.

## 36.6 Forbidden Fork Conditions
The system must block:
- Any two transitions producing incompatible state deltas  
- Any competing transitions sharing the same causal parent  
- Any governance directive contradicting active policy  
- Any ADT/MAIAi proposal violating autonomy or safety limits  
- Any federated truth contradicting verified local truth  

Forks are not resolved — they are **prevented**.

## 36.7 ADT/MAIAi Fork Prevention Rules
Agents must never:
- Generate incompatible parallel transitions  
- Speculate state outside constraint windows  
- Treat provisional truth as final  
- Emit ambiguous proposals  

Agents must always:
- Respect ordering windows  
- Respect governance boundaries  
- Escalate ambiguity  
- Produce proofs for every proposal  

## 36.8 Federated Fork Prevention

### 36.8.1 Truth Boundary Enforcement
Domains maintain sovereignty; cross-domain mappings must:
- Resolve conflicts deterministically  
- Reject incompatible states  
- Prevent divergent finalities  

### 36.8.2 External Proof Verification
Federated truth must pass:
- Identity verification  
- Provenance verification  
- Causal consistency checks  
- Integrity proofs  

### 36.8.3 Federated Conflict Resolution
If conflict persists:
- Foreign truth is rejected  
- Governance escalation triggers  
- Local canonical truth is preserved  

## 36.9 Observability & Reporting
System must expose:
- Fork-risk maps  
- Transition conflict graphs  
- Provenance inconsistency detectors  
- ADT/MAIAi proposal analyzers  
- Federated conflict dashboards  

Auditors must reconstruct:
- Why no fork occurred  
- How conflicts were blocked  
- How deterministic ordering prevailed  

## 36.10 Interaction With Other Layers
- **L11** — cryptographic anchors  
- **L12** — deterministic evaluation  
- **L13** — historical immutability  
- **L14** — temporal ordering  
- **L15** — causal ordering  
- **L16** — undo consistency  
- **L17** — recovery consistency  
- **L18** — provenance enforcement  
- **L19** — auditability  
- **L20** — authority attestations  
- **L21** — custody conflict prevention  
- **L22–L24** — authority coherence  
- **L25** — context consistency  
- **L26** — agent constraint enforcement  
- **L27** — validation blocking  
- **L28** — verification blocking  
- **L29** — governance resolution  
- **L30** — delegation limits  
- **L31** — constraint hard-stops  
- **L32** — unified state model  
- **L33** — single-path transitions  
- **L34** — deterministic consensus  
- **L35** — immutable finality  

## 36.11 Invariants
1. FORK_IMPOSSIBLE — canonical truth must never diverge.  
2. FORK_DETECTABLE — attempted forks are immediately identified.  
3. FORK_BLOCKED — conflicts are blocked before execution.  
4. FORK_TRACEABLE — all prevention events appear in provenance.  
5. FORK_SAFE — safety prevails over throughput.  
6. FORK_GOVERNED — governance resolves residual conflicts.  
7. FORK_CONTEXTUAL — context and constraints are always applied.  

## 36.12 Informative Guidance
Fork prevention is not conflict resolution — it is **conflict elimination**.  
Parallel truth is unacceptable under all conditions.  
Agents must operate conservatively under ambiguity.  
Federated systems must reject divergence, not harmonize it.  
Fork prevention is foundational to compliance, auditability, and determinism.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

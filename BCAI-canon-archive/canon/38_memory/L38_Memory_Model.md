<!--
CANONICAL: TRUE
LAYER: L38
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L38 — Recovery Model (How the Substrate Restores Itself to Canonical Truth After Disruption)
Defines the systemic, architectural, and governance-level model for how the Sovereign Substrate detects deviation, halts unsafe evolution, reconstructs canonical truth, and restores global coherence after faults, corruption, drift, or federated inconsistency.

L38 answers the question:  
**“How does the system bring itself *back* into truth?”**

## 38.0 Purpose
L38 establishes:
- The substrate-wide approach to identifying recovery conditions  
- How the system prioritizes safety, truth, and determinism during restoration  
- How recovery interacts with provenance, consensus, causality, and finality  
- How ADT/MAIAi participate in or initiate recovery  
- How cross-domain/federated recovery works  
- How the system ensures no partial, inconsistent, or forked truth persists  

Recovery is a **global coherence function**, not merely a repair mechanism.

## 38.1 Scope
Applies to:
- All canonical data and states  
- All transitions and partial transitions  
- All actor, agent, and governance actions  
- All provenance structures  
- Undo and remediation workflows (L16/Krollback)  
- Consensus safety (L34) and finality (L35)  
- Fork prevention and resolution (L36)  
- Causality re-anchoring (L15, L37)  
- Federated domain reconciliation  
- Constraint and safety rule restoration (L31)  

Recovery applies whenever truth, safety, or determinism is threatened.

## 38.2 Core Principles
1. **Truth First** — recovery restores canonical truth before progress resumes.  
2. **Safety Over Liveness** — the system halts unsafe evolution until repaired.  
3. **Deterministic Reconstruction** — recovery always yields the same canonical outcome.  
4. **No Partial Truth** — incomplete or unverified states may not persist.  
5. **No Divergent Truth** — recovery eliminates incompatible branches or forks.  
6. **Provenance Supreme** — recovery depends on complete, intact lineage (L18).  
7. **Governance Overrides** — governance provides ultimate authority in conflicts.  
8. **Minimal Loss, Maximal Integrity** — recovery preserves all lawful, canonical work.  
9. **Transparency** — the system exposes recovery steps for audit (L19).  

## 38.3 Recovery Triggers
Recovery is invoked when any of the following are detected:

### 38.3.1 Structural Failure
- Node malfunction  
- Storage corruption  
- Missing or damaged provenance  

### 38.3.2 Logical Failure
- Invalid state transition  
- Mutability violation (L13)  
- Logical impossibility in state  

### 38.3.3 Causal Failure
- Broken parent references  
- Contradictory causal paths  
- Retroactive or cyclical causality  

### 38.3.4 Temporal Failure (L14)
- Clock drift  
- Illegal ordering  
- Stale transitions applied out of window  

### 38.3.5 Verification Failure (L28)
- Signature mismatch  
- Hash mismatch  
- Invalid or unverifiable proof  

### 38.3.6 Governance Violation (L29)
- Unauthorized rule change  
- Conflicting governance directives  

### 38.3.7 Agent / AI Noncompliance
- ADT/MAIAi producing inconsistent or unsafe transitions  
- Violated agent constraints (L26)  

### 38.3.8 Federated Domain Conflict
- Incompatible cross-domain provenance  
- Conflicting external finality  
- Mismatched truth boundaries  

Any single trigger can freeze evolution and initiate recovery.

## 38.4 Recovery Object Model
Recovery operates on a structured object containing:

### Required Inputs
- Most recent canonical state  
- Verified provenance graph  
- Causal DAG  
- Constraint context  
- Failed transition  
- Actor/agent identity  

### Produces Outputs
- Reconstructed canonical state  
- Validated causal chain  
- Updated provenance markers  
- Recovery report  
- Governance decision logs (if escalated)  

### Anchoring
- Timestamp  
- Recovery epoch identifier  
- Recovery signature (system + governance)  

## 38.5 Recovery Phases

### 38.5.1 Phase 1 — Detection
System detects a fault or inconsistency.  
Execution halts immediately.  
Recovery mode activates.

### 38.5.2 Phase 2 — Isolation
System identifies:
- Faulty transition(s)  
- Impacted objects  
- Divergent paths  
- Unsafe agent actions  
- Federated conflicts  

All non-impacted state remains intact.

### 38.5.3 Phase 3 — Regression
System walks backward through:
- Provenance chain  
- Causal DAG  
- Temporal ordering  
- Governance directives  

Regression stops at the last known-good canonical truth.

### 38.5.4 Phase 4 — Canonical Reconstruction
From the last valid state:
- Rebuild state deterministically  
- Reapply permitted transitions  
- Reject unsafe or unverifiable transitions  
- Re-align agent context  

### 38.5.5 Phase 5 — Reintegration
System restores:
- Global state  
- Consensus participants  
- Agent reasoning environments  
- Federated truth boundaries  

Recovery completes when substrate-wide coherence is restored.

## 38.6 Recovery Determinism Rules
Recovery must be fully deterministic across:
- Nodes  
- Clusters  
- Federated domains  
- ADT/MAIAi agents  

Given the same provenance and rules, recovery *must* yield the same result.

## 38.7 Governance and Recovery

### 38.7.1 Governance Primacy
If ambiguity exists:
- Governance determines the canonical truth.  
- Governance may reject transitions, override state, or redefine resolution rules.  

### 38.7.2 Emergency Governance Actions
Governance may:
- Freeze domains  
- Revoke permissions or delegations  
- Trigger rollback windows  
- Remove agent capabilities  
- Mandate re-verification of entire state segments  

### 38.7.3 Post-Recovery Policy Updates
Governance may update:
- Constraints  
- Causal laws  
- Validation rules  
- Domain trust boundaries  
- Agent compliance ceilings  

## 38.8 ADT/MAIAi Participation in Recovery

### Agents must:
- Halt on recovery trigger  
- Provide reasoning trace for inspection  
- Rebuild causal and context models  
- Accept revised or reconstructed truth  
- Remove invalid assumptions  
- Re-enter substrate in safe mode  

### Agents may not:
- Attempt self-directed repair  
- Guess missing causal or provenance information  
- Reapply transitions autonomously  

Agents are **participants**, not **decision-makers**, in recovery.

## 38.9 Federated Recovery Model

### 38.9.1 Truth Boundary Enforcement
If federated truth conflicts with local truth:
- Local truth prevails  
- Federated transitions enter quarantine  

### 38.9.2 Cross-Domain Reconciliation
System verifies:
- External provenance  
- External finality  
- External constraints  

Conflicts are resolved through governance escalation.

### 38.9.3 Canonical Import Rules
A federated object may only be imported if:
- Provenance is complete  
- Causality is consistent  
- Finality is legitimate  
- Identity is verified  
- Domain trust policy allows import  

## 38.10 Recovery Observability & Reporting
System must expose:
- Recovery timeline  
- Impact graph  
- Failed transition analysis  
- Reconstruction steps  
- Governance decisions  
- Agent compliance diagnostics  

Auditors must be able to reproduce:
- Why recovery was triggered  
- What was rejected  
- What was restored  
- How canonical truth was re-established  

## 38.11 Interaction With Other Layers
- **L11** — cryptographic proofs protect recovery data.  
- **L12** — deterministic evaluation ensures consistent reconstruction.  
- **L13** — mutability constraints limit allowable rollback.  
- **L14** — temporal legality preserved during restoration.  
- **L15** — causal chains must be repaired and validated.  
- **L16** — rollback operations enforced during regression.  
- **L17** — rule-level restoration guides L38’s structural model.  
- **L18** — provenance is the foundation of recovery.  
- **L19** — audits recovery events.  
- **L20** — attestations validate recovery authority.  
- **L21** — custody handoffs must be restored.  
- **L22–L24** — permissions, capabilities, accountability restored correctly.  
- **L25** — context must be reconstructed.  
- **L26** — agent constraint boundaries re-imposed.  
- **L27** — invalid transitions are excluded.  
- **L28** — verification validates reconstructed truth.  
- **L29** — governance is final arbiter of recovery decisions.  
- **L30** — delegation structures restored.  
- **L31** — safety constraints enforced.  
- **L32** — state model rebuilt.  
- **L33** — transitions reapplied deterministically.  
- **L34** — consensus restored in unified form.  
- **L35** — finality re-established.  
- **L36** — fork prevention ensures a single recovered truth.  
- **L37** — causal relationships repaired and preserved.  

## 38.12 Invariants
1. RECOVERY_REQUIRED — any break in truth triggers recovery.  
2. RECOVERY_DETERMINISTIC — reconstruction yields one possible canonical state.  
3. RECOVERY_SAFE — unsafe transitions never survive.  
4. RECOVERY_TRACEABLE — full provenance and audit visibility required.  
5. RECOVERY_COMPLETE — partial restoration forbidden.  
6. RECOVERY_AUTHORIZED — governance has final authority.  
7. RECOVERY_GLOBAL — coherence restored across entire substrate.  

## 38.13 Informative Guidance
Recovery is not a patch; it is the substrate’s immune system.  
When in doubt, the system chooses safety over progress.  
Agents should assume recovery states invalidate assumptions made close to the failure boundary.  
Federated recovery must err toward stricter truth, not compromise.  
Recovery is a core feature of a sovereign, authenticated substrate — not an afterthought.

Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

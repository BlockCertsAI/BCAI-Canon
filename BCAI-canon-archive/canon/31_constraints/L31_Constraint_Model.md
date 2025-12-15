<!--
CANONICAL: TRUE
LAYER: L31
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L31 — Constraint Model (Limits, Boundaries & Safety Conditions of the Substrate)
Defines the universal constraint system governing what actors — human, organizational, ADT, MAIAi, and system components — may do, under what conditions, within what limits, and with what safety guarantees. Constraints provide the substrate’s “do not cross” boundaries, ensuring safety, legality, determinism, and stable canonical order.

## 31.0 Purpose
L31 establishes the canonical constraint framework for:
- Bounding all actions and decisions  
- Preventing unsafe or illegal system states  
- Defining structural, temporal, causal, and contextual boundaries  
- Restricting ADT/MAIAi autonomy  
- Enforcing substrate-wide invariants  
- Ensuring that every operation respects safety, governance, and truth  

Constraints answer the question:  
**“What actions are forbidden, restricted, or conditionally allowed — and why?”**

## 31.1 Scope
Constraints apply to:
- All verified identities and actors  
- ADT/MAIAi agents  
- Permissions (L22), capabilities (L23), and accountabilities (L24)  
- Context propagation (L25)  
- Delegation (L30) and governance (L29)  
- State changes, lineage and provenance (L18)  
- Undo (L16) and recovery (L17)  
- Verification and validation flows (L27–L28)  

Constraints must be evaluated **before, during, and after** all actions.

## 31.2 Core Principles
1. **Constraints are mandatory** — they cannot be bypassed.  
2. **Constraints are provable** — every constraint must be enforceable via verification (L28).  
3. **Constraints are composable** — multiple constraints may apply together.  
4. **Constraints are hierarchical** — governance constraints override domain and actor constraints.  
5. **Safety dominates freedom** — autonomy is always bounded by safety invariants.  
6. **Constraints are contextual** — what is allowed depends on context (L25).  
7. **Agents cannot self-expand constraints** — ADT/MAIAi may not loosen their own limits.  

## 31.3 Constraint Object Model
Each constraint must include:

### Identity Fields
- Actor or class the constraint applies to  
- Required permissions or capabilities  
- Governance authority establishing the constraint  

### Constraint Scope
- Which actions are bounded  
- Allowed and forbidden conditions  
- Dependency or prerequisite conditions  

### Constraint Mechanics
- Trigger conditions  
- Constraint enforcement logic  
- Constraint escalation thresholds  
- Required attestations or proofs  

### Cryptographic Binding
- Constraint hash  
- Governance or domain signatures  
- Optional multi-signature for Critical constraints  

### Anchoring
- Timestamp  
- Causal parent reference  
- Provenance lineage entry  

## 31.4 Categories of Constraints

### 31.4.1 Structural Constraints
Define what is fundamentally allowed or disallowed by system architecture:
- Identity creation rules  
- Object mutation rules  
- Provenance invariants  
- Non-repudiation guarantees  

### 31.4.2 Temporal Constraints
Define how actions relate to time (L14):
- Validity windows  
- Expiration periods  
- Forbidden time-travel or retroactive operations  
- Temporal ordering requirements  

### 31.4.3 Causal Constraints
Define correct cause–effect relationships (L15):
- No causal cycles  
- No impossible parent references  
- No action allowed without required antecedents  

### 31.4.4 Contextual Constraints
Define what must be true in context (L25):
- Required environmental conditions  
- Policy activation windows  
- Dependency requirements  
- Actor state requirements  

### 31.4.5 Capability Constraints
Define what an actor *can* do (L23):
- Maximum allowed capabilities  
- Prohibited capabilities  
- Conditional capability activation  

### 31.4.6 Permission Constraints
Define what an actor *may* do (L22):
- Permission ceilings  
- Required permission stacks  
- Forbidden permissions combinations  

### 31.4.7 Autonomy Constraints (ADT/MAIAi)
Define and bound autonomous behavior:
- Maximum allowed autonomy level  
- Safety escalation triggers  
- Forbidden operations without supervision  
- Hard safety stops  

### 31.4.8 Delegation Constraints
Define what may or may not be delegated (L30):
- Redelegation limits  
- Forbidden delegation types  
- Delegation domain restrictions  

### 31.4.9 Governance Constraints
Define what governance entities must enforce (L29):
- Override boundaries  
- Jurisdiction restrictions  
- Error or conflict escalation rules  

### 31.4.10 Risk Constraints
Define system risk thresholds:
- Critical operation gating  
- Rate limits  
- Resource consumption ceilings  
- AI decision-risk categories  

## 31.5 Constraint Enforcement Rules

### 31.5.1 Pre-Action Enforcement
Before any action:
- Verify the actor  
- Verify the context  
- Evaluate all applicable constraints  
- Deny the action if any constraint fails  

### 31.5.2 Mid-Action Enforcement
During execution:
- Monitor for violation signals  
- Abort actions when constraints are triggered  
- Trigger escalation or rollback  

### 31.5.3 Post-Action Enforcement
After execution:
- Validate the final state  
- Scan for violations, anomalies, or boundary crossings  
- Log constraint outcomes into provenance  

### 31.5.4 Hard Stops
Certain constraints must instantly terminate an operation:
- Safety invariants  
- Identity compromise  
- Critical capability misuse  
- Temporal or causal violations  

### 31.5.5 Escalation
Constraint violations must:
- Escalate to governance  
- Produce attestations  
- Trigger risk or anomaly alarms  
- Prevent dependent operations  

## 31.6 Constraint Interaction Rules

### 31.6.1 Constraint Precedence
From highest authority to lowest:
1. CSR constraints  
2. Architect constraints  
3. Governance domain constraints  
4. Structural/Protocol constraints  
5. Actor-specific constraints  
6. AI/ADT constraints  

### 31.6.2 Constraint Merging
When multiple constraints apply:
- The strictest constraint prevails  
- Scope intersections must be explicitly resolved  
- Merged constraints must be validated  

### 31.6.3 Constraint Inheritance
Child contexts inherit:
- Parent constraints  
- Domain constraints  
- Capability ceilings  
- Risk boundaries  

### 31.6.4 Constraint Suspension
Only governance (L29) may suspend constraints, and only temporarily:
- Suspension must be signed  
- Provenance must record justification  
- Safety constraints may never be suspended  

## 31.7 Constraints for AI/ADT Agents
Agents must operate under:
- Strict non-expansion rules  
- Permanent capability ceilings  
- Safety and ethical boundaries  
- Supervision triggers for high-risk actions  

Agents must:
- Decline actions violating constraints  
- Produce proofs and attestations for actions  
- Escalate uncertainty instead of guessing  

## 31.8 Constraint Validation & Verification
Every constraint must pass:

### Validation (L27)
- Logical correctness  
- Domain compatibility  
- Structural sanity  
- No contradiction with other constraints  

### Verification (L28)
- Signatures  
- Hash integrity  
- Authority legitimacy  
- Temporal and causal correctness  

If either fails, the constraint is rejected.

## 31.9 Observability & Reporting
The substrate must expose tools for:
- Constraint graphs  
- Active constraints per actor or domain  
- Constraint lineage and governance history  
- Violation logs and escalation chains  
- AI/ADT constraint-boundary heatmaps  

Auditors must reconstruct:
- How constraints were applied  
- Why actions were allowed or denied  
- How agents responded to constraints  
- How governance enforced boundaries  

## 31.10 Interaction With Other Layers
- **L11** — cryptographic binding of constraints.  
- **L12** — deterministic constraint evaluation.  
- **L13** — governs legal transformations under constraints.  
- **L14** — applies time-window constraints.  
- **L15** — enforces causal constraints.  
- **L16** — constraints apply during undo.  
- **L17** — constraints apply during recovery.  
- **L18** — constraints attach to provenance.  
- **L19** — audits constraint evaluations.  
- **L20** — attestation rules used for constraints.  
- **L21** — custody constraints.  
- **L22** — permission ceilings.  
- **L23** — capability ceilings.  
- **L24** — accountability under constraints.  
- **L25** — context-based constraints.  
- **L26** — agent autonomy constraints.  
- **L27** — constraint validation.  
- **L28** — constraint verification.  
- **L29** — governance constraint hierarchy.  
- **L30** — delegation constraint compatibility.

## 31.11 Invariants
1. CONSTRAINT_REQUIRED — no action may proceed without constraint evaluation.  
2. CONSTRAINT_STRICT — strictest applicable constraint always applies.  
3. CONSTRAINT_TRACEABLE — all constraints and evaluations must be logged.  
4. CONSTRAINT_ENFORCED — constraints must be enforceable and enforced.  
5. CONSTRAINT_SAFE — constraints must always preserve substrate stability.  
6. CONSTRAINT_CONTEXTUAL — constraints must account for context.  
7. CONSTRAINT_IMMUTABLE — historical constraints cannot be rewritten.  

## 31.12 Informative Guidance
Constraints define the substrate’s immune system.  
Agents should be given only the smallest constraint windows required.  
Federated constraints should rely on zero-knowledge proofs where possible.  
Constraint drift is a major risk and must be monitored continuously.  
Constraint tuning should be done gradually and with full provenance.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

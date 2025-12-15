<!--
CANONICAL: TRUE
LAYER: L27
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Defines canonical validation rules that every event, state transition, and agent action MUST satisfy before the Sovereign Substrate will accept it.
NOTES:
  - Applies to all layers, agents, and sovereign domains.
  - Prevents forged state, policy bypass, and inconsistent views of truth.
-->

# L27 — Validation Rules (What Must Be True Before Anything Executes)
Defines the universal validation framework that determines whether an event, action, state transition, process, or agent behavior is allowed to proceed within the Sovereign Substrate. Validation ensures correctness, integrity, safety, legality, and consistency at every layer.

## 27.0 Purpose
L27 establishes the canonical rules governing:
- What must be checked before execution  
- How validation integrates identity, permissions, capabilities, context, constraints, provenance, causality, and temporal alignment  
- How invalid actions are rejected, escalated, or remediated  
- How validation persists across undo and recovery  
- How validation applies uniformly to humans, ADT, MAIAi, and system actors  

Validation is the substrate’s gatekeeper: **nothing proceeds without passing every required rule**.

## 27.1 Scope
Validation applies to:
- All canonical events  
- All state transitions  
- All object mutations  
- All ADT/MAIAi autonomous actions  
- All cross-domain or federated interactions  
- All permissions, capabilities, and accountability checks  
- All provenance and causal chain updates  
- All handoffs, attestations, and context flows  

Every operation must undergo validation before it becomes canonical.

## 27.2 Core Principles
1. **Validation First** — no action may execute before validation completes.  
2. **Holistic Validation** — validation checks all relevant layers (L11–L26).  
3. **Deterministic Results** — identical input yields identical validation outcomes (L12).  
4. **Fail-Closed** — any uncertainty results in rejection, not acceptance.  
5. **Non-Repudiable Evidence** — validation must generate auditible proof.  
6. **Immutable Outcome** — validation result becomes part of provenance.  
7. **Consistency Across Undo/Recovery** — validation applies to all forward and corrective paths (L16–L17).

## 27.3 Validation Object Model
Each validation event must include:

### Input Bundle
- Actor identity  
- Intended action  
- Target object or domain  
- Context (L25)  
- Permissions (L22)  
- Capabilities (L23)  
- Accountability bindings (L24)  
- Constraints (L26)  
- Provenance references  
- Timing and causality markers  

### Validation Outputs
- Validation result (PASS / FAIL)  
- Reason codes  
- Hash of validation context  
- List of validation rules applied  
- Signatures and attestations produced  
- Any escalation or remediation actions required  

### Anchoring
- Timestamp (L14)  
- Causal link to attempted action (L15)  
- Provenance entry (L18)  

## 27.4 Validation Rule Classes

### 27.4.1 Identity Validation
Confirms:
- Actor is verifiably authenticated  
- Identity is uncompromised  
- Identity is authorized to request action  

### 27.4.2 Permission Validation
Checks:
- Actor has explicit permission for requested action (L22)  
- Permission is active, unexpired, unrevoked  
- Permission scope matches the target object or domain  

### 27.4.3 Capability Validation
Confirms:
- Actor is *capable* of performing the requested action (L23)  
- Preconditions for capability are satisfied  
- Capability does not conflict with active constraints  

### 27.4.4 Accountability Validation
Ensures:
- Actor is accountable for this action (L24)  
- Accountability window is active  
- No conflicting accountability claims exist  

### 27.4.5 Constraint Validation
Ensures:
- Action complies with all agent constraints (L26)  
- No safety, governance, or risk constraints forbid the action  
- Required human oversight is present when needed  

### 27.4.6 Context Validation
Checks:
- Required context exists  
- Context is fresh, relevant, and fully inherited (L25)  
- No conflicting or contradictory contexts  

### 27.4.7 Provenance Validation
Ensures:
- Object lineage is complete and unbroken (L18)  
- No tampering or missing lineage nodes  
- Custody is correct and consistent  

### 27.4.8 Temporal Validation
Confirms:
- Timestamp is within permitted window  
- No expired or premature operation (L14)  
- Temporal ordering aligns with causal chain  

### 27.4.9 Causal Validation
Checks:
- Required parent events exist and are canonical  
- No causal loops or paradoxes (L15)  
- Causal chain integrity is intact  

### 27.4.10 State Validation
Confirms:
- Object is in valid state for requested mutation  
- No conflicting simultaneous mutations  
- Mutability rules (L13) are satisfied  

### 27.4.11 Domain & Boundary Validation
Checks:
- Actor is allowed within domain  
- Cross-substrate routes are verified  
- Jurisdictional context is valid  

## 27.5 Validation Failures
If any validation step fails:

### Immediate Effects
- Action is rejected  
- No state change occurs  
- Agent execution halts (if applicable)  

### Required Side Effects
- Generate failure attestation (L20)  
- Update audit logs (L19)  
- Update provenance fork markers (L18)  
- Emit context about failure reason (L25)  

### Optional Remediation
Depending on severity:
- Automatic correction  
- Escalation to human supervisor  
- Re-validation request after context update  
- System-level quarantine for unsafe operations  

## 27.6 Validation in Undo (L16) and Recovery (L17)
Validation must apply symmetrically to corrective flows:

### Undo Validation
Ensures:
- Undo operation is legal  
- Undo state is valid and reversible  
- No causal distortions  
- Provenance remains intact  

### Recovery Validation
Ensures:
- Restored state is canonical  
- Constraints, permissions, and capabilities re-validate correctly  
- Prior validation failures are not reintroduced  

## 27.7 Validation of Autonomous Systems (ADT/MAIAi)
Agents must:
- Validate all autonomous actions as if performed by a human actor  
- Produce validation evidence  
- Reject any action lacking required validation resources  
- Escalate when validation cannot complete  

Agents may not bypass validation under any circumstances.

## 27.8 Observability & Reporting
The substrate must provide:
- Validation rule history  
- Validation reason codes  
- Causal validation graphs  
- AI/ADT validation trace viewers  
- Domain-specific validation summaries  
- Real-time validation diagnostics  

Auditors must reconstruct:
- Why an action passed or failed  
- Which rules applied  
- Whether validation followed canonical procedures  
- Whether failures were correctly handled  

## 27.9 Interaction With Other Layers
- **L11** — verifies all signatures & hashes used in validation.  
- **L12** — ensures deterministic validation outcomes.  
- **L13** — governs whether requested mutations are legal.  
- **L14** — governs timing windows for validation.  
- **L15** — governs causal alignment.  
- **L16** — validation ensures undo does not break state.  
- **L17** — validation ensures recovery produces canonical state.  
- **L18** — validation attaches to provenance.  
- **L19** — validation produces auditable evidence.  
- **L20** — attestations bind validation truth.  
- **L21** — validation applies to handoff transitions.  
- **L22** — permissions are checked during validation.  
- **L23** — capabilities are checked during validation.  
- **L24** — accountability determines whether actor is responsible.  
- **L25** — context defines how validation interprets the event.  
- **L26** — constraints limit what validation may approve.

## 27.10 Invariants
1. VALIDATION_REQUIRED — nothing executes without validation.  
2. VALIDATION_TOTAL — all rule classes must be evaluated.  
3. VALIDATION_DETERMINISTIC — same input → same result.  
4. VALIDATION_TRACEABLE — all validation events must appear in provenance.  
5. VALIDATION_FAIL_CLOSED — any uncertainty yields rejection.  
6. VALIDATION_ATTESTED — validation outcomes require signatures.  
7. VALIDATION_CONTEXTUAL — validation depends on active context.  
8. VALIDATION_GOVERNED — validation rules cannot be bypassed.  

## 27.11 Informative Guidance
Validation should be optimized for speed but never at the cost of safety.  
Federated domains may implement additional validation layers.  
AI/ADT systems should prioritize validation clarity and explainability.  
Validation failures are critical signals for risk escalation and governance oversight.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

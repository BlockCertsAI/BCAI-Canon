<!--
CANONICAL: TRUE
LAYER: L16
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L16 — Reversibility (Rollback & Canonical Undo Rules)  
*Defines how Canon reverses, compensates, or restores authenticated state changes without violating identity, causality, or proof guarantees.*

---

## 16.0 Purpose

The Reversibility layer establishes **how the Sovereign Substrate safely rolls back or undoes events** while preserving:

- Causality (L15)  
- Mutability constraints (L13)  
- Temporal validity (L14)  
- Proof integrity (L11)  

L16 ensures that the system can correct errors, revoke compromised chains, and restore canonical truth without introducing inconsistencies or unauthorized rewrites.

---

## 16.1 Scope

L16 governs:

- Rollback of mutable state changes  
- Compensating actions for irreversible events  
- Architect-controlled restorative sequences  
- ADT-initiated corrective workflows  
- MAIAi-driven anomaly responses  
- System-wide canonical recovery after detected corruption  

L16 does **not** allow arbitrary mutation or deletion of history.  
It defines **how to correct forward**, not rewrite the past.

---

## 16.2 Core Principles

1. **History Is Immutable; Effects Are Not**  
   No event is deleted.  
   Rollback is achieved by **applying a new corrective event** that nullifies or compensates the prior effect.

2. **Rollback Requires Higher Authority**  
   Only Architect-, CSR-, or policy-validated agents may initiate rollback for Critical events.

3. **Causal Integrity Must Hold**  
   Undo actions MUST NOT break the causal chain (L15).  
   They MUST explicitly reference the event being corrected.

4. **Rollback Must Be Deterministic**  
   For any reversible effect, the undo result MUST be predictable and invariant.

---

## 16.3 Event Types Under L16

### 16.3.1 Compensating Event (Primary Undo Type)

A **Compensating Event** is a forward-applied canonical action that:

- References a prior event  
- Declares a dependency type: `COMPENSATION_FOR`  
- Applies corrective transitions defined by L13 (mutability)  

Compensation MUST be used for all irreversible effects that cannot be directly rolled back.

### 16.3.2 Reversal Event (Direct Rollback)

A **Reversal Event**:

- Reverts a mutable state to a prior known-good state  
- MUST reference a state snapshot or anchor  
- MUST comply with idempotence guarantees (L12)  
- MUST be allowed by the object’s mutability class (L13.3)  

Reversal events may be restricted to specific object types or security classes.

### 16.3.3 Revocation Event

Revocation applies to:

- Identity permissions  
- Credentials  
- Tokens  
- Access keys  

A **Revocation Event** MUST:

- Reference the original issuance event  
- Set the revoked object into a terminal INVALIDATED state  
- Trigger cascading checks in dependent chains (L15.5.3)

---

## 16.4 Anchor Points for Reversal

L16 defines three valid anchor types for rollback operations:

1. **Canonical State Snapshot**  
   A system-level baseline defined by Architect policy.

2. **Pre-Event State Hash**  
   A hash of the last known-valid version of the object.

3. **Causal Root Reference**  
   A valid ancestor event that represents a stable baseline.

If an anchor cannot be validated under L11–L15, rollback MUST NOT proceed.

---

## 16.5 Rollback Validation Rules

Before any rollback or undo event is accepted, Canon MUST validate:

### 16.5.1 Authority Validation
- The initiating agent MUST have a reversal/compensation role.  
- Critical undo operations MUST include CSR authorization.

### 16.5.2 Causal Compatibility  
- Undo MUST reference the event to be reversed.  
- Undo MUST NOT introduce cycles (L15).  
- Undo MUST define dependency type: `REVERSAL_OF`, `COMPENSATION_FOR`, or `REVOCATION_OF`.

### 16.5.3 Mutability Constraints  
- Only mutable state may be reversed.  
- Immutable effects require a Compensating Event.  
- Attempts to reverse immutable state MUST be rejected.

### 16.5.4 Temporal Consistency  
- Undo MUST occur after the event it reverses.  
- Undo MUST declare a valid temporal anchor window (L14).

### 16.5.5 Integrity Validation  
Undo MUST include:

- Parent event hash  
- Object hash before and after undo  
- Required signatures (per L11)  
- Chain-of-custody metadata  

Events failing these checks MUST be rejected or deferred.

---

## 16.6 Canonical Undo Algorithm (Normative)

A rollback sequence is valid if and only if:

1. The targeted event exists and is fully committed.  
2. The targeted event is mutable OR compensable.  
3. The initiating agent is authorized.  
4. A valid anchor point is identified.  
5. The undo event is constructed referencing the target.  
6. The undo action is evaluated under L12–L15.  
7. The undo passes integrity validation.  

If all conditions are satisfied:

- The undo event becomes part of canonical history.  
- The affected object returns to a stable canonical state.  
- Downstream dependencies MAY require additional compensations.

---

## 16.7 Cascading Undo & Chain Reconciliation

When reversing a Critical event, Canon MUST:

- Walk the causal DAG (L15)  
- Identify dependent events  
- Classify them as:
  - **REQUIRES_COMPENSATION**
  - **REQUIRES_REEVALUATION**
  - **REMAINS_VALID**

Architect MAY then:

- Apply a chain-wide restorative sequence  
- Invalidate compromised paths  
- Generate new anchor baselines  

Cascading rollback MUST preserve invariants.

---

## 16.8 Idempotence Guarantees for Undo (L12 Interaction)

Undo events MUST be idempotent:

- Applying the same undo multiple times MUST NOT lead to divergence.  
- Reversal actions MUST check current object state before executing.  
- Compensation MUST NOT recursively re-trigger itself.

---

## 16.9 Observability & Auditing

Canonical undo operations MUST expose:

- Complete rollback chain  
- Before/after state hashes  
- Integrity proofs  
- Authority signatures  
- CSR involvement where applicable  

System logs MUST clearly mark:

- Reversal events  
- Compensation events  
- Revocations  
- Cascading adjustments  

Auditors MUST be able to reconstruct the complete rollback path at any time.

---

## 16.10 Prohibited Actions

The following operations MUST NOT occur:

- Deleting historical events  
- Mutating historical records  
- Retroactively changing parent–child dependencies  
- Time-reversing event sequences  
- Silent rollbacks without exposure through Canon logs

Any attempt must be rejected and flagged as a violation.

---

## 16.11 Invariants

L16 MUST uphold:

1. **HISTORY_IMMUTABLE**  
   No historical record is altered or removed.

2. **DETERMINISTIC_UNDO**  
   Undo results are predictable and invariant.

3. **CAUSAL_COMPATIBILITY**  
   Undo does not break L15 causal chains.

4. **ANCHOR_VALIDITY**  
   Rollbacks only occur relative to validated anchors.

5. **CRITICAL_CHAIN_PROTECTION**  
   Critical undo forces downstream revalidation.

---

## 16.12 Interaction With Other Layers

- **L11 — Proof Primitives**  
  Ensures all undo signatures and hashes are valid.

- **L12 — Idempotence**  
  Ensures undo events never create divergence.

- **L13 — Mutability Constraints**  
  Determines which events can be reversed vs. compensated.

- **L14 — Temporal Rules**  
  Ensures undo events occur after the event they reverse.

- **L15 — Causality Chain**  
  Ensures that undo actions reference prior events without breaking the DAG.

---

## 16.13 Informative Guidance

- Rollback SHOULD be rare; robust domain validation (L27+) SHOULD prevent most incorrect states.  
- Architect MAY throttle or rate-limit reversals to prevent oscillation attacks.  
- Systems SHOULD expose a diff tool for comparing pre- and post-undo states.

---

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

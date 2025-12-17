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

---

### 16.3.2 Reversal Event (Direct Rollback)

A **Reversal Event**:

- Reverts a mutable state to a prior known-good state  
- MUST reference a state snapshot or anchor  
- MUST comply with idempotence guarantees (L12)  
- MUST be allowed by the object’s mutability class (L13)  

Reversal events may be restricted to specific object types or security classes.

---

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
2. **Pre-Event State Hash**  
3. **Causal Root Reference**

If an anchor cannot be validated under L11–L15, rollback MUST NOT proceed.

---

## 16.5 Rollback Validation Rules

Before any rollback or undo event is accepted, Canon MUST validate:

### 16.5.1 Authority Validation
- Initiator holds reversal authority  
- CSR approval for Critical undo  

### 16.5.2 Causal Compatibility  
- Explicit reference to target event  
- No cycle creation  
- Valid dependency type  

### 16.5.3 Mutability Constraints  
- Immutable state requires compensation  
- Direct reversal only for mutable state  

### 16.5.4 Temporal Consistency  
- Undo occurs after target event  
- Valid temporal window  

### 16.5.5 Integrity Validation  
- Parent event hash  
- Before/after object hashes  
- Required signatures  
- Chain-of-custody metadata  

---

## 16.6 Canonical Undo Algorithm (Normative)

A rollback is valid iff:

1. Target event exists and is committed  
2. Target is mutable or compensable  
3. Initiator is authorized  
4. Anchor is valid  
5. Undo event references target  
6. Undo passes L12–L15  
7. Integrity validation succeeds  

Undo becomes canonical history; dependencies may require compensation.

---

## 16.7 Cascading Undo & Chain Reconciliation

For Critical events, Canon MUST:

- Traverse causal DAG  
- Classify dependent events  
- Apply compensations or revalidation  

Invariants MUST hold.

---

## 16.8 Idempotence Guarantees for Undo

Undo events MUST be idempotent:

- No duplicate effects  
- State checked before execution  
- No recursive compensation  

---

## 16.9 Observability & Auditing

Undo operations MUST expose:

- Full rollback chain  
- Before/after hashes  
- Proofs and signatures  
- CSR involvement  

Rollback is always visible and auditable.

---

## 16.10 Prohibited Actions

MUST NOT:

- Delete history  
- Mutate historical records  
- Rewrite dependencies  
- Reverse time  
- Perform silent rollback  

Violations MUST be flagged.

---

## 16.11 Invariants

1. **HISTORY_IMMUTABLE**  
2. **DETERMINISTIC_UNDO**  
3. **CAUSAL_COMPATIBILITY**  
4. **ANCHOR_VALIDITY**  
5. **CRITICAL_CHAIN_PROTECTION**

---

## 16.12 Interaction With Other Layers

- **L11 Proof Primitives**  
- **L12 Idempotence**  
- **L13 Mutability Constraints**  
- **L14 Temporal Rules**  
- **L15 Causality Chain**

---

## 16.13 Real-World Capability Enabled by Reversibility

Reversibility enables **legally defensible correction without erasing history**.

It allows:
- Financial systems to reverse erroneous transfers while preserving audit trails.
- Governments to revoke credentials, access, or authority with provable cause and scope.
- Enterprises to unwind contracts, permissions, or configurations safely after disputes or breaches.
- Security teams to contain compromise by revoking effects without corrupting system truth.
- Regulators and courts to see not just *what* was undone, but *why* and *by whom*.

Reversibility turns error correction from a liability into a **governed, auditable process**.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

<!--
CANONICAL: TRUE
LAYER: L15
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

## L15 — Causality Chain (Cause–Effect Integrity Rules)  
*Defines how Canon tracks, validates, and preserves cause–effect relationships across all authenticated events.*

---

## 15.0 Purpose

The Causality Chain layer ensures that:

- Every authenticated effect has a traceable, justified cause.
- Cause–effect relationships remain intact under concurrency, retries, and recovery.
- No actor can manufacture effects without satisfying required causal preconditions.

L15 binds identity, time, mutability, and proof primitives into a consistent, verifiable causal graph for the Sovereign Substrate.

---

## 15.1 Scope

L15 applies to:

- All Canon events that mutate state across any Sovereign Substrate layer.
- All ADT, MAIAi, Architect, and BAINCA workloads that depend on historical context.
- All CSR-governed actions requiring explicit causal justification.

L15 does **not** define business semantics.  
It defines structural rules for causal correctness of events.

---

## 15.2 Core Guarantees

L15 MUST enforce the following guarantees:

1. **No Effect Without Cause**  
   Every state-mutating event MUST reference one or more valid causal anchors.

2. **No Broken Chains**  
   The full causal ancestry of any committed event MUST be reconstructable and verifiable.

3. **No Time-Reversed Causality**  
   An effect MUST NOT be logically or temporally prior to its declared cause.

4. **No Orphaned Critical Effects**  
   Critical effects (as defined in §15.4) MUST NOT exist without a Canonical Causal Chain.

---

## 15.3 Canonical Causality Graph

Canon represents causality as a directed acyclic graph (DAG) of events:

- **Node**: A Canon event with a globally unique Event ID.
- **Edge**: A directed dependency `cause → effect`.

Every L15-compliant event MUST:

- Declare one or more **Causal References** to prior events, or
- Declare itself as a **Root Event** under specific allowed conditions (§15.4.1).

The resulting graph MUST remain acyclic under all valid operations.

---

## 15.4 Event Classification

### 15.4.1 Root Events

A **Root Event** is an event that introduces new causal context.  
Root Events MUST be limited to:

- Genesis initialization events.
- CSR-approved configuration baselines.
- Admitted external anchor events (e.g., regulatory checkpoints) explicitly whitelisted by Architect policy.

Root Events MUST include:

- Justification type (GENESIS, BASELINE, REGULATORY_ANCHOR, etc.).
- CSR authority reference where applicable.
- Immutable rationale metadata.

### 15.4.2 Derived Events

A **Derived Event** depends on one or more prior events.

Derived Events MUST:

- Reference all direct causal parent Event IDs.
- Declare dependency types (e.g., READ_FROM, UPDATE_OF, COMPENSATION_FOR, REVOCATION_OF).
- Comply with applicable mutability, temporal, and idempotence rules (L12–L14).

### 15.4.3 Critical vs. Non-Critical Effects

Architect policy MAY classify effects as:

- **Critical**: Identity, access, financial, compliance, governance, canonical configuration.
- **Non-Critical**: Low-risk telemetry, non-authoritative hints, ephemeral analytics.

L15 MUST enforce stricter causality checks for Critical effects (§15.5.3).

---

## 15.5 Causality Validation Rules

### 15.5.1 Basic Causality Checks

For every event `E`, Canon MUST validate:

1. **Existence**  
   All referenced parent Event IDs MUST exist in Canon.

2. **Visibility**  
   Parents MUST be visible within the same or an authorized Sovereign Substrate scope.

3. **Temporal Order**  
   Parents MUST NOT occur after `E` under the chosen canonical time model (L14).

4. **Acyclicity**  
   Adding `E` and its edges MUST NOT introduce cycles.

If any check fails, the event MUST be rejected or deferred (§15.6).

### 15.5.2 Dependency Type Compatibility

For every `parent → child` relation, Canon MUST validate:

- Dependency type is allowed for the parent’s event class.
- Dependency does not violate mutability constraints (L13).
- Dependency does not break idempotence expectations (L12).

Examples:

- An event of type UPDATE_OF MUST reference a parent that is mutable and in a valid state for update.
- An event of type COMPENSATION_FOR MUST reference a prior event that is compensable.

### 15.5.3 Critical Effect Causality

For Critical effects:

- At least one parent MUST be:
  - A CSR-approved directive, or
  - A previously validated Critical event in a valid state.
- All parents MUST pass enhanced integrity checks:
  - Valid signatures (L11).
  - Valid temporal window (L14).
  - Non-broken mutable lineage (L13).

If any parent in a Critical chain becomes invalidated, Architect MUST:

- Mark dependent Critical effects as **CAUSALLY_COMPROMISED**, and
- Trigger compensating or rollback actions per policy.

### 15.5.4 Multi-Parent Causality

When events have multiple parents, Canon MUST:

- Evaluate each parent independently against L12–L14.
- Enforce any declared dependency mode:
  - **ALL_OF**: All parents MUST be satisfied.
  - **ANY_OF**: At least one parent MUST be satisfied.
  - **QUORUM_OF(N, K)**: At least `K` of `N` parents MUST be satisfied.

Dependency mode MUST be explicitly encoded in the event metadata.

---

## 15.6 Failure Handling & Deferred Causality

### 15.6.1 Immediate Rejection

Events MUST be **rejected** when:

- They introduce cycles.
- They reference parents that are definitively invalid.
- They attempt forbidden dependency types.

Rejected events MUST be:

- Logged with a cause code.
- Exposed through observability channels as permanently invalid.

### 15.6.2 Deferred Evaluation

Events MAY be **deferred** when:

- Parents are unknown but may appear later.
- Parents are pending CSR or Architect decisions.
- Cross-substrate anchors are not yet synchronized.

Deferred events MUST:

- Be stored in a dedicated **Pending Causality Queue**.
- Be re-evaluated when missing parents are resolved or timeout occurs.
- Expire under a policy-defined TTL, after which they become rejected.

---

## 15.7 Observability & Instrumentation

L15 MUST expose:

- Causal chain inspection APIs for:
  - Single event ancestry.
  - Impact analysis of event invalidation.
- Metrics:
  - Average causal depth.
  - Deferred event counts and aging.
  - Causality failure rates by reason code.
- Traces:
  - End-to-end chains from initiating Root Events to terminal effects.

Implementations SHOULD provide visual tools for causal graph exploration.

---

## 15.8 Invariants

L15 MUST maintain these invariants at all times:

1. **CAUSAL_CHAIN_RECONSTRUCTIBLE**  
   For any committed event, its complete causal ancestry is discoverable.

2. **NO_CAUSAL_CYCLES**  
   The Canon causal graph remains acyclic.

3. **CRITICAL_CHAIN_COMPLETE**  
   No committed Critical effect exists without a valid, validated chain to at least one Root or CSR anchor.

4. **CONSISTENT_DEPENDENCY_TYPES**  
   Declared dependency types do not contradict parent or child semantics.

---

## 15.9 Interactions With Other Layers

- **L11 — Proof Primitives**  
  Provides cryptographic integrity for causal links and event authenticity.

- **L12 — Idempotence Rules**  
  Ensures repeated effects do not create divergent or contradictory chains.

- **L13 — Mutability Constraints**  
  Defines which state transitions are legal along a causal chain.

- **L14 — Temporal Rules**  
  Establishes valid temporal order and windows for cause–effect relations.

- **L27+ — Higher-Level Validation Rules**  
  MAY define domain-specific causal templates and patterns that refine L15.

L15 is a structural foundation.  
Higher layers MAY add semantics but MUST NOT weaken L15 guarantees.

---

## 15.10 Implementation Notes (Informative)

- Implementations MAY choose different internal representations (graphs, logs with indices, etc.) as long as L15 invariants hold.
- Causality MAY be approximated for non-Critical analytics events, but MUST remain exact for Critical effects.
- For distributed deployments, L15 SHOULD leverage:
  - Logical clocks or vector clocks (L14).
  - Canonical reconciliation protocols to keep the causal graph consistent.

---

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

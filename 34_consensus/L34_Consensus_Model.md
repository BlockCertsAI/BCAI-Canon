## L34 — Consensus Model

### Definition

The L34 Consensus Model defines how Sovereign Substrate nodes independently verify the same authenticated event, derive the same state outcome, and recognize one canonical result without relying on token-weighted voting, probabilistic settlement, or competing validator authority.

Consensus answers the question:

**“How does every participating node arrive at the same canonical truth?”**

Within the Sovereign Substrate, consensus is not an opinion, election, or market outcome. It is the deterministic convergence of authenticated identity, valid authority, complete proofs, preserved causality, invariant compliance, and identical execution.

---

## 1. Purpose

The Consensus Model ensures that:

- identical authenticated inputs produce identical decisions  
- nodes cannot establish competing versions of canonical state  
- economic power cannot influence truth  
- invalid or incomplete events cannot gain acceptance through majority support  
- cross-domain state changes remain causally and semantically aligned  
- divergence is detected before it becomes canonical  
- only one valid successor may extend a sealed state  

Consensus exists to confirm a truth already demonstrated by proof.

It does not manufacture truth through agreement.

---

## 2. Consensus Foundation

Consensus is derived from the following canonical sequence:

**Authenticated Origin → Valid Authority → Proven Intent → Constraint Compliance → Causal Validity → Deterministic Execution → Identical State Result**

Every participating node MUST evaluate this sequence using the same canonical rules.

A node MUST NOT accept an event merely because another node accepted it.

Each node MUST be able to verify the event independently.

---

## 3. Core Consensus Principles

### 3.1 Proof-Based Convergence

Consensus MUST result from independently verified proof.

Required proof categories include:

- identity proof  
- authentication proof  
- authority proof  
- delegation proof, where applicable  
- intent proof  
- state proof  
- causal proof  
- constraint-satisfaction proof  
- execution proof  
- cross-domain proof, where applicable  

A vote, endorsement, reputation score, or economic stake MUST NOT substitute for proof.

---

### 3.2 Deterministic Evaluation

Given the same:

- canonical parent state  
- event payload  
- proof bundle  
- execution rules  
- constraint set  
- domain context  

every compliant node MUST derive the same:

- validation result  
- verification result  
- execution result  
- state commitment  
- failure classification, if rejected  

Different outcomes from identical inputs constitute a consensus fault.

---

### 3.3 Independent Verification

Each node MUST independently confirm:

- the event’s authenticated origin  
- the actor’s authority  
- the validity of any delegation  
- the event’s causal position  
- the integrity of its proof bundle  
- the preservation of all applicable invariants  
- the deterministic result of execution  

Consensus MUST NOT depend on trusting a prior node’s conclusion.

---

### 3.4 Single Canonical Successor

A sealed state may have only one canonical successor at a given causal position.

Competing events that claim the same canonical position MUST NOT both be accepted.

The substrate MUST resolve eligibility before sealing. It MUST NOT create parallel canonical histories and attempt to reconcile them later.

---

### 3.5 Non-Economic Consensus

Consensus MUST NOT be influenced by:

- token ownership  
- staking weight  
- mining power  
- validator rewards  
- market value  
- fee priority  
- purchased governance influence  

Correctness cannot be bought, accumulated, or outvoted.

---

### 3.6 No Privileged Truth Authority

No node, operator, organization, cloud provider, AI system, or governance body may declare an invalid event canonical.

Administrative status does not create truth.

All participants remain subordinate to the same verification rules.

---

## 4. Consensus Preconditions

An event is eligible for consensus only when all required preconditions are satisfied.

### 4.1 Authenticated Origin

The event MUST originate from an authenticated identity or from an agent operating under valid, traceable authority.

Unauthenticated events are ineligible.

---

### 4.2 Current State Reference

The event MUST reference the correct canonical parent state.

Events based on:

- stale state  
- superseded state  
- nonexistent state  
- provisional state presented as final  
- conflicting state lineage  

MUST be rejected.

---

### 4.3 Complete Proof Bundle

All required proofs MUST be:

- present  
- internally consistent  
- cryptographically valid  
- temporally valid  
- bound to the event  
- reproducible across nodes  

Incomplete proof cannot produce partial consensus.

---

### 4.4 Constraint and Invariant Compliance

The event MUST preserve:

- identity constraints  
- authority constraints  
- delegation constraints  
- state constraints  
- causal constraints  
- domain invariants  
- safety requirements  

Consensus cannot legitimize a prohibited event.

---

### 4.5 Deterministic Executability

The event MUST be executable through canonical rules without relying on:

- node-local configuration  
- hidden state  
- uncontrolled randomness  
- external interpretation  
- unverifiable AI inference  
- mutable off-substrate assumptions  

An event that cannot be reproduced cannot become canonical.

---

## 5. Consensus Lifecycle

### 5.1 Event Intake

The canonical event enters the consensus process with:

- authenticated origin  
- transition payload  
- parent-state reference  
- proof bundle  
- domain context  
- temporal context  

Receipt alone does not imply acceptance.

---

### 5.2 Local Validation

Each node determines whether the event follows:

- schema rules  
- authority rules  
- delegation rules  
- mutability rules  
- temporal rules  
- causal rules  
- domain rules  

Validation asks:

**“Is this event permitted to proceed?”**

---

### 5.3 Proof Verification

Each node verifies that the event’s claims can be proven.

Verification asks:

**“Can every required claim be demonstrated cryptographically and causally?”**

---

### 5.4 Deterministic Execution

Each node independently computes the proposed result from the same authenticated inputs.

The computation MUST yield an identical post-state commitment.

---

### 5.5 Convergence Check

Consensus exists only when compliant nodes derive the same:

- event validity  
- execution output  
- canonical state hash  
- causal successor position  
- sealing commitment  

A mismatch prevents sealing.

---

### 5.6 Canonical Commitment

Once all consensus requirements are satisfied, the resulting event and state commitment become eligible for sealing.

Consensus prepares canonical truth.

Sealing finalizes it.

---

## 6. Consensus Roles Within the Substrate

### 6.1 ADT

The ADT submits authenticated intent and the proof-bearing event required for evaluation.

The ADT does not determine consensus.

---

### 6.2 MAIAi

MAIAi may evaluate:

- semantic coherence  
- contextual alignment  
- policy interpretation  
- anomalous meaning  
- cross-domain semantic consistency  

MAIAi MUST NOT vote on truth, override proof failure, or negotiate acceptance.

---

### 6.3 The Architect

The Architect applies canonical execution law and determines whether the event:

- satisfies structural rules  
- preserves constraints  
- fits causal lineage  
- produces a valid deterministic result  
- is eligible for commitment  

The Architect enforces consensus rules but does not possess discretionary authority over them.

---

### 6.4 BAINCA Sovereign Servers

BAINCA sovereign servers independently:

- verify proofs  
- execute canonical logic  
- derive state commitments  
- detect divergence  
- preserve sealed consensus outcomes  

No sovereign server may substitute trust for verification.

---

### 6.5 Canonical Routing

Routing preserves:

- event integrity  
- proof integrity  
- causal order  
- domain context  
- identical event delivery  

Routing MUST NOT alter the event or determine its validity.

---

## 7. Cross-Domain Consensus

A cross-domain event requires consensus over every affected domain boundary.

Each affected domain MUST verify:

- identity acceptability  
- authority applicability  
- delegation scope  
- semantic compatibility  
- local invariant preservation  
- causal continuity  
- state-result compatibility  

Cross-domain consensus MUST NOT erase domain sovereignty.

A domain may reject an event that violates its canonical rules, even when the event is valid elsewhere.

An event becomes cross-domain canonical only when the complete multi-domain proof set is valid.

---

## 8. Conflict Prevention

The substrate MUST prevent competing canonical outcomes before commitment.

Conflict conditions include:

- two events claiming the same parent and causal position  
- different payloads carrying the same event identifier  
- inconsistent state commitments  
- conflicting authority claims  
- contradictory domain proofs  
- mismatched execution results  
- competing sealing requests  

Conflicting events MUST remain unsealed until one valid canonical outcome can be proven.

Consensus MUST NOT resolve conflict through popularity or economic weight.

---

## 9. Consensus During Network Partition

A network partition MUST NOT create independent canonical truth.

During a partition:

- nodes may continue receiving candidate events  
- nodes may perform local validation and verification  
- uncoordinated candidates MUST remain provisional where global commitment is required  
- no node may rewrite the last shared sealed state  
- no competing partition outcome may be treated as globally canonical  

When connectivity is restored:

- nodes compare sealed anchors  
- provisional events are re-evaluated against canonical state  
- stale or conflicting candidates are rejected  
- valid events may be resubmitted against the current state  

Partition tolerance MUST preserve truth, not multiply it.

---

## 10. Consensus Failure Modes

The substrate MUST detect and reject consensus when:

- nodes derive different results from identical inputs  
- the parent state is disputed or stale  
- proofs differ across routed copies  
- execution depends on hidden or local state  
- causal ordering cannot be established  
- domain invariants conflict  
- authority is ambiguous  
- delegation cannot be resolved  
- event semantics are materially inconsistent  
- the resulting state hash does not match  
- sealing commitments diverge  

Consensus failure MUST NOT mutate canonical state.

---

## 11. Consensus Failure Response

When consensus fails:

1. The candidate event remains unsealed.  
2. No canonical state mutation occurs.  
3. The conflicting inputs or outputs are isolated.  
4. The last sealed state remains authoritative.  
5. Nodes produce deterministic fault records.  
6. The Architect identifies the failed consensus condition.  
7. MAIAi may produce a human-readable semantic explanation.  
8. Recovery or reconciliation begins from the last valid sealed boundary.  

Consensus failure is a containment event, not a competing truth.

---

## 12. Consensus Invariants

The following MUST always remain true:

- consensus depends on proof, not opinion  
- identical inputs produce identical outcomes  
- every node can verify independently  
- no economic mechanism determines validity  
- no authority can override failed proof  
- only one canonical successor occupies a causal position  
- invalid events cannot become valid through majority support  
- network partitions cannot create separate canonical histories  
- cross-domain consensus preserves each domain’s invariants  
- consensus failure cannot mutate canonical state  
- sealed consensus outcomes cannot be reinterpreted retroactively  

---

## 13. Security Guarantees

### 13.1 Byzantine Input Resistance

Malicious, malformed, or contradictory event submissions cannot alter state unless they satisfy every canonical proof and execution requirement.

---

### 13.2 Validator-Capture Resistance

Control over nodes does not create the ability to redefine valid execution law.

A captured node may become noncompliant, but it cannot make an invalid state canonical under the substrate rules.

---

### 13.3 Fork Resistance

The single-successor rule, causal validation, and sealing discipline prevent competing histories from becoming simultaneously canonical.

---

### 13.4 Replay Resistance

Previously accepted events cannot produce duplicate effects or occupy a new causal position.

Idempotence and state binding prevent replay-based consensus.

---

### 13.5 Semantic Consistency

Consensus cannot be reached on structurally identical events whose meaning differs materially across domains or nodes.

Semantic disagreement must be resolved before commitment.

---

## 14. Relationship to Other Layers

### L07 — Canonical State

Consensus determines whether all compliant nodes derive the same next canonical state.

### L08 — Canonical Routing

Routing delivers identical events and proofs while preserving causal order.

### L09 — Canonical Event Model

Consensus evaluates canonical events as the atomic units of state change.

### L10 — Unified Execution Law

Consensus is subordinate to the substrate-wide laws governing execution.

### L11 — Proof Primitives

Consensus relies on universally valid and reproducible proof structures.

### L12 — Idempotence Rules

Repeated processing cannot produce duplicate or divergent effects.

### L13 — Mutability Constraints

Consensus cannot authorize prohibited state mutation.

### L14 — Temporal Rules

Consensus requires valid temporal position and ordering.

### L15 — Causality Chain

Consensus requires a valid cause–effect relationship and unbroken lineage.

### L27 — Validation Rules

Validation establishes whether the event follows canonical rules.

### L28 — Verification Rules

Verification establishes whether the event’s claims can be proven.

### L31 — Constraint Model

Consensus cannot override non-negotiable constraints.

### L32 — State Model

Consensus requires identical derivation of the proposed next state.

### L33 — Transition Model

Consensus applies to the authenticated transition between canonical states.

### L35 — Integrity

Consensus outcomes must preserve structural, cryptographic, causal, and execution integrity.

### L49 — Resilience

Consensus faults are isolated without compromising the last valid canonical state.

### L51 — Sealing

A consensus-qualified event becomes authoritative only after canonical sealing.

---

## 15. Outcomes of the Consensus Model

L34 ensures:

- one canonical state across compliant nodes  
- deterministic convergence without token voting  
- no market-based control over truth  
- no acceptance by popularity  
- no competing canonical histories  
- independent verification at every node  
- safe cross-domain state agreement  
- deterministic containment of divergence  
- proof-based eligibility for sealing  
- persistent alignment with authenticated human authority  

Consensus within the Sovereign Substrate is not a negotiation among participants.

It is the shared recognition of a result that every compliant node can independently prove.

---

## Return to Navigation

- [Root Specification](../CANON_ROOT.md)  
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)  
- [Human Navigation Map](../CANON_NAV.md)

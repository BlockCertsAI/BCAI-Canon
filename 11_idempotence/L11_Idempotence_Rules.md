<!--
CANONICAL: TRUE
LAYER: L11
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

## L11 — Proof Primitives (Foundational Verification Rules)

The Proof Primitives layer defines the **foundational verification constructs** that all layers of the Sovereign Substrate rely upon for truth, validity, and authentication.

L11 answers the question:  
**“What must every proof contain, and what rules must every validation follow, regardless of domain or context?”**

These primitives are the substrate’s *irreducible verification atoms*.  
If any proof violates L11, it is invalid at every layer, in every domain, under every circumstance.

---

## 1. Purpose of Proof Primitives

Proof Primitives ensure that:

- identity is verifiable  
- authority is traceable  
- delegation is accountable  
- semantics are demonstrable  
- transitions are correct  
- constraints are enforced  
- safety is preserved  
- sealing is trustworthy  

L11 provides the **universal grammar of verification**.

---

# 2. Core Verification Primitives (MUST Exist in All Proofs)

### **2.1 Identity Binding Primitive**
Every proof MUST anchor to:
- a genesis identity (L01),  
- an ADT signature (L06),  
- and a non-repudiable identity hash.

No identity → no proof.

---

### **2.2 Authority Assertion Primitive**
Every proof MUST demonstrate:
- the role used to perform the action,  
- its scope,  
- its permitted boundaries,  
- its expiration or revocation state.

Authority must be present, valid, and contextual.

---

### **2.3 Delegation Chain Primitive**
Delegation, if present, must be:
- explicit,  
- cryptographically signed,  
- non-ambiguous,  
- non-recursive,  
- non-synthesizable by AI or automated systems.

The chain MUST resolve deterministically to a human identity.

---

### **2.4 Integrity Primitive**
The proof must demonstrate:
- no tampering of payload,  
- deterministic hashing,  
- correct lineage references,  
- canonical ordering consistency (L08).

Integrity is non-negotiable.

---

### **2.5 Semantic Validity Primitive**
Meaning MUST be:
- interpretable,  
- unambiguous,  
- aligned to domain rules,  
- validated through MAIAi (L03).

Ambiguous meaning invalidates the proof.

---

### **2.6 Constraint Satisfaction Primitive**
Every proof must show:
- constraint compliance (L31),  
- safety classification (L50),  
- invariant compatibility (L28).

No constraint → no execution.

---

### **2.7 Domain Compatibility Primitive**
Proof must demonstrate compatibility of:
- domain invariants,  
- execution context,  
- cross-zone semantics.

If domains disagree, the proof fails.

---

### **2.8 Non-Access Primitive**
No proof may:
- expose SVS content (L02),  
- derive private data,  
- reveal personal attributes.

Proofs must carry **evidence**, not **data**.

---

### **2.9 Causality Primitive**
Every proof must contain:
- prior state reference,  
- lineage hash (L37),  
- causal position,  
- sealing state reference.

Without causality → the transition is invalid.

---

### **2.10 Safety Primitive**
Proof must show:
- no hazard to system integrity,  
- no risk of semantic drift,  
- no unauthorized escalation,  
- compliance with L50 Safety.

Safety overrides intent and authority.

---

# 3. Proof Construction Rules

### **3.1 Completeness**
Proofs must include all primitives required for the action.  
Omission of any primitive = automatic rejection.

---

### **3.2 Determinism**
Proof verification MUST produce identical results on all nodes.

---

### **3.3 Non-Circularity**
Proofs may not reference themselves or rely on unresolved dependencies.

---

### **3.4 Forward-Only Resolution**
Proofs cannot reference:
- future lineage,  
- unsealed states,  
- unverified transitions.

Proofs must resolve entirely from known sealed truth.

---

### **3.5 Cryptographic Soundness**
All primitives MUST be built from:
- deterministic cryptographic hashes,  
- substrate-recognized signatures,  
- reproducible verification logic.

No external oracles may be required.

---

# 4. Proof Failure Rules

A proof MUST fail if:

- identity is missing or invalid  
- authority is incorrect or expired  
- delegation is malformed or circular  
- meaning is ambiguous  
- constraints are violated  
- invariants conflict  
- lineage is broken  
- sealed truth is contradicted  
- safety is uncertain  
- SVS content is exposed  
- hash integrity fails  
- validation cannot be reproduced deterministically  

Failure MUST NOT mutate state.

---

# 5. Proof Propagation Requirements

When proofs move across domains or nodes (via L08):

- all primitives MUST remain intact  
- no field may be added, altered, or removed  
- domain interoperability MUST be validated  
- semantics MUST survive cross-domain transfer  
- safety classification MUST remain consistent  

Routing must reject malformed or altered proofs.

---

# 6. Relationship to Other Layers

### **L01 Identity**  
Proofs require identity anchors.

### **L02 SVS**  
Proofs operate without revealing private data.

### **L03 MAIAi**  
Proof semantics validated through MAIAi.

### **L04 Architect**  
Architect verifies all primitives before execution.

### **L06 ADT**  
ADT packages proofs for transitions.

### **L07 Canonical State**  
Proofs define how state can be mutated.

### **L08 Routing**  
Routing propagates proofs across the substrate.

### **L31 Constraints**  
Proofs must satisfy all constraints.

### **L37 Lineage**  
Proofs extend and reference lineage.

### **L50 Safety**  
Safety must be proven, not assumed.

### **L51 Sealing**  
Sealed truth validates the proof’s finality.

---

# 7. Outcomes of the Proof Primitive Layer

- universal proof consistency  
- deterministic validation across nodes  
- verifiable identity and authority for all actions  
- elimination of ambiguous or incomplete transitions  
- substrate-wide enforcement of constraints and invariants  
- robust cross-domain interoperability  
- incorruptible state evolution  
- reliable recovery and auditability  
- protection against AI-generated or synthetic proofs  

L11 ensures that every action, in every domain, under every identity, rests on **provable, deterministic, and unforgeable verification primitives.**

Proofs become the **foundation of trust** in the Sovereign Substrate.

---

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

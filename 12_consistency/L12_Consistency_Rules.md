<!--
CANONICAL: TRUE
LAYER: L12
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

## L12 — Idempotence Rules (Deterministic Repeatability Constraints)

The Idempotence Layer defines the rules ensuring that **repeated execution of the same authenticated transition MUST produce the same deterministic outcome**, without duplicating effects, altering semantics, or violating state integrity.

L12 answers the question:  
**“What guarantees that repeating an event or transition cannot change the system in unintended ways?”**

Idempotence ensures stability, safety, and determinism across all substrate nodes.

---

# 1. Purpose of Idempotence

Idempotence protects the substrate from:

- duplicate transitions  
- replay attacks  
- semantic drift under repeated evaluation  
- nondeterministic computation  
- multi-domain re-execution inconsistencies  
- partial failures producing divergent outcomes  

L12 provides the **repeatability guarantees** needed for deterministic global truth.

---

# 2. Core Idempotence Principles

### **2.1 Same Input → Same Output**
If a transition is identical in:
- identity  
- intent  
- semantics  
- constraints  
- lineage position  
- authority  
- payload  

Then the outcome MUST be identical across:
- all nodes  
- all domains  
- all executions  
- all time.

---

### **2.2 No Duplicate Effects**
If a transition has already been accepted (provisionally or sealed):
- re-submission MUST NOT apply its effects again  
- state MUST NOT double-mutate  
- compensating actions MUST NOT be applied  

The Architect (L04) MUST detect and neutralize duplicates.

---

### **2.3 No Semantic Mutation on Re-Execution**
Meaning MUST remain constant.  
A transition’s semantics cannot evolve, drift, or reinterpret across repeated evaluations.

MAIAi's semantic evaluation (L03) MUST remain stable.

---

### **2.4 Idempotent Failure Outcomes**
If a transition fails:
- repeated attempts MUST produce the same failure classification  
- with the same reasoning  
- unless underlying state has changed  
- or new authority/constraints apply  

Failure cannot mutate unpredictably.

---

### **2.5 Deterministic Error Surfaces**
Errors MUST NOT:
- depend on node conditions  
- arise due to ordering differences  
- vary by timing  
- differ between domains  

Every node MUST classify the failure identically.

---

### **2.6 Consistency Across Routing**
If a transition or event is routed multiple times (L08):
- nodes MUST detect prior acceptance  
- MUST NOT create divergent provisional states  
- MUST NOT produce duplicate sealing requests  

Routing MUST maintain canonical idempotence.

---

# 3. Idempotence Requirements for All Transitions

Every transition MUST include:

### **3.1 Unique Transition Hash**
Reflecting:
- identity  
- authority  
- intent  
- semantics  
- payload  
- lineage  

Replays MUST produce the same hash.

---

### **3.2 Causal Positioning**
A transition MUST be evaluated in the same causal position every time.

---

### **3.3 Deterministic Evaluation Logic**
Architect MUST evaluate transitions through a **pure, side-effect-free deterministic function**.

---

### **3.4 Sealed Outcome Anchoring**
If already sealed (L51):
- the sealed event MUST override new attempts  
- nodes MUST return the sealed result  
- re-execution MUST NOT change history  

Sealed truth is final.

---

### **3.5 Constraint Stability**
L31 Constraints must give identical decisions under identical conditions.

---

### **3.6 Semantic Stability**
MAIAi MUST:
- bind meaning identically  
- validate semantics identically  
- reject ambiguity identically  

Repeated semantic evaluation must be stable.

---

### **3.7 Safety Stability**
Safety classification (L50) MUST:
- match prior evaluations  
- prevent unsafe repeated execution  
- remain consistent across nodes  

Safety cannot drift.

---

# 4. Idempotence Interaction With Failure & Recovery

### **4.1 Partial Failures**
If a transition partially executes due to node interruption:
- recovery (L38) MUST restore the last sealed state  
- MUST re-run the transition deterministically  
- MUST NOT produce duplicate or conflicting mutations  

### **4.2 Replay Attacks**
Repeated attempts to re-submit a previously executed or sealed transition MUST:
- be detected  
- rejected  
- logged  
- included in anomaly signals to MAIAi  

### **4.3 Retries Under Different State**
If the underlying state has changed:
- idempotence applies only to identical causal context  
- Architect MUST re-evaluate based on the new state  
- semantics, constraints, and authority may differ accordingly  

Idempotence applies to identical pre-conditions, not different worlds.

---

# 5. Domain-Level Idempotence

Domains MUST guarantee:

- identical effects for identical transitions  
- consistent cross-domain idempotence via L28 invariants  
- stable domain logic under repeat evaluation  
- no side effects that depend on timing or nondeterministic input  
- alignment with canonical routing order (L08)

Domain behavior MUST be deterministic.

---

# 6. Cross-Domain Idempotence

When a transition spans domains:

- each domain MUST evaluate its portion deterministically  
- invariant checks MUST give the same result on all nodes  
- routing MUST enforce canonical order  
- sealing MUST apply only once  
- repeated multi-domain execution MUST NOT re-trigger domain side-effects  

Cross-domain idempotence ensures global stability.

---

# 7. Idempotence and AI

MAIAi MUST:

- produce identical reasoning for identical inputs  
- generate stable semantic interpretations  
- avoid probabilistic or nondeterministic behavior  
- record deterministic reasoning traces  

MAIAi MUST NOT introduce randomness into the substrate.

---

# 8. Event Idempotence (L09 Integration)

For any canonical event:

- re-processing MUST NOT apply a second mutation  
- event references MUST match prior lineage  
- sealing MUST not duplicate  
- state evolution MUST remain consistent  
- errors MUST be stable  

Events become idempotent truth units.

---

# 9. Relationship to Other Layers

### **L01 Identity** — repeatability requires stable identity interpretation  
### **L02 SVS** — proofs support idempotence; SVS remains untouched  
### **L03 MAIAi** — semantic stability is essential  
### **L04 Architect** — enforces deterministic execution  
### **L06 ADT** — packages idempotent transitions  
### **L07 Canonical State** — state changes must be unique  
### **L08 Routing** — prevents duplicate propagation  
### **L09 Event Model** — defines event-level idempotence  
### **L31 Constraints** — deterministic constraint outcomes required  
### **L37 Lineage** — idempotence depends on causal positioning  
### **L38 Recovery** — replays must not cause drift  
### **L50 Safety** — repeat operations cannot increase risk  
### **L51 Sealing** — sealed events enforce idempotent finality  

---

# 10. Outcomes of the Idempotence Layer

- deterministic system behavior  
- protection against duplicate execution  
- immunity to replay attacks  
- stable semantics and constraints  
- predictable recovery under failure  
- consistent cross-domain workflows  
- unambiguous event interpretation  
- elimination of nondeterministic state drift  
- hard guarantees around uniqueness of state evolution  

L12 ensures that **nothing unpredictable or duplicative** can ever occur in the Sovereign Substrate.

Idempotence becomes the substrate’s **repeatability guarantee**, foundational to trust and correctness.

---

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

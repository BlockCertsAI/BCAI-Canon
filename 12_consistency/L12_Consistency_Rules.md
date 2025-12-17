<!--
CANONICAL: TRUE
LAYER: L12
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for Idempotence rules governing deterministic repeatability.
NOTES:
 - Do not remove this header.
 - This file defines canonical idempotence constraints for the substrate.
-->

## L12 — Idempotence Rules  
### (Deterministic Repeatability Constraints)

The Idempotence Layer defines the rules ensuring that **repeated execution of the same authenticated transition MUST produce the same deterministic outcome**, without duplicating effects, altering semantics, or violating state integrity.

L12 answers the question:  
**“What guarantees that repeating an event or transition cannot change the system in unintended ways?”**

Idempotence ensures stability, safety, and determinism across all substrate nodes.

---

## 1. Purpose of Idempotence

Idempotence protects the substrate from:

- duplicate transitions  
- replay attacks  
- semantic drift under repeated evaluation  
- nondeterministic computation  
- multi-domain re-execution inconsistencies  
- partial failures producing divergent outcomes  

L12 provides the **repeatability guarantees** required for global canonical truth.

---

## 2. Core Idempotence Principles

### **2.1 Same Input → Same Output**
If a transition is identical in:
- identity  
- intent  
- semantics  
- constraints  
- lineage position  
- authority  
- payload  

then the outcome MUST be identical across:
- all nodes  
- all domains  
- all executions  
- all time  

---

### **2.2 No Duplicate Effects**
If a transition has already been accepted (provisionally or sealed):
- re-submission MUST NOT apply effects again  
- state MUST NOT double-mutate  
- compensating or inverse actions MUST NOT occur  

The Architect (L04) MUST detect and neutralize duplicates.

---

### **2.3 No Semantic Mutation on Re-Execution**
A transition’s meaning MUST remain constant.

MAIAi semantic validation (L03) MUST produce identical interpretations under identical inputs.

Semantic drift is forbidden.

---

### **2.4 Idempotent Failure Outcomes**
If a transition fails:
- repeated evaluation MUST yield the same failure class  
- the same reasoning trace  
- the same rejection semantics  

unless underlying state, authority, or constraints have changed.

---

### **2.5 Deterministic Error Surfaces**
Errors MUST NOT:
- vary by node  
- depend on timing  
- depend on execution order  
- differ across domains  

Every node MUST classify failure identically.

---

### **2.6 Consistency Across Routing**
If a transition or event is routed multiple times (L08):
- prior acceptance MUST be detected  
- duplicate provisional states MUST NOT be created  
- duplicate sealing MUST NOT occur  

Routing MUST preserve idempotence globally.

---

## 3. Idempotence Requirements for All Transitions

### **3.1 Unique Transition Hash**
Every transition MUST include a deterministic hash covering:
- identity  
- authority  
- intent  
- semantics  
- payload  
- lineage  

Replays MUST produce the same hash.

---

### **3.2 Causal Positioning**
Transitions MUST be evaluated at the same causal position on every execution.

---

### **3.3 Deterministic Evaluation Logic**
The Architect MUST evaluate transitions through a **pure, side-effect-free deterministic function**.

---

### **3.4 Sealed Outcome Anchoring**
If a transition is already sealed (L51):
- the sealed result MUST be returned  
- re-execution MUST NOT alter history  

Sealed truth is final.

---

### **3.5 Constraint Stability**
Constraint evaluation (L31) MUST produce identical results under identical conditions.

---

### **3.6 Semantic Stability**
MAIAi MUST:
- bind meaning identically  
- validate semantics identically  
- reject ambiguity identically  

---

### **3.7 Safety Stability**
Safety classification (L50) MUST:
- match prior evaluations  
- prevent unsafe repeat execution  
- remain consistent across nodes  

---

## 4. Idempotence and Failure & Recovery

### **4.1 Partial Failures**
If a node fails mid-execution:
- recovery (L38) MUST restore last sealed state  
- transition MUST re-evaluate deterministically  
- no duplicate or conflicting mutations may occur  

---

### **4.2 Replay Attacks**
Re-submission of previously executed or sealed transitions MUST:
- be detected  
- be rejected  
- be logged  
- be surfaced as anomaly signals  

---

### **4.3 Retries Under Changed State**
If underlying state has changed:
- idempotence applies only to identical preconditions  
- the transition MUST be re-evaluated  
- outcomes may legitimately differ  

Idempotence applies to the **same world-state**, not different ones.

---

## 5. Domain-Level Idempotence

Domains MUST ensure:

- identical effects for identical transitions  
- deterministic domain logic  
- no time-based or nondeterministic side effects  
- invariant-aligned repeatability (L28)  
- routing-order consistency (L08)  

---

## 6. Cross-Domain Idempotence

For cross-domain transitions:

- each domain MUST evaluate deterministically  
- invariant checks MUST be consistent  
- sealing MUST occur only once  
- repeated execution MUST NOT re-trigger domain effects  

Global idempotence is mandatory.

---

## 7. Idempotence and AI

MAIAi MUST:

- produce identical reasoning for identical inputs  
- avoid probabilistic behavior  
- emit deterministic reasoning traces  

AI MUST NOT introduce randomness into substrate execution.

---

## 8. Event Idempotence (L09 Integration)

For canonical events:

- re-processing MUST NOT apply duplicate mutations  
- lineage references MUST remain stable  
- sealing MUST NOT duplicate  
- error states MUST be consistent  

Events are idempotent units of truth.

---

## 9. Real-World Capability Enabled by Idempotence

Idempotence enables **failure-tolerant, legally reliable automation**.

It allows:
- Financial, healthcare, and government systems to safely retry operations without risk of double-spend, double-issuance, or duplicated authority.
- Distributed infrastructure to recover from crashes, partitions, or restarts without reconciliation or manual correction.
- Regulators and auditors to rely on execution outcomes even under repeated processing.
- Global systems to resist replay attacks, message duplication, and network instability by design.

Idempotence turns retrying from a risk into a guarantee.

---

## 10. Relationship to Other Layers

- **L01 Identity** — stable identity interpretation  
- **L02 SVS** — proofs enable idempotence without data exposure  
- **L03 MAIAi** — semantic stability  
- **L04 Architect** — deterministic enforcement  
- **L06 ADT** — idempotent transition packaging  
- **L07 Canonical State** — unique state evolution  
- **L08 Routing** — duplicate suppression  
- **L09 Event Model** — event-level idempotence  
- **L31 Constraints** — deterministic constraint outcomes  
- **L37 Lineage** — causal positioning  
- **L38 Recovery** — safe replay  
- **L50 Safety** — repeat execution cannot increase risk  
- **L51 Sealing** — idempotent finality  

---

## 11. Outcomes of the Idempotence Layer

- deterministic system behavior  
- immunity to duplicate execution  
- resistance to replay attacks  
- stable semantics and constraints  
- predictable recovery under failure  
- consistent cross-domain workflows  
- elimination of nondeterministic drift  
- guaranteed uniqueness of state evolution  

L12 ensures that **nothing unpredictable or duplicative** can occur in the Sovereign Substrate.

Idempotence becomes the substrate’s **repeatability guarantee**, foundational to trust and correctness.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

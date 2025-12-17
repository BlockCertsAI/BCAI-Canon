<!--
CANONICAL: TRUE
LAYER: L14
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

## L14 — Temporal Rules (Time, Ordering & Validity Constraints)

The Temporal Rules Layer establishes the canonical framework for **time, ordering, validity windows, and temporal consistency** across the Sovereign Substrate.

L14 answers the question:  
**“What does it mean for an event to happen *before*, *after*, or *now* — and how is temporal validity guaranteed?”**

Time inside the substrate is **logical, causal, and sealed**, not dependent on physical clocks or node-local timing.

---

## 1. Purpose of Temporal Rules

L14 prevents:

- replay attacks  
- ordering inconsistencies  
- temporal paradox (e.g., referencing future state)  
- cross-domain time drift  
- validity-window violations  
- race conditions  
- nondeterministic evaluation  
- node clock manipulation  

Temporal Rules form the substrate’s **shared sense of time** and guarantee globally consistent truth.

---

## 2. Types of Time in the Sovereign Substrate

### **2.1 Canonical Time**
Derived from:
- sealed event order (L51)  
- lineage (L37)  
- causal dependencies  

Canonical Time is the **only authoritative timeline**.

---

### **2.2 Logical Time**
Derived from:
- Architect evaluation sequencing (L04)  
- deterministic transition ordering  
- internal execution dependencies  

Logical Time is how the substrate *evaluates*, not how it *remembers*.

---

### **2.3 Domain Time**
Domains may have local temporal semantics, but:

- they MUST map to Canonical Time deterministically  
- domain clocks MUST NOT override sealed truth  
- differences MUST NOT change event order  

---

### **2.4 External Time**
Physical clocks may provide informational context, but:

- they MUST NOT determine canonical ordering  
- they MUST NOT be trusted for truth  
- they MUST NOT influence sealing  

External timestamps are advisory only.

---

## 3. Temporal Ordering Rules

### **3.1 No Event May Reference the Future**
A transition MUST fail if it references:

- an unsealed state  
- a future lineage hash  
- a future ADT  
- an event that does not yet exist  

---

### **3.2 Ordering Must Be Deterministic**
All nodes MUST derive event order identically using:

- lineage  
- domain invariants  
- deterministic Architect evaluation  

Clocks MUST NOT influence ordering.

---

### **3.3 Ordering Is Strict**
Events MUST obey strict causal order:

**Predecessor → Successor → Sealed Successor**

There are no parallel canon states.

---

### **3.4 No Retroactive Mutation**
An event MUST NOT:

- rewrite past sealed truth  
- inject earlier events  
- override sealed sequences  
- reinterpret historical meaning  

Sealed time is immutable forever.

---

## 4. Validity Windows

### **4.1 Validity MUST Be Explicit**
All time-sensitive transitions MUST define:

- start-of-validity  
- end-of-validity  
- authority expiration  
- delegation expiration  

No implicit validity windows are permitted.

---

### **4.2 Expired Transitions MUST Be Rejected**
If the transition is outside its validity window:
- it MUST NOT execute  
- it MUST NOT influence state  

---

### **4.3 Renewal Must Follow Canon**
Renewing authority, credentials, or permissions requires:

- new proofs  
- new lineage  
- new semantic evaluation  

Renewal is never automatic.

---

## 5. Temporal Consistency Requirements

### **5.1 Causal Position MUST Match**
A transition MUST be evaluated at its correct causal location:

- based on lineage  
- based on semantic context  
- based on domain invariants  

Incorrect positioning invalidates the event.

---

### **5.2 Deterministic Replay**
Upon replay or retry:

- ordering MUST remain identical  
- placement MUST be deterministic  
- sealing MUST enforce original position  

---

### **5.3 Cross-Domain Temporal Alignment**
Domains MUST:

- reconcile local time to canonical time  
- validate local events against global ordering  
- reject temporal conflicts  

---

### **5.4 Routing Temporal Guarantees**
Routing (L08) MUST ensure:

- no event bypasses predecessors  
- no out-of-order evaluation  
- no event is processed twice at different times  

---

## 6. Temporal Proof Requirements

Transitions requiring temporal validity MUST include:

### **6.1 Temporal Anchors**
- predecessor reference  
- lineage hash  
- validity window  

### **6.2 Temporal Justification**
- why now  
- domain-specific temporal semantics  

### **6.3 Temporal Safety Guarantee**
Ensures the transition:

- causes no paradox  
- remains stable across nodes  
- cannot diverge upon replay  

---

## 7. Temporal Failure Modes

A transition MUST fail if:

- its validity window has expired  
- authority or delegation is expired  
- it references future state  
- its ordering is nondeterministic  
- its position conflicts with lineage  
- domain clocks disagree with canonical truth  
- replay would produce a different ordering  

Rejected transitions MUST NOT mutate state.

---

## 8. Temporal Reconciliation

### **8.1 Drift Detection**
If a domain or node drifts:

- MAIAi detects drift  
- Architect enforces canonical time  
- domain activity may be suspended  

### **8.2 Deterministic Temporal Recovery**
Recovery (L38) restores:

- correct event position  
- correct lineage chain  
- correct ordering  

### **8.3 Out-of-Order Correction**
Out-of-order events MUST:

- be deferred  
- or rejected  
- NEVER reorder sealed truth  

---

## 9. Temporal Safety

A transition MUST be rejected if it:

- introduces timeline divergence  
- allows nondeterministic execution  
- enables replay-based mutation  
- violates sealed ordering  
- breaks semantic continuity  

Temporal Safety integrates with the L50 Safety Layer.

---

## 10. Real-World Capability Enabled by Temporal Rules

Temporal Rules enable **legally defensible, globally synchronized execution**.

They allow:
- Financial systems to enforce settlement windows, expirations, and sequencing without relying on wall-clock trust.
- Governments to guarantee the order of filings, votes, or authorizations across jurisdictions.
- Healthcare and compliance systems to prove *when* consent, access, or revocation occurred with canonical certainty.
- Distributed infrastructure to eliminate race conditions, double-spend timing exploits, and clock-based attacks.
- Auditors and courts to rely on a single authoritative timeline immune to manipulation.

Temporal rules turn time from a **source of dispute** into a **provable property of truth**.

---

## 11. Relationship to Other Layers

### **L01 Identity** — identity origin cannot be time-shifted  
### **L02 SVS** — proofs reference time but reveal no content  
### **L03 MAIAi** — resolves domain temporal semantics  
### **L04 Architect** — enforces deterministic ordering  
### **L06 ADT** — binds transitions to correct temporal anchors  
### **L07 Canonical State** — stores unified timeline  
### **L08 Routing** — preserves correct propagation order  
### **L09 Events** — events *define* canonical time  
### **L11 Proof Primitives** — require temporal anchors  
### **L12 Idempotence** — replay must yield identical position  
### **L13 Mutability Constraints** — no retroactive mutation  
### **L28 Invariants** — include domain temporal invariants  
### **L37 Lineage** — expresses temporal sequence  
### **L38 Recovery** — corrects improper temporal placement  
### **L50 Safety** — includes temporal hazard detection  

---

## 12. Outcomes of Temporal Rules

- one universal timeline  
- no replay-based mutation  
- no temporal paradox  
- strict causal consistency  
- deterministic ordering  
- predictable recovery  
- cross-domain time coherence  
- sealed truth protected from retroactive change  
- no clock-based attacks  
- guaranteed auditability of temporal flow  

L14 ensures that **the substrate cannot be desynchronized, reversed, spoofed, or placed into temporal conflict**.

It forms the backbone of canonical truth.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

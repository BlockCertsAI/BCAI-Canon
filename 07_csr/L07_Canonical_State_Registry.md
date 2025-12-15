<!--
CANONICAL: TRUE
LAYER: L7
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for the Sovereign Substrate CSR (Credential, State & Responsibility) layer.
-->

## L07 Canonical State

The Canonical State is the **authoritative representation of truth** within the Sovereign Substrate.  
It expresses the complete, consistent, and sealed condition of all domains at a given moment.

L07 answers the question:  
**“What is the official state of the system, how is it structured, and how does it evolve without ambiguity, drift, or contradiction?”**

Canonical State is not a log, a ledger, a cache, or an opinion.  
It is *the* truth — globally consistent, provable, and immutable in its historical form.

---

## Core Principles

### **1. Singular Truth**
At any time, the substrate has exactly **one canonical state** across all nodes.  
If a node diverges, it is corrected through recovery (L38) until it matches the canonical truth.

### **2. Forward-Only Evolution**
State evolves strictly forward through validated, verified, constrained, and sealed transitions.  
Rollback is forbidden.  
History is immutable.

### **3. Domain-Isolated, Substrate-Integrated**
Each domain maintains its own state, but all domain states are bound together in a single canonical global structure.

### **4. Deterministic Representation**
Canonical State must be representable identically across:
- all nodes  
- all domains  
- all environments  
- all architectures  

No nondeterministic representation of state is allowed.

---

## Components of Canonical State

Canonical State consists of:

### **1. Global Root State**
A sealed representation of:
- domain states  
- lineage position  
- global invariants  
- substrate metadata  

This is the “system snapshot” of truth.

---

### **2. Domain State Structures**
Each domain maintains:
- entity records  
- domain-specific invariants  
- local transition effects  
- role and authority mappings  
- zone-level rules  

Domain state must obey:
- L28 invariants  
- L31 constraints  
- L50 safety rules  

---

### **3. Identity State**
Identity state includes:
- active identities  
- role bindings  
- delegations  
- revocation states  
- identity lifecycle metadata  

Identity state is immutable in origin but may evolve through valid transitions.

---

### **4. Authority State**
Authority state defines who is allowed to do what:
- role assignments  
- scope definitions  
- permission levels  
- delegation graphs  

Authority state must align with L21–L22.

---

### **5. Constraint State**
All constraints (L31) are part of canonical state:
- system-wide invariants  
- domain-specific constraints  
- safety thresholds  
- semantic boundaries  

Constraints are immutable except via governance processes.

---

### **6. Semantic State**
Semantic State captures:
- meaning mappings  
- domain-specific context rules  
- MAIAi-supported semantic definitions  
- lineage-bound interpretation references  

This ensures semantic continuity across time.

---

### **7. Sealing State**
A record of:
- last sealed transition  
- seal chain position  
- cryptographic commitments  
- global sealing certificate references  

State is not canonical until sealed (L51).

---

## How Canonical State Evolves

Canonical State evolves only through:

### **1. Transition Intake (via ADT)**
A transition arrives from L06.

### **2. Semantic Validation (MAIAi, L03)**
Ensures meaning is correct and domain-compatible.

### **3. Constraint Enforcement (L31)**
Ensures safety, invariants, and domain rules.

### **4. Deterministic Execution (Architect, L04)**
Architect applies the mutation consistently across all nodes.

### **5. Sealing (L51)**
Once sealed, the new state becomes official truth.

---

## What Canonical State Cannot Contain

Canonical State must **never** include:
- private SVS data  
- inferred or synthetic information  
- undecided or provisional transitions  
- ambiguous meaning  
- incomplete authority references  
- nondeterministic metadata  
- AI-generated assumptions  
- speculative predictions  
- temporary caches or logs  

State contains only **verified truth**.

---

## Guarantees of Canonical State

### **1. Integrity**
No unauthorized state mutation is possible.

### **2. Immutability of History**
Once sealed, the historical state is never modified.

### **3. Causality**
Every state follows correctly from the prior sealed state (L37).

### **4. Safety**
State must always satisfy L50 Safety Model.

### **5. Global Agreement**
Every node that claims to be part of the substrate must maintain identical canonical state.

### **6. Non-Leakage**
State may reference private data via proofs but never exposes or stores raw SVS content.

---

## Relationship to Other Layers

### **L01 Genesis Identity**
Identity forms part of state’s root structure.

### **L02 SVS**
State stores references and proofs, not contents of SVS.

### **L03 MAIAi**
State includes semantic structures determined and validated by MAIAi.

### **L04 Architect**
Architect executes state transitions.

### **L06 ADT**
ADT submits state-changing transitions.

### **L28 Invariants**
State enforces invariants at domain boundaries.

### **L31 Constraints**
State cannot violate constraints.

### **L37 Lineage**
Every state has a clear and unbroken lineage reference.

### **L38 Recovery**
Recovery restores nodes to the canonical state.

### **L50 Safety**
State evolution must respect strict safety rules.

### **L51 Sealing**
State becomes canonical only when sealed.

---

## Outcomes of the Canonical State Layer

- all nodes converge to a single authoritative truth  
- users interact with a consistent substrate regardless of domain  
- privacy is preserved while still enabling global verification  
- ambiguity, drift, or forks are impossible by design  
- the system becomes self-consistent and self-validating  
- governance and compliance are enforced at the state level  

Canonical State is the **center of gravity** of the Sovereign Substrate —  
the point from which truth flows and to which all computation returns.

---

Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

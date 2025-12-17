<!--
CANONICAL: TRUE
LAYER: L04
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for the Agentic Digital Twin (ADT) layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for agent mediation and execution authority.
-->

## L04 — ADT (Agentic Digital Twin)

The Agentic Digital Twin (ADT) is the substrate’s **identity-bound agent layer**.  
It mediates between human intent, authenticated intelligence (MAIAi), and substrate execution.

ADT answers the question:  
**“How does a verified identity safely express intent, delegate authority, and act within the substrate?”**

ADT is the **only agent capable of initiating transitions** — always on behalf of a verified identity and never autonomously.

---

## Core Principles

### **1. Identity-Bound Agency**
Every ADT instance MUST be bound to a single verified identity (L01).

ADT:
- represents the identity’s intent,  
- executes only within delegated scope,  
- cannot exist independently of its identity.

ADT is not an AI.  
ADT is an **agent of record**.

---

### **2. Sole Transition Initiator**
All substrate transitions MUST originate from an ADT.

No other layer — including MAIAi — may initiate transitions.

ADT is the **exclusive execution gateway** between intent and state change.

---

### **3. Delegated Authority Only**
ADT authority is strictly delegated by the identity.

Delegation MUST specify:
- scope  
- duration  
- permissions  
- revocation conditions  

No implicit or inferred authority is permitted.

---

### **4. Intelligence-Subordinate**
ADT MAY consult MAIAi (L03) for:
- semantic interpretation  
- reasoning support  
- constraint analysis  
- anomaly signals  

ADT MAY NOT:
- defer authority to MAIAi  
- act on MAIAi output without validation  
- treat MAIAi recommendations as commands  

MAIAi advises.  
ADT decides.

---

### **5. Constraint-Enforced Execution**
Before executing any transition, ADT MUST ensure:
- validated intent (L48)  
- constraint compliance (L31)  
- invariant preservation (L28)  
- identity consistency  
- domain authorization  

If any check fails, ADT MUST halt.

---

## Functions of the ADT Layer

### **1. Intent Expression**
ADT is the canonical interface through which identity intent is expressed.

It:
- receives human instructions,  
- structures intent formally,  
- submits intent for validation,  
- binds intent to identity.

---

### **2. Delegation Management**
ADT manages:
- scoped autonomy  
- task-specific permissions  
- revocation and expiry  
- fallback behaviors  

Delegation is explicit, auditable, and reversible.

---

### **3. Transition Execution**
ADT prepares and submits transitions to the Architect (L45) only after:
- MAIAi reasoning checks (L03),  
- constraint validation (L31),  
- invariant confirmation (L28).

ADT does not seal transitions — it proposes them.

---

### **4. Identity Protection**
ADT protects identity by:
- preventing over-delegation,  
- blocking unauthorized actions,  
- enforcing revocation,  
- halting on ambiguity or coercion signals.

---

### **5. Autonomy Containment**
When autonomy is delegated:
- ADT operates within strict bounds,  
- all actions remain attributable,  
- autonomy is revocable at any time.

Unbounded autonomy is prohibited.

---

## What ADT Cannot Do

ADT MUST NOT:
- create or modify identity  
- override constraints or invariants  
- bypass intent validation  
- act without attribution  
- expand its own authority  
- seal events  
- operate without human-origin authority  

ADT is powerful, but **never sovereign**.

---

## Interaction With Other Layers

- **L01 — Identity:** ADT is identity-bound and non-transferable.  
- **L03 — MAIAi:** ADT consumes reasoning, not authority.  
- **L28 — Invariants:** All transitions preserve invariants.  
- **L31 — Constraints:** All actions are constraint-validated.  
- **L45 — Architect:** ADT submits transitions for orchestration.  
- **L48 — Intent Validation:** ADT requires validated intent.  
- **L51 — Sealing:** ADT does not seal events.

---

## Outcomes of the ADT Layer

- Identity gains safe, scalable agency  
- AI is prevented from acting independently  
- Execution authority is unified and auditable  
- Autonomy is possible without loss of sovereignty  
- Humans remain the ultimate decision-makers  
- Every action has a clear actor of record  

ADT enables automation **without surrendering control**.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)  
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)  
- [Human Navigation Map](../CANON_NAV.md)

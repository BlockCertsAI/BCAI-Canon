<!--
CANONICAL: TRUE
LAYER: L06
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for the Agentic Digital Twin (ADT) layer.
NOTES:
  - Do not remove this header.
  - This file defines canonical rules for this substrate layer.
-->

## L06 — Agentic Digital Twin (ADT)

The Agentic Digital Twin (ADT) is the authenticated operational extension of a human’s genesis identity.  
It acts as a **proxy agent** that performs permitted actions, manages domain interactions, submits transitions, and translates human intent into substrate-ready form — all under strict constraint and verification.

ADT answers the question:  
**“How does a human participate in the substrate without exposing private keys, revealing SVS contents, or interacting with raw protocol complexity?”**

ADT is a controlled, identity-bound, rule-constrained agent — not an autonomous actor.

---

## Core Principles

### **1. Identity-Origin Only**
ADT cannot exist without a genesis identity (L01).  
It inherits:
- permissions  
- constraints  
- domain roles  
- delegation rules  

ADT is always subordinate to its human owner.

---

### **2. No Autonomy**
ADT cannot:
- self-initiate actions  
- generate intent  
- alter identity  
- override constraints  
- expand its authority  
- act without explicit human-triggered cause  

ADT operates **only** as a vehicle for authenticated human-origin transitions.

---

### **3. Boundary Coordination**
ADT mediates interactions between:
- the user  
- domains  
- MAIAi  
- Architect  
- SVS (access proofs, not data)  
- cross-domain workflows  

It is the substrate’s **primary coordination vessel**.

---

### **4. SVS Protection**
ADT cannot access, read, modify, or infer contents of the Secure Virtual Space (L02).  
It can only:
- request proofs  
- submit user-authorized disclosures  
- validate permissions  

ADT respects privacy boundaries absolutely.

---

## ADT Responsibilities

### **1. Intent Translation**
ADT receives explicit human intent and translates it into:
- structured transition requests  
- domain-specific formats  
- constraint-respecting actions  

ADT cannot infer or guess intent — it only carries declared intent.

---

### **2. Transition Submission**
ADT is the **only entity allowed** to submit transitions to the Architect (L04).  
A transition must come through ADT or it is invalid.

ADT attaches:
- identity proofs  
- authority proofs  
- delegation context  
- semantic metadata  
- safety flags  

MAIAi evaluates meaning; the Architect constructs execution plans.

---

### **3. Authority Execution**
ADT applies authority rules from L21–L22:
- acts within granted scope  
- enforces role boundaries  
- respects domain permissions  
- prevents privilege escalation  

ADT cannot exceed user-granted authority.

---

### **4. Delegation Handling**
ADT manages delegated permissions (L30), including:
- scope  
- duration  
- revocation  
- inheritance rules  
- cross-domain delegation  

Delegation is never automatic — ADT enforces all constraints.

---

### **5. Domain Integration**
ADT handles:
- domain-specific requests  
- acquisition of domain roles  
- domain invariants (L28)  
- domain-switch execution contexts  

Domain drift or inconsistency triggers immediate rejection.

---

### **6. Semantic Context for MAIAi**
ADT provides MAIAi with:
- safe prompts  
- structured inputs  
- non-private context  
- role and domain framing  

MAIAi cannot request raw data from ADT — it must operate on permitted abstractions.

---

### **7. Verification Coordination**
ADT ensures all elements needed for verification are present:
- proofs  
- authority attestations  
- identity bindings  
- lineage references  
- safety attributes  

If verification cannot complete, ADT halts the transition.

---

### **8. Error & Exception Handling**
ADT:
- receives Architect rejection diagnostics  
- interprets MAIAi warnings  
- provides user-level explanations  
- resolves domain conflicts  
- resubmits corrected transitions  

ADT ensures the user never interacts with raw failure states.

---

## What ADT Cannot Do

ADT is strictly limited:

- cannot generate intent  
- cannot modify sealed state  
- cannot access SVS contents  
- cannot bypass constraints  
- cannot escalate its own authority  
- cannot create identities  
- cannot operate without identity signatures  
- cannot override MAIAi or Architect  
- cannot act autonomously  
- cannot circumvent safety or domain rules  

ADT is a **mediator**, not a decision-maker.

---

## Real-World Capability Enabled by ADT

The ADT enables **human participation at scale** in complex, regulated digital systems without requiring technical expertise or direct key custody.

Specifically, ADT allows:
- Individuals and enterprises to interact with blockchain, AI, governance, and compliance systems  
  without handling cryptographic primitives or protocol mechanics.
- Secure delegation of authority to assistants, workflows, or organizations  
  while retaining ultimate human control and revocation rights.
- Safe cross-domain participation  
  (identity, healthcare, finance, governance, enterprise operations)  
  without data leakage or loss of sovereignty.
- AI-assisted interaction  
  where intelligence supports users but cannot act independently or override intent.

ADT makes advanced digital infrastructure **usable by humans**,  
without compromising security, privacy, or accountability.

---

## Interaction With Other Layers

### **With L01 Identity**
ADT is bound permanently to the genesis identity that created it.

### **With L02 SVS**
ADT may request proofs but cannot access or interpret vault content.

### **With L03 MAIAi**
ADT supplies structured context; MAIAi ensures semantic correctness.

### **With L04 Architect**
ADT submits transitions; the Architect plans lawful execution sequences.

### **With L05 Execution**
ADT-origin transitions are executed deterministically once approved.

### **With L28 Invariants**
ADT must conform to domain-level invariants.

### **With L31 Constraints**
ADT enforces constraints before submission.

### **With L48 Intent Validation**
ADT carries user intent and proves its authenticity.

### **With L51 Sealing**
ADT delivers necessary metadata but does not seal transitions.

---

## ADT Lifecycle

### **1. Creation**
ADT is instantiated after Genesis Identity creation.  
It inherits constraints and authority from the identity.

### **2. Operation**
ADT acts only when triggered by:
- human instruction  
- domain workflows requiring user confirmation  
- delegated authorization  
- verified system prompts requiring consent  

### **3. Extension**
ADT may gain additional roles or permissions with explicit authorization.

### **4. Revocation**
The identity owner may revoke:
- permissions  
- roles  
- delegations  
- the ADT itself  

### **5. Termination**
ADT may be destroyed by the identity owner; its sealed history remains immutable.

---

## Outcomes of the ADT Layer

- users participate safely without exposing keys  
- transitions remain traceable to verified identity  
- semantic correctness is maintained  
- system rules cannot be bypassed  
- intent and authority become structurally enforceable  
- privacy is preserved through SVS boundaries  
- domains remain interoperable without leaking sensitive data  
- AI remains subordinate and guided  

ADT is the user’s **trusted operational interface**,  
ensuring that participation in the substrate is safe, authenticated, and correctly interpreted.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

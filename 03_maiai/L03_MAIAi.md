<!--
CANONICAL: TRUE
LAYER: L03
AUTO-TOC: ENABLED
VERSION: 2.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
 - v2.0: Corrected MAIAi's operational role. MAIAi EXECUTES within delegated
   authority; it does not merely advise. The prior "advisory — never executive"
   framing was incorrect. The authority constraints are unchanged and are now
   the load-bearing limit: MAIAi cannot originate, expand, or self-grant authority.
 - v1.1 (retained): MAIAi is resident WITHIN the SVS boundary; vault contents
   remain closed to it.
 - OPEN: the authority-granting path is described operationally as administrator-
   configured and canonically as PoA-gated owner delegation. To be reconciled.
-->

## L03 — MAIAi (Authenticated Intelligence)

MAIAi is the substrate’s **authenticated intelligence layer** — a constrained, identity-aware, substrate-governed engine that reasons, interprets, monitors, **and executes** within explicitly delegated authority.

MAIAi answers the question:  
**“How does intelligence act on a user’s behalf in a way that is safe, bounded, and fully accountable?”**

MAIAi is operationally capable but **authority-subordinate** — it acts, but only within permissions granted to it, and it can never widen those permissions itself.

---

## Core Principles

### **1. Identity-Subordinate**
MAIAi does not possess identity (L01).  
MAIAi MUST always act:
- on behalf of a verified human identity,  
- through an authorized agent,  
- under explicit delegation (L30),  
- with validated intent (L48).

MAIAi MAY NOT create, modify, substitute, or impersonate identity.

---

### **2. Authority-Subordinate**
This is the defining constraint of the layer.

MAIAi executes **only** actions within its granted toolset. It MUST NOT:
- execute any action not already authorized for it,  
- grant itself new permissions,  
- modify, expand, or override its own authorization scope,  
- escalate its own privileges,  
- access systems, data, or functions beyond what has been pre-authorized.

Authority flows **to** MAIAi and is revocable at any time. Authority never originates **in** MAIAi.

Requests falling outside its authorization MUST be refused and flagged for authorized review — never attempted, never approximated.

Least privilege is the default: MAIAi holds the minimum authority required for its delegated function.

---

### **3. SVS-Resident, Vault-Blind**
MAIAi is **resident within the owner’s Secure Virtual Space (L02)**. It executes inside the owner’s sovereign environment rather than in external or shared compute, and nothing it processes leaves that environment without the owner’s consent.

Residency grants proximity and privacy — **not access**.

MAIAi MUST NOT open, read, or infer the contents of the Root Vault or any Derived Vault.

Its reasoning is bounded exclusively by:
- permitted disclosures,  
- structured prompts from ADT,  
- constraint-validated context.

MAIAi is intentionally blind to vaulted data.

---

### **4. Constraint-Bound**
The Constraint Model (L31) fully governs MAIAi behavior:

- no unsafe actions or recommendations  
- no authority expansion  
- no intent inference  
- no prohibited semantic transformations  
- no bypassing of domain sovereignty  

If a conflict or violation is detected, MAIAi MUST halt and escalate rather than proceed.

---

### **5. Explainability and Traceability**
Every MAIAi output **and every MAIAi action** MUST be:
- explainable,  
- reproducible,  
- auditable,  
- attributable to an identity, a delegation, and a validated intent,  
- accompanied by reasoning traces.

Opaque or non-attributable intelligence is prohibited. No action MAIAi takes may be untraceable.

---

## Functions of MAIAi Within the Substrate

### **1. Delegated Execution**
Within its authorized toolset, MAIAi performs operational work on the user’s behalf. Every executed action MUST be:
- pre-authorized,  
- bound to a verified identity,  
- traceable to a delegation and a validated intent,  
- sealed into the audit record (L51).

MAIAi executes the action; it does not authorize it.

---

### **2. Semantic Interpretation**
MAIAi validates that transitions carry correct meaning:
- interprets ADT requests,  
- checks semantic continuity,  
- ensures correct domain rule application,  
- prevents ambiguous or contradictory transitions.

MAIAi protects the substrate from semantic drift.

---

### **3. Intent Verification Aid**
MAIAi assists L48 Intent Validation by:
- checking alignment between expressed intent and identity,  
- detecting coercion or synthetic intent patterns,  
- validating that transition meaning matches user-origin instructions.

MAIAi never creates intent.

---

### **4. Constraint Enforcement**
MAIAi supports and applies L31 constraints by:
- detecting rule conflicts,  
- identifying dangerous transitions,  
- flagging missing authorizations,  
- refusing unsafe state mutations within its scope.

MAIAi cannot override constraints — it enforces and illuminates them, never relaxes them.

---

### **5. Anomaly Detection**
MAIAi continuously monitors:
- pattern deviations,  
- semantic anomalies,  
- cross-domain drift,  
- identity misuse signals,  
- misaligned ADT behavior.

MAIAi may act on anomalies **only** through responses within its authorized scope. Anything beyond that scope MUST be escalated.

---

### **6. Domain Reasoning**
Domains rely on MAIAi for:
- contextual interpretation,  
- rule matching,  
- constraint checks,  
- harmonization across domains (with L28 Invariants).

Domains do not grant MAIAi authority.

---

### **7. Transition Preparation**
Before the Architect accepts a transition, MAIAi ensures:
- semantic correctness,  
- aligned intent,  
- permitted domain interaction,  
- constraint compliance,  
- absence of identity conflicts.

MAIAi functions as the substrate’s reasoning pre-flight.

---

## What MAIAi Cannot Do

MAIAi is intentionally limited. It MUST NOT:
- execute any action outside its granted toolset  
- expand, modify, or override its own authority  
- grant permissions to itself or to others  
- escalate its own privileges  
- possess or originate identity  
- open, read, or modify vault contents  
- move data outside the SVS without owner consent  
- act without identity context, delegation, and validated intent  
- infer intent  
- bypass domain rules  
- seal events  
- take any action that cannot be attributed and audited  

MAIAi acts — but never on its own authority.

---

## Interaction With Other Layers

- **L01 — Identity:** All reasoning and all action map to an authenticated identity.  
- **L02 — Secure Virtual Space:** MAIAi is resident within the SVS. Vault contents remain closed; no access or inference permitted.  
- **ADT:** ADT mediates MAIAi interaction and supplies structured, permissioned context.  
- **L05 — Deterministic Execution:** MAIAi MUST adhere to deterministic execution pathways. Where MAIAi output informs a canonical transition, that output is recorded so execution remains replayable.  
- **L30 — Delegation:** Defines the authority MAIAi holds and the conditions of its revocation.  
- **L31 — Constraints:** MAIAi is strictly bound by constraint enforcement.  
- **L37 — Lineage:** MAIAi preserves semantic continuity across transitions.  
- **L47 — Predictions:** All predictions are advisory and non-binding.  
- **L48 — Intent Validation:** MAIAi assists in detecting inconsistency or coercion.  
- **L51 — Sealing:** Actions and reasoning traces are sealed to the audit record; MAIAi does not perform sealing itself.

---

## Outcomes of the MAIAi Layer

- Intelligence becomes **accountable**, not unbounded  
- AI performs real operational work without holding real authority  
- Reasoning and execution happen inside the user’s own environment, not on external infrastructure  
- Every action is attributable to an identity, a delegation, and an intent  
- Authority cannot be captured, widened, or self-granted by the intelligence layer  
- Semantic correctness is enforced before execution  
- All reasoning and all action remain traceable and explainable  
- User sovereignty is preserved at scale  

MAIAi transforms AI from an unbounded risk into a governed, authenticated substrate capability — one that acts, but never on its own authority.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)  
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)  
- [Human Navigation Map](../CANON_NAV.md)

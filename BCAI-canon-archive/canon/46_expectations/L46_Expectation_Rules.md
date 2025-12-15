<!--
CANONICAL: TRUE
LAYER: L46
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L46 — Audit Model (Evidence, Inspection, Replayability & Accountability Framework)
Defines the canonical audit framework for the Sovereign Substrate.  
The Audit Model establishes **how all actors, transitions, state changes, and governance operations become permanently inspectable, reconstructable, and accountable**.

While L19 defines *auditability rules*,  
**L46 defines the complete model and system behavior enabling full-spectrum auditing.**

The Audit Model answers:  
**“How can every action, actor, and state change be inspected, proven, verified, and replayed at any time?”**

---

## 46.0 Purpose
L46 establishes:
- The canonical event evidence model  
- How audit data is captured, stored, indexed, and retrieved  
- How audits remain tamper-evident and replay-capable  
- How transitions and states expose audit trails  
- How identity, provenance, governance, and constraints become auditable  
- How auditors reconstruct substrate behavior with perfect fidelity  

Auditing is the substrate’s **truth enforcement layer**.

---

## 46.1 Scope
Applies to:
- All transitions (L33–L45)  
- All actors (human, ADT, MAIAi, system)  
- All identity operations (L43)  
- All authentication/authorization flows (L41–L42)  
- All governance actions (L29)  
- All provenance events (L18)  
- All constraint violations (L31)  
- All enforcement actions (L40)  
- All recovery and rollback events (L16, L38)  
- All federated domain interactions  

Audit data is required at:
- Proposal  
- Validation  
- Verification  
- Commit  
- Finality  
- Replay  
- Recovery  
- Governance adjudication  

---

## 46.2 Core Principles
1. **Everything must be auditable.**  
2. **Audit data must be tamper-evident.**  
3. **Audit logs must be independently reconstructable.**  
4. **Auditors must be able to replay any historical sequence.**  
5. **Audit evidence must be cryptographically provable.**  
6. **Audit obligations cannot be disabled, bypassed, or downgraded.**  
7. **Auditability is sovereign — governance determines visibility.**  

---

## 46.3 Audit Object Model
Each canonical event must produce an Audit Object with:

### Required Fields
- Event ID  
- Actor identity + authentication evidence  
- Authorization context  
- Causal anchors (L37)  
- Temporal markers (L14)  
- Transition Structure (L33)  
- State delta references (L32)  
- Provenance linkage (L18)  
- Constraint envelope state (L31)  
- Verification evidence (L28)  
- Validation evidence (L27, L39)  
- Governance policy version  
- Enforcement actions (if any)  
- Cryptographic fingerprint  

### Optional Fields
- Agent reasoning traces (L26)  
- Delegation chains (L30)  
- Risk scoring metadata  
- Domain metadata for federated audits  

Missing required fields → **NONCANONICAL AUDIT OBJECT**.

---

## 46.4 Audit Evidence Requirements

### 46.4.1 Integrity of Evidence
Evidence must be:
- Complete  
- Correct  
- Cryptographically sealed  
- Bound to identity  
- Bound to provenance  
- Immutable  

---

### 46.4.2 Replayability
Audit logs must permit:
- Full event replay  
- Partial replay  
- Causal replay  
- Counterfactual “re-run” analysis  
- Forensic investigation  

Replay must always yield deterministic results (L12).

---

### 46.4.3 Inspectability
Auditors must be able to:
- Trace all transitions from origin to finality  
- Inspect all deltas  
- Inspect all validation + verification  
- Inspect all governance decisions  
- Inspect all enforcement actions  
- Inspect all identity state changes  

---

### 46.4.4 Accountability
Audit must link:
- Actor → Capability → Action → Result  
- Delegator → Delegatee → Performed Action  
- Governance → Policy → Enforcement  
- Agent → Reasoning Trace → Outcome  

---

## 46.5 Audit Log Structure

### 46.5.1 Append-Only Log
Audit logs must be:
- Append-only  
- Versioned  
- Cryptographically hash-linked  
- Resistant to reordering  

### 46.5.2 Multi-Layer Indexing
Logs must support:
- Identity indexing  
- Transition indexing  
- Provenance indexing  
- Governance indexing  
- Time-based indexing  
- Constraint-based indexing  

### 46.5.3 Partitioned Domains
Federated audits require:
- Domain isolation  
- Cross-domain anchors  
- Jurisdiction metadata  

---

## 46.6 Auditor Roles & Capabilities

### 46.6.1 Auditor Identity
Auditors must:
- Have a verified identity  
- Have auditing capability (L23)  
- Have required governance authorization (L29)  

### 46.6.2 Auditor Powers
Auditors may:
- Inspect any event within their authority  
- Request full evidence bundles  
- Reconstruct state from scratch  
- Trigger governance escalation  

### 46.6.3 Auditor Limitations
Auditors may:
- Not modify logs  
- Not alter provenance  
- Not change or inject transitions  

Audit is read-only by design.

---

## 46.7 Audit Pipeline

### 46.7.1 Capture
Audit data captured automatically during:
- Validation  
- Verification  
- Transition execution  
- Governance decisions  
- Enforcement actions  

### 46.7.2 Sealing
Audit objects must be:
- Compressed if necessary  
- Hash-linked  
- Signed  
- Stored redundantly  

### 46.7.3 Export
Audits must be exportable for:
- Compliance  
- External investigation  
- Cross-domain verification  
- Historical archiving  

### 46.7.4 Replay
Audit pipeline must support full restoration of:
- State  
- Identity  
- Provenance  
- Governance decisions  

---

## 46.8 Audit During Exceptions
Exceptions include:
- Constraint violations  
- Unauthorized access attempts  
- Failed validation/verification  
- Governance override  
- Recovery events  
- Federated conflict detection  

Audit must record:
- Full context  
- Violation type  
- Enforcement response  
- Identity chain  

---

## 46.9 Observability Requirements
Audit framework must expose:
- Event timelines  
- Causal graphs  
- Transition integrity maps  
- Provenance trails  
- Governance decision logs  
- Constraint violation logs  
- Recovery intervention logs  
- Agent reasoning trace calls  

Auditors must always see **why** the system behaved the way it did.

---

## 46.10 Layer Interactions
- **L11** — cryptographic primitives secure audit evidence.  
- **L12** — deterministic replay essential for audit correctness.  
- **L13** — mutability limits govern how audit logs evolve.  
- **L14** — timestamps drive ordering.  
- **L15/L37** — causality model required for audit graphs.  
- **L16/L38** — recovery logs audit transition corrections.  
- **L18** — provenance enriches audit context.  
- **L19** — auditability rules define baseline requirements.  
- **L20** — attestations strengthen event truth.  
- **L21** — custody events must be auditable.  
- **L22–L24** — permissions, capabilities, accountabilities enforced in audit.  
- **L25** — context propagation must be logged.  
- **L26** — agent reasoning is auditable.  
- **L27–L28** — validation/verification evidence recorded.  
- **L29** — governance overlays audited.  
- **L31** — constraint envelope affects audit interpretation.  
- **L32–L33** — state + transition structures auditable.  
- **L34–L36** — consensus, finality, and fork-prevention logs required.  
- **L39** — validation model persistence included in audits.  
- **L40** — enforcement actions logged fully.  
- **L41–L43** — authentication, authorization, identity events auditable.  
- **L44–L45** — transitions must expose integrity evidence.  

---

## 46.11 Invariants
1. **AUDIT_COMPLETE** — every event must generate an audit record.  
2. **AUDIT_IMMUTABLE** — audit records cannot change once sealed.  
3. **AUDIT_TRACEABLE** — auditors must reconstruct full lineage.  
4. **AUDIT_REPLAYABLE** — history must replay deterministically.  
5. **AUDIT_PROVABLE** — all evidence must be cryptographically valid.  
6. **AUDIT_ACCOUNTABLE** — every action tied to identity and purpose.  
7. **AUDIT_GOVERNED** — governance defines auditor access and scope.  

Violating any invariant → **SYSTEM SAFETY DEGRADATION → GOVERNANCE ESCALATION**.

---

## 46.12 Informative Guidance
Audit is the substrate’s backbone of trust.  
A strong audit model eliminates ambiguity, prevents corruption, and ensures long-term safety.  
Governance and compliance bodies should periodically review audit structures to detect drift.  
Agents should generate self-describing transitions to improve audit clarity.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

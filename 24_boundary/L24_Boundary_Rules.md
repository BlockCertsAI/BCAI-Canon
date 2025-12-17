<!--
CANONICAL: TRUE
LAYER: L24
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L24 — Accountabilities Model (Who Is Responsible for What & When)
Defines how responsibility, liability, obligation, and answerability are assigned, tracked, and enforced across all actors and components within the Sovereign Substrate. Accountability ensures that every action, event, and outcome has a clear, provable owner.

## 24.0 Purpose
L24 establishes the canonical rules governing:
- Who is responsible for each action, decision, or state change  
- When responsibility becomes active, suspended, or transferred  
- How accountability persists through automation, delegation, or AI/ADT operation  
- How responsibility is proven, audited, escalated, or revoked  
- How blame, liability, and compliance responsibility are assigned  

Accountability is foundational to trust: every effect must have a responsible actor.

## 24.1 Scope
Accountability applies to:
- Human actors  
- ADT and MAIAi systems  
- Organizational and system identities  
- Governance authorities (CSR, Architect)  
- Cross-substrate and federated actors  
- All canonical events, states, and provenance objects  
- All permissions, capabilities, and handoff flows  

Every action in the substrate must be tied to an accountable identity.

## 24.2 Core Principles
1. **No action without accountable ownership** — nothing may occur without someone being responsible for it.  
2. **Accountability survives delegation** — delegating tasks does not eliminate responsibility.  
3. **Accountability is explicit** — never inferred or assumed.  
4. **Accountability is temporal** — responsibility has a defined start and end.  
5. **Accountability is traceable** — provenance and audit chains must reflect who was responsible and when.  
6. **Accountability is layered** — actions may have multiple accountable parties.  
7. **Automated actors remain accountable** — ADT/MAIAi cannot operate without a responsible human or governance identity.  

## 24.3 Accountability Object Model
Each accountability record must define:

### Actor Binding
- Identity (Genesis-KYC verified)  
- Actor type (human, ADT, MAIAi, system, governance)  
- Role and organizational association  

### Responsibility Definition
- What the actor is accountable for  
- Scope of responsibility  
- Expected duties or obligations  
- Jurisdiction or domain  

### Temporal Boundaries
- Activation timestamp  
- Deactivation or transfer timestamp  
- Conditional triggers (start/stop rules)  

### Cryptographic Anchoring
- Accountability hash  
- Signatures of responsible parties  
- Multi-party signatures for Critical responsibilities  
- Revocation reference  

### Causal & Provenance Anchoring
- Parent responsibility (if inherited or delegated)  
- Link to actions, permissions, and capabilities (L22–L23)  
- Integration with provenance (L18) and audit (L19)  

## 24.4 Categories of Accountability
- **Direct Accountability** — direct execution or causation  
- **Supervisory Accountability** — oversight and enforcement  
- **Delegated Accountability** — delegated but retained responsibility  
- **Derived Accountability** — role- or context-derived responsibility  
- **Autonomous-Agent Accountability** — ADT/MAIAi actions mapped to humans or governance  
- **Collective Accountability** — shared responsibility with defined escalation  

## 24.5 Accountability Assignment Rules
Accountability may be assigned only when:
1. Identity authenticity is verified  
2. Authority to hold responsibility exists  
3. Required capability is present (L23)  
4. Required permission exists (L22)  
5. Temporal validity holds (L14)  
6. Causal ordering is correct (L15)  
7. Provenance is linked (L18)  
8. Audit visibility is guaranteed (L19)  

Invalid assignments must be rejected.

## 24.6 Accountability Use Rules
Before any action executes, the substrate must verify:
- Active accountability exists  
- Scope matches the action  
- Accountability has not expired or transferred  
- No conflicting responsibility exists  
- AI/ADT actions map to a responsible identity  

Failure blocks execution.

## 24.7 Accountability Transfer & Handoff
Transfers follow L21 and must:
- Reference prior accountability  
- Define full or partial transfer  
- Require acceptance  
- Update provenance  
- Re-evaluate permissions and capabilities  

## 24.8 Accountability Escalation
Escalation assigns higher-level responsibility when risk, conflict, automation limits, or governance intervention is required. Escalations must be explicit, time-bound, justified, and auditable.

## 24.9 Accountability Revocation
Revocation may occur due to compromise, policy change, governance action, or misassignment. Revocation must be immediate, justified, signed, and cascaded.

## 24.10 Observability & Reporting
The substrate must expose:
- Accountability maps  
- Temporal responsibility timelines  
- Handoff and escalation histories  
- ADT/MAIAi responsibility boundaries  

Auditors must reconstruct full responsibility chains.

## 24.11 Interaction With Other Layers
- **L11** cryptographic verification  
- **L12** deterministic replay  
- **L13** lawful mutation  
- **L14** temporal anchoring  
- **L15** causal correctness  
- **L16–L17** undo and recovery  
- **L18** provenance binding  
- **L19** auditability  
- **L20** responsibility attestations  
- **L21** responsibility handoff  
- **L22** permission alignment  
- **L23** capability alignment  

## 24.12 Invariants
1. ACCOUNTABILITY_REQUIRED  
2. ACCOUNTABILITY_TRACEABLE  
3. ACCOUNTABILITY_EXPLICIT  
4. ACCOUNTABILITY_TEMPORAL  
5. ACCOUNTABILITY_REVOCABLE  
6. ACCOUNTABILITY_NONREPUDIABLE  
7. ACCOUNTABILITY_SUPERVISORY  

## 24.13 Real-World Capability Enabled by the Accountability Model

The Accountability Model enables **legally and operationally enforceable responsibility in automated systems**.

It allows:
- Regulators to trace liability through AI, automation, and delegation without ambiguity.
- Enterprises to deploy autonomous systems while retaining provable human or governance accountability.
- Governments to enforce compliance without relying on self-reporting or post-incident reconstruction.
- Courts and auditors to reconstruct responsibility chains with cryptographic certainty.
- Complex federated systems to assign responsibility across jurisdictions without trust assumptions.

Accountability becomes **a property of the system**, not a promise made after failure.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

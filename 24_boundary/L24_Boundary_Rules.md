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
6. **Accountability is layered** — actions may have multiple accountable parties (originator, executor, overseer).  
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

### 24.4.1 Direct Accountability
The actor directly causes or performs an action.
Examples: executing a transaction, signing an attestation.

### 24.4.2 Supervisory Accountability
An actor oversees or governs the execution of a process.
Examples: compliance, oversight, quality assurance.

### 24.4.3 Delegated Accountability
Responsibility that is handed off but not surrendered.
The delegator remains accountable even after delegation (L21).

### 24.4.4 Derived Accountability
Responsibility derived from role or context, not explicitly granted.

### 24.4.5 Autonomous-Agent Accountability
Responsibilities tied to ADT/MAIAi actions.
There must always be:
- A responsible human or governance identity  
- A chain of justification for autonomous decisions  

### 24.4.6 Collective Accountability
Shared responsibilities among:
- Teams  
- Departments  
- Multi-party governance processes  

Collective accountability must define:
- Shared vs. individual obligations  
- Escalation paths  
- Conflict resolution processes  

## 24.5 Accountability Assignment Rules
Accountability may be assigned only when the system verifies:

1. **Identity authenticity**  
2. **Authority to hold responsibility**  
3. **Capability to perform tasks (L23)**  
4. **Permission to execute related actions (L22)**  
5. **Temporal validity** (L14)  
6. **Causal consistency** — responsibility must precede actions (L15)  
7. **Provenance chain linkage** (L18)  
8. **Auditor visibility** (L19)  

Assignments lacking validated justification must be rejected.

## 24.6 Accountability Use Rules
Before any action executes, the substrate must verify:

1. **The actor has active accountability for the action or domain**  
2. **Accountability has not expired or transferred**  
3. **No conflicting accountability claims exist**  
4. **The actor’s accountability scope covers the required effect**  
5. **Audit trails will record the action under the correct identity**  
6. **AI/ADT actions map to a responsible human or governance identity**  

If any check fails, the action must not proceed.

## 24.7 Accountability Transfer & Handoff
Transfers follow L21 rules but must also:

- Reference the prior accountable actor  
- Define whether accountability is fully transferred or partially retained  
- Update provenance (L18)  
- Require explicit acceptance by the new accountable party  
- Trigger reevaluation of permissions (L22) and capabilities (L23)  

Partial transfers must specify:
- What remains with the original actor  
- What moves with the transferee  
- When full responsibility may resume or escalate  

## 24.8 Accountability Escalation
Escalation occurs when:
- Risk increases  
- Conflict or exceptions arise  
- AI/ADT actions trigger supervisory review  
- Human oversight is required  
- A governance entity must intervene  

Escalation must:
- Generate an accountability event  
- Assign higher-level responsible parties  
- Provide justification and temporal scope  
- Map clearly in auditability chains  

## 24.9 Accountability Revocation
Accountability may be revoked if:
- Actor becomes untrusted or compromised  
- Actor loses required capability or permission  
- Governance mandates removal  
- Responsibility was incorrectly assigned  
- Misconduct, negligence, or system violation occurs  

Revocation must:
- Reference the original accountability assignment  
- Provide justification  
- Immediately deactivate responsibility  
- Update provenance and audit chains  
- Cascade adjustments into dependent responsibilities  

## 24.10 Observability & Reporting
The substrate must expose:
- Accountability maps (who is responsible for what)  
- Handoff and escalation histories  
- ADT/MAIAi responsibility bounds  
- Time-indexed accountability timelines  
- Conflict or overlap detection tools  

Auditors must reconstruct:
- Who was responsible  
- When responsibility was active  
- What actions occurred under that responsibility  
- Whether duties were fulfilled or violated  

## 24.11 Interaction With Other Layers
- L11 provides cryptographic identity & signature verification.  
- L12 ensures deterministic replay of responsibility sequences.  
- L13 ensures accountable actors can legally modify objects.  
- L14 anchors accountability in time.  
- L15 ensures causal correctness of responsibility flows.  
- L16 ensures accountability persists through undo.  
- L17 ensures accountability is maintained or restored after recovery.  
- L18 binds accountability to provenance.  
- L19 ensures accountability remains auditable.  
- L20 attaches attestations of responsibility.  
- L21 governs responsibility transfer.  
- L22 governs who is permitted to perform accountable actions.  
- L23 governs whether the actor is capable of performing them.

## 24.12 Invariants
1. ACCOUNTABILITY_REQUIRED — no action may occur without an accountable actor.  
2. ACCOUNTABILITY_TRACEABLE — all responsibility must appear in provenance and audit chains.  
3. ACCOUNTABILITY_EXPLICIT — responsibility must be declared, not inferred.  
4. ACCOUNTABILITY_TEMPORAL — responsibility must have a defined active window.  
5. ACCOUNTABILITY_REVOCABLE — responsibilities can be revoked at any time.  
6. ACCOUNTABILITY_NONREPUDIABLE — responsible actors cannot deny involvement.  
7. ACCOUNTABILITY_SUPERVISORY — AI/ADT actions must always map to a human or governance identity.  

## 24.13 Informative Guidance
Accountability should be granular, explicit, and tailored to risk. Supervisory lines must be clear for all automated systems. Transfers and escalations should be minimal, well-documented, and auditable. Accountability drift should be regularly audited to ensure alignment with current permissions and capabilities.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

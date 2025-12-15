<!--
CANONICAL: TRUE
LAYER: L22
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L22 — Permissions (Who May Do What, Under Which Conditions)
Defines how Canon determines which identities, agents, and systems may perform which actions, under what constraints, and with what required proofs. Permissions ensure authenticated, rule-bound operation across the Sovereign Substrate.

## 22.0 Purpose
L22 establishes the canonical permission model governing:
- Which actions any actor may perform  
- Under what conditions those actions are allowed  
- Which proofs are required for authorization  
- When permissions may escalate, delegate, or be revoked  

Permissions unify identity, role, authority, context, and policy into a deterministic, verifiable access-control framework.

## 22.1 Scope
Permissions apply to:
- Human actors  
- ADT and MAIAi agents  
- System processes  
- Architect-level mechanisms  
- CSR/governance authorities  
- Cross-substrate and federated interactions  
- All canonical actions including reads, writes, updates, delegation, execution, control, and handoff  

L22 defines substrate-level permission mechanics; domain policies may extend but never weaken them.

## 22.2 Core Principles
1. **No action without permission** — authorization is mandatory.  
2. **Permissions must be authenticated** — all decisions rely on verified identity.  
3. **Permissions must be explicit** — never assumed or inherited implicitly.  
4. **Least authority** — actors receive only the minimum permissions required.  
5. **Context-bound** — permissions depend on time, location, domain, and object state.  
6. **Causally valid** — permissions must be checked at the moment of action, respecting L15.  
7. **Non-repudiable** — permission grants and uses must be auditable.  
8. **Revocable** — permissions may be suspended, reduced, or removed at any time under canonical rules.

## 22.3 Permission Object Model
Permission definitions must include:

### Actor Definition
- Identity (Genesis-KYC bound)  
- Type (human, ADT, MAIAi, system)  
- Role(s)  
- Trust domain or jurisdiction  

### Action Definition
- The exact operation allowed (read, write, modify, delete, control, execute, approve, delegate)  
- Object or domain where the action applies  
- Scope limits  

### Conditions of Use
- Temporal constraints (L14)  
- Causal preconditions (L15)  
- Policy or compliance requirements  
- Required attestations (L20)  
- Required custody or control (L21)  

### Cryptographic Bindings
- Permission hash  
- Grant signatures  
- Optional multi-signature approvals  
- Revocation key references  

### Lifecycle Metadata
- Creation timestamp  
- Expiration or renewal conditions  
- Revocation or suspension rules  

## 22.4 Types of Permissions

### 22.4.1 Static Permissions
Assigned at identity creation or organizational onboarding.  
Examples: baseline read or inspection rights, non-critical queries.

### 22.4.2 Dynamic Permissions
Condition-dependent permissions that may be granted:
- Temporarily  
- On-demand  
- Based on context or risk level  

Dynamic permissions must include activation and expiration events.

### 22.4.3 Delegated Permissions
Permissions granted to another actor by one holding authority.  
Delegations must:
- Reference the original permission  
- Specify scope and expiration  
- Be traceable in provenance (L18)  

### 22.4.4 Derived Permissions
Permissions inferred from role or domain-specific rules, but still explicit.  
Derived permissions must not bypass identity or attestation requirements.

### 22.4.5 Emergency Permissions
Temporary elevated permissions issued under exceptional conditions.  
Emergency permissions must:
- Be time-limited  
- Be logged  
- Require post-event audit (L19)  

### 22.4.6 AI/ADT Operational Permissions
Define:
- What an ADT or MAIAi may autonomously execute  
- What human approvals are required  
- Safe boundaries for automated action  
These must be strict, traceable, and auditable.

## 22.5 Permission Granting Rules
A permission may be granted only if:

1. **Identity is authenticated** under Genesis-KYC.  
2. **Authority to grant** is verified through attestations (L20).  
3. **Scope is valid** for the granting actor.  
4. **Action is legal** under mutability rules (L13).  
5. **Temporal window is valid** (L14).  
6. **Causal conditions are satisfied** (L15).  
7. **Provenance chain is correct** (L18).  
8. **Auditable records are generated** (L19).  

Handoff rules (L21) apply when permission is transferred rather than granted.

## 22.6 Permission Use Rules
Before executing an action, the substrate must verify:

1. **Actor identity**  
2. **Permission validity** (active, unexpired, not revoked)  
3. **Scope compliance** (domain, object, level)  
4. **Proof requirements** (attestations, custody, context) are met  
5. **Temporal and causal alignment** with the action  
6. **Absence of conflicts** (no mutually exclusive permissions)  
7. **No superseding revocation**  

If validation fails, the action must be rejected.

## 22.7 Permission Escalation
Escalation occurs when:
- Additional authority is needed  
- Context changes (risk, urgency, jurisdiction)  
- A higher-level actor approves elevation  

Escalation must:
- Be explicit  
- Be recorded as a canonical event  
- Have defined expiration  
- Require proper attestations (L20)  
- Trigger heightened auditing (L19)

## 22.8 Permission Revocation
Permissions may be revoked if:
- Keys or identities are compromised  
- Actor becomes untrusted or suspended  
- Policy or legal requirements change  
- Misuse or anomaly is detected  
- Governance orders revocation  

Revocation must:
- Reference the original permission  
- Include authority justification  
- Immediately deactivate the permission  
- Trigger provenance updates  
- Remain visible permanently  

## 22.9 Observability & Reporting
The system must support:
- Permission maps (who may do what)  
- Delegation graphs  
- Escalation histories  
- Revocation timelines  
- AI/ADT permission boundaries  
- Contextual permission queries  

Auditors must reconstruct:
- Why permission existed  
- When it was used  
- Under what context  
- Whether usage complied with canonical rules  

## 22.10 Interaction With Other Layers
- L11 supplies cryptographic verification.  
- L12 ensures deterministic replay of permission logic.  
- L13 governs permissible mutations.  
- L14 defines time windows.  
- L15 enforces causal validity.  
- L16 ensures permissions survive or adjust under undo logic.  
- L17 ensures permissions remain valid after recovery.  
- L18 binds permissions to provenance.  
- L19 ensures permissions remain auditable.  
- L20 supplies the attestations required for authorization.  
- L21 governs handoff of permissions between actors.

## 22.11 Invariants
1. PERMISSION_EXPLICIT — no implicit permissions.  
2. PERMISSION_AUTHENTIC — identity and authority must be cryptographically proven.  
3. PERMISSION_TRACEABLE — all permissions appear in provenance and audit chains.  
4. PERMISSION_SCOPE_BOUND — cannot exceed its defined limits.  
5. PERMISSION_REVOCABLE — any permission may be revoked.  
6. PERMISSION_NONREPUDIABLE — usage and grant must be undeniable.  
7. PERMISSION_CONTEXTUAL — permissions must match actor, environment, and object state.

## 22.12 Informative Guidance
Permissions should be defined narrowly and escalated only when required. Delegation should be explicit, short-lived, and traceable. AI/ADT permissions should be strict and enforceable. Periodic audits should reconcile permissions with actual usage and detect drift.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

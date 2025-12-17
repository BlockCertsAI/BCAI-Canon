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

### 22.4.2 Dynamic Permissions
Condition-dependent, time-bound permissions granted on demand.

### 22.4.3 Delegated Permissions
Permissions granted by an authorized actor to another, with explicit scope and expiration.

### 22.4.4 Derived Permissions
Explicit permissions inferred from role or domain rules without bypassing proof requirements.

### 22.4.5 Emergency Permissions
Temporary elevated permissions issued under exceptional conditions, always time-limited and audited.

### 22.4.6 AI/ADT Operational Permissions
Strictly defined autonomous action boundaries for ADT and MAIAi agents.

## 22.5 Permission Granting Rules
A permission may be granted only if identity, authority, scope, mutability, temporal validity, causality, provenance, and audit requirements are all satisfied.

## 22.6 Permission Use Rules
Before execution, the substrate must validate identity, permission state, scope, required proofs, temporal and causal alignment, and absence of conflicts or revocations.

## 22.7 Permission Escalation
Escalation must be explicit, attested, time-limited, recorded as a canonical event, and subject to heightened audit.

## 22.8 Permission Revocation
Revocation must reference the original permission, include authority justification, deactivate immediately, update provenance, and remain permanently visible.

## 22.9 Observability & Reporting
The system must expose permission maps, delegation graphs, escalation histories, revocation timelines, AI/ADT boundaries, and contextual queries.

## 22.10 Interaction With Other Layers
- **L11** cryptographic verification  
- **L12** deterministic replay  
- **L13** mutation legality  
- **L14** temporal validation  
- **L15** causal validity  
- **L16–L17** undo and recovery  
- **L18** provenance binding  
- **L19** auditability  
- **L20** authorization attestations  
- **L21** permission handoffs  

## 22.11 Invariants
1. PERMISSION_EXPLICIT  
2. PERMISSION_AUTHENTIC  
3. PERMISSION_TRACEABLE  
4. PERMISSION_SCOPE_BOUND  
5. PERMISSION_REVOCABLE  
6. PERMISSION_NONREPUDIABLE  
7. PERMISSION_CONTEXTUAL  

## 22.12 Real-World Capability Enabled by Permissions

Permissions enable **fine-grained, auditable access control without centralized administrators**.

They allow:
- Governments to enforce role-based authority with cryptographic proof instead of trust in institutions.
- Enterprises to replace IAM systems with deterministic, cross-domain permission enforcement.
- Healthcare and finance systems to grant time-bound, case-specific access without overexposure.
- Supply chains to restrict who may modify records at each custody stage.
- AI systems to act autonomously within provable, revocable boundaries defined by humans.

Permissions transform access control from policy enforcement into **verifiable protocol truth**.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

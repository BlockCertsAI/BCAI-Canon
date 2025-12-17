<!--
CANONICAL: TRUE
LAYER: L23
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L23 — Capability Model (What an Actor Can Do in the Substrate)
Defines the fundamental capability system that determines what actions an actor *is able* to perform within the Sovereign Substrate, independent of permissions. Capabilities represent the inherent, structural, or role-derived potential of an identity or agent.

## 23.0 Purpose
L23 establishes the canonical rules governing:
- What actors *can* do from a structural, architectural, or functional standpoint  
- How capabilities differ from permissions  
- How capabilities constrain or enable system behavior  
- How capabilities are declared, inherited, composed, or withdrawn  
- How capabilities interact with identity, roles, ADT/MAIAi autonomy, and system boundaries  

Capabilities define the *possibility space* of actions.  
Permissions define which actions are *allowed* at a given moment.

## 23.1 Scope
Capabilities apply to:
- Human actors  
- ADT (Agentic Digital Twins)  
- MAIAi intelligent agents  
- System identities  
- Verified domains and substrate partitions  
- Federated or cross-jurisdictional actors  

Capabilities govern:
- What operations an actor can *technically* perform  
- What resources an actor can interface with  
- What processes an actor can initiate or influence  
- What instruments, proofs, or controls the actor can generate  

## 23.2 Core Principles
1. **Capabilities precede permissions** — an actor cannot be permitted to do something they lack capability for.  
2. **Capabilities reflect architecture, not policy** — they describe functional potential, not authorization.  
3. **Capabilities are deterministic** — if two actors share identical structure, their capabilities match.  
4. **Capabilities are discoverable** — the system must be able to enumerate an actor’s capabilities.  
5. **Capabilities are composable** — larger capabilities may be constructed from smaller primitives.  
6. **Capabilities must be provenance-bound** — they must attach to identity, lineage, and role.  
7. **Capabilities must be revocable or suppressible** when identity, trust, or context changes.  

## 23.3 Capability Object Model
Each capability must define:

### Identity Binding
- Actor identity (Genesis-KYC verified)  
- Actor type (human, ADT, MAIAi, system)  
- Domain or jurisdiction  

### Capability Definition
- Functional description of what the actor *can* do  
- Capability class (structural, computational, operational, governance, AI-autonomy)  
- Capability scope (local, domain, substrate-wide)  

### Preconditions
- Required context (environment, custody, control)  
- Required instruments (keys, proofs, attestations)  
- Required causal or temporal conditions  

### Constraints
- Safety boundaries  
- Trust boundaries  
- Role-based limitations  
- Interaction or concurrency limits  

### Cryptographic Attributes
- Capability hash  
- Issuance signature  
- Optional multi-party cosignatures  
- Revocation reference  

## 23.4 Categories of Capabilities

### 23.4.1 Structural Capabilities
Inherent abilities based on system design.

### 23.4.2 Operational Capabilities
Abilities tied to tasks or workloads.

### 23.4.3 Governance Capabilities
Abilities to influence system state or policy.

### 23.4.4 Supervisory Capabilities
Abilities to monitor, evaluate, or enforce.

### 23.4.5 AI/ADT Autonomy Capabilities
Abilities unique to agentic systems.

### 23.4.6 Cross-Substrate Capabilities
Abilities to operate across trust boundaries.

## 23.5 Capability Assignment
Capabilities may be assigned through identity initialization, role assignment, system architecture, provenance-based derivation, delegation, or capability packages. Delegation MUST NOT exceed the delegator’s own capabilities.

## 23.6 Capability Validation Rules
Before a capability becomes active, the system must verify identity authenticity, integrity, scope compatibility, satisfied preconditions, enforceable constraints, absence of conflicts, revocation status, and compliance with mutability and governance rules.

## 23.7 Capability Use Rules
The substrate must confirm capability presence, contextual validity, constraint adherence, target compatibility, safety boundaries, and lack of conflict. Permissions (L22) remain mandatory.

## 23.8 Capability Revocation
Capabilities may be revoked due to trust changes, compromise, invalidated provenance, safety risks, domain shifts, or governance mandate. Revocation MUST be immediate, justified, signed, and auditable.

## 23.9 Observability & Reporting
The substrate must expose capability inventories, lineage, delegation graphs, conflict maps, activation logs, and AI/ADT boundaries.

## 23.10 Interaction With Other Layers
- **L11** cryptographic binding  
- **L12** deterministic activation  
- **L13** mutability limits  
- **L14** temporal legality  
- **L15** causal correctness  
- **L16–L17** undo and recovery  
- **L18** provenance binding  
- **L19** auditability  
- **L20** attestation support  
- **L21** capability handoff  
- **L22** permission ceiling  

## 23.11 Invariants
1. CAPABILITY_STRUCTURAL  
2. CAPABILITY_BOUND  
3. CAPABILITY_TRACEABLE  
4. CAPABILITY_REVOCABLE  
5. CAPABILITY_COMPOSABLE  
6. CAPABILITY_SAFE  
7. CAPABILITY_REQUIRED  

## 23.12 Real-World Capability Enabled by the Capability Model

The Capability Model enables **system-level safety and correctness before policy is applied**.

It allows:
- Governments to separate *what systems can do* from *what they are allowed to do*, preventing accidental overreach.
- Enterprises to design secure-by-architecture platforms where dangerous actions are structurally impossible.
- AI systems to be constrained at the capability layer, eliminating reliance on post-hoc permission checks alone.
- Critical infrastructure to prevent classes of failure by removing capabilities entirely, not just denying access.
- Federated systems to interoperate safely by exposing and verifying capability surfaces before engagement.

Capabilities transform security from access control into **architectural truth**.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

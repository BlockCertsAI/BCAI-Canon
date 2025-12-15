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
Inherent abilities based on system design:
- Read/write interfaces  
- Execution ability  
- Access to communication channels  
- Ability to generate proofs or hashes  

### 23.4.2 Operational Capabilities
Abilities tied to tasks or workloads:
- Execute workflows  
- Initiate transactions  
- Perform computations or transforms  
- Manage custody transitions  

### 23.4.3 Governance Capabilities
Abilities to influence system state or policy:
- Issue directives  
- Approve exceptions  
- Validate or certify objects  
- Initiate escalations or overrides  

### 23.4.4 Supervisory Capabilities
Abilities to monitor, evaluate, or enforce:
- Audit processes  
- Enforce compliance  
- Evaluate ADT/MAIAi behavior  
- Trigger remediation  

### 23.4.5 AI/ADT Autonomy Capabilities
Abilities unique to agentic systems:
- Autonomous decision execution  
- Predictive reasoning or planning  
- Continuous monitoring  
- Self-correction or self-escalation  
- Generation of attestations, proofs, or corrective actions  

### 23.4.6 Cross-Substrate Capabilities
Abilities to operate across trust boundaries:
- Federation interactions  
- Cross-domain validation  
- Inter-substrate routing  

## 23.5 Capability Assignment
Capabilities may be assigned through:

### Identity Initialization
Actors are issued baseline capabilities at creation (human, ADT, MAIAi, or system identity).

### Role Assignment
Roles provide additional capabilities that reflect functional duties.

### System Architecture
Some capabilities are inherent to actor type (e.g., MAIAi’s ability to run continuous evaluations).

### Provenance-Based Derivation
Actors may gain capabilities by demonstrating lineage, credentials, or training.

### Delegation
Capabilities may be delegated temporarily or conditionally, but must never exceed the delegator’s own capabilities.

### Capability Packages
Capabilities may be grouped into bundles for efficiency but must remain individually traceable.

## 23.6 Capability Validation Rules
Before a capability becomes active, the system must verify:

1. **Identity authenticity**  
2. **Capability integrity** (hash, signatures)  
3. **Scope compatibility** with identity and domain  
4. **Preconditions are satisfied**  
5. **Constraints are enforceable**  
6. **No conflicting or unsafe combinations**  
7. **Capability is not revoked or expired**  
8. **Capability does not violate mutability or governance rules (L13)**  

Capabilities failing validation must not activate.

## 23.7 Capability Use Rules
When an actor attempts an action, the substrate must check:

1. Does the actor possess the required capability?  
2. Are its preconditions satisfied in the current context?  
3. Are its constraints upheld?  
4. Does the capability allow initiation of this action type?  
5. Does the capability allow interaction with the target object or domain?  
6. Are safety, governance, and trust boundaries respected?  
7. Does the capability conflict with other active capabilities?  

Even if capability is present, **permissions (L22)** must still allow the action.

## 23.8 Capability Revocation
Capabilities may be revoked if:
- Identity trust level changes  
- Actor becomes compromised  
- Provenance or lineage is invalidated  
- A capability becomes unsafe  
- Domain boundaries shift  
- Governance mandates termination  

Revocation must:
- Reference the original capability  
- Provide justification  
- Be signed by a valid authority  
- Immediately deactivate the capability  
- Update provenance and audit chains  

## 23.9 Observability & Reporting
The substrate must expose:
- Capability inventories for each actor  
- Capability lineage and provenance  
- Delegation graphs  
- Capability conflict maps  
- AI/ADT capability boundaries  
- Capability activation and deactivation logs  

Auditors must reconstruct:
- How capabilities were issued  
- Why the actor possesses them  
- Whether they are currently active  
- Whether they were used safely and lawfully  

## 23.10 Interaction With Other Layers
- **L11** — ensures cryptographic binding of capabilities.  
- **L12** — ensures deterministic activation and validation.  
- **L13** — governs allowable capability effects on mutability.  
- **L14** — ensures capabilities obey temporal constraints.  
- **L15** — ensures causal correctness of capability-based actions.  
- **L16** — ensures capability survival across undo sequences.  
- **L17** — ensures capability persistence across recovery.  
- **L18** — binds capabilities to their provenance.  
- **L19** — ensures capabilities remain auditable.  
- **L20** — supports capability verification via attestations.  
- **L21** — governs capability handoff when transferred.  
- **L22** — governs permissions, which must not exceed capabilities.

## 23.11 Invariants
1. CAPABILITY_STRUCTURAL — capabilities reflect architecture, not policy.  
2. CAPABILITY_BOUND — capabilities define what is possible, not what is allowed.  
3. CAPABILITY_TRACEABLE — all capabilities must appear in provenance.  
4. CAPABILITY_REVOCABLE — any capability may be rescinded.  
5. CAPABILITY_COMPOSABLE — capabilities may be built from smaller units.  
6. CAPABILITY_SAFE — capabilities must enforce trust and safety boundaries.  
7. CAPABILITY_REQUIRED — no action may occur without required capabilities.  

## 23.12 Informative Guidance
Capabilities should be modular, minimal, and composable. Avoid granting broad capability bundles when narrow ones suffice. AI/ADT capabilities should be tightly scoped and continuously monitored. Federated capabilities should include strong cross-domain proofs.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

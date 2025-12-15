<!--
CANONICAL: TRUE
LAYER: L42
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L42 — Authorization Model (How the Substrate Determines What an Actor Is Allowed to Do)
Defines the persistent, systemic, substrate-wide model for determining what an authenticated identity (L41) is allowed to do. Authorization governs **permissions, capabilities, delegations, constraints, governance boundaries, and safety scopes**, ensuring that every action is explicitly allowed and cannot exceed granted authority.

The Authorization Model answers:  
**“Given who you are — what are you allowed to do, under which conditions, and with what limits?”**

---

## 42.0 Purpose
L42 establishes:
- The unified authorization architecture  
- How permissions and capabilities are assigned, persisted, replayed, and validated  
- How governance defines, updates, revokes, or escalates authorization  
- How constraints and safety ceilings limit permitted behavior  
- How federated domains enforce sovereign authorization boundaries  
- How agents (ADT/MAIAi) must operate within authorization limits  
- How consensus, finality, and recovery depend on correct authorization  

Authorization is **the substrate’s control over agency** — defining not only *what can be done*, but *what cannot*.

---

## 42.1 Scope
Applies to:
- Humans, agents, systems, federated identities  
- All transitions (L33) and state mutations (L32)  
- All delegated authority (L30)  
- All permissions/capabilities (L22–L23)  
- All governance rules and overrides (L29)  
- All constraint frameworks (L31)  
- All provenance events (L18)  
- All enforcement decisions (L40)  
- All validation/verification steps (L27–L28)  

Authorization attaches to **every action, every actor, every domain, every time.**

---

## 42.2 Core Principles
1. **Authorization follows authentication** — identity first, authority second.  
2. **Authorization is explicit** — no implicit permissions.  
3. **Authorization is persistent** — must survive replay, recovery, synchronization.  
4. **Authorization is contextual** — depends on state, time, domain, and causality.  
5. **Authorization is capability-based** — authority derives from explicit capabilities.  
6. **Authorization is safety-bounded** — constraints (L31) limit permitted actions.  
7. **Authorization is governed** — governance defines and can override policy.  
8. **Authorization is non-repudiable** — all grants and uses must be provable.  

---

## 42.3 Authorization Object Model
Each authorization decision is represented as a persistent object:

### Inputs
- Actor identity (from L41)  
- Permission or capability requested  
- Delegation chain, if applicable  
- Context state (L25)  
- Governance and policy version  
- Provenance reference  
- Constraint window  

### Outputs
- Authorization decision (ALLOW / DENY / CONDITIONAL / ESCALATE)  
- Scope of allowed action  
- Duration (time window)  
- Required conditions / constraints  
- Authorizing signatures  
- Evidence and attestation references  

### Anchoring
- Authorization hash  
- Timestamp  
- Policy snapshot  
- Provenance linkage  

Authorization objects become part of canonical lineage and compliance logs.

---

## 42.4 Authorization Categories

### 42.4.1 Permission-Based Authorization
Determines **what actions** an actor may perform:
- Read/write/modify state  
- Create or update objects  
- Initiate transitions  
- Access domains or restricted resources  

### 42.4.2 Capability-Based Authorization (L23)
Determines **what powers** an actor possesses:
- Ability to mutate objects  
- Ability to modify governance structures  
- Ability to act on behalf of others  
- Ability to operate autonomous logic (agents)  

### 42.4.3 Delegated Authorization (L30)
Allows actors to use authority granted by:
- A delegator  
- A delegation chain  
- A governance body  

Delegation must be explicit and reviewable.

### 42.4.4 Contextual Authorization (L25)
Authorization depends on:
- State  
- Time  
- Governance mode  
- Constraint level  

Context changes authorization outcomes.

### 42.4.5 Federated Authorization
Ensures cross-domain operations respect:
- Domain sovereignty  
- Local governance  
- Compatibility of authority schemas  

Foreign authorization cannot override local rules.

### 42.4.6 Agent Authorization (L26)
Agents must:
- Operate within capability ceilings  
- Honor delegation boundaries  
- Respect safety constraints  

Agents receive **restricted**, not general, authorization.

---

## 42.5 Authorization Workflow

### 42.5.1 Pre-Validation Authorization Check
Occurs before L27 validation:
- Ensures actor may perform the intended action  
- Confirms correct permission/capability  
- Checks constraints and safety windows  

If unauthorized → HARD BLOCK.

### 42.5.2 Validation-Integrated Authorization
Validation (L27) enforces:
- Authorization correctness  
- Delegation chain integrity  
- Policy adherence  

### 42.5.3 Verification-Based Authorization
Verification (L28) ensures:
- Attestation of authority  
- Signature correctness  
- Hash continuity  
- No forged authorization tokens  

### 42.5.4 Consensus & Finality Authorization
During L34–L35:
- Invalid authority → transition dropped  
- Conflicting authority → governance escalation  

### 42.5.5 Post-Finality Authorization
After finality:
- Authorization logs appended to provenance  
- Agent contexts updated  
- Delegation expirations checked  

---

## 42.6 Authorization Enforcement (L40 Integration)
Authorization violations cause:
- BLOCK action  
- REVOKE permission/capability  
- QUARANTINE identity or transition  
- ESCALATE to governance  

Enforcement ensures authorization cannot be bypassed or ignored.

---

## 42.7 Authorization & Governance (L29)

### 42.7.1 Governance as Root Authority
Governance defines:
- Authorization structure  
- Allowed capability types  
- Delegation rules  
- Special or emergency powers  

### 42.7.2 Governance Overrides
Governance may:
- Grant temporary capabilities  
- Revoke any authorization  
- Override authorization outcomes  
- Impose stricter constraints  

### 42.7.3 Governance Auditing
Governance actions involving authorization must:
- Be logged  
- Be reproducible  
- Be linked to provenance  

---

## 42.8 Authorization & Constraints (L31)
Authorization interacts with constraints as follows:
- Constraint ceilings override authorization  
- Safety rules cannot be bypassed  
- Temporal and causal conditions apply  
- Constraints may tighten or disable capabilities  

Authorization defines **permission**.  
Constraints define **limits**.  
Enforcement (L40) ensures both are honored.

---

## 42.9 Authorization & Agents (ADT/MAIAi)
Agents must:
- Request permission for each action  
- Provide reasoning traces for authorization decisions  
- Stay within allocated autonomy windows  

Agents may NOT:
- Self-authorize  
- Generate or modify capabilities  
- Inherit unauthorized privileges from context  

Agent violations → sandbox or revoke.

---

## 42.10 Authorization in Recovery (L38)
During recovery:
- Authorization state must be restored  
- Expired or invalid authorization removed  
- Delegation chains revalidated  
- Governance may impose stricter authorization  

Recovery never restores unauthorized or ambiguous authority.

---

## 42.11 Federated Authorization Model
Cross-domain authorization requires:
- Verified external identity  
- Compatible authorization schemas  
- Local acceptance of external authority  
- Finality alignment  

If mismatch → reject or quarantine.

---

## 42.12 Observability & Reporting
System must expose:
- Authorization logs  
- Delegation graphs  
- Capability maps  
- Governance authorization decisions  
- Agent authorization history  

Auditors must reconstruct:
- Who acted  
- Under what authority  
- Under what conditions  
- With what limits  

---

## 42.13 Interaction With Other Layers
- **L11** — cryptographic proof of authority.  
- **L12** — deterministic authorization outcomes.  
- **L13** — mutability restrictions on authorization records.  
- **L14** — temporal windows shape valid authorization.  
- **L15/L37** — causality defines allowable effects of authorization.  
- **L16/L38** — replay authorization during rollback & recovery.  
- **L17** — authorized recovery paths only.  
- **L18** — provenance stores authorization outcomes.  
- **L19** — audits authorization actions.  
- **L20** — attestations serve as authorization tokens.  
- **L21** — custody transitions require authorization.  
- **L22–L24** — permissions/capabilities/accountability are authorization primitives.  
- **L25** — context affects authorization validity.  
- **L26** — agents operate under authorization ceilings.  
- **L27–L28** — authorization validated and verified.  
- **L29** — governance defines ultimate authority.  
- **L30–L31** — delegation and constraints bound authorization.  
- **L32–L33** — state and transitions require authorization.  
- **L34–L36** — authorization affects consensus, finality, fork prevention.  
- **L39** — validation model uses authorization evidence.  
- **L40** — enforcement blocks unauthorized action.  
- **L41** — authentication precedes authorization.  

---

## 42.14 Invariants
1. AUTHZ_REQUIRED — no action may occur without authorization.  
2. AUTHZ_EXPLICIT — authorization must be explicit, not inferred.  
3. AUTHZ_VERIFIABLE — all granted or used authority must be provable.  
4. AUTHZ_PERSISTENT — authorization survives replay and recovery.  
5. AUTHZ_CONTEXTUAL — authorization depends on active state and constraints.  
6. AUTHZ_GOVERNED — governance defines or overrides authorization rules.  
7. AUTHZ_LEAST_PRIVILEGE — minimum necessary authority only.  

---

## 42.15 Informative Guidance
Authorization governs **power**, and so must be conservative.  
Privileges expand rarely, contract frequently, and expire naturally.  
Agents must assume the least authority necessary and validate continuously.  
Federated identities must not assume equivalence — authorization is local first.  
Authorization review is one of the most important substrate-level audits.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

<!--
CANONICAL: TRUE
LAYER: L30
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L30 — Delegation Rules (How Authority, Responsibility & Rights Are Safely Transferred)
Defines how actors delegate authority, permissions, capabilities, responsibilities, custody, and decision rights to other actors — human, organizational, ADT, MAIAi, or federated — while preserving authenticity, accountability, traceability, and governance boundaries.

## 30.0 Purpose
L30 establishes the canonical rules that govern:
- Who may delegate authority  
- What may be delegated  
- How delegations are created, verified, and revoked  
- How delegated actions are attributed and audited  
- How ADT/MAIAi may receive limited or conditional delegation  
- How delegation interacts with governance, permissions, capabilities, and context  

Delegation answers the question: **“Who may act on behalf of whom, under what constraints, with what authority?”**

## 30.1 Scope
Delegation rules apply to:
- Human identities  
- Organizational and federated authorities  
- ADT/MAIAi agents  
- CSR, Architect, and domain governance entities  
- Permissions (L22), capabilities (L23), accountabilities (L24)  
- Custody (L21) and attestations (L20)  
- Cross-substrate delegation and federated trust  

Delegation is universal and must be cryptographically binding.

## 30.2 Core Principles
1. **Delegation must be explicit** — no implicit delegation is valid.  
2. **Delegation must be authenticated** — the delegator’s identity must be cryptographically verified.  
3. **Delegation must be bounded** — in scope, time, capability, permission, and context.  
4. **Delegation must be traceable** — provenance (L18) must record every delegation.  
5. **Delegation must be revocable** — revocation must be immediate and enforceable.  
6. **Delegation must respect governance** — no delegation may exceed governance authority (L29).  
7. **Delegation does not remove accountability** — responsibility may shift, but accountability remains (L24).  

## 30.3 Delegation Object Model
Each delegation must contain:

### Identity Fields
- Delegator (who grants authority)  
- Delegatee (who receives authority)  
- Verification of both identities  

### Delegation Scope
- Actions permitted  
- Capabilities granted (L23)  
- Permissions granted (L22)  
- Custody rights (if applicable, L21)  
- Context-specific boundaries (L25)  

### Constraints
- Time window  
- Quantity or repetition limits  
- Safety or governance boundaries  
- Requirement for human supervision  
- Required attestations (L20)  

### Cryptographic Binding
- Delegation hash  
- Delegator signature  
- Optional multisig for Critical delegations  
- Optional zero-knowledge forms for federated delegation  

### Anchoring
- Timestamp  
- Causal parent events (L15)  
- Provenance insertion  

## 30.4 Delegable Entities
The substrate defines what may be delegated:

### 30.4.1 Actions
Discrete or structured tasks:
- Approvals  
- State transitions  
- Data transformations  
- Execution of workflows  

### 30.4.2 Permissions (L22)
Delegable if:
- The delegator holds them  
- They are marked as delegable  
- Governance does not restrict them  

### 30.4.3 Capabilities (L23)
Delegable only if:
- The capability model allows delegation  
- Safety constraints remain intact  

### 30.4.4 Custody (L21)
Delegable when:
- Custody transitions are authenticated  
- Delegation does not break lineage  

### 30.4.5 Attestation Authority (L20)
Delegable only when:
- Domain policy allows it  
- Delegation carries attestation responsibility  

### 30.4.6 ADT/MAIAi Decision Rights
Delegable under:
- Strict constraint windows (L26)  
- Verified permission/capability ceilings  
- Oversight triggers  
- Context boundaries  

## 30.5 Delegation Rules

### 30.5.1 Authority Validation
Delegator must:
- Possess the authority being delegated  
- Have active, verified identity  
- Operate within jurisdiction boundaries  

### 30.5.2 Scope Limitation
Delegation must specify:
- Exact actions  
- Exact capabilities  
- Exact permissions  
- Maximum autonomy permitted  

### 30.5.3 Minimal Delegation Principle
Grant only what is required.  
Never grant more than necessary.

### 30.5.4 Temporal Boundaries
Delegations must define start and end times.  
No indefinite delegation is valid unless governance-approved.

### 30.5.5 Context Binding
Delegations must specify context windows (L25):
- Who  
- What  
- Where  
- Under what policy  
- Under what dependencies  

### 30.5.6 Cascade Prevention
Delegations cannot be redelegated unless explicitly permitted.

### 30.5.7 Delegation Chaining
If allowed, each link must:
- Be independently verifiable  
- Maintain lineage  
- Track cumulative constraints  

### 30.5.8 Revocation
Delegation must be:
- Immediately revocable  
- Auditable  
- Enforceable at the next verification cycle  

### 30.5.9 Conflict Handling
Conflicting delegations must:
- Trigger escalation  
- Defer to governance hierarchy (L29)  
- Be resolved through CSR or Architect rules  

## 30.6 Delegation to Agents (ADT/MAIAi)
ADT/MAIAi may receive limited delegation, under strict rules:

### Requirements
- Capability ceilings (L23)  
- Permission ceilings (L22)  
- Constraint activation (L26)  
- Context propagation checks (L25)  
- Oversight or supervision requirements  

### Obligations
Agents must:
- Not exceed delegated scope  
- Produce proofs (L28)  
- Log all delegated actions (L19)  
- Escalate when uncertain  

Delegation to AI is always conditional, never absolute.

## 30.7 Verification & Validation of Delegations
Delegations must pass:

### Verification (L28)
- Signatures  
- Hash integrity  
- Authority legitimacy  
- Scope correctness  

### Validation (L27)
- Dependencies  
- Policy legality  
- Safety constraints  
- Causal and temporal correctness  

Invalid delegations cannot be accepted or used.

## 30.8 Revocation Rules
Delegations must support:

### Immediate Revocation
- No grace period  
- No ability for delegatee to delay enforcement  

### Cascading Revocation
All dependent delegations must be recursively revoked.

### Revocation Evidence
Revocation must:
- Produce attestations  
- Update provenance  
- Trigger downstream safety checks  

## 30.9 Observability & Reporting
The substrate must expose:
- Delegation graphs  
- Active delegation lists  
- Delegation lineage  
- Conflicts and overrides  
- Delegation-to-agent audit trails  
- Revocation logs  

Auditors must reconstruct:
- Who delegated what  
- Under what authority  
- Under what constraints  
- How the delegation was used  
- Whether responsibilities were fulfilled  

## 30.10 Interaction With Other Layers
- **L11** — provides signature primitives for delegate authority.  
- **L12** — ensures deterministic interpretation of delegation.  
- **L13** — governs mutability of delegated objects.  
- **L14** — enforces delegation time windows.  
- **L15** — ensures causal correctness of delegation flows.  
- **L16** — handles delegation during undo operations.  
- **L17** — ensures delegated authority survives or is corrected during recovery.  
- **L18** — attaches delegation to provenance.  
- **L19** — audits delegated actions.  
- **L20** — manages delegation of attestation authority.  
- **L21** — defines delegated custody transfers.  
- **L22** — governs delegable permissions.  
- **L23** — governs delegable capabilities.  
- **L24** — defines accountability under delegation.  
- **L25** — governs contextual boundaries for delegation.  
- **L26** — defines constraints on agent-delegated behavior.  
- **L27** — performs delegation validation.  
- **L28** — verifies delegation correctness.  
- **L29** — governs delegation authority hierarchy.  

## 30.11 Invariants
1. DELEGATION_EXPLICIT — nothing may be delegated implicitly.  
2. DELEGATION_AUTHENTIC — only authenticated delegators may delegate.  
3. DELEGATION_BOUNDED — scope and time must always be limited.  
4. DELEGATION_TRACEABLE — provenance must always reflect delegation.  
5. DELEGATION_REVOCABLE — delegations must always be immediately revocable.  
6. DELEGATION_ACCOUNTABLE — delegators remain accountable for delegated actions.  
7. DELEGATION_SAFE — delegations must never break substrate safety invariants.  

## 30.12 Informative Guidance
Delegation is most powerful when used minimally.  
Agents should receive granular, not broad, delegation.  
Federated delegations should rely on zero-knowledge authority proofs.  
Delegation drift must be monitored continuously as a systemic risk.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

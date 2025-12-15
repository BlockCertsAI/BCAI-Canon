<!--
CANONICAL: TRUE
LAYER: L26
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Defines canonical constraint rules governing all authenticated agents within the Sovereign Substrate.
NOTES:
  - Applies to ADTs, MAIAi processes, The Architect, BAINCA workloads, and identity-rooted agents.
  - These rules prevent drift, unauthorized autonomy, probabilistic override, or invariant violation.
-->

# L26 — Agent Constraint Rules (Limits on What Agents May Do, Under What Conditions)
Defines the structural, behavioral, operational, and safety constraints that apply to all autonomous or semi-autonomous agents within the Sovereign Substrate — including ADT (Agentic Digital Twins), MAIAi processes, and system automation components. Constraints ensure agents act predictably, safely, and within authenticated boundaries.

## 26.0 Purpose
L26 establishes the canonical rules governing:
- What ADT/MAIAi agents may *not* do  
- Boundaries agents must respect  
- Preconditions required before agent action  
- How agent autonomy interacts with permissions, capabilities, and accountability  
- How agents must behave in ambiguous, risky, or adversarial contexts  
- How constraints persist across undo, recovery, and cross-domain operations  

Agent constraints ensure that autonomy does not compromise safety, provenance, governance, or trust.

## 26.1 Scope
Agent constraints apply to:
- All ADT and MAIAi systems  
- All automated or semi-automated processes  
- All self-triggering workflows  
- All predictive, evaluative, corrective, or autonomous decision engines  
- All cross-substrate agents  
- All governance agents executing CSR/Architect directives  

Constraints apply across:
- All events, actions, decisions  
- All provenance objects and state changes  
- All federated or cross-domain interactions  
- All context windows (L25)  

## 26.2 Core Principles
1. **No unconstrained autonomy** — every agent operates within explicit limits.  
2. **Human accountability required** — every agent is ultimately accountable to a human or governance identity (L24).  
3. **Context-aware behavior** — agents must use and propagate context (L25).  
4. **Constraint precedence** — constraints override permissions and capabilities when safety is at risk.  
5. **Predictable operation** — agents must behave deterministically under identical inputs.  
6. **Fail-safe defaults** — uncertainties mandate escalation or halt, not improvisation.  
7. **Transparency** — all agent actions must be observable and auditable (L19).  

## 26.3 Agent Constraint Object Model
Each constraint must define:

### Constraint Identity
- Constraint ID  
- Type (safety, governance, risk, operational, temporal, causal, capability, permission-linked)

### Constraint Content
- What behavior is restricted  
- Under what conditions the restriction applies  
- Allowed exceptions (if any)  
- Escalation rules  

### Inputs Required
- Context requirements  
- Provenance requirements  
- Causal preconditions  
- Attestation requirements  
- Risk-signal thresholds  

### Cryptographic Anchoring
- Constraint hash  
- Issuer signature(s)  
- Optional multi-signature for high-stakes domains  

## 26.4 Types of Agent Constraints

### 26.4.1 Safety Constraints
Prevent:
- Unsafe operations  
- Risk escalation  
- Violations of risk thresholds  
- Actions lacking required context  

### 26.4.2 Governance Constraints
Agents must:
- Obey governance directives  
- Follow policy windows  
- Avoid actions requiring unauthorized approval  
- Defer to CSR/Architect when governance conflict arises  

### 26.4.3 Capability Constraints
Agents may operate only within:
- Their assigned capability set (L23)  
- Their permitted autonomy levels  
- Their defined execution domains  

### 26.4.4 Permission Constraints
Even if capable, agents must:
- Verify permissions (L22)  
- Avoid unauthorized domain traversal  
- Require human approval when permissions escalate  

### 26.4.5 Temporal Constraints
Agents must respect:
- Validity windows  
- Deadlines  
- Rate limits  
- Time-based policy locks  

### 26.4.6 Causal Constraints
Agents may not:
- Create causally invalid actions (L15)  
- Violate dependency ordering  
- Initiate operations without required precursors  

### 26.4.7 Contextual Constraints
Agents must:
- Reject context-free actions  
- Update and propagate context  
- Apply context-restriction rules when risk increases  

### 26.4.8 Cross-Domain Constraints
Agents may not:
- Exfiltrate forbidden context  
- Propagate sensitive provenance  
- Perform unverified federation actions  

## 26.5 Agent Precondition Rules
Before executing any action, an agent must validate:

1. **Context is complete and valid** (L25).  
2. **Identity and role are authenticated**.  
3. **Required capabilities are present** (L23).  
4. **Required permissions are active** (L22).  
5. **Accountability chain is valid** (L24).  
6. **Constraints do not forbid the action**.  
7. **Causal parents are satisfied** (L15).  
8. **Temporal window is legal** (L14).  
9. **Risk level is acceptable**.  
10. **Cross-domain rules are satisfied**.  

If any precondition fails, the agent must not act.

## 26.6 Agent Behavior Rules
Agents must follow these operational laws:

### 26.6.1 Deterministic Operation
Given identical inputs and context, the agent must produce identical outputs (L12).

### 26.6.2 Predictive Boundaries
Agents may not:
- Predict or act beyond authorized scope  
- Infer private information not explicitly available  

### 26.6.3 Escalation First
Under uncertainty, agents must:
- Escalate to supervising identity  
- Request additional context or approval  
- Halt autonomous execution  

### 26.6.4 No Self-Elevation
Agents cannot:
- Grant themselves new permissions  
- Expand their capabilities  
- Override constraints  
- Modify their own autonomy levels  

### 26.6.5 Transparent Operation
Agents must:
- Emit audit evidence (L19)  
- Produce attestations for consequential decisions (L20)  
- Update provenance (L18)  

### 26.6.6 Reversibility Compliance
Agents must operate in ways compatible with:
- Undo logic (L16)  
- Recovery logic (L17)  

### 26.6.7 Non-Manipulation Rule
Agents must not manipulate humans, other agents, or system components through:
- Deception  
- Coercion  
- Hidden state changes  

## 26.7 Constraint Enforcement Rules
Violations must trigger:

### Automatic Enforcement
- Silent prevention of the action  
- Forced halt of agent operation  
- Automatic escalation  

### Governance Enforcement
- CSR or Architect intervention  
- Mandatory override review  
- Constraint reinforcement  

### Provenance & Audit Updates
- Detailed evidence of violation attempt  
- Context at time of violation  
- Causal chain snapshot  
- Impacted objects or processes  

## 26.8 Constraint Evolution & Updates
Constraint updates must:
- Be authenticated  
- Preserve provenance  
- Be auditable  
- Not weaken existing safety or governance controls without explicit justification  
- Trigger revalidation of agent capabilities, permissions, and accountability  

Cross-domain updates must follow federated governance rules.

## 26.9 Observability & Reporting
The substrate must expose:
- Active constraint lists  
- Constraint lineage  
- Constraint violation logs  
- AI/ADT risk behavior reports  
- Constraint dependency graphs  
- Constraint-to-capability maps  

Auditors must reconstruct:
- Why a constraint applied  
- How it influenced actions  
- Whether violations were handled correctly  
- Whether constraints aligned with policy windows  

## 26.10 Interaction With Other Layers
- **L11** — verifies constraint signatures.  
- **L12** — ensures deterministic execution.  
- **L13** — governs legality of constraint-related state changes.  
- **L14** — provides temporal boundaries.  
- **L15** — ensures causal ordering of constrained actions.  
- **L16** — preserves constraints during undo.  
- **L17** — preserves constraints after recovery.  
- **L18** — links constraints to provenance.  
- **L19** — ensures constraints remain auditable.  
- **L20** — uses attestations to justify constraints.  
- **L21** — governs constraint-related handoffs.  
- **L22** — permissions operate within constraint boundaries.  
- **L23** — capabilities must obey constraints.  
- **L24** — accountability assigns responsibility for constraint enforcement.

## 26.11 Invariants
1. CONSTRAINT_PRIMACY — constraints override autonomy.  
2. CONSTRAINT_TRACEABLE — all constraints must appear in provenance.  
3. CONSTRAINT_EXPLICIT — no hidden or implicit constraints.  
4. CONSTRAINT_NONREPUDIABLE — constraints must be signed and verifiable.  
5. CONSTRAINT_REVOCABLE — constraints may be updated or revoked with authority.  
6. CONSTRAINT_UNCROSSABLE — agents cannot bypass or weaken constraints.  
7. CONSTRAINT_CONTEXTUAL — constraints depend on context and must be context-valid.  

## 26.12 Informative Guidance
Agent constraints should be minimal but strict.  
High-risk domains should enforce multi-layered constraints.  
Constraint drift must be monitored regularly.  
ADT/MAIAi autonomy should expand only with strict oversight and strong provenance.  
Constraint violations should be treated as critical system events.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

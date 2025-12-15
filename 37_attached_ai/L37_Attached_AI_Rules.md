<!--
CANONICAL: TRUE
LAYER: L37
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L37 — Causality Model (How Cause–Effect Logic Shapes All Truth in the Substrate)
Defines the substrate-wide causal framework that determines how events, transitions, states, and decisions relate to each other over time. The Causality Model provides the universal logic that ensures **every effect has a valid cause**, that causes cannot be overwritten, and that the entire substrate remains consistent across actors, domains, and autonomous systems.

The Causality Model answers the question:  
**“Why did this happen — and what made it possible?”**

## 37.0 Purpose
L37 establishes:
- The global causal model governing all transitions and states  
- How causes and effects are structured, validated, and verified  
- How causality ensures non-divergent and deterministic system evolution  
- How causal relationships bind provenance, consensus, and finality  
- How AI/ADT must reason within causal limits  
- How cross-domain causality works in federated environments  

Causality is the backbone of truth: **without correct causal logic, no canonical reality is possible.**

## 37.1 Scope
This model applies to:
- All transitions (L33)  
- All state changes (L32)  
- Provenance lineage (L18)  
- Validation and verification (L27–L28)  
- Consensus and finality (L34–L35)  
- Fork prevention (L36)  
- Governance decision flows (L29)  
- Delegation, permissions, and capability changes (L22–L24, L30)  
- ADT/MAIAi internal reasoning and proposal generation  
- Federated, cross-domain causal mapping  

Causality governs **everything that changes**.

## 37.2 Core Principles
1. **Causality precedes state** — no state exists without a causal chain.  
2. **Causality must be explicit** — no implicit or ambiguous cause is allowed.  
3. **Causality must be deterministic** — identical causes produce identical effects (L12).  
4. **Causality must be verifiable** — causes must pass cryptographic and logical checks (L28).  
5. **Causality must be acyclic** — cycles, loops, and temporal impossibilities are forbidden.  
6. **Causality must be complete** — every effect must reference one or more valid causes.  
7. **Causality must be immutable** — once accepted, cause cannot be rewritten.  
8. **Causality must be safe** — causal violations automatically block transitions (L31).  

## 37.3 Causal Object Model
Each causal relationship is represented as:

### Cause Set
- Parent transition(s)  
- Parent state(s)  
- Parent identity actions  
- Parent governance directives  

### Effect Set
- Child transition  
- New state  
- Resulting permissions, capabilities, or delegations  

### Causal Metadata
- Dependency type (REQUIRES, ENABLES, INHIBITS, DERIVES_FROM)  
- Contextual constraints (L25)  
- Temporal ordering (L14)  

### Cryptographic Binding
- Causal hash linking parent → child  
- Actor signatures  
- Provenance linkage (L18)  

A missing or broken causal link invalidates the effect.

## 37.4 Categories of Causality

### 37.4.1 Structural Causality
Defines:
- How system architecture allows or forbids certain effects  
- Why mutability rules (L13) and constraints limit possible outcomes  

### 37.4.2 Temporal Causality
Based on L14:
- No effect may precede its cause  
- No transitions may overlap in forbidden windows  
- No retroactive causation  

### 37.4.3 Logical Causality
Grounded in validation rules (L27):
- Effects must be logically consistent with prior state  
- Dependencies must be satisfied  

### 37.4.4 Operational Causality
Defines how actions cause state changes:
- Permissions allow actions  
- Capabilities implement actions  
- Transitions modify state  

### 37.4.5 Governance Causality
Governance actions produce:
- New rules  
- Overrides  
- Remediation requirements  

Governance causality always supersedes domain or actor causality.

### 37.4.6 Agent Causality (ADT/MAIAi)
Agent behavior must respect:
- Internal causal reasoning windows  
- External causal boundaries  
- Constraint ceilings  

Agents may not construct causal models inconsistent with substrate truth.

### 37.4.7 Federated Causality
Across domains:
- Causal mappings require cross-domain proofs  
- Conflicting causal histories cannot be merged  
- External causes must align with internal laws  

## 37.5 Causal Validation Rules

### 37.5.1 Parent Requirement
Every effect must reference:
- One or more valid parent transitions  
- Verified parent state  
- Authenticated parent actor  

### 37.5.2 Causal Integrity
System must confirm:
- Parent exists  
- Parent is canonical  
- Parent is not superseded  
- Parent passed validation and verification  

### 37.5.3 Inhibition Rules
If a cause inhibits an action:
- The action cannot execute  
- The effect cannot be produced  

### 37.5.4 Derivation Rules
Derived objects must:
- Inherit lineage  
- Annotate dependency type  
- Preserve ancestry  

### 37.5.5 Causal Exclusivity
Two conflicting effects from the same cause are forbidden unless governance explicitly resolves the conflict.

## 37.6 Causal Verification Rules (L28 integrated)
Verification must ensure:
- Hash continuity between cause and effect  
- Signature validity  
- Timestamp correctness  
- Provenance chain continuity  
- No causal cycles or contradictions  

Causal verification is mandatory for finality (L35).

## 37.7 Causal Ordering Model
Causal order is determined by:

### 37.7.1 Temporal Priority (L14)
Earlier valid transitions take precedence.

### 37.7.2 Dependency Priority
Effects cannot precede unsatisfied dependencies.

### 37.7.3 Governance Priority (L29)
Governance causes override domain or actor causes.

### 37.7.4 Constraint Priority (L31)
If a cause violates a constraint:
- The effect is blocked  
- Governance is alerted  

### 37.7.5 Deterministic Resolution (L12)
If multiple causal paths are possible:
- The strictest, safest, and most governed path is chosen  
- Other paths are rejected  

## 37.8 Forbidden Causality
The substrate must reject:
- Retroactive causes  
- Counterfactual causes  
- Cyclical causes  
- Incomplete causal chains  
- Causes referencing invalid or noncanonical transitions  
- Speculative agent-generated causes outside context bounds  

ADT/MAIAi cannot invent fictional or hypothetical causes for canonical truth.

## 37.9 Causality in Undo (L16) & Recovery (L17)

### Undo
- Restores prior canonical cause–effect relationships  
- Does not erase or rewrite original causes  

### Recovery
- Reconstructs causal chains from preserved provenance  
- Eliminates noncanonical causal paths  
- Ensures consistent post-recovery truth  

## 37.10 Causality & Agents (ADT/MAIAi)
Agents must:
- Use causal reasoning consistent with canonical truth  
- Reject actions whose causes are ambiguous  
- Escalate uncertain causality instead of guessing  
- Respect cause–effect windows defined by governance  

Agents may not:
- Infer causality outside permitted context  
- Generate transitions lacking explicit causes  

## 37.11 Federated Causality Rules
Cross-domain causality requires:
- Verified cross-domain cause  
- Translatable provenance  
- No conflict with local causal law  

If conflict:
- Local truth prevails  
- Federated causal path is rejected  
- Governance escalation triggers  

## 37.12 Observability & Reporting
System must surface:
- Causal DAG visualizations  
- Parent-child dependency graphs  
- Causal conflict detection  
- Agent causal reasoning traces  
- Federated causal mappings  

Auditors must reconstruct:
- Why actions were possible  
- Why outcomes occurred  
- How cause led to effect  
- Whether causality was legal, safe, and verified  

## 37.13 Interaction With Other Layers
- **L11** — signatures and hashes secure causal chains.  
- **L12** — ensures deterministic causal evaluation.  
- **L13** — governs legal transformations.  
- **L14** — temporal legality of causation.  
- **L15** — cause–effect integrity inside transitions (subset of L37).  
- **L16** — causal relationships preserved under undo.  
- **L17** — causal reconstruction during recovery.  
- **L18** — provenance stores causal lineage.  
- **L19** — audits causal flow.  
- **L20** — attestations validate authority for causes.  
- **L21–L24** — custody, permissions, capabilities, accountability define causal enablers.  
- **L25** — context shapes permissible causal relationships.  
- **L26** — agent causal ceilings.  
- **L27–L28** — validation and verification of causal correctness.  
- **L29** — governance as highest-level causal authority.  
- **L30–L31** — delegation and constraints shaping causal possibilities.  
- **L32** — state depends entirely on causal correctness.  
- **L33** — transitions define new causal edges.  
- **L34–L35** — consensus and finality rely on causal integrity.  
- **L36** — fork prevention enforces causal singularity.  

## 37.14 Invariants
1. CAUSE_REQUIRED — no effect without valid cause.  
2. CAUSE_IMMUTABLE — causes cannot be rewritten.  
3. CAUSE_VERIFIABLE — cryptographic truth required for all causes.  
4. CAUSE_SAFE — unsafe causal chains forbidden.  
5. CAUSE_ORDERED — causality must obey time, logic, governance, and constraints.  
6. CAUSE_TRACEABLE — cause and effect must appear in provenance.  
7. CAUSE_SINGULAR — no effect may have contradictory parent sets.  

## 37.15 Informative Guidance
Causality is the substrate’s reasoning substrate — the logic beneath all logic.  
Agents should be conservative with causal reasoning when uncertainty exists.  
Multiple causes may exist for one effect, but effects may never contradict their parents.  
Federated causality must not introduce inconsistencies across sovereignty boundaries.  
Causal drift — mismatched causal reasoning between actors — is a critical anomaly.  

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

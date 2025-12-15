<!--
CANONICAL: TRUE
LAYER: L34
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L34 — Consensus Model (How the Substrate Reaches Agreement on Canonical Truth)
Defines how the Sovereign Substrate determines, confirms, and finalizes shared truth — not through mining, staking, or probabilistic voting, but through **authenticated, deterministic, constraint-aligned agreement** built directly into the substrate’s identity, governance, verification, and provenance layers.

The Consensus Model answers the question:  
**“How does the system agree on what is true?”**

## 34.0 Purpose
L34 establishes:
- How consensus is defined in a Proof-of-Authentication substrate  
- How actors participate in consensus implicitly through verified actions  
- How truth is established deterministically rather than probabilistically  
- How consensus depends on identity, state, provenance, validation, and verification  
- How consensus determines canonical inclusion or rejection of transitions  
- How consensus operates in single-domain, multi-domain, and federated environments  

Consensus in the Sovereign Substrate is **deterministic, identity-bound, rule-driven, and provable**.

## 34.1 Scope
Consensus applies to:
- All canonical transitions (L33)  
- All state updates (L32)  
- Identity and permission/capability changes (L22–L23)  
- Provenance acceptance (L18)  
- Governance directives (L29)  
- Delegation flows (L30)  
- Context propagation (L25)  
- ADT/MAIAi agent-generated proposals  
- Undo (L16) and Recovery (L17)  
- Cross-domain and federated truth reconciliation  

No canonical truth can exist without consensus.

## 34.2 Core Principles
1. **Identity precedes consensus** — only authenticated identities may participate.  
2. **Consensus is deterministic** — same events → same result everywhere (L12).  
3. **Consensus is rule-governed** — not probabilistic, economic, or competitive.  
4. **Consensus is evidence-based** — verified proofs (L28) determine acceptance.  
5. **Consensus is constraint-bound** — unsafe transitions cannot be accepted (L31).  
6. **Consensus is governance-aligned** — governance rules supersede domain rules (L29).  
7. **Consensus is causal** — event ordering determines validity (L15).  
8. **Consensus is temporal** — transitions must be time-legitimate (L14).  
9. **Consensus is non-repudiable** — once accepted, truth cannot be denied (L20).  

## 34.3 Consensus Object Model
Every consensus decision must include:

### Inputs
- Transition intent and delta  
- Identity proofs  
- Permissions/capabilities  
- Constraint evaluations  
- Verification artifacts (signatures, hashes, proofs)  
- Causal and temporal anchors  
- Governance references  
- Provenance chain  

### Outputs
- Consensus outcome (ACCEPT / REJECT / DEFER)  
- Evidence bundle supporting the decision  
- Consensus hash  
- Canonicalization status  
- Any required attestations  
- Escalation triggers (if applicable)  

### Anchoring
- Consensus timestamp  
- Causal ordering relative to nearby transitions  
- Provenance update  

## 34.4 Consensus Phases
Consensus proceeds through deterministic, rule-governed phases:

### 34.4.1 Proposal Phase
A transition is proposed by:
- A human identity  
- An organizational identity  
- An ADT/MAIAi  
- A governance entity  

All proposals must be authenticated.

### 34.4.2 Eligibility Phase
System verifies:
- Identity validity  
- Permission/capability floor  
- Delegation legitimacy  
- Governance boundaries  
- Required context  

If failed → REJECT (not eligible).

### 34.4.3 Validation Phase (L27)
System checks:
- Logical correctness  
- Schema conformity  
- Mutability legality  
- Safety rules  
- Dependency resolution  

If failed → REJECT (invalid).

### 34.4.4 Verification Phase (L28)
System verifies:
- Signatures  
- Hashes  
- Temporal correctness  
- Causal correctness  
- Provenance continuity  

If failed → REJECT (unverifiable).

### 34.4.5 Constraint Phase (L31)
System evaluates:
- Safety constraints  
- Risk ceilings  
- Autonomy limits  
- Governance-critical constraints  

If violated → BLOCK (requires escalation).

### 34.4.6 Governance Phase (L29)
System checks:
- Whether governance directly influences this transition  
- Whether governance overrides apply  
- Whether domain boundaries impose conditions  

### 34.4.7 Consensus Finalization Phase
If all phases succeed:
- Transition becomes canonical  
- State updates (L32)  
- Provenance updates (L18)  
- Accountability updates (L24)  

If unclear → DEFER (waiting for missing evidence).  

## 34.5 Deterministic Consensus Rules
Consensus is **not** derived from:
- Hash difficulty  
- Economic stake  
- Lottery randomness  
- Validator voting  
- Majority participation  

Instead, consensus emerges automatically when **all canonical rules agree**.

### 34.5.1 Deterministic Input Model
Every participant must:
- See identical prior state  
- Have identical transition inputs  
- Produce identical validation/verification results  

### 34.5.2 Deterministic Output Model
Consensus must yield:
- Identical canonical truth everywhere  
- Identical rejection reasons  
- Identical provenance entries  

### 34.5.3 Deterministic Conflict Resolution
Conflicts are resolved by:
- Causality (L15)  
- Temporal precedence (L14)  
- Governance hierarchy (L29)  
- Constraint severity (L31)  

## 34.6 Consensus for AI/ADT Agents
AI-involved transitions require additional safeguards:

### Requirements
Agents must:
- Provide explanation traces  
- Prove constraint compliance  
- Stay within capability ceilings  
- Provide attestation bundles  

### Limitations
Agents may not:
- Self-elect to bypass consensus  
- Declare a transition canonical  
- Influence governance layers  
- Rewrite or reorder events  

### Escalation
If an agent cannot determine consensus:
- Escalate to human or governance authority  

## 34.7 Federated Consensus (Cross-Domain)
Federated environments require:

### 34.7.1 Truth Mapping
State and transitions must be mapped across trust boundaries.

### 34.7.2 Cross-Domain Proof Exchange
Domains exchange:
- Identity proofs  
- Provenance fragments  
- Attestation bundles  
- Consistency checks  

### 34.7.3 Federated Conflict Resolution
Conflicts resolved by:
- Domain sovereignty  
- Pre-negotiated trust anchors  
- External governance agreements  

Federated consensus must still produce a singular canonical truth within each domain.

## 34.8 Consensus Failure Modes

### 34.8.1 Hard Rejection
When validation, verification, or identity fails.

### 34.8.2 Deadlock
Two transitions mutually block due to:
- Causality conflicts  
- Governance conflicts  

Deadlocks defer until resolved by governance or domain policy.

### 34.8.3 Incomplete Evidence
Transition remains pending until evidence arrives.

### 34.8.4 Unsafe Transition
Violates constraints → BLOCKED.

All failures must produce governance-visible evidence.

## 34.9 Observability & Reporting
System must expose:
- Consensus logs  
- Conflict maps  
- Consensus graphs  
- Federated truth maps  
- Rejection explanations  
- ADT/MAIAi consensus traces  

Auditors must reconstruct:
- Why consensus was achieved  
- Why transitions were accepted or rejected  
- How governance influenced outcomes  
- Whether actors behaved lawfully  

## 34.10 Interaction With Other Layers
- **L11** — cryptographic primitives supporting consensus.  
- **L12** — deterministic execution of consensus rules.  
- **L13** — determines what transitions are legal.  
- **L14** — temporal constraints on consensus.  
- **L15** — causal ordering of consensus events.  
- **L16** — consensus rollback behavior.  
- **L17** — consensus reconstruction after recovery.  
- **L18** — provenance inclusion of consensus decisions.  
- **L19** — audits consensus.  
- **L20** — attestation requirements.  
- **L21** — custody transitions requiring consensus.  
- **L22** — permission-based consensus eligibility.  
- **L23** — capability-based consensus eligibility.  
- **L24** — accountability for consensus actions.  
- **L25** — context evaluation during consensus.  
- **L26** — agent constraint checks.  
- **L27** — transition validation.  
- **L28** — transition verification.  
- **L29** — governance override and approval.  
- **L30** — delegation legitimacy.  
- **L31** — system-wide constraints.  
- **L32** — state formation after consensus.  
- **L33** — transition construction leading to consensus.  

## 34.11 Invariants
1. CONSENSUS_DETERMINISTIC — consensus must produce identical results everywhere.  
2. CONSENSUS_AUTHENTIC — only authenticated actors may create transitions.  
3. CONSENSUS_RULE_GOVERNED — consensus follows rules, not voting or competition.  
4. CONSENSUS_SAFE — unsafe transitions must never be accepted.  
5. CONSENSUS_TRACEABLE — all consensus decisions must be provenanced.  
6. CONSENSUS_FINAL — once accepted, transitions become immutable history.  
7. CONSENSUS_CONTEXTUAL — must consider environmental and policy context.  

## 34.12 Informative Guidance
Consensus should be viewed not as a *competition*, but as **a truth-engine** powered by identity, rules, safety, and evidence.  
Cross-domain consensus should be conservative and privacy-preserving.  
AI/ADT consensus requires enhanced transparency.  
Consensus drift or instability is a critical governance event.  
Federated consensus must minimize trust assumptions.
Return to Navigation:

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

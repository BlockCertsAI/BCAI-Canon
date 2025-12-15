<!--
CANONICAL: TRUE
LAYER: L35
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L35 — Finality Model (How Truth Becomes Permanent, Immutable & Canonical)
Defines how transitions, events, states, and decisions reach **irrevocable canonical status** within the Sovereign Substrate. Finality represents the moment when truth is sealed — no longer provisional, no longer reversible, no longer challengeable except through recovery procedures governed by authenticated evidence.

Finality answers the question:  
**“When does something become permanent truth?”**

## 35.0 Purpose
L35 establishes:
- What it means for a transition to become final  
- How finality is reached deterministically in a PoA substrate  
- How finality interacts with consensus (L34), state (L32), and transitions (L33)  
- How governance, provenance, and constraints guarantee immutable truth  
- How ADT/MAIAi must treat final vs. provisional truth  
- How finality persists across undo (L16), recovery (L17), and federation  

Finality is the substrate’s **guarantee that truth cannot be altered retroactively**.

## 35.1 Scope
The Finality Model applies to:
- All state transitions  
- Identity and object states  
- Governance directives  
- Delegations, permissions, and capability changes  
- Custody transitions  
- Provenance commitments  
- AI/ADT decisions incorporated into canonical truth  
- Federated and cross-domain truth synchronization  

Finality binds the substrate’s entire truth model.

## 35.2 Core Principles
1. **Finality is deterministic** — same evidence → same final outcome everywhere (L12).  
2. **Finality is authenticated** — only verified actors and transitions may become final.  
3. **Finality is rule-governed** — driven by validation, verification, and constraints.  
4. **Finality is irreversible** — once canonical, transitions cannot be rewritten.  
5. **Finality is sequenced** — dependent on temporal and causal order (L14–L15).  
6. **Finality is provenanced** — every final truth has an unbroken lineage (L18).  
7. **Finality is safe** — unsafe transitions can never be finalized (L26, L31).  
8. **Finality is visible** — auditors must be able to reconstruct how truth became final.  

## 35.3 Finality Object Model
Each finality event contains:

### Inputs
- Validated transition (L27)  
- Verified evidence (L28)  
- Consensus outcome (L34)  
- Constraints evaluation  
- Governance implications  

### Outputs
- Finality decision (FINAL / NOT_FINAL / DEFERRED)  
- Finality hash  
- Provenance commitment  
- Accountability mapping  
- Required attestations (L20)  

### Anchoring
- Finality timestamp  
- Causal ordering reference  
- State snapshot linkage  
- Governance signature (if required)  

## 35.4 Types of Finality

### 35.4.1 Structural Finality
Applied to:
- Identity origins  
- Object origins  
- Immutable data formations  

These cannot be undone except through recovery.

### 35.4.2 Transition Finality
A transition becomes final when:
- All validation and verification criteria are met  
- Consensus (L34) accept is sealed  
- Provenance entry is committed  
- No constraints have been violated  

### 35.4.3 State Finality
A new canonical state (L32) becomes immutable once:
- Transition finality is achieved  
- No competing transitions exist  
- Governance does not impose provisional status  

### 35.4.4 Governance Finality
Governance directives become final when:
- Proper authority signatures attach  
- No conflicting governance rules apply  
- Provenance insertion succeeds  

### 35.4.5 Delegation & Permission Finality
Authority changes become final when:
- Delegations validated and verified  
- No higher-order governance rule blocks acceptance  
- Context is satisfied  

### 35.4.6 Federated Finality
Cross-domain truth becomes final when:
- External proofs pass verification  
- Domain mapping resolves consistently  
- No sovereignty conflict exists  

## 35.5 Finality Lifecycle

### 35.5.1 Provisional Phase
Transition is proposed, validated, verified, and evaluated — but not yet canonical.

### 35.5.2 Consensus Phase (L34)
If consensus resolves acceptably:
- Transition is ready for finalization  

If consensus defers:
- Await additional data or external proofs  

If consensus rejects:
- Finality is impossible.

### 35.5.3 Pre-Finality Safety Check
System must confirm:
- No constraint violations  
- No risk thresholds exceeded  
- No governance prohibitions  
- No causal conflicts  

### 35.5.4 Finalization Phase
Occurs when:
- Transition passes all checks  
- Provenance is updated  
- State is updated  
- Consensus acceptance is sealed  

### 35.5.5 Post-Finality Immutability
Once final:
- Transition becomes permanent record  
- History cannot be rewritten  
- Undo (L16) rewinds *from* finality but does not modify final truth  
- Recovery (L17) reconstructs finality, not sidestep it  

## 35.6 Forbidden Finality
Finality cannot be granted if:
- Identity is unverified or compromised  
- Validation fails  
- Verification fails  
- Constraints violated  
- Governance override applies  
- Transition introduces causal or temporal inconsistencies  
- Provenance incomplete  

No object or transition may enter canonical truth without satisfying all mandatory conditions.

## 35.7 Finality Ordering Rules

### 35.7.1 Temporal Ordering
No transition may be finalized before:
- Valid timestamp  
- Satisfied time windows  
- No retroactivity  

### 35.7.2 Causal Ordering
Finality must:
- Respect causal chains  
- Avoid double-finalization of mutually exclusive branches  
- Maintain system DAG structure  

### 35.7.3 Governance Ordering
Governance may:
- Preempt finality  
- Require human confirmation  
- Override or block transitions  
- Force re-verification  
- Declare emergency provisional states  

## 35.8 ADT/MAIAi Finality Rules
Agents must:
- Treat final truth as absolute  
- Never attempt to rewrite or circumvent finality  
- Always escalate when encountering conflicting states  
- Use final snapshots for deterministic reasoning  

Agents may not:
- Declare finality  
- Modify final objects  
- Act on provisional truth as if final  

## 35.9 Federated Finality Rules
Cross-domain finality requires:
- Bidirectional verification  
- Proof-of-origin and proof-of-integrity  
- Attestations of sovereignty  
- Consistency with local governance  

If conflict persists:
- Finality is deferred  
- Escalation procedures apply  

## 35.10 Observability & Reporting
System must expose:
- Finality logs  
- Finality DAG visualization  
- Divergence maps  
- Pending/provisional transitions  
- Federated finality states  
- Rejection or deferral evidence  

Auditors must reconstruct:
- Why a transition became final  
- What rules determined finality  
- What governance conditions applied  
- Whether system behaved deterministically  

## 35.11 Interaction With Other Layers
- **L11** — finality relies on cryptographic binding.  
- **L12** — ensures deterministic finality outcomes.  
- **L13** — governs legality of finalized transformations.  
- **L14** — enforces temporal finality constraints.  
- **L15** — enforces causal finality constraints.  
- **L16** — controls how finality behaves under undo.  
- **L17** — controls recovery of final truth.  
- **L18** — provenance captures finality commitment.  
- **L19** — audits finality processes.  
- **L20** — attestations required for some finalities.  
- **L21** — custody finality rules.  
- **L22** — permission implications.  
- **L23** — capability implications.  
- **L24** — accountability for finality outcomes.  
- **L25** — context-dependent finality conditions.  
- **L26** — constraint ceilings shaping finality.  
- **L27** — finality requires valid objects.  
- **L28** — finality requires verified objects.  
- **L29** — governance can preempt or authorize finality.  
- **L30** — delegation rules for finality authority.  
- **L31** — global constraints on finality.  
- **L32** — finality produces new canonical state.  
- **L33** — transitions lead into finality.  
- **L34** — consensus is the gatekeeper of finality.  

## 35.12 Invariants
1. FINALITY_IMMUTABLE — final truths cannot be rewritten.  
2. FINALITY_DETERMINISTIC — finality must yield the same result everywhere.  
3. FINALITY_TRACEABLE — fully captured in provenance.  
4. FINALITY_AUTHENTIC — based only on verified evidence.  
5. FINALITY_SAFE — must preserve system stability.  
6. FINALITY_CONTEXTUAL — governed by context and policy windows.  
7. FINALITY_ORDERED — bound to time, causality, and governance order.  

## 35.13 Informative Guidance
Finality is the backbone of trust.  
Without finality, the substrate cannot guarantee truth, safety, or compliance.  
Finality should be conservative — only transitions fully proven safe may be finalized.  
Federated finality must prioritize domain sovereignty.  
ADT/MAIAi must operate with extreme care around final objects.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

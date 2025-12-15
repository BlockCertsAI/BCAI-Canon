<!--
CANONICAL: TRUE
LAYER: L28
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L28 — Verification Rules (How the Substrate Proves Truth, Authenticity & Correctness)
Defines the canonical mechanisms for proving that identities, actions, objects, states, processes, and decisions are authentic, correct, and trustworthy. Verification provides the mathematical, cryptographic, and procedural evidence required for the Substrate to assert truth.

## 28.0 Purpose
L28 establishes the rules governing:
- What must be *proven*, not merely assumed  
- How the substrate verifies signatures, hashes, identities, states, causality, provenance, and attestations  
- How AI/ADT outputs are verified before acceptance  
- How verification differs from validation (L27)  
- How verifiable evidence becomes part of canonical state  
Verification answers the question: **“Is this true?”**

## 28.1 Scope
Verification applies to:
- Identities and credentials  
- Permissions, capabilities, and accountability claims  
- Attestations and delegations  
- Provenance and lineage structures  
- State transitions and object mutations  
- AI/ADT decisions and predictions  
- Temporal and causal correctness  
- Cross-domain or federated truth proofs  

Verification is required both before and after actions occur.

## 28.2 Core Principles
1. **Truth must be provable** — no unverifiable claim may be accepted.  
2. **Verification precedes acceptance** — nothing becomes canonical until verified.  
3. **Verification is cryptographic** — hashing, signing, proof generation.  
4. **Verification is deterministic** — the same inputs yield identical verification results (L12).  
5. **Verification produces evidence** — verifiable artifacts become part of the audit chain (L19).  
6. **Verification extends across domains** — federated trust requires cross-substrate proofs.  
7. **Verification must be minimal** — sufficient to prove correctness without overexposure.

## 28.3 Verification Object Model
Each verification event must include:

### Inputs
- Target object or claim  
- Associated identity or actor  
- Required proofs (hashes, signatures, keys, attestations)  
- Context (L25)  
- Provenance lineage (L18)  
- Temporal and causal markers (L14–L15)  

### Outputs
- Verification status (TRUE / FALSE / INDETERMINATE)  
- Verification evidence bundle  
- Hash of verification process  
- Signatures from verifiers  
- Optional zero-knowledge proof (if required)  

### Anchoring
- Timestamp  
- Causal relationship to action being verified  
- Provenance entry  

## 28.4 Types of Verification

### 28.4.1 Identity Verification
Confirms:
- Identity authenticity  
- Key ownership  
- Certificate validity  
- Non-compromise of identity  

### 28.4.2 Signature Verification
Ensures:
- All required signatures are present  
- Signatures match underlying content  
- Multi-signature thresholds are met  

### 28.4.3 Hash Verification
Checks:
- Object integrity  
- State hash correctness  
- No tampering or mutation  

### 28.4.4 Provenance Verification
Ensures:
- Complete, unbroken lineage  
- Custody correctness  
- Transformation legitimacy  
- No missing or altered lineage nodes  

### 28.4.5 Causal Verification
Confirms:
- Parent events exist  
- No causal cycles or contradictions  
- Causal chain integrity  

### 28.4.6 Temporal Verification
Ensures:
- Timestamps are valid  
- Ordering complies with L14  
- No backward time drift  

### 28.4.7 Permission & Capability Verification
Checks:
- Claim of permission matches signed record (L22)  
- Claim of capability matches structural definition (L23)  
- No forged or altered permissions  

### 28.4.8 Accountability Verification
Ensures:  
- Responsible party is correct (L24)  
- Accountability window is active  
- Responsibility chain is intact  

### 28.4.9 Constraint Verification
Ensures:  
- No constraint violation would occur (L26)  
- Safety and governance boundaries remain intact  

### 28.4.10 Attestation Verification
Confirms:
- Attestation hash is correct  
- Attestation signatures valid  
- Attestation issuer has authority (L20)  

### 28.4.11 AI/ADT Output Verification
Before any agent output is accepted:
- Verify reasoning trace  
- Verify constraint adherence  
- Verify permissions used  
- Verify capability boundaries  
- Verify context propagation  
- Verify attestations produced  
AI/ADT outputs may not be accepted without successful verification.

### 28.4.12 Cross-Substrate Verification
Confirms:  
- Correctness of federated proofs  
- Authenticity of external identities  
- Legitimacy of cross-domain context  

## 28.5 Verification Failures
If verification fails:

### Immediate Effect
- The claim or object is rejected  
- The associated action cannot proceed  
- Dependent processes must halt  

### Required Side Effects
- Failure attestation (L20)  
- Audit record (L19)  
- Provenance fork marker (L18)  
- Diagnostic context record (L25)  

### Optional Remediation
- Request new proofs  
- Request federated re-verification  
- Escalation to human review  
- Initiate risk or integrity alarms  

## 28.6 Verification in Undo (L16) and Recovery (L17)
Verification must be enforced during corrective processes:

### Undo Verification
- Verify reversibility  
- Verify undo signature authority  
- Verify undo target is consistent with lineage  

### Recovery Verification
- Verify recovered state matches canonical truth  
- Verify no unverifiable data re-enters the system  
- Verify structural invariants remain intact  

## 28.7 Verification of Autonomous Agents
Agents must:
- Submit outputs for verification  
- Accept verification failures as binding  
- Never bypass verification  
- Produce all required proofs automatically  
- Escalate if verification resources are missing  

Verification failures from agents must trigger remediation workflows.

## 28.8 Observability & Reporting
The substrate must expose tools for:
- Viewing verification chains  
- Checking signature validity  
- Inspecting proofs  
- Reviewing federated trust lines  
- Viewing AI/ADT verification traces  
- Producing verification summaries  

Auditors must reconstruct:
- How truth was proven  
- Which proofs were used  
- Whether evidence was complete  
- Whether verification aligned with policy and governance  

## 28.9 Interaction With Other Layers
- **L11** — provides signature and hash primitives.  
- **L12** — ensures deterministic verification logic.  
- **L13** — governs legality of state change being verified.  
- **L14** — ensures temporal correctness.  
- **L15** — verifies causal integrity.  
- **L16** — ensures verification applies in undo.  
- **L17** — ensures verification applies in recovery.  
- **L18** — ensures verified lineage integrates correctly.  
- **L19** — ensures verification evidence is auditable.  
- **L20** — supports attestations used in verification.  
- **L21** — verifies legitimacy of handoffs.  
- **L22** — verifies permissions supporting the action.  
- **L23** — verifies capabilities supporting the action.  
- **L24** — verifies accountability.  
- **L25** — verifies context correctness.  
- **L26** — verifies constraints are respected.  
- **L27** — validation depends on underlying verification.

## 28.10 Invariants
1. VERIFICATION_REQUIRED — nothing becomes canonical without verification.  
2. VERIFICATION_COMPETE — all required proofs must be present.  
3. VERIFICATION_TRUTHFUL — verification must be cryptographically sound.  
4. VERIFICATION_TRACEABLE — all verification events must appear in provenance.  
5. VERIFICATION_NONREPUDIABLE — results must be signed and permanent.  
6. VERIFICATION_CONTEXTUAL — verification must consider context.  
7. VERIFICATION_DETERMINISTIC — same input → same truth outcome.  

## 28.11 Informative Guidance
Verification should be lightweight when possible, heavy when required.  
Federated verification should prioritize zero-knowledge and privacy-preserving methods.  
AI/ADT verification must be strict, explainable, and consistent.  
Verification drift is a critical governance issue and must be audited regularly.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

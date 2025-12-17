<!--
CANONICAL: TRUE
LAYER: L29
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L29 — Governance Rules (How Power, Control & Decisions Are Exercised in the Substrate)
Defines the structures, authorities, boundaries, and rules that govern how decisions are made, how policies are enforced, how exceptions are handled, and how the Sovereign Substrate maintains lawful, safe, and coherent operation across all actors — human, organizational, ADT, MAIAi, and system processes.

## 29.0 Purpose
L29 establishes the canonical framework for:
- Who may govern, and under what authority  
- How governance decisions are expressed, validated, and enforced  
- How control flows between entities  
- How oversight, accountability, and compliance operate  
- How power transitions occur safely and traceably  
- How governance interacts with autonomy, risk, and cross-domain coordination  

Governance defines *who decides what*, *how decisions become binding*, and *how the substrate preserves lawful order*.

## 29.1 Scope
Governance rules apply to:
- CSR (Canonical System Regulator)  
- Architect (Execution & Enforcement Mechanism)  
- Verified governance identities  
- Human supervisory authorities  
- Cross-substrate federated governance entities  
- All ADT/MAIAi agents operating within governance windows  
- All canonical processes, events, and state changes  

Governance is substrate-wide and cannot be overridden by domain-specific rules.

## 29.2 Core Principles
1. **Authenticated Authority** — governance requires cryptographically verified identity.  
2. **Lawful Direction** — all governance actions must follow substrate law and constraints.  
3. **Traceable Power** — every governance action must appear in provenance (L18).  
4. **Non-Repudiation** — governance actors cannot deny issued directives (L20).  
5. **Causal Validity** — governance actions must respect causal order (L15).  
6. **Temporal Validity** — governance windows must be respected (L14).  
7. **Oversight Over Autonomy** — governance constrains ADT/MAIAi behavior (L26).  
8. **Fail-Safe Governance** — ambiguous cases require escalation, not silent execution.  

## 29.3 Governance Object Model
Every governance action must specify:

### Actor
- Identity (Genesis-KYC verified)  
- Governance role (CSR, Architect, domain regulator, federated authority)  
- Authority justification  

### Directive
- Action required  
- Scope and target (object, domain, flow, actor, policy)  
- Expected outcomes  
- Allowed exceptions  
- Escalation paths  

### Constraints
- Safety rules  
- Legal or regulatory rules  
- Policy windows  
- Context dependencies  

### Cryptographic Binding
- Governance hash  
- Signatures of authorized governance actors  
- Optional multi-signature for Critical governance actions  

### Anchoring
- Timestamp  
- Causal parent events  
- Provenance lineage  

## 29.4 Governance Structures

### 29.4.1 CSR (Canonical System Regulator)
CSR is the highest governance identity responsible for:
- Issuing canonical rules  
- Approving global policy changes  
- Mandating corrective actions  
- Managing federated trust and governance boundaries  

CSR decisions override all internal domain rules **within the Sovereign Substrate**.

### 29.4.2 Architect
The Architect executes governance decisions and enforces system rules:
- Validates all actions against governance policy  
- Performs remediation, override, and exception enforcement  
- Ensures system-wide safety, order, and self-healing  

The CSR governs *what*; the Architect governs *how* and *when*.

### 29.4.3 Domain Regulators
Govern verified domains or partitions:
- Interpret CSR/Architect policy  
- Enforce local rules  
- Manage domain-specific operations  

Routes of authority must be explicitly defined.

### 29.4.4 Federated Governance Partners
External or cross-substrate authorities:
- Govern only what federated agreements define  
- Must provide verifiable governance proofs  
- Cannot exceed granted governance scope  

## 29.5 Governance Powers
Governance entities may:

### 29.5.1 Issue Directives
Mandate actions across:
- State transitions  
- Permissions, capabilities, roles  
- ADT/MAIAi autonomy levels  
- Domain boundaries  
- Policy activation or suspension  

### 29.5.2 Override Behavior
Override:
- Permissions (L22)  
- Capabilities (L23)  
- Context windows (L25)  
- Constraints (L26)  
- Validation or verification *outcomes* (L27–L28)  

Governance MAY override the **result** of validation or verification in exceptional cases,  
but MUST NOT alter, bypass, or weaken the underlying validation or verification rules themselves.

Overrides must be:
- Exception-only  
- Auditable  
- Justified  
- Signed by proper authority  

### 29.5.3 Mandate Escalation
Governance may require:
- Human review  
- Additional verification  
- Additional attestations  
- Constraint tightening  
- Capability suppression  

### 29.5.4 Suspend or Revoke Authority
Governance may suspend:
- Identities  
- Permissions  
- Capabilities  
- Context propagation  
- Autonomous systems  
- Whole domains (under emergency governance)  

### 29.5.5 Initiate Recovery or Undo
Governance can:
- Trigger corrective recovery (L17)  
- Activate undo flows (L16)  
- Rebuild canonical order after anomalies  

## 29.6 Governance Decision Rules

### 29.6.1 Authority Validation
Before a governance action proceeds, the system must verify:
- Identity authenticity  
- Authority scope  
- Jurisdiction boundary  
- Delegation correctness  
- Required approvals  

### 29.6.2 Impact Analysis
Governance must compute:
- Impact on causal chains  
- Risk level  
- Downstream effects on provenance  
- Interactions with constraints  
- ADT/MAIAi behavioral shifts  

### 29.6.3 Justification Requirement
Every governance directive must include a justification attestation.

### 29.6.4 Safety Priority
Safety and system integrity *always* supersede policy convenience.

### 29.6.5 Minimal Intervention
Governance must choose the least intrusive method to restore order and correctness.

## 29.7 Governance Conflicts
If governance-level conflicts occur:

### Detection
- Inconsistent directives  
- Conflicting authorities  
- Contradictory causal flows  

### Resolution
- CSR directive overrides all non-CSR directives  
- Federated rules yield to internal governance unless explicitly negotiated  
- Architect ensures causal and temporal coherence  

### Evidence
All conflicts and resolutions must be:
- Logged  
- Provenanced  
- Auditable  

## 29.8 Governance Lifecycle

### Activation
Governance directive is issued and signed.

### Enforcement
The Architect enforces:
- Validation  
- Overrides  
- Constraint application  
- Remediation  

### Monitoring
Governance is observed for:
- Compliance  
- Emergent risks  
- ADT/MAIAi adaptation  

### Termination
Directive expires or is rescinded by proper authority.

### Archival
Directive becomes permanent part of canonical provenance.

## 29.9 Observability & Reporting
The substrate must provide:
- Governance dashboards  
- Directive lineage  
- Override history  
- Conflict resolution logs  
- ADT/MAIAi governance-boundary visualizers  
- Federated governance trace maps  

Auditors must reconstruct:
- Who governed  
- Why they governed  
- What decisions were made  
- How decisions affected substrate state  

## 29.10 Interaction With Other Layers
- **L11** — verifies governance signatures and proofs.  
- **L12** — ensures deterministic interpretation of governance rules.  
- **L13** — governs legality of governance-induced state changes.  
- **L14** — anchors governance in time windows.  
- **L15** — anchors governance in causal order.  
- **L16** — ensures governance survives or corrects undo sequences.  
- **L17** — ensures governance integrity after recovery.  
- **L18** — ties governance to provenance.  
- **L19** — enables auditability of governance actions.  
- **L20** — provides attestations required for governance authority.  
- **L21** — governs how authority is transferred.  
- **L22** — governs permissions in governance contexts.  
- **L23** — governs capabilities under governance control.  
- **L24** — governs accountability structures.  
- **L25** — governs context shifts under governance actions.  
- **L26** — constrains agent autonomy under governance.  
- **L27** — validates governance actions.  
- **L28** — verifies governance truth claims.

## 29.11 Invariants
1. GOVERNANCE_AUTHENTIC — governance must be authenticated.  
2. GOVERNANCE_TRACEABLE — all governance actions must be in provenance.  
3. GOVERNANCE_SUPREMACY — governance overrides all non-governance rules.  
4. GOVERNANCE_MINIMAL — governance intervenes only when necessary.  
5. GOVERNANCE_SAFE — governance must protect substrate stability.  
6. GOVERNANCE_ACCOUNTABLE — governance actions must be answerable.  
7. GOVERNANCE_NONREPUDIABLE — governance signatures cannot be denied.  
8. GOVERNANCE_BOUND — governance cannot exceed its jurisdiction.  

## 29.12 Informative Guidance
Governance should be predictable, explainable, and minimal.  
AI/ADT must always remain within governance windows.  
Cross-domain governance should rely on zero-knowledge proofs where possible.  
Governance drift or misalignment is a systemic risk and must be continuously monitored.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

<!--
CANONICAL: TRUE
LAYER: L21
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L21 — Handoffs (Transfer of Control, Responsibility & Custody)
Defines how control, responsibility, authority, and custody of identities, objects, processes, and domains are transferred across actors within the Sovereign Substrate, ensuring continuity, accountability, and integrity.

## 21.0 Purpose
L21 establishes the canonical rules for safe, authenticated handoffs of:
- Control over objects, domains, or processes  
- Responsibility for actions, decisions, or duties  
- Custody of data, assets, credentials, or workflows  

The purpose is to ensure that every transfer is:
- Authenticated  
- Authorized  
- Traceable  
- Non-repudiable  
- Temporally and causally valid  
- Fully accountable in provenance and audit chains  

Handoffs are foundational to multi-actor, multi-domain coordination without trust assumptions.

## 21.1 Scope
L21 applies to:
- Human → human transfers  
- Human → ADT or MAIAi transfers  
- ADT/MAIAi → human transfers  
- System → system and domain → domain transfers  
- Cross-substrate, cross-jurisdiction, and federated handoffs  
- All Critical objects, decisions, and credentials  
- All processes requiring continuity or chain-of-custody  

L21 defines substrate-level handoff rules, independent of domain-specific meanings.

## 21.2 Core Principles
1. **No implicit handoffs** — all transfers must be explicit.  
2. **Handoffs must be authenticated** — both parties must provide verifiable identity.  
3. **Authority must be proven** — the sender must have the right to transfer; the receiver must have the right to receive.  
4. **Custody and responsibility must be traceable** — provenance chains must reflect handoff transitions.  
5. **Continuity must be preserved** — transfers cannot orphan processes or objects.  
6. **Handoffs must be non-repudiable** — neither party can deny participation.  
7. **Handoffs must be causally valid** — ordering must follow L15.  
8. **Handoffs must survive rollback and recovery** — L16–L17 invariants must be maintained.

## 21.3 Handoff Object Model
A canonical handoff event must include:

### Sender Information
- Identity (Genesis-KYC rooted)  
- Role and authorization scope  
- Proof of authority to transfer  

### Receiver Information
- Identity and trust classification  
- Role and authorization to accept  
- Optional constraints or limited-scope acceptance  

### Transfer Payload
- Object(s), duty, domain, or authority being transferred  
- Current state hash or signature  
- Context metadata (jurisdiction, domain, risk classification)

### Cryptographic Bindings
- Sender signatures  
- Receiver signatures  
- Handoff hash (object + intent + state)  
- Multi-party signature set for Critical transfers  

### Temporal & Causal Anchoring
- Timestamp (L14)  
- Causal parents (L15)  
- Expiration or revocation rule if applicable  

### Chain-of-Custody Update
- New custodian assignment  
- Record of previous custodian  
- Pointer to provenance lineage (L18)

## 21.4 Types of Handoffs

### 21.4.1 Custody Handoffs
Transfer of physical or digital custody of:
- Data  
- Vault objects  
- Credentials or keys  
- Tokens or assets  
- Domain certificates  
Custody handoffs must update provenance (L18).

### 21.4.2 Control Handoffs
Transfer of execution control over:
- Processes  
- Workflows  
- ADT or MAIAi operational scopes  
- BAINCA workloads  
- Governance routines  

### 21.4.3 Responsibility Handoffs
Transfer of duty, obligation, or accountability:
- Regulatory compliance responsibilities  
- Operational oversight  
- Decision-making authority  

### 21.4.4 Domain Handoffs
Transfer of authority over:
- Verified domains  
- Substrate partitions  
- Organizational boundaries  
- Cross-jurisdictional or federated trusts  

### 21.4.5 AI/ADT Handoffs
Transfer between humans and ADT/MAIAi:
- Control  
- Custody  
- Execution authority  
- Decision space  
Each must include traceable justification and scope limits.

## 21.5 Handoff Validation Rules
A handoff must be rejected unless ALL conditions below are met:

1. **Sender Authorization**  
   Sender must be cryptographically verified and authorized for the asset or role.

2. **Receiver Authorization**  
   Receiver must be eligible and authorized to accept the handoff.

3. **Object Integrity**  
   Object or responsibility must have complete provenance (L18).

4. **Causal Correctness**  
   Handoff must follow valid event ordering (L15).

5. **Temporal Validity**  
   Timestamp must align with L14 constraints.

6. **Non-Repudiation**  
   Both sender and receiver signatures must validate under L11.

7. **Scope Matching**  
   Handoff scope must not exceed either party’s domain authority.

8. **Conflict-Free Transfer**  
   No conflicting active custodians or controllers may remain.

## 21.6 Handoff Lifecycle

### Initiation
Sender constructs the handoff event with all required fields.

### Acceptance
Receiver signs acceptance, closing the cryptographic loop.

### Activation
System updates:
- Custody  
- Authority  
- Provenance  
- State ownership  

### Optional Conditions
Handoffs may include:
- Timed validity  
- Conditional responsibilities  
- Revocation windows  
- Post-transfer reporting requirements  

### Revocation
Handoffs may be revoked if:
- Sender authority was invalid  
- Receiver became ineligible  
- Policy change mandates revocation  
- Handoff contradicts canonical state  

Revocation must itself be a canonical event referencing the original handoff.

## 21.7 Observability & Reporting
The substrate must provide:
- Handoff history viewers  
- Custody-chain visualization  
- Control flow lineage  
- Authority maps  
- AI/ADT responsibility transfer logs  
- Cross-substrate handoff trace maps  

Auditors must be able to reconstruct:
- Who transferred what  
- When it occurred  
- Why it occurred  
- What state changed as a result  
- Whether all validation rules were satisfied  

## 21.8 Interaction With Other Layers
- L11 provides signature and hash integrity.  
- L12 ensures deterministic replay of handoff sequences.  
- L13 ensures transfer legality relative to mutability rules.  
- L14 ensures temporal validation.  
- L15 ensures causal validity.  
- L16 ensures handoffs survive rollback.  
- L17 ensures handoffs persist through recovery.  
- L18 ensures provenance reflects handoff transitions.  
- L19 ensures handoffs remain fully auditable.  
- L20 asserts truth and authority behind each handoff.

## 21.9 Invariants
1. HANDOFF_EXPLICIT — no implicit or hidden transfers.  
2. HANDOFF_AUTHENTIC — sender and receiver identities must be cryptographically validated.  
3. HANDOFF_TRACEABLE — all handoffs must appear in provenance and audit chains.  
4. HANDOFF_ATOMIC — either the handoff fully completes or it does not occur.  
5. HANDOFF_NONREPUDIABLE — both parties must sign.  
6. HANDOFF_CASCADE_SAFE — downstream effects must remain causally consistent.

## 21.10 Informative Guidance
Handoffs should be used to formalize:
- Role transitions  
- Operational coverage shifts  
- Human-to-AI supervisory cycles  
- Multi-party workflow continuity  
- Compliance responsibility changes  
- Cross-domain hierarchical or lateral transfers  

Clear, authenticated handoffs strengthen accountability and resilience across federated environments.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

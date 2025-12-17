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
Transfer of custody of data, vault objects, credentials, tokens, assets, or domain certificates.  
Custody handoffs MUST update provenance (L18).

### 21.4.2 Control Handoffs
Transfer of execution control over processes, workflows, ADT/MAIAi scopes, BAINCA workloads, or governance routines.

### 21.4.3 Responsibility Handoffs
Transfer of duty or accountability, including regulatory, operational, or decision authority.

### 21.4.4 Domain Handoffs
Transfer of authority over verified domains, substrate partitions, organizational boundaries, or federated trusts.

### 21.4.5 AI / ADT Handoffs
Transfers between humans and ADT/MAIAi of control, custody, execution authority, or decision space, with explicit scope limits and justification.

## 21.5 Handoff Validation Rules
A handoff MUST be rejected unless all conditions below are met:

1. **Sender Authorization** — sender is verified and authorized.  
2. **Receiver Authorization** — receiver is eligible and authorized.  
3. **Object Integrity** — complete provenance exists (L18).  
4. **Causal Correctness** — valid ordering (L15).  
5. **Temporal Validity** — conforms to L14.  
6. **Non-Repudiation** — both signatures validate (L11).  
7. **Scope Matching** — scope does not exceed authority.  
8. **Conflict-Free Transfer** — no parallel custodians remain.

## 21.6 Handoff Lifecycle

### Initiation
Sender constructs the canonical handoff event.

### Acceptance
Receiver signs acceptance.

### Activation
Custody, authority, provenance, and state ownership are updated.

### Optional Conditions
Timed validity, conditional scope, revocation windows, or reporting duties may apply.

### Revocation
Revocation requires a canonical event referencing the original handoff and valid authority justification.

## 21.7 Observability & Reporting
The substrate MUST expose:
- Handoff history viewers  
- Custody-chain visualization  
- Control and authority maps  
- AI/ADT responsibility transfer logs  
- Cross-substrate handoff traces  

Auditors MUST be able to reconstruct full handoff context and outcomes.

## 21.8 Interaction With Other Layers
- **L11** signatures and hashes  
- **L12** deterministic replay  
- **L13** mutability legality  
- **L14** temporal validation  
- **L15** causal correctness  
- **L16–L17** rollback and recovery  
- **L18** provenance updates  
- **L19** auditability  
- **L20** authority and truth attestations  

## 21.9 Invariants
1. **HANDOFF_EXPLICIT**  
2. **HANDOFF_AUTHENTIC**  
3. **HANDOFF_TRACEABLE**  
4. **HANDOFF_ATOMIC**  
5. **HANDOFF_NONREPUDIABLE**  
6. **HANDOFF_CASCADE_SAFE**

## 21.10 Real-World Capability Enabled by Handoffs

Handoffs enable **formal transfer of responsibility without institutional intermediaries**.

They allow:
- Governments to transfer regulatory authority or case ownership with provable continuity.
- Enterprises to rotate operational control, keys, or compliance duties without gaps or ambiguity.
- Supply chains to maintain uninterrupted custody across jurisdictions and organizations.
- AI systems to assume and relinquish authority under explicit human governance.
- Incident response teams to transfer control during crises without losing accountability.

Handoffs convert transitions of power and responsibility into **cryptographically provable events**.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

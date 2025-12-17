<!--
CANONICAL: TRUE
LAYER: L20
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L20 — Attestations (Cryptographic Statements of Truth & Authority)
Defines how Canon produces, verifies, and preserves cryptographic statements that assert truth, authority, validity, compliance, and intent across all layers of the Sovereign Substrate.

## 20.0 Purpose
L20 provides the formal structure for attestations — authenticated, tamper-evident statements that express:
- Truth about an event or object  
- Authority of an actor or system component  
- Compliance with rules, policy, or law  
- State validity at a specific moment  
- Assertions required for governance, verification, or interoperability  

Attestations form the substrate’s universal trust primitive.

## 20.1 Scope
Attestations apply to:
- All identities (human, organizational, ADT, MAIAi, system actors)  
- All events and state transitions  
- All provenance and lineage objects  
- All cross-substrate interactions  
- All governance actions, certifications, endorsements, and approvals  
- All compliance or regulatory checkpoints  
- All AI or ADT outputs that require verification  

L20 specifies the structure, generation, validation, and lifecycle of attestations.

## 20.2 Core Principles
1. **Attestations must be cryptographically provable.**  
2. **Attestations must bind identity, intent, and truth into a single immutable statement.**  
3. **Attestations must survive rollback and recovery.**  
4. **Attestations must be non-repudiable.**  
5. **Attestations must remain verifiable for the lifetime of the Canon.**  
6. **Attestations must be minimal: sufficient to prove truth without revealing private data.**

## 20.3 Attestation Object Model
Every attestation must contain:

### Identity Proof
- Issuer identity (verified via Genesis-KYC identity root)  
- Key material and certificate references  
- Role classification (human, ADT, MAIAi, CSR, Architect, federated partner)

### Statement of Truth
- What is being asserted  
- Why it is true  
- Which event, object, or state it refers to  
- Version or revision number, if applicable  

### Authority Justification
- Why the issuer is permitted to make this claim  
- Policy or governance rules invoked  
- Scope of effect (local, domain-wide, substrate-wide)

### Cryptographic Binding
- Attestation hash  
- Event or object hash  
- Issuer signatures  
- Optional multi-signature set  
- Integrity chain pointers  

### Temporal & Causal Anchoring
- Timestamp (L14)  
- Causal parents (L15)  
- Expiration or renewal rule (if applicable)

### Optional Privacy Layer
- Redacted content proofs  
- Zero-knowledge assertions  
- Selective disclosure keys  
- Differential exposure masks  

## 20.4 Types of Attestations

### 20.4.1 Truth Attestations
Assert factual correctness.

### 20.4.2 Authority Attestations
Assert permission, delegation, or jurisdiction.

### 20.4.3 Compliance Attestations
Assert regulatory, policy, or standards compliance.

### 20.4.4 Validity Attestations
Assert correctness of state, credentials, or configuration.

### 20.4.5 Cross-Substrate Attestations
Assert authenticity of federated or external interactions.

### 20.4.6 AI / ADT Attestations
Assert decision correctness and policy alignment.

## 20.5 Attestation Generation Rules
Attestations must:
1. Be generated only by authorized identities.  
2. Include complete cryptographic binding to the asserted object.  
3. Include correct temporal stamps (L14).  
4. Reference causal parents where required (L15).  
5. Comply with mutability, recovery, and undo rules (L13–L17).  
6. Use approved signature and hashing primitives (L11).  
7. Be stored as immutable canonical events.  

ADT and MAIAi must generate attestations for autonomous actions requiring accountability.

## 20.6 Attestation Validation Rules
Validation must confirm issuer authenticity, cryptographic correctness, authority scope, temporal validity, causal consistency, and cross-substrate integrity. Invalid attestations must be rejected or quarantined.

## 20.7 Attestation Lifecycle
Creation → Active Use → Expiration / Renewal → Revocation.  
Expired or revoked attestations remain historically verifiable but lose active authority.

## 20.8 Attestation Revocation Rules
Revocation must reference the original attestation, include authority justification, produce cryptographic proof, and trigger downstream causal reevaluation (L15).

## 20.9 Observability & Reporting
The system must expose attestation viewers, verifiers, trust lineage inspectors, delegation maps, revocation queries, and privacy-preserving proof tools.

## 20.10 Layer Interactions
- **L11** cryptographic primitives  
- **L12** deterministic revalidation  
- **L13** mutability enforcement  
- **L14** temporal correctness  
- **L15** causal integrity  
- **L16–L17** undo and recovery survivability  
- **L18** provenance integration  
- **L19** auditability  

## 20.11 Invariants
1. **ATTESTATION_IMMUTABLE**  
2. **BINDING_CORRECT**  
3. **NONREPUDIATION**  
4. **TRACEABLE**  
5. **REVOCATION_VISIBLE**  
6. **LIFETIME_VERIFIABLE**

## 20.12 Informative Guidance
Attestations should be lightweight, privacy-preserving, and multi-signature for high-stakes contexts. AI/ADT systems should emit attestations automatically for consequential decisions.

## 20.13 Real-World Capability Enabled by Attestations

Attestations enable **machine-verifiable trust without institutional intermediaries**.

They allow:
- Regulators to verify compliance cryptographically instead of relying on reports.
- Enterprises to prove authorization, approval, and policy adherence in real time.
- Courts to evaluate claims, responsibility, and authority with tamper-proof evidence.
- Governments to issue licenses, permits, and credentials that are instantly verifiable.
- AI systems to operate under enforceable accountability, not opaque inference.

Attestations convert trust from a social assumption into a **portable, cryptographic fact**.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

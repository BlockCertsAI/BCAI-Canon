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
Assert factual correctness, such as:
- “Object X has not been modified since event Y.”  
- “Identity Z validated this data at time T.”  

### 20.4.2 Authority Attestations
Assert permission, delegation, or jurisdiction, such as:
- “Actor A is authorized to perform action B within domain C.”  

### 20.4.3 Compliance Attestations
Assert rules, standards, or policies were met:
- Regulatory compliance  
- Internal policy compliance  
- AI/ADT alignment compliance  

### 20.4.4 Validity Attestations
Assert correctness of:
- State  
- Configuration  
- Credentials  
- Domain boundaries  

### 20.4.5 Cross-Substrate Attestations
Assert authenticity of:
- Federation trust lines  
- External identity proofs  
- Inter-jurisdictional transfers  

### 20.4.6 AI/ADT Attestations
Assert:
- Decision trace correctness  
- Alignment with policy  
- Adherence to ADT/MAIAi integrity rules  

## 20.5 Attestation Generation Rules
Attestations must:
1. Be generated only by authorized identities.  
2. Include complete cryptographic binding to the asserted object.  
3. Include correct temporal stamps (L14).  
4. Reference causal parents where required (L15).  
5. Comply with mutability, recovery, and undo rules (L13–L17).  
6. Use approved signature and hashing primitives (L11).  
7. Be stored as immutable canonical events.  

ADT and MAIAi must generate attestations for any autonomous action requiring auditability.

## 20.6 Attestation Validation Rules
Validation must confirm:
- Authenticity of issuer identity  
- Correctness of signatures and hash bindings  
- Integrity of referenced objects or events  
- Authority of issuer to make the claim  
- Temporal validity and expiration rules  
- Causal consistency  
- Cross-substrate verification, if relevant  
Invalid or unverifiable attestations must be rejected or quarantined.

## 20.7 Attestation Lifecycle
### Creation
Issued at event time or state checkpoint.

### Active State
Used for:
- Verification  
- Governance decisions  
- AI/ADT enforcement  
- Compliance workflows  
- Federation trust chains  

### Expiration or Renewal
Some attestations may expire:
- Time-based  
- Policy-based  
- Revocation-based  

Expired attestations remain historically valid but lose active authority.

### Revocation
Attestations may be revoked if:
- Issuer key compromised  
- Policy changes  
- False or invalid claim discovered  

Revocation must itself produce a canonical revocation attestation.

## 20.8 Attestation Revocation Rules
Revocation must:
- Reference the original attestation directly  
- Include authority justification  
- Provide cryptographic proof of revocation  
- Trigger downstream causal reevaluation (L15)  
- Update validation rules for any dependent states  

Revoked attestations remain in history but are marked non-authoritative.

## 20.9 Observability & Reporting
The system must expose:
- Attestation viewers  
- Signature and hash verifiers  
- Trust lineage inspectors  
- Delegation and authority maps  
- Zero-knowledge proof validators  
- Revocation status queries  

Auditors must be able to reconstruct:
- Attester’s identity  
- Why an attestation was issued  
- Whether it is still valid  
- What states depend on it  

## 20.10 Layer Interactions
- L11 supplies cryptographic primitives.  
- L12 ensures deterministic revalidation.  
- L13 ensures attestation-related objects follow mutability rules.  
- L14 ensures time and validity correctness.  
- L15 ensures attestation causal links remain valid.  
- L16 ensures attestations survive undo/compensation sequences.  
- L17 ensures attestations remain authoritative after recovery.  
- L18 ensures attestations integrate with provenance and lineage.  
- L19 ensures attestations remain verifiable during audits.

## 20.11 Invariants
1. ATTESTATION_IMMUTABLE — once issued, cannot change.  
2. BINDING_CORRECT — must always bind correctly to subject object/event.  
3. NONREPUDIATION — issuer cannot deny having issued it.  
4. TRACEABLE — all attestations must appear in provenance chains.  
5. REVOCATION_VISIBLE — revocation must be globally detectable.  
6. LIFETIME_VERIFIABLE — attestations must remain verifiable forever.

## 20.12 Informative Guidance
Attestations should be lightweight but expressive. Zero-knowledge variants are preferred for privacy-sensitive domains. Multi-signature attestations should be used for high-stakes governance. AI/ADT systems should generate attestations automatically for all consequential decisions.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

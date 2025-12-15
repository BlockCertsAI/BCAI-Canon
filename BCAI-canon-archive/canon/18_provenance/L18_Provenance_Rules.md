<!--
CANONICAL: TRUE
LAYER: L18
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L18 — Provenance Rules (Origin, Lineage & Traceability)
Defines how Canon establishes, verifies, and preserves the origin, lineage, and traceability of all identities, data, actions, and artifacts within the Sovereign Substrate.

## 18.0 Purpose
L18 ensures that everything inside the Sovereign Substrate — identities, events, data objects, artifacts, ADT actions, MAIAi decisions, Architect policies, BAINCA workloads — has a verifiable origin and an unbroken lineage. It guarantees authenticity (every object has a proven source), accountability (nothing exists without attributable origin), traceability (full reconstruction from creation to present), and tamper-evidence (any break or mutation is visible).

## 18.1 Scope
L18 applies to all identities, all canonical events, all objects stored or managed in Vaults, SVS, ADT contexts, or distributed clusters, all cross-substrate interactions, all credentials, tokens, certificates, and all governance actions. L18 defines structural provenance rules, not business semantics.

## 18.2 Core Principles
1. Every object has an authenticated origin.  
2. Lineage is immutable and can only grow forward.  
3. Provenance must be complete or the object is invalid.  
4. All origin and lineage steps must be cryptographically verifiable.  
5. Traceability must be lossless from origin to present state.

## 18.3 Provenance Object Model
Each canonical object must contain:
- Origin Record: creator identity (Genesis-KYC), timestamp, origin hash, signature.  
- Lineage Record: ordered list of transformations, each with event ID, parent references, dependency type, and signatures.  
- Custody Record: full chain-of-custody including human, ADT, MAIAi, or system actors.  
- Traceability Index: bidirectional pointers, cross-substrate proofs, optional privacy-preserving routing proofs.  
Missing any required component renders the object noncanonical.

## 18.4 Origin Rules
### 18.4.1 Identity Requirement
The creator must be a verified human identity, a verified ADT or MAIAi identity, a CSR/Architect identity, or a certified federated anchor identity. Anonymous origins are prohibited.

### 18.4.2 Creation Event Requirements
A creation event must declare the object type, intent metadata, object hash, required signatures, causal parent references when applicable, and must bind the object to the Sovereign Substrate’s trust boundary.

### 18.4.3 Immutable Origin Binding
Origin information must never change and must survive rollback (L16) and recovery (L17).

## 18.5 Lineage Rules
### 18.5.1 Completeness
Canon must be able to reconstruct: Origin → All Transformations → Present State. The chain must be connected, acyclic (L15), and cryptographically sealed (L11).

### 18.5.2 Continuity
Each transformation event must reference parents, declare dependency type (L15), comply with mutability (L13) and temporal legality (L14). Any break invalidates the object.

### 18.5.3 Mutability
Lineage can only extend forward. Historical lineage cannot be rewritten.

### 18.5.4 Derived Objects
Derivations must declare derivation type (CLONE_OF, TRANSFORMATION_OF, etc.), must preserve ancestry, and must annotate lossy or irreversible transformations.

## 18.6 Traceability Rules
### 18.6.1 Bidirectional Traceability
The provenance system must support backward tracing (present → origin) and forward tracing (origin → all derivatives, custody transitions, and effects).

### 18.6.2 Time-Indexed Traceability
Traceability must include timestamps, logical clocks, and cross-substrate ordering proofs.

### 18.6.3 Cross-Substrate Traceability
Federation events must carry federated identity proofs, bridge provenance markers, routing authenticity proofs, and jurisdiction metadata.

## 18.7 Custody Rules
All custody transitions must be authenticated, must record issuer and receiver identities, must include custody hash-chain validation, and must trigger evaluation for Critical objects under L15 and L16. Automated ADT/MAIAi custody actions must remain fully traceable.

## 18.8 Provenance Validation
Before object acceptance, Canon must validate:
1. Origin authenticity  
2. Origin signatures and hashes  
3. Complete lineage chain  
4. Stepwise integrity  
5. Causal correctness (L15)  
6. Temporal correctness (L14)  
7. Custody correctness  
8. Traceability completeness  
9. Cross-substrate validity  
Objects failing validation must be rejected, deferred, or forwarded to recovery (L17).

## 18.9 Observability & Reporting
The system must expose complete lineage graphs, hash proofs, custody timelines, derivation maps, and cross-substrate movement logs. Auditors must be able to replay lineage, obtain evidence bundles, view noncanonical forks, and request privacy-preserving proofs.

## 18.10 Layer Interactions
L11 supplies signature and hash primitives.  
L12 ensures deterministic reconstruction.  
L13 defines transformation legality.  
L14 controls temporal correctness.  
L15 ensures causal chain integrity.  
L16 preserves provenance under rollback.  
L17 preserves provenance under recovery.  
L18 builds on all prior layers and cannot be weakened.

## 18.11 Invariants
1. ORIGIN_IMMUTABLE — origin cannot change.  
2. LINEAGE_COMPLETE — all steps from origin to present must exist.  
3. TRACEABILITY_LOSSLESS — no gaps in backward or forward traceability.  
4. NO_ANONYMOUS_OBJECTS — all objects must have a verifiable creator.  
5. PROVENANCE_CHAIN_VALID — every lineage step satisfies L11–L17.

## 18.12 Informative Guidance
Provenance should be visualized as a DAG when possible. Privacy rules may redact content but never provenance structure. High-security contexts should use multi-signature origins. Provenance should be exportable for external verification.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

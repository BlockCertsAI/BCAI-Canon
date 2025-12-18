<!--
CANONICAL: TRUE
LAYER: L01
AUTO-TOC: ENABLED
VERSION: 1.1
PURPOSE: Canon rule file for the Sovereign Substrate’s Identity Layer.
NOTES:
- Do not remove this header.
- This file defines canonical rules governing identity establishment,
  identity-bound state transitions, identity invariants, identity integrity,
  and explicit exclusion of credential-based identity models.
-->

# L01 — Identity Layer (Genesis Identity)

The Identity Layer establishes the Sovereign Substrate’s root identity model.
All sovereign, organizational, delegated, or machine identities derive
their existence, authority, and provability from the rules defined here.

Identity is the first canonical requirement of the Sovereign Substrate.
Every authenticated entity participating in the substrate MUST originate
from a provable, cryptographically bound identity established at L01.

Identity is not an application-level concept.
It is a substrate-level canonical state that governs all authenticated
operations defined at higher layers.

---

## 1. Identity Establishment

Identity establishment is the process by which an entity becomes a
recognized actor within the Sovereign Substrate.

Identity establishment MUST:

- Bind a real-world or verifiable logical entity to a canonical identity record.
- Produce an immutable identity root hash.
- Assign a unique Substrate Identity Key (SIK).
- Produce an Identity Genesis Event recorded canonically.
- Establish the initial set of identity invariants.
- Seal the identity state with a Canonical Sealing Rule (CSR-L01).

Once established:

- Identity cannot be deleted.
- Identity cannot be anonymized.
- Identity cannot be overwritten.
- Identity MAY evolve only through canonical mutation rules (see §5).

The substrate MUST reject any identity request that cannot be validated
against real-world verification systems or structured verification sources.

---

## 2. Identity Invariants (Non-Mutable Properties)

The following MUST remain invariant for the lifetime of an identity:

1. **Global uniqueness** — Every identity MUST have exactly one SIK.
2. **Non-repudiation** — Identity operations MUST be cryptographically attributable.
3. **Canonical provenance** — Identity MUST be established through a recognized verification source.
4. **Traceable lineage** — All mutations, delegations, and transitions MUST be provably linked to the identity root.
5. **Immutable genesis** — Identity creation time, method, and CSR-L01 signature MUST remain immutable.

These invariants form the root of all authenticated operations at higher layers.

---

## 3. Explicit Exclusion of Credential-Based Identity Models

The Sovereign Substrate does NOT implement identity through credentials.

The following models are explicitly excluded at the canonical level:

- Issuer-controlled credentials
- Portable credential artifacts
- Presentation-based access using static or semi-static proofs
- Credential possession as a substitute for authenticated execution
- Identity verification through third-party credential validation

Identity within the Sovereign Substrate is NOT:

- A credential
- A token
- A certificate
- A document
- An issuer-dependent artifact

No action, access, or authority MAY be granted through credential
presentation alone.

All authority derives exclusively from:

- A canonical identity established at genesis
- Cryptographic proof bound to that identity
- Deterministic validation enforced before execution
- Canonical state transitions sealed through CSR-L01

Any system, process, or integration that attempts to introduce
credential-based identity semantics MUST be rejected as non-canonical.

---

## 4. Identity-Bound Operations

All canonical events MUST bind to an identity in one of the following roles:

### 4.1 Actor  
The entity responsible for initiating a canonical event.

### 4.2 Subject  
The entity whose state is affected by the canonical event.

### 4.3 Steward  
An entity authorized to maintain or manage identity-bound resources.

### 4.4 Delegated Actor  
A downstream identity operating under limited authority granted through
canonical delegation (§6).

Every event MUST include:

- Actor SIK
- Actor cryptographic signature
- Identity verification hash
- CSR lineage reference

Events lacking these MUST be rejected at validation time.

---

## 5. Identity Mutation Rules (Controlled State Changes)

Identity MAY evolve through mutation events, but only under strict rules.

Mutation events MUST:

- Reference the identity’s root hash.
- Pass CSR-L01 validation.
- Maintain all invariants defined in §2.
- Preserve provable lineage and chain-of-custody metadata.
- Be replayable and deterministic.

Permitted mutations include:

- Updating verified attributes.
- Adding authentication factors.
- Revoking compromised authentication factors.
- Extending identity trust scopes.

Prohibited mutations include:

- Changing identity provenance.
- Resetting or cycling identity lineage.
- Removing identity existence.
- Creating ambiguity between two identities.

Any mutation request violating these rules MUST be rejected.

---

## 6. Delegated Identity Rules

Delegated identity allows an identity to authorize another identity to act
within a constrained scope.

Delegation MUST:

- Be explicitly granted.
- Define authority limits.
- Be cryptographically sealed.
- Reference the delegating identity’s SIK.
- Define a deterministic expiration time.

Delegation MUST NOT:

- Transfer genesis rights.
- Modify identity provenance.
- Circumvent authentication requirements.

All delegations MUST be revocable through canonical mutation.

---

## 7. Temporal Identity Rules

Identity exists within canonical time.

All identity temporal proofs MUST be:

- Deterministic
- Replayable
- Verifiable
- Immutable once sealed

Temporal mutations MUST be rejected if they:

- Conflict with prior sealed timeframes
- Attempt retroactive alteration
- Introduce ambiguity into lineage

---

## 8. Identity Sealing Rules (CSR-L01)

A valid CSR-L01 seal MUST:

- Include the SIK
- Include the identity root hash
- Bind the event to canonical time
- Include the actor’s cryptographic signature
- Produce a unique canonical event hash

Identity operations lacking a valid CSR-L01 MUST be rejected.

---

## 9. Deterministic Identity Validation

All identity validation MUST:

- Be environment-independent
- Produce identical results across implementations
- Be replayable from genesis
- Terminate deterministically
- Fail deterministically when invariants are violated

---

## Result

Identity at L01 is a **canonical execution primitive**, not a credential.
It is precise, enforceable, non-transferable, and provably correct.

All authenticated execution within the Sovereign Substrate depends on this layer.

---

Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

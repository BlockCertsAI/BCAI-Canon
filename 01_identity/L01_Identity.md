<!--
CANONICAL: TRUE
LAYER: L1
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

<!--
CANONICAL: TRUE
LAYER: L01
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for the Sovereign Substrate’s Identity Layer.
NOTES:
- Do not remove this header.
- This file defines canonical rules governing identity establishment,
  identity-bound state transitions, identity invariants, and identity
  integrity constraints within the Sovereign Substrate.
-->

# L01 — Identity Layer (Genesis Identity)

The Identity Layer establishes the substrate’s root identity model.
All sovereign, organizational, delegated, or machine identities derive
their existence, authority, and provability from the rules defined here.

Identity is the first canonical requirement of the Sovereign Substrate.
Every authenticated entity participating in the substrate must originate
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
- Identity MAY evolve through canonical mutation rules (see §4).

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

## 3. Identity-Bound Operations

All canonical events MUST bind to an identity in one of the following roles:

### 3.1 Actor
The entity responsible for initiating a canonical event.

### 3.2 Subject
The entity whose state is affected by the canonical event.

### 3.3 Steward
An entity authorized to maintain or manage identity-bound resources.

### 3.4 Delegated Actor
A downstream identity operating under limited authority granted through
canonical delegation (§5).

Every event MUST include:

- Actor SIK
- Actor cryptographic signature
- Identity verification hash
- CSR lineage reference

Events lacking these MUST be rejected at validation time.

---

## 4. Identity Mutation Rules (Controlled State Changes)

Identity may evolve through mutation events, but only under strict rules:

Mutation events MUST:

- Reference the identity’s root hash.
- Pass CSR-L01 validation.
- Maintain all invariants defined in §2.
- Preserve provable lineage and chain of custody metadata.
- Be replayable and deterministic.

Permitted mutations include:

- Updating verified attributes (e.g., name change, organizational role).
- Adding authentication factors (keys, hardware proofs, biometrics).
- Revoking compromised authentication factors.
- Extending identity trust scopes.

Prohibited mutations include:

- Changing identity provenance.
- Resetting or cycling identity lineage.
- Removing identity existence.
- Creating ambiguity between two identities.

Any mutation request violating these rules MUST be rejected.

---

## 5. Delegated Identity Rules (DAOs, Agents, Processes)

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

Examples of valid delegated identities:

- A machine agent acting on behalf of a user.
- An organizational role acting within a defined scope.
- A process identity executing scheduled tasks.

All delegations MUST be revocable through canonical mutation.

---

## 6. Cross-Substrate Identity Embedding

Identity MUST be portable across Sovereign Substrate instances through:

- Canonical identity export frames.
- Identity embedding proofs.
- Cross-substrate CSR reference linkage.

Cross-substrate identity MUST preserve:

- Identity invariants (§2)
- Genesis provenance
- Delegation constraints
- CSR lineage integrity

Identity MUST NOT be duplicated across substrates.
A derived identity MUST reference its upstream canonical origin.

---

## 7. Temporal Identity Rules

Identity exists within canonical time.

Time-bounded constraints include:

- Delegation expiration
- Key rotation windows
- Identity attribute validity periods

All identity temporal proofs MUST be:

- Deterministic
- Replayable
- Verifiable
- Immutable once sealed

Temporal mutations MUST be rejected if they:

- Conflict with prior sealed timeframes
- Attempt to retroactively alter identity activity
- Introduce ambiguity into identity lineage

---

## 8. Identity Sealing Rules (CSR-L01)

CSR-L01 defines the sealing requirements for all identity operations.

A valid CSR-L01 seal MUST:

- Include the SIK
- Include the identity root hash
- Bind the event to canonical time
- Include the actor’s cryptographic signature
- Include the validation signature of the identity steward (if applicable)
- Produce a unique canonical event hash

A CSR-L01 seal MUST be generated for:

- Identity creation
- Identity mutation
- Delegation creation or revocation
- Key additions or revocations

Identity operations lacking a valid CSR-L01 MUST be rejected.

---

## 9. Deterministic Identity Validation

All identity validation MUST:

- Be environment-independent
- Produce identical results across implementations
- Be replayable from genesis
- Terminate deterministically
- Fail deterministically when invariants are violated

Validation MUST reject:

- Ambiguous identities
- Duplicate SIKs
- Incomplete lineage records
- Invalid CSR-L01 seals
- Non-deterministic mutation requests

---

## Result

Identity established at L01 serves as the foundation for all sovereign,
organizational, and system identities throughout the Sovereign Substrate.

Only identity operations that are:

- Deterministic  
- Constraint-bounded  
- Replayable  
- Environment-independent  

ARE permitted to affect canonical state at L01.

Identity is not “best effort.”
Identity is **precise, enforceable, and provably correct**, forming the
foundation upon which all authenticated execution depends.

---

## Real-World Capability Closure (Non-Normative)

The Identity Layer enables real-world systems to eliminate fraud,
impersonation, and ambiguity at the root of digital interaction.

When enforced as defined in L01, this layer makes the following
capabilities possible **by construction**, not by policy:

- One-time, lifetime identity verification without repeated KYC cycles
- Elimination of fake accounts, bots, and Sybil attacks at the substrate level
- Cryptographically provable attribution for every action, message, or transaction
- Delegated machine agents (AI, automation, devices) acting with bounded authority
- Portable identity usable across governments, enterprises, healthcare, finance, and voting systems
- Audit-grade identity trails suitable for regulators without exposing private data
- Secure replacement of passwords, usernames, and centralized SSO systems
- Identity-safe AI execution where every model action is attributable and reversible

In real-world terms, L01 allows societies and institutions to
**trust who is acting without trusting the platform they are acting on**.

This layer transforms identity from a revocable service
into a permanent, user-owned, cryptographically enforced foundation
for the authenticated internet.

---

Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

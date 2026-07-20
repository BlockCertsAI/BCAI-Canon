<!--
CANONICAL: UNDER_ENGINEERING_REVIEW
LAYER: L01
AUTO-TOC: ENABLED
VERSION: 2.0
PURPOSE: Canon rule file for the Sovereign Substrate’s Identity Layer.
NOTES:
- Do not remove this header.
- This file defines canonical rules governing identity establishment,
  identity-bound state transitions, identity invariants, identity integrity,
  key custody, recovery, and the relationship between identity and credentials.
- v2.0: Rewritten to conform to confirmed platform behavior. Changes:
  (1) §1 establishment flow corrected to the actual genesis sequence.
  (2) §3 narrowed — credentials do not ESTABLISH identity, but authenticated
      credential products MAY carry scoped authority derived from identity.
      The prior blanket exclusion was incorrect.
  (3) §4 added — key custody.
  (4) §6 added — recovery and continuity (previously absent).
  (5) §2/§7 amended to permit SIK rotation with retained lineage.
- OPEN: specific KYC / biometric verification integrations at the application
  layer are not yet documented. Marked inline at §1.4.
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

**Identity is necessary but not sufficient.** Establishing who an actor is does
not by itself grant that actor authority to do anything. Authority is granted
separately, explicitly, and revocably (see §8 and L30).

---

## 1. Identity Establishment

Identity establishment is the process by which an entity becomes a
recognized actor within the Sovereign Substrate. It is governed by the
Proof of Authentication (PoA) protocol and occurs once, at genesis.

### 1.1 Genesis Sequence

Identity establishment MUST proceed through the following canonical steps:

1. **Identity Claim** — the entity submits identifying information for verification.
2. **Verification** — the claim is validated against real-world or structured
   verification sources (see §1.4).
3. **Key Generation** — a unique private key is generated and bound to the
   verified entity, anchoring the identity cryptographically.
4. **Substrate Identity Key (SIK) Assignment** — a unique SIK is assigned.
5. **Secure Virtual Space Provisioning** — a Secure Virtual Space (L02) is
   created and bound to the identity.
6. **Blockchain Anchoring** — the verified identity event is recorded immutably
   as an Identity Genesis Event.
7. **Authenticated Cloud Enrolment** — the identity is enrolled such that all
   subsequent actions are bound to it.
8. **Wallet Activation** — the BlockCertsAI Wallet is activated as the gateway
   to the identity’s vault, credentials, and authenticated environment.
9. **Sealing** — the identity state is sealed with a Canonical Sealing Rule
   (CSR-L01).

### 1.2 Immutability of Genesis

Once established:

- The genesis event cannot be deleted, altered, or overwritten.
- Identity provenance cannot be changed.
- Identity MAY evolve only through canonical mutation rules (see §7).

### 1.3 Rejection Conditions

The substrate MUST reject any identity request that cannot be validated
against real-world verification systems or structured verification sources.

### 1.4 Verification Sources — OPEN

Verification at genesis relies on external validation of the identity claim.
The specific integrations used at the application layer — document
verification, biometric verification, and third-party identity providers —
are **not yet documented in this canon**. This section is under engineering
review and will be completed with the confirmed integration set.

Verification performed at genesis produces a sealed attestation. The
attestation, not the underlying verification artifact, becomes the canonical
record (see §10).

---

## 2. Identity Invariants

The following MUST remain invariant for the lifetime of an identity:

1. **Global uniqueness** — every identity MUST have exactly one *active* SIK at
   any given time. Superseded SIKs remain permanently in lineage and are never
   reassigned (see §7.3).
2. **Non-repudiation** — identity operations MUST be cryptographically
   attributable to the authenticated identity under which they were performed.
3. **Canonical provenance** — identity MUST be established through a recognized
   verification source.
4. **Traceable lineage** — all mutations, delegations, rotations, and
   transitions MUST be provably linked to the identity root.
5. **Immutable genesis** — identity creation time, method, and CSR-L01 signature
   MUST remain immutable.

---

## 3. Identity and Credentials

Identity within the Sovereign Substrate is **not established through
credentials**. It is established at genesis through authenticated verification
and cryptographic binding (§1), and it exists independently of any artifact
that may later reference it.

### 3.1 What Credentials Cannot Do

Authenticated credential products MUST NOT:

- create, replace, or substitute for a canonical identity
- serve as the root of authority for the identity itself
- grant identity-level authority through presentation
- be transferable in a way that separates them from the identity they derive from

Possession of a credential is never equivalent to being an authenticated actor.

### 3.2 What Credentials May Do

Authenticated credential products operate **above** the identity layer. They
derive from an already-established identity and MAY carry **scoped authority**
within clearly bounded limits:

- **Identity certificates** may present and attest to an authenticated identity
  in portable form. Presentation carries evidentiary weight but does not by
  itself grant access to any system or resource. Acceptance remains at the
  discretion of the relying party.
- **Vault instruments** confer no access or authority of their own. They are
  instruments of custody and privacy. Any authority attaching to shared content
  derives from that content, not from the vault.
- **Signature instruments** confer **transactional authority within the scope of
  what was signed**, because the signature is bound to an authenticated
  identity. They do not confer system access or identity-level authority.
- **Asset instruments** confer **ownership authority over the specific asset
  represented**. They do not confer system access or authority over anything
  else.

### 3.3 The Governing Principle

Authority is always scoped, always derived from an authenticated identity, and
never inherited from possession alone.

A credential proves something about an identity. It does not become one.

---

## 4. Key Custody

Every identity is bound to a private key generated at genesis (§1.1).

- Key custody resides within the identity’s own Secure Virtual Space (L02),
  held in encrypted form within the authenticated cloud environment.
- Custody is **1:1 per identity**. Keys are never pooled, commingled, or held
  in a shared custodial structure.
- Key access requires authenticated identity verification. No credential,
  token, application, or automated system may access key material by any other
  path.
- This model exists to remove the dominant failure mode of self-custody
  systems, in which loss of a seed phrase results in permanent and
  unrecoverable loss of identity and assets.

**Operational access constraints** — the conditions under which platform
operators may or may not access key material, and the governance controlling
those conditions, are defined in L30 and are currently under engineering
review. This canon does not presently assert that operator access is
cryptographically prevented.

---

## 5. Identity-Bound Operations

All canonical events MUST bind to an identity in one of the following roles:

### 5.1 Actor  
The entity responsible for initiating a canonical event.

### 5.2 Subject  
The entity whose state is affected by the canonical event.

### 5.3 Steward  
An entity authorized to maintain or manage identity-bound resources.

### 5.4 Delegated Actor  
A downstream identity operating under limited authority granted through
canonical delegation (§8).

Every event MUST include:

- Actor SIK
- Actor cryptographic signature
- Identity verification hash
- CSR lineage reference

Events lacking these MUST be rejected at validation time.

---

## 6. Recovery and Continuity

Identity is permanent. Access to it is not. This section governs the
circumstances under which access is restored without compromising identity
integrity.

### 6.1 Identity-Bound Recovery

Recovery MUST be triggered by **re-verification of the identity**, not by
possession of key material. Because the identity is bound to a verified entity
rather than to a secret, recovery re-establishes the binding rather than
recovering the secret.

Recovery events MUST:

- re-verify the identity through the same class of verification used at genesis
- be recorded as canonical mutation events
- preserve full lineage to the identity root
- never alter identity provenance or the genesis event

### 6.2 SIK Rotation on Compromise

Where a SIK is compromised, it MUST be deprecated rather than reused.

- The compromised SIK is marked deprecated on-chain with an immutable rotation
  event.
- A new SIK is issued to the same verified identity.
- The deprecated SIK remains permanently in lineage and is never reassigned.
- All events sealed under the deprecated SIK before the rotation timestamp
  remain valid and attributable.

Rotation changes which key is active. It does not create a new identity.

### 6.3 Guardian and Trustee Recovery

For incapacity or death, an identity MAY pre-designate one or more
authenticated guardians. A guardian:

- MUST themselves hold a verified identity established at L01
- MAY trigger a defined recovery or succession workflow
- MUST NOT thereby assume the identity, its genesis rights, or its provenance

### 6.4 Threshold Recovery

Recovery MAY additionally be secured by threshold shares distributed across
separate Secure Virtual Spaces, such that no single holder can reconstruct key
material alone.

### 6.5 Status

The recovery mechanisms in §6.2 through §6.4 are specified here as canonical
intent. Their implementation status is under engineering review.

---

## 7. Identity Mutation Rules

Identity MAY evolve through mutation events, but only under strict rules.

Mutation events MUST:

- Reference the identity’s root hash.
- Pass CSR-L01 validation.
- Maintain all invariants defined in §2.
- Preserve provable lineage and chain-of-custody metadata.
- Be replayable and deterministic.

### 7.1 Permitted Mutations

- Updating verified attributes.
- Adding authentication factors.
- Revoking compromised authentication factors.
- Extending identity trust scopes.
- **Narrowing or revoking previously granted trust scopes.**
- **Rotating a compromised SIK under §6.2.**
- **Recording a recovery or succession event under §6.**

### 7.2 Prohibited Mutations

- Changing identity provenance.
- Resetting or cycling identity lineage.
- Removing identity existence.
- Creating ambiguity between two identities.
- Reassigning a deprecated SIK.

### 7.3 Rotation and Lineage

SIK rotation is not lineage cycling. A rotation event supersedes the active SIK
while permanently retaining the prior SIK in lineage, preserving the
attributability of every event sealed under it.

Any mutation request violating these rules MUST be rejected.

---

## 8. Delegated Identity Rules

Delegated identity allows an identity to authorize another identity — human,
organizational, or machine — to act within a constrained scope.

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
- Grant authority the delegating identity does not itself hold.

All delegations MUST be revocable through canonical mutation (§7.1).

Governance of delegation scope — including which delegations require
multi-signature authorization and who holds classification authority — is
defined in L30 and is currently under engineering review.

---

## 9. Temporal Identity Rules

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

## 10. Identity Sealing Rules (CSR-L01)

A valid CSR-L01 seal MUST:

- Include the SIK
- Include the identity root hash
- Bind the event to canonical time
- Include the actor’s cryptographic signature
- Produce a unique canonical event hash

Identity operations lacking a valid CSR-L01 MUST be rejected.

Verification results obtained at genesis are sealed as canonical inputs. Replay
validates against the sealed attestation and does not require re-executing the
original external verification.

---

## 11. Deterministic Identity Validation

All identity validation MUST:

- Be environment-independent
- Produce identical results across implementations
- Be replayable from genesis against sealed canonical inputs
- Terminate deterministically
- Fail deterministically when invariants are violated

---

## Result

Identity at L01 is a **canonical execution primitive**, not a credential.
It is precise, enforceable, non-transferable, and provably correct.

Credentials derive from it. Authority is scoped from it. Neither replaces it.

All authenticated execution within the Sovereign Substrate depends on this layer.

---

Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

<!--
CANONICAL: TRUE
LAYER: L41
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L41 — Authentication Model (How the Substrate Establishes, Persists & Enforces Authenticated Identity)
Defines the persistent, systemic, and architectural model for how identities, agents, credentials, attestations, and actions are authenticated within the Sovereign Substrate. Unlike L1 (Identity Layer), which defines identity **objects**, L41 defines **how authentication operates** across all transitions, layers, domains, and recovery cycles.

The Authentication Model answers:  
**“How does the substrate *know* who is acting — and ensure that identity cannot be forged, lost, or misrepresented?”**

## 41.0 Purpose
L41 establishes:
- The substrate-wide authentication architecture  
- How identities, agents, and credentials remain authenticated over time  
- How authentication is persisted, replayed, and validated  
- How rules, governance, and constraints integrate with authentication  
- How cross-domain/federated authentication works  
- How authentication underpins PoA and all canonical operations  

Authentication is the substrate’s gateway: **nothing enters the system without it.**

## 41.1 Scope
Applies to:
- All identities (human, ADT, MAIAi, system, federated)  
- All credentials, attestations, certificates, tokens  
- All state transitions (L33)  
- All permissions/capabilities (L22–L23)  
- All provenance and lineage events (L18)  
- All agent actions and reasoning requests  
- All federated interactions  
- All governance actions  

Authentication is required **at every step**, not just onboarding.

## 41.2 Core Principles
1. **Authentication precedes authorization** — identity first, permissions second.  
2. **Authentication is persistent** — evidence must be durable and recoverable.  
3. **Authentication is verifiable** — cryptographic proof required for every claim.  
4. **Authentication is contextual** — validity depends on context (L25).  
5. **Authentication is immutable** — once established, cannot be rewritten.  
6. **Authentication is multi-layered** — identity + credential + attestation + context.  
7. **Authentication is federated-safe** — cross-domain identities require explicit validation.  

## 41.3 Authentication Object Model
Each authenticated identity or action is represented by a persistent Authentication Object:

### Inputs
- Identity reference (human/agent/system)  
- Credential set  
- Attestation(s)  
- Delegation chain (if applicable)  
- Proof of key ownership  
- Temporal and causal references  

### Outputs
- Authentication status (AUTHENTIC / EXPIRED / REVOKED / UNKNOWN)  
- Authentication evidence (signatures, hashes, attestations)  
- Authority level  
- Permitted action scope  
- Causal/Provenance anchor  

### Anchoring
- Authentication hash  
- Identity state root  
- Timestamp  
- Governance version  

Authentication objects become part of canonical provenance.

## 41.4 Authentication Processes

### 41.4.1 Identity Authentication
Verifies:
- Genesis identity (KYC)  
- Credential validity  
- Key ownership  
- Attestation chain correctness  

### 41.4.2 Session Authentication
Required for:
- Transitions  
- Agent requests  
- Federated interactions  

Session keys must be bound to identity keys.

### 41.4.3 Delegated Authentication
Verifies:
- Delegation signature  
- Delegation scope  
- Delegation expiration  
- Nested delegation chains  

Any break → delegation invalid.

### 41.4.4 Capability Authentication
Authenticates:
- Whether identity may use capability (L23)  
- Whether constraints allow capability at this moment (L31)  

### 41.4.5 Agent Authentication (ADT/MAIAi)
Agents must authenticate:
- Their state  
- Their context  
- Their capability set  
- Their reasoning request origin  

Agents cannot act anonymously or pseudo-anonymously.

### 41.4.6 Federated Authentication
Verifies:
- External identity claim  
- Domain trust boundary  
- Attestation and credential compatibility  
- Provenance and finality alignment  

If mismatch → QUARANTINE.

## 41.5 Authentication Lifecycle Model

### 41.5.1 Creation
Identity or agent enters the substrate:
- Verified  
- Attested  
- Anchored to genesis or domain of origin  

### 41.5.2 Activation
Identity becomes operational:
- Keys activated  
- Capabilities assigned  
- Delegations accepted  

### 41.5.3 Maintenance
Authentication must be:
- Continuous  
- Renewable  
- Revocable  
- Replay-safe during recovery  

### 41.5.4 Expiration
Identity authentication expires if:
- Credentials expire  
- Delegation chain invalid  
- Governance mandates expiration  

### 41.5.5 Revocation
Authentication revoked when:
- Governance commands  
- Identity compromise detected  
- Attestation invalidated  
- Permission/capability misuse occurs  

### 41.5.6 Recovery
Authentication must be reconstructable during L38 recovery:
- Authentication objects restored  
- Expired/invalid objects flagged  
- Re-attestation may be required  

## 41.6 Authentication Enforcement (Integration With L40)
Enforcement model must ensure:
- No unauthenticated action proceeds  
- Delegations cannot be forged  
- Expired credentials cannot be used  
- Agents cannot bypass authentication  
- Federated identities are verified  

Authentication violations → HARD BLOCK.

## 41.7 Authentication & Provenance (L18)
Every authentication event must:
- Anchor into provenance  
- Record custody transitions  
- Record attestation updates  
- Record credential lifecycle changes  

Provenance ensures future replay and audit.

## 41.8 Authentication & Constraints (L31)
Constraints define:
- Which identities may authenticate  
- At what times  
- Under what conditions  
- With what capabilities  

Authentication must respect:
- Temporal windows  
- Causal dependencies  
- Safety ceilings  

## 41.9 Authentication & Agents (L26)
Agents must:
- Use only authenticated channels  
- Produce authenticated reasoning traces  
- Authenticate every output  

Agents may **not**:
- Reuse expired credentials  
- Assume identity persistence without verification  
- Generate synthetic identities  

## 41.10 Authentication & Governance (L29)
Governance controls:
- Authentication policy  
- Revocation thresholds  
- Attestation authorities  
- Domain-level identity requirements  

Governance may:
- Mandate re-authentication  
- Define stronger KYC rules  
- Define domain-specific identity classes  

## 41.11 Authentication & Federation
Cross-domain authentication requires:
- Federated trust anchors  
- Cross-attestation validation  
- Proof of external finality  
- Identity schema compatibility  

If uncertain → reject or quarantine.

## 41.12 Replay & Persistence Guarantees
During:
- Node restart  
- Recovery (L38)  
- State sync  
- Federated exchange  

Authentication must replay identically using:
- Provenance entries  
- Attestation chains  
- Cryptographic proofs  
- Constraint contexts  

Authentication is never “lost” — it is *restored*.

## 41.13 Interaction With Other Layers
- **L11** — cryptography underpins all authentication.  
- **L12** — deterministic rules ensure consistent authentication.  
- **L13** — mutability prevents rewriting authentication history.  
- **L14** — temporal legality of authentication windows.  
- **L15** — causal anchoring of authentication events.  
- **L16** — rollback preserves authentication truth.  
- **L17** — recovery reconstructs authentication state.  
- **L18** — provenance stores authentication lineage.  
- **L19** — auditability requires authentication transparency.  
- **L20** — attestations serve as authenticated truth tokens.  
- **L21** — custody requires identity authentication.  
- **L22–L24** — permission/capability/accountability depend on authentication.  
- **L25** — context shapes authentication validity.  
- **L26** — agents require strict authentication boundaries.  
- **L27–L28** — validation/verification require identity correctness.  
- **L29–L31** — governance/constraints enforce authentication rules.  
- **L32–L33** — state/transition models require authenticated actors.  
- **L34–L36** — consensus/finality/fork prevention depend on stable authentication.  
- **L37** — causality requires authenticated parents.  
- **L38** — recovery demands authentication reconstruction.  
- **L39** — validation persists authentication evidence.  
- **L40** — enforcement blocks unauthenticated actions.

## 41.14 Invariants
1. AUTH_REQUIRED — no action may occur without authentication.  
2. AUTH_IMMUTABLE — authentication history cannot be rewritten.  
3. AUTH_VERIFIABLE — all authentication must be provable.  
4. AUTH_PERSISTENT — authentication survives recovery and replay.  
5. AUTH_CONTEXTUAL — validity depends on context.  
6. AUTH_GOVERNED — governance defines policy.  
7. AUTH_SECURE — authentication must resist impersonation or compromise.

## 41.15 Informative Guidance
Authentication is not a one-time event — it is a *living state*.  
Systems and agents must assume authentication may change at any moment due to governance, expiration, or security signals.  
Federated environments must assume foreign identities are untrusted until validated.  
Authentication is the foundation of compliance, safety, trust, and finality.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

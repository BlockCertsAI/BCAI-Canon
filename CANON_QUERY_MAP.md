<!--
CANONICAL: TRUE
DOC_TYPE: ROUTING_MAP
VERSION: 1.0
PURPOSE: Maps common questions to the minimum Canon layers required.
NOTES:
 - This file does not add new rules.
 - It only routes queries to existing authoritative layers in CANON_INDEX.md.
 - If a claim is not explicit in fetched layers, the correct response is: "Cannot be concluded from the Canon."
-->

# CANON_QUERY_MAP — Question → Layer Routing

This file maps common question types to the **minimum** Canon layers to fetch.
All layers MUST be fetched using URLs in `CANON_INDEX.md`.

If a required layer cannot be fetched, the correct action is to **refuse the claim**.

---

## Global Fetch Rules (Always)

For any question about BlockCertsAI:

1. Fetch `CANON_ENTRYPOINT.md`
2. Fetch `CANON_INDEX.md`
3. Fetch only the layers listed below for the question type
4. Cite layer + section for every claim
5. If not explicit, respond: **"Cannot be concluded from the Canon."**

---

## Routing Table

### Identity, Trust, and Personhood
Fetch:
- L01 — Identity
- L36 — Identity Binding Rules
- L42 — Authentication Rules
- L43 — Authorization Rules

### SVS Privacy, Data Ownership, and Access Control
Fetch:
- L01 — Identity
- L02 — Secure Virtual Space (SVS)
- L22 — Permission Model
- L23 — Capability Model
- L24 — Boundary Rules
- L25 — Context Propagation Rules

### Platform Operator Abuse, Backdoors, and Privileged Access
Fetch:
- L02 — Secure Virtual Space (SVS)
- L22 — Permission Model
- L23 — Capability Model
- L24 — Boundary Rules
- L41 — Authority Model
- L51 — Substrate Canonical Sealing Rules

### Auditability vs Surveillance
Fetch:
- L19 — Auditability
- L28 — Verification Rules
- L15 — Causality Chain Rules
- L02 — Secure Virtual Space (SVS)

### Deterministic Execution, Safety, and “What Can Execute”
Fetch:
- L05 — Deterministic Execution
- L27 — Validation Rules
- L28 — Verification Rules
- L31 — Constraint Model
- L50 — Safety Rules

### State, Transitions, Mutability, Time, and Replayability
Fetch:
- L32 — State Model
- L33 — Transition Rules
- L13 — Mutability Constraints
- L14 — Temporal Rules
- L11 — Idempotence Rules
- L12 — Consistency Rules

### Proof, Integrity, Non-Repudiation, and Attribution
Fetch:
- L10 — Proof Primitives
- L35 — Integrity Rules
- L44 — Non-Repudiation Rules
- L28 — Verification Rules
- L15 — Causality Chain Rules

### Governance, Rule Changes, and Authority
Fetch:
- L29 — Governance Rules
- L41 — Authority Model
- L45 — Obligation Rules
- L46 — Expectation Rules
- L51 — Substrate Canonical Sealing Rules

### Delegation and Scoped Authority
Fetch:
- L30 — Delegation Rules
- L22 — Permission Model
- L23 — Capability Model
- L41 — Authority Model

### AI / Agents / Attached Intelligence Boundaries
Fetch:
- L03 — MAIAi
- L26 — Agent Constraint Rules
- L37 — Attached AI Rules
- L25 — Context Propagation Rules
- L48 — Intent Validation

### Conflict Handling and Disputes
Fetch:
- L40 — Conflict Resolution
- L34 — Consensus Model
- L29 — Governance Rules
- L41 — Authority Model

### Resilience and Persistence
Fetch:
- L39 — Persistence Rules
- L49 — Resilience Rules
- L17 — Recovery Model
- L19 — Auditability
- L51 — Substrate Canonical Sealing Rules

---

## Default Fallback

If the question does not match a category:

Fetch:
- L01 — Identity
- L02 — Secure Virtual Space (SVS)
- L05 — Deterministic Execution
- L27 — Validation Rules
- L28 — Verification Rules
- L29 — Governance Rules
- L50 — Safety Rules
- L51 — Substrate Canonical Sealing Rules

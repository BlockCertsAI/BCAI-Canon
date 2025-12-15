<!--
CANONICAL: TRUE
LAYER: L48
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# L48 — Intent Validation Model (Purpose Verification, Safety Qualification & Pre-Transition Eligibility)
Defines the canonical framework for validating **intent** before any transition, request, or action may enter the substrate’s transition pipeline.

Intent is the *precondition*.  
Transition is the *execution*.  
L48 determines whether the system should **even consider** the actor’s proposed action.

The Intent Validation Model answers:  
**“Is this actor allowed to propose this action, for this purpose, in this context — and does the system understand the intent safely and unambiguously?”**

---

## 48.0 Purpose
L48 establishes:
- How intents are structured, represented, and validated  
- How the system confirms that an actor’s declared purpose is legal, safe, authorized, and comprehensible  
- How ADTs and MAIAi must expose intent traces  
- How governance and constraints regulate intent-level permissions  
- How malicious, ambiguous, or unsafe intent is prevented before transitions begin  
- How context shapes interpretability and legitimacy of intent  

Intent validation is the **front gate** before transition validation (L27) and transition integrity (L45).

---

## 48.1 Scope
Applies to:
- Human actor intents  
- ADT intents (agentic action proposals)  
- MAIAi intents (autonomous evaluation proposals)  
- Governance intents (policy shift proposals)  
- Federated system intents  
- Predictive intents (intent-to-transition from forecasts)  
- Delegated intents (L30)  

Intent validation is required:
- Before any transition is considered  
- Before any capability is exercised  
- Before any predictive action is escalated  
- Before any governance override is applied  

---

## 48.2 Core Principles
1. **Intent must be explicit.**  
2. **Intent must be interpretable and unambiguous.**  
3. **Intent must be legal under governance policy.**  
4. **Intent must be permitted under permissions and capabilities.**  
5. **Intent must respect constraints.**  
6. **Intent must be safe — not harmful, destabilizing, or deceptive.**  
7. **Intent must be traceable and auditable.**  
8. **No intent may lead to illegal or impossible transitions.**  

---

## 48.3 Intent Object Model
Every intent is captured as an **Intent Object**, containing:

### Required Fields
- Actor identity (L43)  
- Authentication proofs (L41)  
- Authorization context (L42)  
- Intent type (action, transition, inquiry, delegation, governance, predictive)  
- Declared purpose  
- Proposed scope and boundaries  
- Expected transition targets (if applicable)  
- Causal context (L37)  
- Temporal validity (L14)  
- Constraint envelope (L31)  
- Provenance anchor (L18)  
- Reasoning trace (for agents, L26)  
- Cryptographic signature  

### Optional Fields
- Risk markers  
- Prediction references (L47)  
- Delegation details (L30)  
- Domain metadata (federated cases)  

Missing required fields → **NONCANONICAL INTENT**.

---

## 48.4 Intent Categories

### 48.4.1 Action Intent
Actor wants to perform a discrete action.

### 48.4.2 Transition Intent
Actor proposes a state mutation.

### 48.4.3 Inquiry Intent
Actor asks for information that may influence later actions.

### 48.4.4 Delegated Intent
Actor expresses intent on behalf of a delegator.

### 48.4.5 Governance Intent
Governance expresses intent to apply policy changes.

### 48.4.6 Predictive Intent
Actor expresses intent to evaluate or simulate a scenario (L47).

---

## 48.5 Intent Validation Rules

### 48.5.1 Identity Requirement
Intent must be bound to a valid, unrevoked identity.

### 48.5.2 Authentication Requirement
Intent must include authentication proofs.

### 48.5.3 Authorization Requirement
Actor must be permitted to *intend* the action.

Authorization to intend is distinct from authorization to act.

### 48.5.4 Constraint Requirement
Intent must not request:
- Illegal actions  
- Excluded domains  
- Actions beyond capability ceilings  
- Actions violating safety policies  

### 48.5.5 Causality Requirement
Intent must:
- Respect causal structure (L37)  
- Reference valid parents if required  
- Not propose effects without causes  

### 48.5.6 Temporal Requirement
Intent must:
- Occur within valid time windows  
- Respect policy timing limitations  

### 48.5.7 Provenance Requirement
Intent must:
- Link to prior provenance  
- Establish a new provenance point  

### 48.5.8 Ambiguity Requirement
Intents must be:
- Clear  
- Interpretable  
- Non-contradictory  

Ambiguous intents → **REJECT**.

### 48.5.9 Harm Prevention Requirement
Intent must not:
- Suggest malicious action  
- Target protected resources  
- Attempt constraint evasion  
- Attempt governance bypass  
- Attempt unauthorized data access  

Harmful intent → **ENFORCEMENT (L40)**.

---

## 48.6 Intent Qualification Pipeline

### 48.6.1 Intent Parsing
System extracts:
- Actor  
- Purpose  
- Target  
- Context  

### 48.6.2 Intent Normalization
System converts intent into canonical structure.

### 48.6.3 Intent Safety Check
System evaluates:
- Capability limits  
- Constraint risks  
- Governance prohibitions  

### 48.6.4 Intent Purpose Validation
System determines whether the purpose is:
- Allowed  
- Meaningful  
- Non-destructive  

### 48.6.5 Intent Escalation
If intent carries elevated risk:
- Governance notified  
- Constraints tightened  
- Additional verification required  

### 48.6.6 Intent-to-Transition Eligibility
If intent is validated:
- System may *allow* the transition proposal to form  
Intent validation does **not** approve the transition.  
It only approves that **the actor may ask** for it.

---

## 48.7 Agentic Intent (ADT & MAIAi)

Agents must:
- Declare their intent explicitly  
- Provide full reasoning traces  
- Explain assumptions  
- Use authorized models  
- Obey constraint ceilings  

Agents may not:
- Generate hidden intents  
- Self-authorize transitions  
- Infer actions from predictions without approval  

---

## 48.8 Federated Intent Handling
Federated systems must:
- Declare domain of origin  
- Bind intent to federated identity proofs  
- Respect local governance policies  
- Pass verification requirements  

Federated intent may be **quarantined** if unclear or misaligned.

---

## 48.9 Observability & Reporting

Intent system must expose:
- Intent logs  
- Safety evaluations  
- Ambiguity detection  
- Governance escalation traces  
- Agentic reasoning traces  
- Intent-to-transition mapping  

Auditors must be able to inspect:
- Why an actor intended something  
- Whether they were permitted  
- Whether the intent was safe  

---

## 48.10 Layer Interactions
- **L11** — cryptographic securing of intent objects  
- **L12** — determinism ensures consistent intent parsing  
- **L13** — immutability prevents retroactive intent changes  
- **L14** — temporal rules define intent windows  
- **L15/L37** — causal consistency for intent chains  
- **L16/L38** — recovery restores intent logs  
- **L18** — provenance anchors all intents  
- **L19** — auditability ensures traceability  
- **L20** — attestations strengthen intent truth claims  
- **L22–L24** — permissions/capabilities/accountability bound intent  
- **L25** — context propagation shapes intent meaning  
- **L26** — agentic reasoning encoded in intent  
- **L27–L28** — validation/verification of intent evidence  
- **L29** — governance rules define allowable intents  
- **L30** — delegations define who may express intent for whom  
- **L31** — constraint system restricts intent scope  
- **L32–L33** — intent may reference state but not alter it  
- **L44–L45** — intent precedes transition legality & integrity  
- **L46** — intent fully audited  
- **L47** — predictions may accompany, not replace, intent  

---

## 48.11 Invariants
1. **INTENT_EXPLICIT** — intent must be clearly declared.  
2. **INTENT_LAWFUL** — no illegal purpose permitted.  
3. **INTENT_AUTHENTICATED** — must come from a proven identity.  
4. **INTENT_AUTHORIZED** — actor must be allowed to form the intent.  
5. **INTENT_SAFE** — must not threaten system integrity.  
6. **INTENT_TRACEABLE** — provenance must be complete.  
7. **INTENT_NONCANONICAL** — intent does not alter state.  
8. **INTENT_INTERPRETABLE** — must be machine- and auditor-understandable.  

Violation → **REJECT + ENFORCEMENT (L40)**.

---

## 48.12 Informative Guidance
Intent validation is a **safety buffer** that prevents harmful, illegal, unclear, or unauthorized actions before they can enter the transition pipeline.

It is essential for:
- Agentic safety  
- Governance oversight  
- Compliance and audit  
- Cross-domain risk control  
- Preventing misuse of prediction-based suggestions  

Designers should ensure that intent schemas are expressive enough for humans and machines, while remaining enforceable and unambiguous.

---
Return to Navigation:
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

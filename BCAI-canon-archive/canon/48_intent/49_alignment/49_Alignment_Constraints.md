<!--
CANONICAL: TRUE
LAYER: L49
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for this Sovereign Substrate layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical rules for this substrate layer.
-->

# Alignment Constraints  
**Layer:** L49  
**Domain:** Intent → Alignment  
**File:** 49_Alignment_Constraints.md  

---

## Purpose  
Alignment Constraints define the required relationship between an actor’s declared intent and the authenticated state of the Substrate.  
They ensure that **all intent-driven operations remain coherent, consistent, and synchronized** with:

- Identity guarantees  
- Current authenticated state  
- System constraints  
- Canonical rules governing transitions  

Alignment protects the Substrate from invalid intent such as stale, conflicting, contradictory, or unauthorized proposals.

---

## Core Constraints  

### **1. State–Intent Synchronization**  
Intent must **match the current authenticated state** at the moment of declaration.  
- Outdated intent is invalid.  
- Intent referencing a superseded or replaced state is rejected.  
- State transitions invalidate any unresolved previous intent.

---

### **2. Identity–Intent Binding**  
Intent must remain bound to the same identity that declared it.  
- Transferred, reassigned, or detached intent is forbidden.  
- MAIAi, ADT, or AI agents may not repurpose another actor’s intent.

---

### **3. Constraint Compliance**  
Intent must conform to all relevant constraints within its domain:  
- Role constraints  
- Authority constraints  
- Safety constraints  
- Conflict rules  
- Execution constraints  

Violating any constraint invalidates the intent.

---

### **4. Authority Alignment**  
Intent must fall within the actor’s authenticated authority class.  
- No actor may propose operations outside or above their granted scope.  
- Authority is evaluated at the time of intent, not execution.

---

### **5. Purpose Alignment**  
Intent must remain aligned to its **declared purpose**, and may not:  
- Expand scope,  
- Shift meaning,  
- Alter semantic boundaries,  
- Introduce side effects outside the declared purpose.

Any drift invalidates alignment.

---

### **6. Temporal Coherence**  
Intent must align with temporal guarantees of the Substrate:  
- Execution windows  
- Time-to-live  
- Sequence order  
- Precedence and dependency rules  

Expired or temporally contradictory intent is automatically rejected.

---

### **7. Non-Conflict Requirement**  
Intent may not contradict:  
- Existing obligations  
- Pending operations  
- System invariants  
- Other actors’ validated intent  

Conflicting intent requires resolution before any transition can proceed.

---

## Enforcement  

Alignment is enforced by:  
- **Identity layer** → verifying actor and authority  
- **State layer** → verifying world-state coherence  
- **Constraint engine** → validating purpose and scope  
- **Architect** → enforcing alignment before constructing any transition  
- **ATTACHED AI (MAIAi)** → ensuring no semantic drift or conflict  

No operation can enter the transition pipeline unless all alignment constraints pass.

---

## Why It Matters  
Misaligned intent is one of the primary causes of system failure in distributed or agentic systems.  
Alignment constraints eliminate:  
- Race conditions  
- Conflicting intent  
- Drift between purpose and execution  
- Unauthorized expansion of scope  
- Temporal inconsistencies  

Alignment is what keeps the Substrate deterministic, safe, and self-governing.

---

## Result  
Only **coherent**, **identity-bound**, **state-aligned**, and **constraint-compliant** intent is allowed to become executable transition proposals.


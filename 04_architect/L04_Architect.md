<!--
CANONICAL: TRUE
LAYER: L04
AUTO-TOC: ENABLED
VERSION: 1.0
PURPOSE: Canon rule file for the Architect orchestration layer.
NOTES:
 - Do not remove this header.
 - This file defines canonical orchestration and execution planning rules.
-->

## L04 — Architect (Orchestration Layer)

The Architect is the substrate’s **orchestration and execution-planning layer**.

It translates validated intent into **ordered, constraint-compliant execution plans**  
without executing, mutating state, or exercising agency.

The Architect answers the question:  
**“What lawful sequence of actions could satisfy this intent?”**

---

## Core Principles

### **1. Non-Agency**
The Architect has no identity, no intent, and no authority.

It does not:
- originate actions  
- express goals  
- exercise discretion  

It plans only.

---

### **2. Non-Execution**
The Architect does not execute transitions.

It:
- proposes execution sequences  
- orders dependencies  
- resolves routing and handoffs  

Execution is performed exclusively by **L05 Deterministic Execution**.

---

### **3. Determinism-Preserving**
Given identical:
- validated intent  
- current state  
- constraints  

the Architect MUST produce:
- the same execution plan  
- with the same ordering and dependencies  

Non-deterministic planning is prohibited.

---

### **4. Constraint-Respecting**
All plans MUST respect:
- constraints (L31)  
- invariants (L28)  
- permissions and delegation (L30)  
- identity bindings (L01 / L06)  

If no lawful plan exists, the Architect MUST fail deterministically.

---

## Functions of the Architect

### **1. Execution Plan Construction**
The Architect decomposes validated intent into:
- ordered execution steps  
- explicit dependencies  
- required execution contexts  

Each step must be independently executable by L05.

---

### **2. Dependency Resolution**
The Architect ensures:
- correct causal ordering  
- no circular dependencies  
- proper handoff between domains  

Unresolvable dependency graphs MUST fail.

---

### **3. Routing and Context Assignment**
The Architect assigns:
- execution domains  
- routing paths (CSR)  
- required execution environments  

Routing decisions are canonical and reproducible.

---

### **4. Plan Validation**
Before submission, the Architect validates that:
- all steps are lawful  
- all constraints are satisfied  
- execution is possible without ambiguity  

Invalid plans MUST NOT be emitted.

---

## What the Architect Cannot Do

The Architect MUST NOT:
- modify state  
- execute transitions  
- override constraints  
- infer or alter intent  
- substitute for ADT or MAIAi  
- seal events  

It is structural, not authoritative.

---

## Interaction With Other Layers

- **L03 — MAIAi:** May assist in analysis, not decision-making  
- **L05 — Execution:** Receives execution plans  
- **L06 — ADT:** Supplies validated intent  
- **L07 — CSR:** Receives routing instructions  
- **L31 — Constraints:** Enforced during plan construction  

---

## Result

The Architect ensures that:
- execution is orderly  
- dependencies are explicit  
- lawful paths are enforced  
- complexity is handled without agency  

Without the Architect, execution becomes ad-hoc.  
With it, the substrate remains **predictable, lawful, and sovereign**.

---

## Return to Navigation
- [Root Specification](../CANON_ROOT.md)
- [Machine-Readable Master Index](../CANON_MASTER_INDEX.md)
- [Human Navigation Map](../CANON_NAV.md)

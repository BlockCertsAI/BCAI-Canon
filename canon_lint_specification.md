<!--
CANONICAL: TRUE
LAYER: META
VERSION: 1.0
PURPOSE: Defines the Canon Lint specification for validating Canon files,
         detecting ambiguity, preventing drift, and enforcing boundary rules.
NOTES:
- This specification is authoritative.
- A Canon file that fails lint is non-canonical.
-->

# Canon Lint Specification

## 1. Purpose

The Canon Lint exists to:

- Enforce Canon Boundary Rules
- Prevent interpretive drift
- Detect ambiguity before execution
- Ensure the Canon remains deterministic, sovereign, and enforceable

The Canon Lint is **non-negotiable**.

---

## 2. Scope of Linting

The Canon Lint MUST be applied to:

- All Canon layer files
- All Canon meta files
- All revisions, amendments, or extensions
- Any document marked `CANONICAL: TRUE`

---

## 3. Deterministic Output

Canon Lint produces exactly one of:

- **PASS**
- **FAIL**

No warnings.  
No suggestions.  
No partial compliance.

---

## 4. Hard Failure Conditions

A Canon file MUST FAIL lint if **any** of the following are detected.

---

### 4.1 Ambiguous Language

The following terms are **forbidden** unless explicitly defined in the same file:

- may
- should
- might
- could
- typically
- generally
- usually
- intended to
- designed to
- reasonable
- best effort
- where possible (unless explicitly bounded)
- as needed
- flexible
- optional (unless paired with explicit scope)

**FAIL if present.**

---

### 4.2 Interpretive Language

The following constructs are forbidden:

- “this implies”
- “this suggests”
- “this allows”
- “this prevents” (without explicit constraint)
- “this enables” (without enforcement rule)
- “in practice”
- “in effect”
- “conceptually”
- “logically”
- “by design” (unless followed by explicit rule)

**FAIL if present.**

---

### 4.3 Undefined Authority

A Canon file MUST FAIL if it references:

- super-admin
- root operator
- platform owner
- emergency access
- override authority
- discretionary control
- trusted party
- governance exception

**Unless** that role is explicitly defined, bounded, and constrained **in the same file or a referenced Canon layer**.

---

### 4.4 Missing Invariants

Any rule that constrains execution, identity, data, authority, or access MUST include at least one of:

- MUST
- MUST NOT
- ONLY
- NEVER
- NO

Rules stated without invariants are **non-canonical**.

---

### 4.5 Absence Violation

If a Canon file:

- introduces a capability
- references an action
- implies a mechanism

without defining:
- who can invoke it
- under what constraints
- with what validation
- and with what failure mode

→ **FAIL**

---

### 4.6 Explanation Leakage

A Canon file MUST FAIL if it:

- justifies a rule instead of enforcing it
- explains motivation without constraint
- argues correctness instead of declaring law
- uses narrative examples as enforcement

Explanation may exist **only after** a rule is fully defined.

---

### 4.7 Override Paths

If a Canon file defines:

- an exception
- an override
- a special case
- a fallback
- a recovery path

It MUST also define:

- exact triggering conditions
- identity authorized to invoke it
- validation requirements
- enforcement boundaries
- explicit prohibition of expansion

Failure to fully specify → **FAIL**

---

### 4.8 Non-Determinism

A Canon file MUST FAIL if it allows:

- environment-dependent behavior
- time-based discretion (outside defined temporal rules)
- probabilistic outcomes
- heuristic evaluation
- AI judgment or interpretation

---

### 4.9 AI Authority Leakage

Any Canon file that states or implies that AI:

- validates Canon compliance
- interprets rules
- adjudicates ambiguity
- resolves conflicts

→ **FAIL**

AI may only operate **inside constraints**, never above them.

---

## 5. Structural Checks

The Canon Lint MUST verify:

- Header integrity (`CANONICAL`, `LAYER`, `VERSION`, `PURPOSE`)
- Layer references exist in Canon Index
- No circular authority references
- No duplicate invariant definitions with conflicting meaning
- All referenced layers exist and are canonical

---

## 6. Absence Enforcement Rule

The Lint MUST enforce:

> If a behavior is not explicitly permitted, it is prohibited.

Any implied permission → **FAIL**

---

## 7. Canon Drift Detection

A revision MUST FAIL if it:

- weakens an invariant without explicit revocation
- replaces MUST with SHOULD
- introduces discretion where none existed
- expands authority scope silently
- redefines existing terms without versioned replacement

---

## 8. Failure Handling

On **FAIL**:

- The file is non-canonical
- The change MUST NOT be merged
- No execution may rely on it
- No exception process exists

---

## 9. Enforcement Priority

Canon Lint enforcement order:

1. Boundary Rules
2. Invariants
3. Constraints
4. Absence Rules

Failure at any level halts evaluation.

---

## Canon Lint Conclusion

The Canon Lint is the **immune system** of the Sovereign Substrate.

If the Canon becomes interpretable,
the system is already compromised.

The Canon Lint prevents that.

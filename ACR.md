# ARG Architectural Constitution (ACR)
**Version:** v1.0 Candidate  
**Status:** FROZEN LAW  
**Scope:** Structural invariants, safety laws, and architectural boundaries for ARG.

---

## 1. Immutable System Laws
1. **Mandate Governance:** All code generation, state mutation, and cognitive execution must strictly adhere to the 9 Core Engineering Mandates (M1–M9).
2. **Four-Layer Isolation:** The system must maintain strict boundary separation between Layer 1 (Operator), Layer 2 (Decision Studio), Layer 3 (ARG Runtime), and Layer 4 (Intelligence Network).
3. **Zero Data Loss:** All state transitions must be backed by the immutable Event Ledger. Transient failures must fall back to safe memory buffers (`safeStorage`).
4. **Sovereign Policy Check:** No cognitive model or LLM prompt can override or subvert the independent Policy Engine and Mandate Linter.

---

## 2. Structural Principles
* **Modular Code Splitting:** Components must be kept small and modular to eliminate token-limit truncation risks.
* **Deterministic Rebuilds:** Given the same Event Ledger sequence, the runtime must reproduce the exact operational state.
* **Non-Destructive Operations:** Data deletions or destructive state rewrites are strictly forbidden without explicit dual authorization.

Architectural boundaries
The following architectural boundaries should hold for ARG:
Project-significant actions must not silently mutate critical workspace state.
Meaningful advancement should occur through visible progression boundaries.
Recovery-relevant changes must produce inspectable continuity records.
Verification-relevant results must remain visible long enough to support review and rollback decisions.
Higher-risk execution paths must not bypass validation or approval surfaces when those surfaces are active.
Recovery must be treated as a core architectural concern rather than a secondary backup convenience.
Non-bypass expectations
The architecture should preserve the following expectations:
checkpoint creation cannot be treated as optional for major state-changing operations,
verification cannot be skipped when the workflow is configured to require completion proof,
failure states must remain observable,
restore capability must target a known prior workspace condition,
builder visibility must not compromise operator simplicity.
Continuity constraints
ARG should preserve enough continuity information to support:
interrupted session resumption,
failed-step recovery,
visible workspace history,
restore-to-known-good behavior,
and human inspection of meaningful project transitions.

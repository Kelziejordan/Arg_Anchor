# ARG Architectural Runtime Specification (ARS)
**Version:** v1.0 Candidate  
**Status:** DRAFT / IMPLEMENTATION SPECIFICATION  
**Scope:** Engineering runtime components, Event Ledger schemas, safe storage wrappers, and capability registry APIs.

---

## 1. Runtime Components
* **Governor Engine (`PolicyEngineService`):** Evaluates system state against Mandates M1–M9.
* **Event Ledger (`EventLedgerService`):** Implements append-only log storage with SHA-256 signatures and safe fallback storage.
* **Storage Abstraction (`safeStorage`):** Wraps `localStorage` with try-catch blocks and in-memory fallbacks to guarantee iframe safety.
* **Capability Registry (`CapabilityRegistryService`):** Manages dynamic tools, pipelines, and execution chains.

---

## 2. Telemetry & Metabolic Constraints
* **Thread Density Limit:** Maximum 10 concurrent async threads.
* **Stress Threshold:** Integrity score monitored continuously; scores below 50% trigger vector dampening and simulation rollback.
* **Storage Key Namespaces:**
  - `arg_onboarding_layer`
  - `arg_onboarding_active_goal`
  - `arg_canonical_intent`
  - `arg_recent_projects_v1.6`
  - `argos_execution_journal`

---

Runtime expectations
ARG runtime behavior should make progress, failure, and recovery visible.
This includes:
explicit execution state,
visible checkpoints,
validation boundaries,
verification outcomes,
failure visibility,
pause and resume support,
and recoverable workspace continuity.
Validation boundaries
External inputs, generated outputs, and execution-affecting state transitions should cross explicit validation boundaries before they are treated as safe advancement.
Observability
The runtime should expose enough evidence for a user or builder to answer:
what changed,
what passed,
what failed,
what was approved,
and what can be resumed safely.
Recovery behavior
Recovery should support:
restore to a known prior state,
continuation after interruption,
inspection of prior checkpoints,
and review of verification or failure evidence linked to significant work steps.
Verification behavior
Verification should remain distinct from execution. Runtime state should make it clear whether work is:
proposed,
in progress,
completed but unverified,
verified,
failed,
or restored from a prior state.

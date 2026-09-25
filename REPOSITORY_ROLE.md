# Repository Role Declaration — Arg_Anchor

Declaration version: 1.0
Effective status: FROZEN AUTHORITY BOUNDARY
Repository: Kelziejordan/Arg_Anchor

## Architectural classification
- Tier: 2 — Product/workspace surface
- Lifecycle: Active / product development
- Source of truth: No for foundational contracts; source of truth for its own UI/workspace implementation
- Historical/reference status: May contain recovered product concepts, which remain non-authoritative unless promoted

## Authority
- Identity: CONSUMER
- State: CONSUMER
- Governance: CONSUMER
- Provenance: CONSUMER
- Execution: OWNER only within its product/workspace boundary

## Dependencies
Anchor consumes ArgCore/Arg runtime governance rather than replacing it. UI state, workspace state, and product workflow state must not be treated as constitutional execution state.

## Owned contracts
Anchor owns product/workspace interaction contracts, presentation behavior, local workflow behavior, and product-specific recovery UX.

It does not own ArgCore identity, state continuity, governance, provenance, or recovery contracts.

## Permitted modifications
May evolve product behavior and workspace UX. Must consume current runtime contracts and may not bypass governed execution or invent a competing authority model.

## Contents
- Original implementation: Yes
- Derived implementation: Yes
- Documentation: Yes
- Packaging/deployment: Yes
- Historical/provenance: Some
- Experimental: Some, when marked

## Promotion rules
Product capabilities that require runtime authority must be implemented through the current Arg/ArgCore boundary and verified there.

## Authority boundary
Anchor is a consumer/product surface. It organizes and presents governed work; it does not become the governing substrate.

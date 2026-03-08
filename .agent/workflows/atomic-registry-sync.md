---
description: Builds the registry for any atoms that already exist
---

# Workflow: /atomic-registry-sync

**Trigger**: `/atomic-registry-sync`

**Action**:

1. Scan the project for all functions implemented via the Atomic Loop.
2. Update or create `docs/atoms_registry.md`.
3. For each atom, record: 
   - **Name**: Function Name.
   - **Purpose**: Concise functional responsibility.
   - **Domain File**: Source path.
   - **Test File**: Test file path
   - **Contract Invariants**: Logical constraints.
   - **Adversarial Status**: Verification of edge-case handling.

**Goal**: Build a searchable library of verified, purpose-driven "atoms" for reuse.
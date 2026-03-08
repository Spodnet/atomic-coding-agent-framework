---
description: This command processes all atoms automatically instead of manually triggering each one.
---

# Workflow: /atomic-auto

**Trigger**: `/atomic-auto`

**Action**: 

You are authorized to execute the implementation plan of each atom sequentially. 

For each task in the plan:
1. **Status Log**: Post a message: 'Now starting Atom [X]: [Name]'.
2. **The Loop**: Execute the full Atomic TDD sequence (Test -> Fail -> Code -> Pass -> Commit) as defined in your rules.
3. **Verification**: You must run the *entire* test suite after each atom to ensure no regressions.
4. **Checkpoint**: If a test fails and you cannot fix it in one attempt, **STOP** and ask for guidance. Do not proceed to the next atom if the current one is 'Red'.

Proceed with the next atom in the list that has not been completed.
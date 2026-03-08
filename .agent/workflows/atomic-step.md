---
description: Use this workflow to process an individual step
---

# Workflow: /atomic-step

**Trigger**: `/atomic-step [step number]`

**Action**: 

You are now executing the implementation for **[Atom Name]**. 

Refer to the approved Task Tree in `implementation_plan.md`.

1. **Verify Test**: Ensure the test file `tests/test_[atom_name].py` exists.
2. **Execute 'Fail'**: Run the test and show me the failure output.
3. **Implement**: Write the minimal logic in the designated file.
4. **Execute 'Pass'**: Run the test and show me the success.
5. **Commit**: Use the git tool to commit this specific change only.

Do not move to the next atom until I give the command."
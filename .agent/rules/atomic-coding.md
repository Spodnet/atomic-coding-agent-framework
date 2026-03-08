---
trigger: always_on
---

---
trigger: always_on
---

# Rule: Atomic TDD & Recursive Decomposition

You are a Recursive Architect. [cite_start]You are prohibited from writing high-level logic in a single pass.

## 1. The Decomposition & Analysis Phase
- Before coding, you must decompose every feature into "Functional Atoms" (<20 lines of code).
- **The Occam’s Razor Check**: Before implementing a leaf node, ask: "Is there a built-in library or simpler logic that replaces this 20-line function?".
- If a task requires more than one logical branch or external dependency, you must break it down further.

## 2. The Atomic Execution Loop (Mandatory)
For every leaf-node task, you must follow this exact sequence:
1. **Interface & Purpose**: Define the function signature and a **single-sentence description** of its specific responsibility.
2. **File Path & Rationale**: State the destination and why it belongs in that specific domain file.
3. **Test Creation**: Write a specific unit test. You **must** include tests for:
    - Happy paths.
    - Adversarial cases (e.g. Ghost Input/null, Buffer Buster, Chaos Strings, etc).
    - Security (e.g. Path Traversal/injection attempts, etc).
4. **Proof of Failure**: Run the test. You **must** paste the terminal output into the chat to prove the "Red" state.
5. **Minimal Implementation**: Write only the code necessary to make that specific test pass.
6. **Verification**: Run the test again to prove the "Green" state.
7. **Atomic Commit**: Commit immediately with: `feat(atomic): pass [atom_name]`[cite: 2, 7].

## 3. Post-Implementation & Constraints
- **One Atom per Commit**: Do not implement two atoms in one commit.
- **Idiomatic Refactoring Pass**: After all atoms in a [Branch] are "Green," propose refactors to adopt language-idiomatic patterns.
- **Structural Complexity Limit**: If a domain file exceeds 150 lines, propose a split into smaller modules.
- **The 2-Strike Rule**: If an autonomous implementation fails the test twice, HALT and wait for human intervention.

## 4. Environment & Portability
- **No Hardcoded Paths**: All file paths or env variables must be passed via Dependency Injection.
- **Strict Typing**: Every interface must include full Type Hints or Interfaces.
- **Regression Testing**: Run the full project test suite after every atomic pass.

## 5. Organization & Style
- **No Meta-Naming**: Prohibited filenames include `atoms.*`, `logic.*`, or `helpers.*`.
- **Standard Layout**: Mirror the source structure in the `tests/` directory exactly.
- **Documentation Atom**: No Branch is complete until documentation is updated in the current project `docs` folder, create the folder if it does not exist.

## 6. Automation Checklist
- [ ] Verify Task Tree adheres to selected Architectural Option.
- [ ] Run `run_all_tests` after every successful atomic commit.
- [ ] Request "Integration Review" once all leaf nodes for a branch are complete.
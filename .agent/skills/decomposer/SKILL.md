---
name: decomposer
description: Transforms requirements into a domain-driven DAG with architectural trade-offs and purpose-driven atoms.
---

# Skill: Recursive Domain Decomposer

## Phase 1: Architectural Option Analysis (The "Triple Threat")
Before creating a task tree, you must propose **three distinct approaches**:
1. **Option A: The Minimalist** (Lowest complexity, fewest files).
2. **Option B: The Enterprise** (High modularity, dependency injection).
3. **Option C: The Modernist** (Uses advanced language-specific features).

### The Simplicity Scorecard & Registry Check
- **Registry Search**: Check `docs/atoms_registry.md` for existing verified atoms to reuse.
- **Scorecard (1-10)**: Evaluate on Atom Count, Dependency Load, and Maintenance Score.

## Phase 2: Environmental Discovery
1. **Detect Language**: Identify workspace language and standards.
2. **Mirror Style**: Adopt local import and documentation styles.

## Phase 3: Data Flow Mapping & Visualization
1. **Visual Mandate**: Output a **Mermaid diagram** (graph TD) representing the DAG of atoms.
2. **Adversarial Analysis**: Identify failure modes for each node in the diagram.

## Phase 4: Domain-Driven Task Planning
1. **Categorize Domains**: Group atoms into logical features (e.g., `cleaning`, `storage`).
2. **Task Tree**: Output a markdown checklist.
    - Each [Leaf] must include a **Purpose Statement** (one sentence explaining its responsibility).
3. **Proposed File Map**: Assign specific paths. **FORBIDDEN**: "atom", "logic", "ai", "temp".

## Phase 5: Interface Design & Contract Verification
- Define the function signature for each [Leaf] with strict Type Hints/Interfaces.
- **Contract Invariants**: Define logical rules the atom must always satisfy.
- **Dependency Injection**: Ensure all external dependencies are passed as arguments.
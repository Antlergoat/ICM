# Stage 02: Mapping

Formalize the stage contracts and finalize world-bible file dependencies for each stage.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Discovery summary | `../01-discovery/output/discovery-summary.md` | Full file | The workflow and bible dependencies to formalize |
| Wiring guide | `../../references/world-bible-wiring-guide.md` | "Which Bible File Goes Where" section | Reference for finalizing bible dependencies per stage |
| Conventions | `/_core/CONVENTIONS.md` | "Pattern 1: Stage Contracts" and "Pattern 3: One-Way Cross-References" | Rules for writing contracts |

## Process

1. Read Inputs
2. For each stage, write the formal Inputs/Process/Outputs contract
3. For each stage, finalize world-bible dependencies: which files, which sections, and why
4. Map cross-references -- verify the dependency graph flows one way only
5. Verify every stage's output is consumed by a downstream stage or is the final output
6. Checkpoint: present dependency diagram and all contracts for review
7. Run audit
8. Save to `output/stage-contracts.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 5 | Dependency diagram and draft contracts with bible dependencies | Whether the flow, contracts, and bible file selections are correct |

## Audit

| Check | Pass Condition |
|-------|----------------|
| No circular references | Dependency graph flows one direction only |
| Output consumption | Every stage's output is read by a downstream stage or is the final deliverable |
| Contract completeness | Every stage has Inputs, Process, and Outputs with no empty fields |
| Bible dependencies specific | Each bible dependency names a section, not just a file |
| One-way references | No bible file references back to any workspace stage |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Stage contracts | `output/stage-contracts.md` | Formal Inputs/Process/Outputs blocks for every stage, bible dependencies per stage, ASCII dependency diagram |

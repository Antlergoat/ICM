# Stage 04: Validation

Verify the scaffolded workspace against ICM conventions and world-bible wiring requirements. Catch errors before the workspace is moved into production.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Scaffolded workspace | `../03-scaffolding/output/` | Full workspace | The workspace being validated |
| ICM conventions | `/_core/CONVENTIONS.md` | Full file | The rules every workspace must follow |
| Wiring guide | `../../references/world-bible-wiring-guide.md` | Full file | World-bible-specific requirements to check |

## Process

1. Read all Inputs
2. Run all checks in the audit table below
3. For each failure: describe the file, the problem, and the fix
4. If any checks fail: fix the scaffolded workspace files and re-run the failed checks
5. When all checks pass: write the validation report
6. Save to `output/validation-report.md`

## Audit

| Check | Pass Condition |
|-------|----------------|
| Bible paths | All world-bible references use `../../../../world-bible/[file].md` |
| Prerequisite check | setup/questionnaire.md opens with the world-bible prerequisite block |
| CLAUDE.md prerequisite | Prerequisite section present and correctly worded |
| No placeholders in CLAUDE.md | Zero `{{` patterns in any CLAUDE.md file |
| No placeholders in top-level CONTEXT.md | Routing table has no `{{` patterns |
| CONTEXT.md size | Every CONTEXT.md is under 80 lines |
| Reference file size | Every reference file is under 200 lines |
| .gitkeep present | Every output/ folder contains .gitkeep |
| One-way references | No bible file references any workspace file |
| Stage contracts match | Every stage in stage-contracts.md has a corresponding folder |
| Questionnaire maps to files | Every placeholder in the questionnaire names the file(s) it populates |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Validation report | `output/validation-report.md` | Markdown: pass/fail per check, fixes applied, final status |

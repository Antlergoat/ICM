# Stage 03: Scaffolding

Generate all files for the new workspace with world-bible references pre-wired. Every file follows ICM conventions. Every stage CONTEXT.md Inputs table references the world-bible files identified in mapping. Every setup questionnaire includes the world-bible prerequisite check.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Stage contracts | `../02-mapping/output/stage-contracts.md` | Full file | The specification for every file to generate |
| Discovery summary | `../01-discovery/output/discovery-summary.md` | Tool Prerequisites and Selected Skills sections | Tools needing setup guides, skills to bundle |
| Wiring guide | `../../references/world-bible-wiring-guide.md` | Full file | Rules for wiring bible references and questionnaire prerequisite |
| Stage template | `/_core/templates/stage-context-template.md` | Full file | Template for stage CONTEXT.md files |
| Workspace template | `/_core/templates/workspace-claude-template.md` | Full file | Template for workspace CLAUDE.md |
| Context template | `/_core/templates/workspace-context-template.md` | Full file | Template for workspace CONTEXT.md |
| Placeholder syntax | `/_core/placeholder-syntax.md` | Full file | Rules for placeholder naming and conditional blocks |

## Process

1. Read all Inputs
2. Generate the folder structure as a tree -- confirm with user before writing any files (checkpoint)
3. Generate files in this order: CLAUDE.md, CONTEXT.md, setup/questionnaire.md, stage CONTEXT.md files, reference stubs, .gitkeep files
4. CLAUDE.md: include a Prerequisite section (see wiring guide)
5. setup/questionnaire.md: open with the world-bible prerequisite check block (see wiring guide), then role-specific questions
6. Each stage CONTEXT.md Inputs table: wire in world-bible files from the stage contracts using `../../../../world-bible/[file].md` paths
7. Create skills/ folder if skills were selected -- copy local skills or note clone commands for GitHub skills
8. Write setup guides in stage references/ for any system-level tool prerequisites
9. Add .gitkeep to every output/ directory
10. Run audit
11. Write all files to `output/[workspace-name]/`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 2 | Folder structure tree | Approve before any files are written |

## Audit

| Check | Pass Condition |
|-------|----------------|
| Bible paths correct | All world-bible references use `../../../../world-bible/[file].md` |
| Prerequisite check in questionnaire | setup/questionnaire.md opens with the world-bible prerequisite block |
| Prerequisite in CLAUDE.md | Prerequisite section present |
| No placeholders in CLAUDE.md | Zero `{{` patterns in any CLAUDE.md |
| No placeholders in top-level CONTEXT.md | Routing table has no `{{` patterns |
| CONTEXT.md size | Every CONTEXT.md is under 80 lines |
| .gitkeep present | Every output/ folder has .gitkeep |
| All stage contracts covered | One stage folder exists per contract in stage-contracts.md |
| Naming conventions | All folders and files use lowercase-with-hyphens |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Generated workspace | `output/[workspace-name]/` | Complete folder tree, world-bible wired, ready for questionnaire design |

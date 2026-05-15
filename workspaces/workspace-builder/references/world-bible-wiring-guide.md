# World Bible Wiring Guide

How to wire world-bible references into any workspace this builder produces. Read this file during Stage 02 (mapping) and Stage 03 (scaffolding).

---

## The Core Rule

Every workspace produced by this builder is a citizen of the shared world. That means two things:

1. Its stage CONTEXT.md Inputs tables reference the world-bible files they need
2. Its setup questionnaire checks that the world bible is populated before asking role-specific questions

---

## Path Convention

World-bible files live at `world-bible/` relative to the repo root. From a stage CONTEXT.md inside any workspace, the path is always:

```
../../../../world-bible/[filename].md
```

Path breakdown from `workspaces/[workspace-name]/stages/[stage-name]/CONTEXT.md`:
- `../` = up to the stage folder
- `../../` = up to stages/
- `../../../` = up to the workspace folder
- `../../../../` = up to workspaces/
- Wait -- world-bible is at the repo root, one level above workspaces/
- Correct path: `../../../../world-bible/` (four levels up from stage CONTEXT.md = repo root, then into world-bible/)

Verify: `workspaces/[name]/stages/[stage]/CONTEXT.md` -> `../../../../` = repo root. Then `world-bible/` = correct.

---

## Which Bible File Goes Where

During Stage 02 mapping, decide which bible files each stage needs. Use this table as a guide:

| Stage purpose | Bible files to consider |
|---------------|------------------------|
| Any creative task | world-overview.md (always load -- tone and premise anchor) |
| Character writing or design | characters.md + character-appearance.md |
| Visual output (art, video, concept) | character-appearance.md (physical descriptions become prompts/briefs) |
| Faction or political content | factions.md |
| World-consistency checks | world-rules.md |
| Narrative with historical context | timeline.md |

Load only what the stage needs. Never load all bible files as a default.

---

## Inputs Table Pattern

In each stage CONTEXT.md Inputs table, world-bible entries follow this format:

```markdown
| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| World overview | `../../../../world-bible/world-overview.md` | Full file | Tone and premise anchor |
| Character appearance | `../../../../world-bible/character-appearance.md` | Full file | Physical details for [reason] |
| World rules | `../../../../world-bible/world-rules.md` | [Specific section] | [Specific constraint] |
```

Always explain WHY in the last column. A vague "context" is not acceptable -- name what the stage actually uses from that file.

---

## Setup Questionnaire Prerequisite Check

Every setup questionnaire produced by this builder must begin with this instruction block:

```markdown
Before asking any questions, verify that `../../world-bible/` contains no remaining `{{` patterns.
If placeholders remain, stop and tell the user: "Run `setup` in the world-bible folder first,
then push to GitHub so this workspace has the populated world files."
```

This check goes at the top of the questionnaire, before any questions.

---

## CLAUDE.md Prerequisite Note

Every CLAUDE.md produced by this builder must include a Prerequisite section:

```markdown
## Prerequisite

The world bible must be set up before this workspace. Verify no `{{` patterns remain
in `../../world-bible/` before running `setup` here.
```

---

## What NOT to Do

- Do not duplicate world bible content inside the new workspace. The canonical source is the bible. If a stage needs the protagonist's appearance, it reads `character-appearance.md` -- it does not copy the description into its own reference file.
- Do not reference world-bible files from CLAUDE.md or top-level CONTEXT.md (these must work before setup runs and should not load content).
- Do not load bible files the stage does not use. An analysis stage that never mentions characters should not load characters.md.

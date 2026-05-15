# Workspace Builder

Builds new workspaces for this sci-fi world. Every workspace this builder produces is world-aware -- world-bible references are wired in during scaffolding.

## Task Routing

| Task | Go To |
|------|-------|
| Discover the new workspace's purpose and world connection | `stages/01-discovery/CONTEXT.md` |
| Define stage contracts and bible file dependencies | `stages/02-mapping/CONTEXT.md` |
| Generate all workspace files with world-bible wiring | `stages/03-scaffolding/CONTEXT.md` |
| Validate conventions compliance and bible paths | `stages/04-validation/CONTEXT.md` |

## Pipeline Flow

```
[01-discovery] --> [02-mapping] --> [03-scaffolding] --> [04-validation]
```

## What to Load

| Task | Load These | Do NOT Load |
|------|-----------|-------------|
| Discover workflow | `references/conventions-reference.md` | Later stage outputs |
| Map stage contracts | `stages/01-discovery/output/`, `references/world-bible-wiring-guide.md` | `stages/03-scaffolding/`, `stages/04-validation/` |
| Scaffold workspace | `stages/02-mapping/output/`, `references/world-bible-wiring-guide.md`, `/_core/templates/`, `/_core/placeholder-syntax.md` | `stages/01-discovery/` |
| Validate workspace | Scaffolded workspace from stage 03 output, `/_core/CONVENTIONS.md`, `references/world-bible-wiring-guide.md` | `stages/01-discovery/`, `stages/02-mapping/` |

# Workspace Builder

Builds new workspaces for this sci-fi world. Any workspace generated here is world-aware from birth -- its stage CONTEXT.md files reference world-bible files and its setup questionnaire includes a world-bible prerequisite check.

## How This Differs from a Generic Builder

Every workspace this builder produces is a citizen of the shared world. The scaffolding stage automatically wires `../../../../world-bible/` references into the new workspace's Inputs tables and adds the world-bible prerequisite check to its setup questionnaire. You choose which bible files each stage needs during the mapping stage.

## Folder Map

```
workspace-builder/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (task routing)
├── setup/
│   └── questionnaire.md   (onboarding -- describes the workspace you want to build)
├── references/
│   ├── world-bible-wiring-guide.md   (how to wire world-bible into scaffolded workspaces)
│   └── conventions-reference.md      (pointer to _core/CONVENTIONS.md)
└── stages/
    ├── 01-discovery/      (understand the workspace purpose and world connection)
    ├── 02-mapping/        (define stage contracts and bible file dependencies)
    ├── 03-scaffolding/    (generate all workspace files with world-bible wiring)
    └── 04-validation/     (verify conventions compliance and bible path correctness)
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding -- describe the workspace you want to build |
| `status` | Show pipeline completion for all four stages |

## Routing

| Task | Go To |
|------|-------|
| Start building a new workspace | `stages/01-discovery/CONTEXT.md` |
| Define stage contracts and bible dependencies | `stages/02-mapping/CONTEXT.md` |
| Generate the workspace files | `stages/03-scaffolding/CONTEXT.md` |
| Validate the output workspace | `stages/04-validation/CONTEXT.md` |

## Stage Handoffs

01-discovery output feeds 02-mapping. 02-mapping output feeds 03-scaffolding. 03-scaffolding output feeds 04-validation. Edit any output file between stages -- the next stage picks up your changes.

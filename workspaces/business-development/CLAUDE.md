# Business Development Workspace

IP strategy and pitch workspace for this sci-fi world. Produces pitch documents, market analysis, and partnership briefs grounded in the world bible.

## Prerequisite

The world bible must be set up before this workspace. Verify no `{{` patterns remain in `../../world-bible/` before running `setup` here.

## Folder Map

```
business-development/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (task routing)
├── setup/
│   └── questionnaire.md   (biz dev onboarding)
└── stages/
    └── 01-analysis/
        ├── CONTEXT.md
        └── output/
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run biz dev onboarding -- configures pitch format, target audience, and IP strategy focus |
| `status` | Show pipeline completion for all stages |

## Routing

| Task | Go To |
|------|-------|
| Develop a pitch or market analysis | `stages/01-analysis/CONTEXT.md` |

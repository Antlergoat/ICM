# Writer Workspace

Narrative writing workspace for this sci-fi world. Produces story drafts, scene scripts, lore entries, and outlines grounded in the world bible.

## Prerequisite

The world bible must be set up before this workspace. Verify no `{{` patterns remain in `../../world-bible/` before running `setup` here.

## Folder Map

```
writer/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (task routing)
├── setup/
│   └── questionnaire.md   (writer-specific onboarding)
└── stages/
    └── 01-draft/
        ├── CONTEXT.md
        └── output/
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run writer onboarding -- configures voice, format, and narrative preferences |
| `status` | Show pipeline completion for all stages |

## Routing

| Task | Go To |
|------|-------|
| Draft a story, scene, or lore entry | `stages/01-draft/CONTEXT.md` |

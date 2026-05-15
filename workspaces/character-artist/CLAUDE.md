# Character Artist Workspace

Visual development workspace for this sci-fi world. Produces character concept briefs, appearance specifications, and design direction documents grounded in the world bible.

## Prerequisite

The world bible must be set up before this workspace. Verify no `{{` patterns remain in `../../world-bible/` before running `setup` here.

## Folder Map

```
character-artist/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (task routing)
├── setup/
│   └── questionnaire.md   (artist-specific onboarding)
└── stages/
    └── 01-concepts/
        ├── CONTEXT.md
        └── output/
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run artist onboarding -- configures style, format, and visual preferences |
| `status` | Show pipeline completion for all stages |

## Routing

| Task | Go To |
|------|-------|
| Develop a character concept brief | `stages/01-concepts/CONTEXT.md` |

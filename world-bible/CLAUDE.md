# World Bible

The canonical source of truth for the shared sci-fi world. All role workspaces reference these files. Run `setup` here first, before setting up any role workspace.

## Folder Map

```
world-bible/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (what is in each bible file and when to load it)
├── setup/
│   └── questionnaire.md   (meta-setup -- populates all world files)
├── world-overview.md      (world name, genre, premise, era, tone)
├── factions.md            (major factions, allegiances, conflicts)
├── characters.md          (protagonist and antagonist archetypes, key figures)
├── world-rules.md         (technology level, physics, society structure)
└── timeline.md            (key historical events, current moment)
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run meta-setup -- ask questions, populate all world bible files |

## Setup Order

Run this setup before any role workspace setup. The writer, character-artist, and business-development workspaces all read from these files. Until setup runs, the files contain `{{PLACEHOLDER}}` variables that will produce bad output.

After setup is complete, commit and push to GitHub so partners can pull the populated world bible before running their own workspace setups.

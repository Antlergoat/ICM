# Interpreted-Context-Methdology

ICM is a framework for building structured, multi-stage AI workflows out of markdown files and folder conventions. Each workspace gives AI agents the right context at each stage of a task, and gives humans clear edit surfaces between stages.

## Folder Map

```
model-workspace-protocol/
├── CLAUDE.md                          (you are here)
├── README.md                          (project overview)
├── LICENSE
├── _core/                             (shared conventions and templates)
│   ├── CONVENTIONS.md                 (source of truth for all patterns)
│   ├── placeholder-syntax.md          (how {{VARIABLES}} work)
│   └── templates/                     (blank starting points for new workspaces)
├── world-bible/                       (shared sci-fi world -- run setup here first)
│   ├── setup/questionnaire.md         (meta-setup -- populates all world files)
│   ├── world-overview.md
│   ├── factions.md
│   ├── characters.md
│   ├── character-appearance.md
│   ├── world-rules.md
│   └── timeline.md
└── workspaces/
    ├── writer/                        (narrative drafting grounded in world bible)
    ├── character-artist/              (character concept briefs grounded in world bible)
    ├── business-development/          (pitch and IP strategy grounded in world bible)
    ├── script-to-video-short/         (world moment -> AI video generation brief)
    ├── workspace-builder/             (builds new world-aware workspaces)
    ├── script-to-animation/           (content idea -> animated video)
    └── course-deck-production/        (unstructured material -> course PowerPoints)
```

## Routing

| You want to... | Go to |
|-----------------|-------|
| Set up the shared sci-fi world (do this first) | `world-bible/CLAUDE.md` |
| Write narrative content for the sci-fi world | `workspaces/writer/CLAUDE.md` |
| Develop character concept briefs | `workspaces/character-artist/CLAUDE.md` |
| Build pitch and IP strategy documents | `workspaces/business-development/CLAUDE.md` |
| Produce AI-generated video shorts from world moments | `workspaces/script-to-video-short/CLAUDE.md` |
| Build a new world-aware workspace for any domain | `workspaces/workspace-builder/CLAUDE.md` |
| Create content with script-to-animation | `workspaces/script-to-animation/CLAUDE.md` |
| Build course slide decks from source material | `workspaces/course-deck-production/CLAUDE.md` |
| Read the full MWP specification | `_core/CONVENTIONS.md` |
| Understand the placeholder system | `_core/placeholder-syntax.md` |
| Use a template for a new workspace | `_core/templates/` |

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding in whatever workspace you are in |
| `status` | Show pipeline completion for the current workspace |

## How It Works

Each workspace is self-contained with its own CLAUDE.md. Navigate into a workspace folder and that workspace's CLAUDE.md takes over. You do not need to read this root file once you are inside a workspace.

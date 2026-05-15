# Script to Video Short

Takes a world bible moment, character, or scene through concept development, narration scripting, shot breakdown, and AI video generation prompts. Output is a ready-to-run generation brief for tools like Kling or Runway.

## Prerequisite

The world bible must be set up before this workspace. Verify no `{{` patterns remain in `../../world-bible/` before running `setup` here.

## Folder Map

```
script-to-video-short/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (task routing)
├── setup/
│   └── questionnaire.md   (configures style, platform, and generation preferences)
└── stages/
    ├── 01-concept/        (world moment -> video concept)
    ├── 02-script-and-shots/ (concept -> narration script + shot list)
    └── 03-generation-prompts/ (shot list -> AI generation brief)
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding -- configures visual style, platform format, and AI tool preferences |
| `status` | Show pipeline completion for all three stages |

## Routing

| Task | Go To |
|------|-------|
| Define the video concept | `stages/01-concept/CONTEXT.md` |
| Write the script and shot list | `stages/02-script-and-shots/CONTEXT.md` |
| Build AI generation prompts | `stages/03-generation-prompts/CONTEXT.md` |

## Stage Handoffs

Each stage writes to its `output/` folder. The next stage reads from there. Edit any output file before running the next stage -- the agent picks up your changes.

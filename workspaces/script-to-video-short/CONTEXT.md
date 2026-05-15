# Script to Video Short

## Task Routing

| Task | Go To |
|------|-------|
| Define the video concept | `stages/01-concept/CONTEXT.md` |
| Write the script and shot list | `stages/02-script-and-shots/CONTEXT.md` |
| Build AI generation prompts | `stages/03-generation-prompts/CONTEXT.md` |

## World Bible

All stages reference `../../world-bible/`. The world bible must be fully populated (no `{{` patterns remaining) before running any stage.

## Pipeline Flow

```
[01-concept] --> [02-script-and-shots] --> [03-generation-prompts]
```

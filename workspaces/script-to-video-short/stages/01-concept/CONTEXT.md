# Stage 01: Concept

**Format:** {{TARGET_FORMAT}}
**Duration:** {{TYPICAL_DURATION}}
**Visual Style:** {{VISUAL_STYLE}}

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| World overview | `../../../../world-bible/world-overview.md` | Full file | Tone, premise, era -- anchors the concept in the world |
| Characters | `../../../../world-bible/characters.md` | Full file | Who appears in the video |
| Character appearance | `../../../../world-bible/character-appearance.md` | Full file | Visual accuracy for any character featured |
| World rules | `../../../../world-bible/world-rules.md` | Key World Rule section | The hook that makes this world distinct on screen |

Load factions.md only if the concept involves faction conflict or faction-specific imagery.

## Process

1. Read all Inputs
2. Ask the user: which character, moment, or scene from the world is the starting point?
3. Propose three concept directions -- each with a one-sentence premise, the emotional hook, and the key visual moment
4. User selects a direction (checkpoint)
5. Expand the selected concept into a full concept brief
6. Run audit
7. Save to `output/[slug]-concept.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 3 | Three concept directions | Select one before expanding |

## Audit

| Check | Pass Condition |
|-------|----------------|
| World consistency | Concept fits the tone and rules of the world bible |
| Visual achievability | Key visual moment is achievable with AI video tools |
| Duration fit | Concept is achievable within {{TYPICAL_DURATION}} |
| Hook clarity | A viewer who knows nothing about the world understands the emotional core |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Concept brief | `output/[slug]-concept.md` | Markdown with premise, hook, key visual moment, and tone notes |

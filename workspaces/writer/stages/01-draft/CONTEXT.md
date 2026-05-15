# Stage 01: Draft

**Role:** {{WRITER_ROLE}}
**Format:** {{OUTPUT_FORMAT}}
**Typical Length:** {{TYPICAL_LENGTH}}

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| World overview | `../../../../world-bible/world-overview.md` | Full file | World name, premise, era, tone |
| World rules | `../../../../world-bible/world-rules.md` | Full file | Consistency constraints |
| Characters | `../../../../world-bible/characters.md` | Full file | Archetype grounding |
| Factions | `../../../../world-bible/factions.md` | Full file | Conflict and political context |
| Timeline | `../../../../world-bible/timeline.md` | Current Moment section | Where we are in the story |

Load character-appearance.md only if the draft includes physical description of a character.

## Voice

{{VOICE_DESCRIPTION}}

Pitfalls: {{VOICE_PITFALLS}}

## Process

1. Read all Inputs
2. Confirm draft scope with the user: topic, scene or entry type, target length
3. Draft the piece
4. Run audit
5. Save to `output/[slug]-draft.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 2 | Proposed angle and opening line | Approve or redirect before drafting |

## Audit

| Check | Pass Condition |
|-------|----------------|
| World consistency | No details contradict world-rules.md |
| Voice | Matches {{VOICE_DESCRIPTION}} and avoids {{VOICE_PITFALLS}} |
| Scope | Covers what was agreed at the checkpoint |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Draft | `output/[slug]-draft.md` | Markdown |

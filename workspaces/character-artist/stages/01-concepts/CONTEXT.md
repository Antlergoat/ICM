# Stage 01: Concepts

**Art Style:** {{ART_STYLE}}
**Deliverable Format:** {{DELIVERABLE_FORMAT}}
**Tools:** {{TOOLS}}

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| World overview | `../../../../world-bible/world-overview.md` | Full file | Tone and era anchor for visual direction |
| Character appearance | `../../../../world-bible/character-appearance.md` | Full file | Canonical physical descriptions, clothing, gear, facial features |
| Characters | `../../../../world-bible/characters.md` | Full file | Personality and archetype -- informs posture, expression, silhouette |
| Factions | `../../../../world-bible/factions.md` | Full file | Faction visual markers and allegiances |
| World rules | `../../../../world-bible/world-rules.md` | Technology Level section | Constrains what gear and materials are plausible |

## Visual Priority

{{VISUAL_PRIORITY}}

**Color Approach:** {{COLOR_APPROACH}}

## Process

1. Read all Inputs
2. Confirm the character and scope with the user: which character, which deliverable format, any specific scene or context
3. Write a concept brief: silhouette notes, key visual details, color direction, reference anchors
4. Run audit
5. Save to `output/[slug]-concept-brief.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 2 | Proposed visual approach and 2-3 direction options | Select direction before the brief is written |

## Audit

| Check | Pass Condition |
|-------|----------------|
| Appearance accuracy | All physical details match character-appearance.md |
| Faction markers | Correct insignia, colors, and gear for the character's faction |
| Style consistency | Brief matches {{ART_STYLE}} and {{COLOR_APPROACH}} |
| World rules | No gear or technology contradicts world-rules.md |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Concept brief | `output/[slug]-concept-brief.md` | Markdown with labeled sections |

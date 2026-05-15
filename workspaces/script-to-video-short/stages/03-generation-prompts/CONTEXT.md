# Stage 03: Generation Prompts

**Tool:** {{VIDEO_TOOL}}
**Visual Style:** {{VISUAL_STYLE}}
**Camera Style:** {{CAMERA_STYLE}}
**Negative Prompts:** {{NEGATIVE_PROMPTS}}

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Script and shots | `../02-script-and-shots/output/` | Full file | The shot list this stage is converting to prompts |
| Character appearance | `../../../../world-bible/character-appearance.md` | Full file | Physical details translated into prompt language |
| World rules | `../../../../world-bible/world-rules.md` | Technology Level section | Constrains what technology and materials appear in prompts |

## Prompt Format

Write one prompt per shot. Each prompt includes:
- **Subject:** who or what is in frame, with physical details drawn from character-appearance.md
- **Action:** what is happening
- **Setting:** environment, lighting, atmosphere
- **Camera:** movement and framing from the shot list
- **Style:** {{VISUAL_STYLE}} applied consistently across all shots
- **Negative:** {{NEGATIVE_PROMPTS}} appended to every prompt

## Process

1. Read all Inputs
2. For each shot in the shot list, write a generation prompt following the prompt format above
3. Write a consistency header -- details that must remain identical across all shots (character appearance, lighting baseline, color grade)
4. Run audit
5. Save to `output/[slug]-generation-brief.md`

## Audit

| Check | Pass Condition |
|-------|----------------|
| Character consistency | Every prompt with a character uses identical physical description |
| Style consistency | {{VISUAL_STYLE}} appears in every shot prompt |
| Negatives | {{NEGATIVE_PROMPTS}} appended to every prompt |
| Shot coverage | One prompt exists for every shot in the shot list |
| Tool compatibility | Prompt language and structure matches {{VIDEO_TOOL}} conventions |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Generation brief | `output/[slug]-generation-brief.md` | Markdown: consistency header, then numbered prompt per shot |

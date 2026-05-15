# Onboarding Questionnaire: Script to Video Short

Read this file when the user types "setup". Before asking any questions, verify that `../../world-bible/` contains no remaining `{{` patterns. If placeholders remain, stop and tell the user: "Run `setup` in the world-bible folder first, then push to GitHub so this workspace has the populated world files."

Ask ALL questions below in a single conversational pass.

---

### Q1: What is your primary AI video generation tool?
- Placeholder: `{{VIDEO_TOOL}}`
- Files: `stages/03-generation-prompts/CONTEXT.md`
- Type: free text
- Examples: "Kling", "Runway Gen-3", "Sora", "Pika"

### Q2: What is the target platform and format?
- Placeholder: `{{TARGET_FORMAT}}`
- Files: `stages/01-concept/CONTEXT.md`, `stages/02-script-and-shots/CONTEXT.md`
- Type: free text
- Examples: "YouTube Shorts (vertical, 60 sec)", "Instagram Reel (vertical, 30 sec)", "Cinematic short (horizontal, 90-120 sec)"

### Q3: What is the visual style for this world on screen? Be specific -- reference films or describe the look.
- Placeholder: `{{VISUAL_STYLE}}`
- Files: `stages/01-concept/CONTEXT.md`, `stages/03-generation-prompts/CONTEXT.md`
- Type: free text
- Example: "Desaturated palette, heavy shadow, practical lighting. Feels like The Expanse meets Sicario -- not clean, not glossy."

### Q4: What camera style do you prefer?
- Placeholder: `{{CAMERA_STYLE}}`
- Files: `stages/02-script-and-shots/CONTEXT.md`, `stages/03-generation-prompts/CONTEXT.md`
- Type: free text
- Examples: "Handheld, close to subjects, minimal camera movement", "Slow deliberate moves, wide establishing shots, clinical framing"

### Q5: What are your negative prompts -- visual elements that must never appear?
- Placeholder: `{{NEGATIVE_PROMPTS}}`
- Files: `stages/03-generation-prompts/CONTEXT.md`
- Type: free text
- Example: "No lens flares, no glowing UI elements, no clean military uniforms, no smiling characters"

### Q6: How long is a typical short for this project?
- Placeholder: `{{TYPICAL_DURATION}}`
- Files: `stages/01-concept/CONTEXT.md`
- Type: free text
- Examples: "30 seconds", "60 seconds", "90 seconds"

---

## After Onboarding

Tell the user: "Script to video short workspace is configured. Start with `stages/01-concept/CONTEXT.md` -- give the agent a character, moment, or scene from the world and it will build out the concept."

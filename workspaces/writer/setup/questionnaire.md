# Onboarding Questionnaire: Writer Workspace

Read this file when the user types "setup". Before asking any questions, verify that `../../world-bible/` contains no remaining `{{` patterns. If placeholders remain, stop and tell the user: "Run `setup` in the world-bible folder first, then push to GitHub so this workspace has the populated world files."

Ask ALL questions below in a single conversational pass.

---

### Q1: What is your writing role in this project?
- Placeholder: `{{WRITER_ROLE}}`
- Files: `stages/01-draft/CONTEXT.md`
- Type: free text
- Examples: "lead narrative writer", "lore writer", "dialogue specialist", "short fiction"

### Q2: What is your primary output format?
- Placeholder: `{{OUTPUT_FORMAT}}`
- Files: `stages/01-draft/CONTEXT.md`
- Type: selection
- Options: Long-form prose, Scene scripts with stage directions, Structured outline plus notes, Short-form lore entries

### Q3: Describe your writing voice in one sentence -- what does it sound like?
- Placeholder: `{{VOICE_DESCRIPTION}}`
- Files: `stages/01-draft/CONTEXT.md`
- Type: free text
- Example: "Precise and understated, with occasional moments of dark humor"

### Q4: What are the hardest things to get right in this world's tone? Give a concrete example of what sounds wrong.
- Placeholder: `{{VOICE_PITFALLS}}`
- Files: `stages/01-draft/CONTEXT.md`
- Type: free text
- Example: "Avoid making the technology feel like magic -- everything should have a cost and a failure mode"

### Q5: How long is a typical draft you would produce in one session?
- Placeholder: `{{TYPICAL_LENGTH}}`
- Files: `stages/01-draft/CONTEXT.md`
- Type: free text
- Examples: "500-800 words", "one scene (1-3 pages)", "full short story (2,000-4,000 words)"

---

## After Onboarding

Tell the user: "Writer workspace is configured. When you are ready to draft, go to `stages/01-draft/CONTEXT.md`."

# Onboarding Questionnaire: Business Development Workspace

Read this file when the user types "setup". Before asking any questions, verify that `../../world-bible/` contains no remaining `{{` patterns. If placeholders remain, stop and tell the user: "Run `setup` in the world-bible folder first, then push to GitHub so this workspace has the populated world files."

Ask ALL questions below in a single conversational pass.

---

### Q1: What is your primary pitch target?
- Placeholder: `{{PITCH_TARGET}}`
- Files: `stages/01-analysis/CONTEXT.md`
- Type: free text
- Examples: "Game studios (narrative game licensing)", "Publishers (novel series)", "Streaming platforms (TV adaptation)", "Angel investors (transmedia IP development)"

### Q2: What is your primary pitch format?
- Placeholder: `{{PITCH_FORMAT}}`
- Files: `stages/01-analysis/CONTEXT.md`
- Type: selection
- Options: Executive one-pager, Full pitch deck summary (5-8 pages), Investment memo, Partnership brief

### Q3: What is the IP strategy focus -- what are you trying to protect or monetize first?
- Placeholder: `{{IP_STRATEGY}}`
- Files: `stages/01-analysis/CONTEXT.md`
- Type: free text
- Example: "Original fiction as the anchor -- everything else (games, merch, adaptation) licenses from the books"

### Q4: What tone does your pitch need -- how formal, and what impression should it leave?
- Placeholder: `{{PITCH_TONE}}`
- Files: `stages/01-analysis/CONTEXT.md`
- Type: free text
- Example: "Professional but not corporate. Should feel like a creative pitch from people who know their world, not a VC deck."

### Q5: What are the two or three comparable properties you would use in a pitch to orient a new audience?
- Placeholder: `{{COMP_TITLES}}`
- Files: `stages/01-analysis/CONTEXT.md`
- Type: free text
- Example: "The Expanse meets Blade Runner, with the faction complexity of Dune"

---

## After Onboarding

Tell the user: "Business development workspace is configured. When you are ready to develop a pitch, go to `stages/01-analysis/CONTEXT.md`."

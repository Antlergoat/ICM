# Onboarding Questionnaire: Workspace Builder

Read this file when the user types "setup". Ask ALL questions below in a single conversational pass. These answers inform the discovery conversation in Stage 01 -- they are not placeholder replacements.

---

### Q1: What is this new workspace for? Describe the domain in one sentence.
- Examples: "Designing creature concepts grounded in the world's biology", "Producing in-world audio drama scripts", "Building game design documents for a faction-based strategy game"
- Type: free text
- Purpose: Names the workspace and scopes Stage 01 discovery

### Q2: Who will use this workspace, and what is their role in the project?
- Type: free text
- Examples: "The creature artist, who designs non-humanoid species", "The audio director, who produces podcast-style lore drops"
- Purpose: Calibrates stage complexity and the setup questionnaire the builder will produce

### Q3: What is the end-to-end workflow in one sentence -- what goes in and what comes out?
- Type: free text
- Example: "Takes a creature brief from the world bible and produces a full design document with anatomy, behavior, and faction relationship notes"
- Purpose: Gives Stage 01 a starting point for deeper discovery

### Q4: Which world bible files does this workspace probably need?
- Type: free text (list any that come to mind -- Stage 02 mapping will finalize this)
- Options to consider: world-overview.md, factions.md, characters.md, character-appearance.md, world-rules.md, timeline.md
- Example: "Probably world-rules.md for biology constraints and factions.md for which faction the creature is associated with"
- Purpose: Gives Stage 02 a starting point for bible dependency mapping

### Q5: Roughly how many stages, and are any optional?
- Type: free text
- Example: "3 stages -- brief, design document, and reference sheet. All required."
- Purpose: Scopes Stage 01 discovery depth

---

## After Onboarding

Tell the user: "Ready to build. Start with Stage 01 -- Discovery. I will walk you through a conversation to map out the full workflow and world connections before we generate any files."

Then point them to `stages/01-discovery/CONTEXT.md`.

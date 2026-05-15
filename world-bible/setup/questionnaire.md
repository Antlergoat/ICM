# Onboarding Questionnaire: World Bible

Read this file when the user types "setup". Ask ALL questions below in a single conversational pass. The user should be able to answer everything in one message. Collect answers. Replace all placeholders across the specified files. After all replacements, scan the entire world-bible folder for remaining `{{` patterns. If any remain, ask for the missing information.

---

### Q1: What is the name of this world?
- Placeholder: `{{WORLD_NAME}}`
- Files: `world-overview.md`, `factions.md`, `characters.md`, `character-appearance.md`, `world-rules.md`, `timeline.md`
- Type: free text
- Example: "The Verant Expanse"

### Q2: What is the genre and subgenre?
- Placeholder: `{{GENRE}}`
- Files: `world-overview.md`
- Type: free text
- Examples: "Hard sci-fi", "Space opera", "Cyberpunk", "Biopunk military thriller"

### Q3: What is the core premise in one sentence?
- Placeholder: `{{CORE_PREMISE}}`
- Files: `world-overview.md`
- Type: free text
- Example: "A dying empire clings to power by controlling the only known source of faster-than-light travel."

### Q4: What is the setting era -- when and where does this take place?
- Placeholder: `{{SETTING_ERA}}`
- Files: `world-overview.md`
- Type: free text
- Example: "2340s, fragmented solar system after the collapse of Earth's governing coalition"

### Q5: What is the tone? Give 2-3 words and a one-sentence description.
- Placeholder: `{{TONE}}`
- Files: `world-overview.md`
- Type: free text
- Example: "Grim, precise, haunted. The world does not celebrate its heroes."

### Q6: What are the major themes of this world?
- Placeholder: `{{THEMES}}`
- Files: `world-overview.md`
- Type: free text
- Example: "Survival vs. loyalty, the cost of power, what gets left behind"

### Q7: Describe Faction 1 -- name, what they want, and what makes them distinct.
- Placeholder: `{{FACTION_1_NAME}}`, `{{FACTION_1_DESCRIPTION}}`
- Files: `factions.md`
- Type: free text

### Q8: Describe Faction 2 -- name, what they want, and what makes them distinct.
- Placeholder: `{{FACTION_2_NAME}}`, `{{FACTION_2_DESCRIPTION}}`
- Files: `factions.md`
- Type: free text

### Q9: Is there a third faction?
- Type: yes/no
- If NO: Remove `{{?FACTION_3}}` block from `factions.md`
- If YES: Fill in `{{FACTION_3_NAME}}` and `{{FACTION_3_DESCRIPTION}}` in `factions.md`

### Q10: Describe the protagonist archetype -- who are they and what drives them?
- Placeholder: `{{PROTAGONIST_ARCHETYPE}}`
- Files: `characters.md`
- Type: free text
- Example: "A former imperial soldier turned defector, driven by guilt over a massacre they failed to stop"

### Q11: Describe the antagonist archetype -- who are they and what do they believe?
- Placeholder: `{{ANTAGONIST_ARCHETYPE}}`
- Files: `characters.md`
- Type: free text
- Example: "A true believer in the empire who is convinced that order requires sacrifice -- and is right about more than the protagonist wants to admit"

### Q12: Are there other key figures (supporting characters, recurring presences)?
- Placeholder: `{{KEY_FIGURES}}`
- Files: `characters.md`
- Type: free text
- Example: "An elderly archivist who holds a secret that predates the empire; a young black-market pilot who only works for cash"
- Default: Leave blank if none defined yet

### Q13: Describe the protagonist's physical appearance -- body type, age range, defining features.
- Placeholder: `{{PROTAGONIST_PHYSICAL}}`
- Files: `character-appearance.md`
- Type: free text
- Example: "Mid-30s, lean and angular, carries old burn scarring across the left forearm. Moves like someone always checking exits."

### Q14: Describe the protagonist's typical clothing and gear -- what do they wear and carry?
- Placeholder: `{{PROTAGONIST_CLOTHING}}`
- Files: `character-appearance.md`
- Type: free text
- Example: "Worn military surplus jacket with insignia removed. Reinforced boots. Compact sidearm holstered low on the right hip."

### Q15: Describe the protagonist's hair and facial features.
- Placeholder: `{{PROTAGONIST_FACE}}`
- Files: `character-appearance.md`
- Type: free text
- Example: "Close-cropped dark hair, greying at the temples. Sharp jaw, narrow eyes. Small scar bisecting the left eyebrow."

### Q16: Describe the antagonist's physical appearance -- how do they present themselves?
- Placeholder: `{{ANTAGONIST_PHYSICAL}}`
- Files: `character-appearance.md`
- Type: free text
- Example: "Tall, immaculate posture, late 40s. Dressed always in formal imperial grey. Nothing out of place, ever."

### Q17: Describe any faction-specific visual markers -- uniforms, insignia, colors, weapons.
- Placeholder: `{{FACTION_VISUAL_MARKERS}}`
- Files: `character-appearance.md`
- Type: free text
- Example: "Imperial soldiers wear slate-grey body armor with a gold sunburst on the chest. Resistance members use no uniform -- identified by a small red thread tied to the left wrist."

### Q18: What is the technology level -- what can people do, and what are the limits?
- Placeholder: `{{TECHNOLOGY_LEVEL}}`
- Files: `world-rules.md`
- Type: free text
- Example: "Interplanetary travel is routine. FTL exists but is controlled by the empire. No AI above narrow task-specific systems -- the AI wars ended that 80 years ago."

### Q19: What is the key world rule -- the one thing that makes this world different from generic sci-fi?
- Placeholder: `{{KEY_WORLD_RULE}}`
- Files: `world-rules.md`
- Type: free text
- Example: "FTL travel requires biological tissue from a specific extinct species. The empire controls the last viable samples."

### Q20: How is society structured -- who has power, and how is it enforced?
- Placeholder: `{{SOCIETY_STRUCTURE}}`
- Files: `world-rules.md`
- Type: free text
- Example: "Three-tier caste system enforced by travel permits. Inner planets are wealthy and policed. Outer settlements are autonomous in practice but dependent on imperial supply lines."

### Q21: Where are we in the story right now -- what is the current moment?
- Placeholder: `{{CURRENT_MOMENT}}`
- Files: `timeline.md`
- Type: free text
- Example: "Six months after the destruction of the Verant Station, the empire has tightened travel restrictions and the resistance is fractured into competing cells."

### Q22: What are the 3-5 key historical events that shaped this world?
- Placeholder: `{{KEY_EVENTS}}`
- Files: `timeline.md`
- Type: free text
- Example: "The AI Wars (260 years ago), the Founding of the Empire (180 years ago), the Great Silence (40 years ago), the Verant Station Incident (6 months ago)"

---

## After Onboarding

Tell the user: "World bible is populated. Commit and push to GitHub so your partners can pull the populated files before running their own workspace setups. Then navigate to the appropriate role workspace and type `setup`."

# ICM World Builder

A collaborative AI workflow system for building a shared sci-fi world. Three roles — writer, character artist, and business development — each work in their own workspace, all grounded in a single shared world bible.

Built on the [Interpreted Context Methodology](https://arxiv.org/abs/2603.16021) by Jake Van Clief. ICM replaces multi-agent frameworks with folder structure: numbered stage folders, markdown context files, and a five-layer loading system that gives one AI agent exactly the right information at each step.

---

## How It Works

Every workspace in this repo reads from a shared `world-bible/` folder at the project root. The world bible is the single source of truth for everything in this world — names, factions, characters, appearance, rules, and history. Role workspaces never duplicate that information. They reference it.

```
ICM/
├── world-bible/               The shared canon. Set up first.
└── workspaces/
    ├── writer/                Narrative drafting
    ├── character-artist/      Character concept briefs
    ├── business-development/  Pitches and IP strategy
    ├── script-to-video-short/ AI video generation pipeline
    └── workspace-builder/     Build new world-aware workspaces
```

The setup order matters: **world-bible first, role workspaces second.** Each role workspace checks that the world bible is fully populated before it lets you proceed.

---

## Prerequisites

Everyone on the team needs these before setup:

1. **Claude Code** — the AI agent that runs these workspaces
   - Download: [claude.ai/code](https://claude.ai/code)
   - Or install via terminal: `npm install -g @anthropic-ai/claude-code`

2. **Git** — for cloning and syncing the repo
   - Download: [git-scm.com](https://git-scm.com)

3. **A GitHub account** — to pull updates after the world bible is set up

---

## Setup: Step by Step

### Step 1 — Clone the repo (everyone)

```bash
git clone https://github.com/Antlergoat/ICM
cd ICM
```

Open the `ICM` folder in VS Code (or your preferred editor) and start Claude Code inside it.

---

### Step 2 — Run world-bible setup (project lead only, do this once)

The world bible is the foundation everything else reads from. **One person runs this — ideally together on a call** so the whole team can answer the world-building questions together.

In Claude Code, navigate to the world-bible folder and run setup:

```
cd world-bible
setup
```

The agent will ask 22 questions covering:

| Category | Questions |
|----------|-----------|
| World identity | Name, genre, premise, setting era, tone, themes |
| Factions | 2-3 factions with names, goals, and what makes each distinct |
| Characters | Protagonist and antagonist archetypes, key supporting figures |
| Appearance | Physical build, clothing, gear, hair, facial features, faction visual markers |
| World rules | Technology level, the key rule that makes this world unique, society structure |
| Timeline | Current moment in the story, 3-5 key historical events |

Answer all questions in one pass. The agent replaces every `{{PLACEHOLDER}}` across the bible files with your answers. When it's done, no placeholders remain.

---

### Step 3 — Commit and push the populated world bible (project lead)

Once setup completes, push the populated bible to GitHub so everyone can access it:

```bash
git add world-bible/
git commit -m "Populate world bible"
git push
```

---

### Step 4 — Pull the world bible (all partners)

Partners pull the populated world bible before running their own workspace setup:

```bash
git pull
```

---

### Step 5 — Run your role workspace setup (each partner independently)

Each person sets up their own workspace. Navigate to your workspace folder and run setup:

**Writer:**
```
cd workspaces/writer
setup
```
Configures: writing role, output format, voice description, tone pitfalls, typical draft length.

**Character Artist:**
```
cd workspaces/character-artist
setup
```
Configures: art style, deliverable format, visual priority, color approach, tools.

**Business Development:**
```
cd workspaces/business-development
setup
```
Configures: pitch target, pitch format, IP strategy, pitch tone, comp titles.

**Script to Video Short:**
```
cd workspaces/script-to-video-short
setup
```
Configures: AI video tool (Kling, Runway, etc.), target platform and format, visual style, camera style, negative prompts, typical duration.

Each workspace setup checks that the world bible is fully populated first. If you see a message about remaining placeholders, go back to Step 4 and pull again.

---

## Using the Workspaces

After setup, every workspace runs the same way: navigate to the folder, open Claude Code, and start a task. The agent reads the right files at the right stage — you never have to tell it where to look.

### Writer

Produces story drafts, scene scripts, lore entries, and outlines grounded in the world bible.

```
cd workspaces/writer
```

Tell the agent what you want to write — a scene, a lore entry, a short story. It will:
1. Read the world bible (overview, rules, characters, factions)
2. Confirm the scope with you before drafting
3. Draft the piece
4. Run quality checks against the world rules
5. Save to `stages/01-draft/output/`

---

### Character Artist

Produces character concept briefs with visual direction, color approach, silhouette notes, and gear callouts grounded in `character-appearance.md`.

```
cd workspaces/character-artist
```

Tell the agent which character you want to develop. It will:
1. Read the world bible (appearance, characters, factions, world rules)
2. Propose 2-3 visual direction options
3. Expand the selected direction into a full concept brief
4. Run accuracy checks against the appearance guide
5. Save to `stages/01-concepts/output/`

---

### Business Development

Produces pitch documents, market analysis, and IP strategy briefs grounded in the world bible.

```
cd workspaces/business-development
```

Tell the agent what you need — a pitch deck summary, an executive brief, a partnership proposal. It will:
1. Read the world bible (overview, factions, characters, timeline, world rules)
2. Confirm the pitch scope and propose a hook sentence
3. Draft the pitch document
4. Run accuracy and tone checks
5. Save to `stages/01-analysis/output/`

---

### Script to Video Short

Takes a world moment, character, or scene through concept development, script writing, shot breakdown, and AI video generation prompts for tools like Kling or Runway.

```
cd workspaces/script-to-video-short
```

Tell the agent the starting point — a character, a scene, a moment in the world. It runs three stages:

| Stage | Input | Output |
|-------|-------|--------|
| 01-concept | A world moment or character | Video concept with premise, hook, and key visual |
| 02-script-and-shots | Approved concept | Narration script + numbered shot list |
| 03-generation-prompts | Approved shot list | Per-shot AI generation prompts with consistency header |

Each stage saves to its `output/` folder. Edit any output file before moving to the next stage — the agent picks up your changes.

---

### Workspace Builder

Builds new world-aware workspaces for any domain. Every workspace it generates automatically references the world bible — correct paths, prerequisite checks, and Inputs tables come pre-wired.

```
cd workspaces/workspace-builder
setup
```

Then work through four stages:

| Stage | What it does |
|-------|-------------|
| 01-discovery | Conversation to understand the new workspace's purpose and world connections |
| 02-mapping | Formalizes stage contracts and finalizes which bible files each stage needs |
| 03-scaffolding | Generates all workspace files with world-bible references wired in |
| 04-validation | Verifies conventions compliance and bible path correctness |

---

## Syncing Updates

When the world bible changes — a new faction, updated character appearance, revised world rules — one person makes the edit, commits, and pushes. Everyone else pulls.

```bash
# After updating a bible file
git add world-bible/
git commit -m "Update [what changed]"
git push

# Partners
git pull
```

The updated bible is immediately available to all workspaces on the next run. No other changes needed.

### In-environment change notifications (optional)

Claude Code can alert you inside the session whenever the AI modifies a world bible file. Add this hook to `.claude/settings.json` in the project root:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write|Edit",
        "hooks": [
          {
            "type": "command",
            "command": "py -c \"import sys,json; d=json.load(sys.stdin); p=d.get('tool_input',{}).get('file_path',''); fname=p.replace('\\\\\\\\','/').split('/')[-1]; print(json.dumps({'systemMessage':'World bible file changed: '+fname+' -- partners should pull before their next session.'})) if 'world-bible' in p else None\" 2>/dev/null || true"
          }
        ]
      }
    ]
  }
}
```

This fires silently for all other file edits and only surfaces when a `world-bible/` file is written. Each team member adds this to their own `.claude/settings.json` — it is gitignored by design so local hook preferences stay personal.

---

## Adding a New Workspace

Use the workspace builder. Navigate to `workspaces/workspace-builder`, run `setup`, describe the new role or domain, and walk through the four stages. The builder handles the ICM conventions and world-bible wiring automatically.

---

## Project Structure Reference

```
ICM/
├── README.md
├── CLAUDE.md                          Project routing (auto-loaded by Claude Code)
├── _core/                             ICM conventions and templates
│   ├── CONVENTIONS.md                 The 15 patterns every workspace follows
│   ├── placeholder-syntax.md          How {{VARIABLES}} work
│   └── templates/                     Blank starting points for new workspaces
├── world-bible/                       Shared world canon
│   ├── CLAUDE.md
│   ├── CONTEXT.md
│   ├── setup/questionnaire.md         22-question meta-setup
│   ├── world-overview.md              Name, genre, premise, era, tone, themes
│   ├── factions.md                    Factions and their relationships
│   ├── characters.md                  Protagonist, antagonist, key figures
│   ├── character-appearance.md        Physical descriptions, clothing, gear, facial features
│   ├── world-rules.md                 Technology, key world rule, society structure
│   └── timeline.md                    Current moment, key historical events
└── workspaces/
    ├── writer/
    ├── character-artist/
    ├── business-development/
    ├── script-to-video-short/
    └── workspace-builder/
```

---

## Credits

ICM framework created by [Jake Van Clief](https://github.com/RinDig/Interpreted-Context-Methdology).
Research paper: [Model Workspace Protocol: Folder Structure as Agent Architecture](https://arxiv.org/abs/2603.16021) (Van Clief, 2026).

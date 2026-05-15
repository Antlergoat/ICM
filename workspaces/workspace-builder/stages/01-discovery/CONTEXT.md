# Stage 01: Discovery

Understand the new workspace's purpose, workflow, and world connection through conversation.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| User | (conversation) | Full workflow description | The domain to build a workspace for |
| Conventions | `../../references/conventions-reference.md` | Full file | Know the ICM patterns to discover toward |

## Process

1. Ask the user to describe their workflow end to end -- what goes in, what comes out
2. Identify the distinct stages: where does one task end and another begin?
3. For each stage, ask: What goes in? What comes out? What does the agent need to know?
4. Identify world-bible dependencies: which bible files does each stage need, and which sections specifically?
5. Identify shared context -- what information is used across multiple stages?
6. Identify user-specific details that become placeholder variables
7. Identify optional stages
8. Identify any external tool prerequisites (system-level installs like Node.js, Python)
9. Discover relevant skills: scan `~/.claude/skills/` for domain-relevant skills, search GitHub for skill repos matching the domain, present candidates to the user
10. Checkpoint: present the workflow map draft -- are all stages captured? Bible dependencies correct?
11. Run audit
12. Save to `output/discovery-summary.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 9 | Draft workflow map: stages, bible dependencies, shared context, variables, tools, skills | Whether stage breakdown and bible dependencies are correct |

## Audit

| Check | Pass Condition |
|-------|----------------|
| Stage clarity | Every stage has a single responsibility and a named output artifact |
| Input/output chain | Every stage's inputs are user-provided or produced by a prior stage |
| Bible dependencies noted | Each stage has at least a first-pass list of world-bible files it needs |
| Variable coverage | Every user-specific detail is captured as a named placeholder |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Discovery summary | `output/discovery-summary.md` | Stages with inputs/outputs, bible dependencies, shared context, variables, tools, skills |

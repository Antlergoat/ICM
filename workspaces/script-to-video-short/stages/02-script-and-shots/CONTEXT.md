# Stage 02: Script and Shots

**Format:** {{TARGET_FORMAT}}
**Camera Style:** {{CAMERA_STYLE}}

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Concept brief | `../01-concept/output/` | Full file | The approved concept this stage is executing |
| Character appearance | `../../../../world-bible/character-appearance.md` | Full file | Physical details needed for shot descriptions |
| World overview | `../../../../world-bible/world-overview.md` | Tone section | Keeps narration voice consistent with world tone |

## Process

1. Read all Inputs
2. Write the narration script (voice-over or on-screen text) with timing markers
3. Break the script into shots -- each shot maps to a narration beat
4. For each shot: write a visual description (what the camera sees, camera move, duration)
5. Checkpoint: present full script and shot list for review
6. Revise based on feedback
7. Run audit
8. Save to `output/[slug]-script-and-shots.md`

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| Step 4 | Full script with shot list | Approve, cut shots, or revise timing before finalizing |

## Audit

| Check | Pass Condition |
|-------|----------------|
| Timing | Total shot durations sum to within 5 seconds of target |
| Character accuracy | All physical descriptions match character-appearance.md |
| Camera consistency | Shot descriptions match {{CAMERA_STYLE}} |
| Narration voice | Script tone matches world-overview.md tone |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Script and shot list | `output/[slug]-script-and-shots.md` | Markdown: narration block, then numbered shot table |

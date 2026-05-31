# Install the `design-path` skill

The `/design-path` skill diagnoses your current design constraint (in 1–2 questions) and outputs the first concrete artifact for the matching lane — Problem-first, Human-first, Craft-first, or Interaction-first.

## Quick install (Claude Code)

From a clone of [`paths-to-design`](https://github.com/mkw202/paths-to-design-):

```bash
# User-level install (works in any project)
mkdir -p ~/.claude/skills
cp -r skill/design-path ~/.claude/skills/

# Or project-level install (only available inside this project)
mkdir -p .claude/skills
cp -r skill/design-path .claude/skills/
```

Restart your Claude Code session (or open a new one). The skill should appear in your available-skills list.

## Invoke

In any Claude Code conversation:

```
/design-path
```

The skill will ask 1–2 questions, name the lane, render the lane's first artifact, and point you at the relevant book(s).

## What you'll get back

| Lane | Artifact you receive |
|---|---|
| **Problem-first** | Outcome statement, target-customer + value-prop sentence, Opportunity Solution Tree starter, 5 story-based interview prompts. |
| **Human-first** | Mental-model sketch frame, 7-stage walkthrough, cognitive-constraints checklist, 5-user usability test plan. |
| **Craft-first** | Brand prompt, color / type / space / shadow scales, hierarchy-by-de-emphasis audit. |
| **Interaction-first** | Persona with goal, scenario walkthrough, posture decision, excise audit, convention check. |

Each artifact references the source book(s) so you can deepen by reading.

## After the first artifact

The skill is v0 — it handles the **first stage** of each lane. Fill in the template, then re-run `/design-path` with your progress and your constraint will likely shift to a different lane.

## Uninstall

```bash
rm -rf ~/.claude/skills/design-path
# or for project-level:
rm -rf .claude/skills/design-path
```

## Feedback / contributing

Open an issue or PR at [github.com/mkw202/paths-to-design-](https://github.com/mkw202/paths-to-design-). Especially welcome: corrections to the lane-routing logic, better artifact templates, and additions covering later stages of each lane.

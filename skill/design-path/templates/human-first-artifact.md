# Human-first — First Artifact

You know what you're building. The job is to find where users get confused or lose trust. This artifact maps the user's mental model, names the cognitive load on each step, and gives you a 5-user usability test you can run in one afternoon.

## Source

- *The Design of Everyday Things* (Norman) — mental models, gulfs, the seven stages of action.
- *100 Things Every Designer Needs to Know About People* (Weinschenk) — cognitive constraints.
- *Don't Make Me Think* (Krug) — small-N usability testing.

---

## Step 1 — Pick ONE flow

Choose the single flow that matters most right now. Don't audit the whole product.

```
Flow:        [e.g., new-user signup → first successful action]
User goal:   [what the user is trying to accomplish]
Success:     [what "it worked" looks like from their POV — not yours]
Frequency:   [how often a user does this]
Stakes:      [low / medium / high]
```

---

## Step 2 — Sketch two mental models

The job is to find the **gulf** between what the user expects and what the system actually does.

**The user's mental model** (what they THINK is happening):

```
[Sketch in plain text.]
Example:
"I press 'Save' → I see a confirmation → my data is safe → I can find this again later by searching my title."
```

**The system's actual model** (what really happens):

```
[Be honest about the implementation reality.]
Example:
"User presses Save → API returns 200 immediately → UI shows 'Saved!' → background validation runs → on failure, silently reverts → user has no idea their save didn't stick."
```

**Gulf:** Name where they diverge.

```
Example:
Gulf of evaluation — the success message and the actual save state don't match.
```

This is the design target. Most "the UX is bad" complaints are unnamed gulfs.

---

## Step 3 — Seven-stage walkthrough

Walk Norman's seven stages of action for ONE critical action in your flow. Name the stage where the user breaks.

| Stage | The user must… | In your flow… |
|---|---|---|
| Goal | Form the goal | "Save and return tomorrow" |
| Plan | Plan how to act | "I'll look for a save button" |
| Specify | Specify the action | "Click that button" |
| Perform | Perform the action | (clicks) |
| Perceive | Perceive the result | "Saw 'Saved!'" |
| Interpret | Interpret what it means | "Great, my work is safe" ← OFTEN WRONG |
| Compare | Compare to goal | "Tomorrow: comes back, sees stale state, confused" |

The stages with friction are your design targets. Most products fail at **Interpret** (the user misreads what happened).

---

## Step 4 — Cognitive-constraints checklist

For your one flow, check each box honestly:

- [ ] **Working memory:** Does the user hold more than ~4 things in their head between screens?
- [ ] **Decisions per screen:** ≤3 visible choices on the primary path?
- [ ] **Recognition over recall:** Are we asking the user to *remember* anything from a previous screen?
- [ ] **Scanning:** Does the eye land on the most important thing first? (5-second test.)
- [ ] **Defaults:** Are defaults safe and what most users want?
- [ ] **Feedback:** Does every meaningful action produce visible, immediate, informative feedback?
- [ ] **Reversibility:** Can the user undo their last action without dread?

Each unchecked box is a fix. Rank them by how often the user touches that part of the flow.

---

## Step 5 — 5-user test plan

```
Recruits:        5 people roughly like your target user
                 (cousins, colleagues, customers — beggars-be-choosers in v0).
Time:            15 minutes each.
Setup:           Screen-share over Zoom. Record with consent.
Tasks:           3 tasks max. Phrase each as a GOAL ("Try to do X"),
                 not as steps.
Observer rule:   SHUT UP. Don't explain. If they ask "what should I do?"
                 say "what would you do?"
Capture:         (1) Where did they hesitate?
                 (2) Where did they pick the wrong thing?
                 (3) Where did they give up?
                 (4) What did they say out loud that surprised you?
```

---

## What "done" looks like

- [ ] One flow scoped and chosen.
- [ ] Two mental-model sketches with the gulf named.
- [ ] 7-stage walkthrough with friction points identified.
- [ ] Cognitive-constraints checklist completed (boxes that fail are now your backlog).
- [ ] 5 users tested; observations documented.

## Next

After fixing what the test surfaced, re-run `/design-path`. You'll likely shift to **Interaction-first** (the flow itself needed redesign, not just polish) or **Craft-first** (the flow is fine; the visuals undersell it).

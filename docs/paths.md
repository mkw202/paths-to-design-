# Four Paths to UI Design

> "There are many paths up the mountain, but the view from the top is the same."

There is no canonical sequence for becoming good at UI design. The classic books each carry strong opinions about where you *should* start, and they're each correct — for a different person at a different moment. Read in the wrong order they contradict each other; read in the right order they compound.

This is a guide to picking the path that fits **where you are right now**, with the understanding that mature practitioners cycle through all four.

## How to use this guide

1. Read the one-line premise of each path below.
2. Pick the one that matches your *current* constraint:
   - "I don't know what to build" → **Problem-first**
   - "I know what to build, but it's confusing to use" → **Human-first**
   - "I need a real artifact in front of people this week" → **Craft-first**
   - "I know the goals; the hard part is the flows" → **Interaction-first**
3. Follow the reading order. Produce the artifacts at each stage — they're how you know you're done, not just done reading.
4. When you hit a wall, switch lanes deliberately. The meta-path at the bottom covers when and how.

The eleven books referenced are summarized in [`/book-notes`](../book-notes/). Each path borrows from several; no book belongs to only one path.

---

## Path A — Problem-first

**Premise.** *"I don't know what to build yet. The first job is finding the right problem."*

Strategy-driven. You earn the right to make pixels by proving the problem is real and the audience is specific. Pixels come last.

### Reading order

1. **Inspired** — Marty Cagan
2. **Continuous Discovery Habits** — Teresa Torres
3. **The Lean Product Playbook** — Dan Olsen
4. **Don't Make Me Think** — Steve Krug
5. **Refactoring UI** — Adam Wathan & Steve Schoger
6. **Thinking with Type** — Ellen Lupton

### Stage artifacts

| Stage | Artifact | Source |
|---|---|---|
| 1 | Outcome statement + success metric | Inspired |
| 2 | Opportunity Solution Tree (outcome → opportunities → solutions → assumptions) | Continuous Discovery Habits |
| 3 | Target customer + one-sentence value proposition | Lean Product Playbook |
| 4 | Scannable IA + 5-second-test pass | Don't Make Me Think |
| 5 | Design tokens (type / color / space / shadow scales) | Refactoring UI |
| 6 | Type pairing + measure check (45–75 chars) | Thinking with Type |

### When this is right

- Genuinely new product, or a pivot.
- The customer and underserved need are not yet clear.
- Founders, early-stage PMs, anyone with a vague "I think there's something here."

### Failure modes

- Months of interviews without pixels. Discovery becomes an excuse to avoid commitment.
- Confusing validation with permission.
- Treating "outcome" as a buzzword instead of a numeric target.

---

## Path B — Human-first

**Premise.** *"I know roughly what I'm building. The job is to make it usable and humane for the people who'll touch it."*

Cognition-driven. The unit of progress is reduced confusion, not added features.

### Reading order

1. **The Design of Everyday Things** — Don Norman
2. **100 Things Every Designer Needs to Know About People** — Susan Weinschenk
3. **Don't Make Me Think** — Steve Krug
4. **About Face** — Alan Cooper et al.
5. **Refactoring UI** — Wathan & Schoger

### Stage artifacts

| Stage | Artifact | Source |
|---|---|---|
| 1 | Mental-model sketch + named gulfs (execution / evaluation) | Design of Everyday Things |
| 2 | Cognitive-constraint checklist for this task (working memory, attention, scanning, decision shortcuts) | 100 Things |
| 3 | Scannable IA + 5-user usability test | Don't Make Me Think |
| 4 | Personas, scenarios, posture decision (sovereign / transient / daemonic) | About Face |
| 5 | Hierarchy via de-emphasis; design tokens | Refactoring UI |

### When this is right

- Reshaping or improving an existing product.
- Professional tools, dashboards, internal apps.
- Healthcare, finance, safety-critical software — anywhere confusion is expensive.

### Failure modes

- Researching every detail without testing real solutions.
- "Right" interfaces no one actually uses because the underlying product is wrong (the problem is one path up).
- Slipping into Path C without admitting it.

---

## Path C — Craft-first

**Premise.** *"I need a real artifact in front of people this week. I'll validate it after it exists."*

Artifact-driven. Momentum is the constraint, and a shippable thing beats a refined deck.

### Reading order

1. **Refactoring UI** — Wathan & Schoger
2. **Thinking with Type** — Ellen Lupton
3. **Grid Systems in Graphic Design** — Josef Müller-Brockmann
4. **Don't Make Me Think** — Steve Krug *(validate)*
5. **About Face** — Alan Cooper et al. *(deepen)*

### Stage artifacts

| Stage | Artifact | Source |
|---|---|---|
| 1 | Color / type / space / shadow scales as **systems**, not ad-hoc values | Refactoring UI |
| 2 | Type pairing rationale (not "looks nice"); measure check | Thinking with Type |
| 3 | A grid (columns, gutter, baseline) chosen before any screen | Grid Systems |
| 4 | One 5-user usability pass on the shipped artifact | Don't Make Me Think |
| 5 | Excise audit and posture decision on the riskiest flows | About Face |

### When this is right

- Engineers and founders who need real screens to attract testers, investors, or co-founders.
- You've shipped enough "ugly" prototypes and lost momentum to them.
- Greenfield where the problem is reasonably clear and the bottleneck is execution speed.

### Failure modes

- Building beautiful versions of the wrong thing.
- Polishing screens for use cases no one has confirmed.
- Mistaking design-system completeness for product progress.

---

## Path D — Interaction-first

**Premise.** *"I know the goals. The hard part is designing the flows."*

Flow-driven. You're not generating ideas; you're choreographing motion through known states.

### Reading order

1. **About Face** — Alan Cooper et al.
2. **Don't Make Me Think** — Steve Krug
3. **The Design of Everyday Things** — Don Norman
4. **Refactoring UI** — Wathan & Schoger
5. **Thinking with Type** — Ellen Lupton

### Stage artifacts

| Stage | Artifact | Source |
|---|---|---|
| 1 | Personas defined by goals (not demographics); explicit scenarios | About Face |
| 2 | Posture decision; excise audit on each flow | About Face |
| 3 | Scannable IA; conventions chosen deliberately | Don't Make Me Think |
| 4 | Feedback and mapping for each significant action | Design of Everyday Things |
| 5 | Visual system applied after the flows are right | Refactoring UI / Thinking with Type |

### When this is right

- Productivity tools, B2B SaaS, multi-step workflows.
- Anything where the *flow* is the product, not the look.
- Existing product, redesigning a specific journey (signup, checkout, onboarding, settings).

### Failure modes

- Feature-shaped designs (lots of screens, no product narrative).
- Beautiful flows solving the wrong problem.
- Posture confusion — designing a sovereign app like it's a transient one.

---

## The meta-path: switching lanes

Real practitioners don't pick one path and stay there. They start where their current constraint is loudest, then switch lanes **deliberately** when the constraint changes.

| Stuck in… | Symptom | Switch to | Because |
|---|---|---|---|
| Problem-first | Months of research, no momentum, team morale eroding | Craft-first | Ship a real artifact and let the customer reaction pull the problem definition into focus. |
| Craft-first | Beautiful prototypes, low engagement, "people love it" but no usage | Problem-first | Talk to customers about the underserved need; the artifact is solving the wrong job. |
| Interaction-first | Flows feel right, screens feel wrong, users hesitate | Human-first | Audit cognitive load: what is the user paying in working memory or attention at each step? |
| Human-first | Refined, accessible, polished — and no one cares | Problem-first | Is this even the right problem? You can usability-test your way to a perfectly humane irrelevance. |

The mature move is **naming which lane you're in out loud**, so the team can call it when you've stayed too long. The lanes are not values; they are constraints. When the constraint changes, the lane changes.

---

## How this framework powers the tools

The four paths aren't a reading list — they're the **architecture** of the assistant being built on top. Every planned tool maps to one or more lanes:

- The **router skill** (`/design-path`) asks 2–3 questions to name your lane and produce the first artifact.
- **Color / typography / spacing generators** serve Craft-first directly (and Path B/D once they've made it to the visual stage).
- The **vertical gallery** serves all four — different lanes look for different things in a reference.
- **Chrome investigation** audits a deployed UI against the lane's specific checklist.

See [`docs/vision.md`](vision.md) for the full product shape and [`docs/tools.md`](tools.md) for concrete tool specs.

## Contributing

If you think a book belongs on a different path, or a path is missing, open a PR. Especially welcome from practicing designers who disagree with the routing.

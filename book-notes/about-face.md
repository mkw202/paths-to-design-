# About Face: The Essentials of Interaction Design

- **Authors:** Alan Cooper, Robert Reimann, David Cronin, Christopher
  Noessel (4th ed)
- **Editions:** 1st (1995), 4th (2014)
- **Field:** Interaction design — heavyweight reference

## Thesis
Goal-directed design — starting from what users are trying to accomplish,
not from features or technology — produces dramatically better interaction
than feature-list design. Personas, scenarios, and explicit goals are
design tools, not marketing fluff.

## Core ideas
- **Goal-directed design.** Build for goals, not tasks. Tasks change with
  the medium; goals (e.g., "feel confident I made the right diagnosis")
  persist.
- **Personas as design tools.** Specific, behaviorally grounded
  archetypes — not demographic abstractions — that designs are tested
  against ("what would Maria do here?").
- **Scenarios.** Concrete narratives walking a persona through a flow,
  used to find friction and unmet goals.
- **Posture.** Sovereign apps (full-attention, primary tool — e.g.,
  Photoshop), transient apps (brief, focused tasks), daemonic apps
  (background, low-attention). Each has a different design language.
- **Idiomatic vs. metaphorical design.** Metaphors don't scale (the
  desktop "trash can"); idioms are learned conventions that *do* scale
  (scroll wheel, undo). Prefer idiomatic.
- **Excise vs. payload.** Payload = work the user wants to do. Excise =
  work the user does for the system (navigating modes, dismissing
  dialogs). Eliminate excise.
- **Direct manipulation principles.** Selection visibility, drag and
  drop feedback, reversibility.
- **Modal dialogs are usually wrong.** Prefer non-modal feedback;
  reversible actions over confirmation prompts.
- **Undo philosophy.** Multi-level, granular, predictable. Cheaper than
  prevention dialogs.
- **Dancing bearware.** Software people tolerate because there is no
  alternative; not the standard you should aim for.

## Named frameworks & heuristics
- **Goal-directed design process:** research → modeling (personas,
  scenarios) → requirements → framework → refinement.
- **Personas, scenarios, posture.**
- **Idiomatic vs metaphorical.**
- **Excise.**

## How to apply
- Replace "user stories" or feature lists with persona goal statements.
- For every dialog you ship, ask whether it can be replaced with an
  inline non-modal interaction.
- Audit interfaces for excise: count the actions per goal that
  contribute zero to the user's intent.
- Choose your posture deliberately; densely informational sovereign apps
  look very different from transient consumer ones.

## When to reach for it
The reference for serious interaction-design work — long-running
products, complex tools, professional / operator software. Skim the
chapters not relevant to your domain.

## Caveats
- Long (~700 pages). Use as reference, not linear read.
- Some platform-specific advice has aged (Windows / desktop examples).
- Strongly opinionated; some recommendations (e.g., almost no modals)
  benefit from real-world tempering.

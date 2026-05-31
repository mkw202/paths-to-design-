# Tools (planned)

These are the executable surfaces of paths-to-design — what the assistant *does*, beyond pointing at the right book. **Every tool maps to one or more of the four paths**; the framework is the architecture, not decoration.

Status legend: **shipped** / **next** / **planned**.

---

## `/design-path` (the router skill)

- **Lane:** all four (it's the diagnostic).
- **Status:** **shipped (v0)** — install instructions at [`skill/design-path/INSTALL.md`](../skill/design-path/INSTALL.md).
- **Spec:** A Claude Code skill that asks the user 1–2 questions about their current constraint, names the lane (Problem / Human / Craft / Interaction), and outputs the first concrete artifact for that lane:
  - Problem-first → outcome statement + target-customer/value-prop + Opportunity Solution Tree + story-based interview prompts
  - Human-first → mental-model sketch + 7-stage walkthrough + cognitive-constraints checklist + 5-user test plan
  - Craft-first → brand prompt + color/type/space/shadow scales + hierarchy-by-de-emphasis audit
  - Interaction-first → persona-with-goal + scenario walkthrough + posture decision + excise audit
- **v0 scope:** first artifact only. Later-stage artifacts (research synthesis, IA, etc.) are next.
- Hands off to the more specific tools below when relevant.

## Color generator

- **Lane:** Craft-first.
- **Status:** planned (next).
- **Spec:** Natural-language prompt → 8–10 named hex values with rationale → output in Tailwind config / CSS custom properties / SwiftUI / Figma tokens.
- **Example:** `"January sunset on Pasadena beach"` → palette with semantic names (`--color-ember`, `--color-haze`, …) and a one-line rationale per color tying back to the prompt.
- **Optional:** reference photo upload → extract dominant colors → LLM names + balances.

## Typography generator

- **Lane:** Craft-first.
- **Status:** planned.
- **Spec:** Same pattern as the color generator.
- **Example:** `"editorial like Apartamento magazine"` → font pairing rationale (a transitional serif body + humanist sans display), recommended weights, measure range (45–75 chars), CSS / Figma output.

## Spacing & shadow generator

- **Lane:** Craft-first.
- **Status:** planned.
- **Spec:** Density + feel prompt → spacing scale + shadow elevations.
- **Examples:** `"dense like Bloomberg Terminal"` → tight 4px scale, flat shadows. `"airy like Linear"` → 8px scale, generous outer padding, layered subtle shadows.

## Vertical gallery

- **Lane:** all four (reference for what good and bad look like in your domain).
- **Status:** planned.
- **Spec:** Curated examples per vertical — restaurants, finance, legal, real estate, healthcare, e-commerce, SaaS, education, … Each entry carries:
  - The lane it represents
  - What's working (specific callouts: hierarchy, type pairing, posture)
  - What's broken (specific failure modes: uniform card grids, missing focus states, default template look)
  - Screenshot + outbound link (screenshots-for-criticism is fair use; never re-host)
- **Growth model:** hand-curated initial seed (5–10 per vertical), AI-augmented growth via crawl → classify → human approval to reach hundreds per vertical over time.
- **Differentiator:** criticism-tagged, not aspirational eye-candy. Both *what to study* and *what to avoid* live in the same gallery.

## Chrome investigation

- **Lane:** all four (audits against each lane's checklist).
- **Status:** planned.
- **Capability:** available today via Playwright MCP and chrome-devtools-mcp; the work is the lane-informed ruleset, not the browser plumbing.
- **Spec:** User points the assistant at a deployed URL. The assistant navigates, snapshots, reads console messages, and audits against the lane's checklist:
  - **Craft-first:** spacing-scale violations, off-scale type sizes, color-system count (too many neutrals? too many accents?), measure (chars per line on body text), shadow consistency, missing focus states.
  - **Human-first:** axe-core accessibility audit; per-screen decision count (working memory load); 5-second-test simulation against the hero; cognitive constraints checklist.
  - **Interaction-first:** posture consistency (sovereign vs transient vs daemonic), excise count per flow, undo coverage, modal-dialog abuse.
  - **Problem-first:** less applicable (the work is upstream of the UI); minimal audit.
- **Output:** ranked findings with line/element references where possible, each tagged with the path principle being violated.
- **Differentiator vs. Lighthouse/axe:** lane-aware, opinionated about *design quality* not just *accessibility/perf rules*.

---

## Why this is the right product shape

Each tool maps to one or more paths. A user enters via the router, gets a lane, and the tools relevant to that lane are immediately useful. The Chrome audit closes the loop:

```
problem → lane → next artifact → build → audit → revise → next lane
```

Books deepen the lane. Tools execute it. The framework is what makes it all hang together.

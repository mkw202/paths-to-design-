# Vision

paths-to-design is the **AI-native design assistant for non-designers** — engineers, founders, and PMs who ship interfaces every week without design training.

## The bet

Most people learning design already have access to the classic books and the prior art. What they don't have is **a map of when each book is the right book**, and the working tools that let them act on it. Build the map well, layer the tools on top, and the existing literature stops contradicting itself and starts compounding.

## Who it's for

**Built for:**
- Engineers, founders, and PMs who can ship code or write specs but freeze when asked to design a UI.
- The person who's read three design books and feels more confused, not less.
- Teams onboarding non-designers into design work.
- Self-taught designers who want a structured framework around the books they've already absorbed.

**Not built for:**
- Trained designers with a working framework already.
- Portfolio-building beginners.
- People looking for a "design school."

## The destination (12–24 months)

A publicly-installable assistant that, given a designer-in-the-moment, asks 2–3 questions about where they are stuck, names the lane (Problem / Human / Craft / Interaction), and produces the **next concrete artifact** for that lane.

- **Books** deepen the lane.
- **Generators** (color, typography, spacing) produce real starting tokens from natural-language prompts like *"January sunset on Pasadena beach"* or *"cherry blossom in Japan"*.
- **Vertical galleries** show what good and bad look like in your domain (restaurants, finance, legal, real estate, healthcare, e-commerce).
- **Chrome investigation** points at your deployed UI and tells you what's actually wrong — grounded in your lane's checklist, not generic Lighthouse rules.

The four paths route you. The skill diagnoses you. The tools execute the lane. The Chrome audit closes the loop.

## Three horizons

| Horizon | State |
|---|---|
| **Now** | Book notes + four-paths framework + lane-switching guide. Static knowledge base. |
| **3–6 months** | Claude Code skill `/design-path` (lane diagnosis + first artifact). Color generator from natural-language prompts (Craft-first MVP). 20–30 vertical samples seeded across 5–6 verticals with critique callouts. |
| **6–12 months** | Chrome investigation — point at a URL, get a lane-informed audit. Typography & spacing generators. Hundreds of vertical samples via AI-augmented curation (crawl, classify, human approval). |
| **12–24 months** | Web-installable skill (not Claude Code only). Community-contributed paths, samples, and generators. Cross-domain spinoffs (paths-to-frontend, paths-to-API-design). |

## Anti-scope

paths-to-design is **not**:
- A design school. No curriculum, no certification, no instructor.
- A portfolio platform. We don't host your work.
- A replacement for a real designer. If you can hire one, do.
- Opinionated about visual style. Brutalism, glass, Swiss, editorial — none of our business. The generators output tokens for whatever style you tell them to.

paths-to-design **is** opinionated about:
- Which path fits which starting point.
- That the four paths are exhaustive enough for v1.
- That every tool should map to one or more paths (the framework is the architecture, not decoration).
- That the Chrome audit critiques the UI against the lane's expectations, not against generic accessibility rules.

The repo is a routing layer plus the tools that execute each lane.

## Why this, why now

Two things shipped in the last 18 months that change what's buildable:

1. **LLM-driven natural-language-to-design-token generation** — "cherry blossom in Japan" → a real palette with named hex values and rationale — works well enough to be a primary surface, not a gimmick.
2. **Browser MCP servers** (Playwright, chrome-devtools-mcp) — an agent can navigate, snapshot, read console messages, and audit a deployed UI against an opinionated checklist.

Building the framework with these tools as **first-class artifacts** (not bolt-ons) is the v1 thesis. A book-based knowledge base alone is 2019. A framework + AI-native tools assistant is 2026.

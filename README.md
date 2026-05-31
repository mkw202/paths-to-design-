# paths-to-design

> The AI-native design assistant for non-designers — engineers, founders, and PMs who ship interfaces every week without design training. There is no single right way to design a UI; there are four. paths-to-design is the routing layer that tells you which fits where you are, plus the tools to execute it.

## The bet

Most people learning design already have access to the classic books and the prior art. What they don't have is **a map of when each one is right**, and the working tools that let them act on it. Build the map well, layer AI-native tools on top, and the existing literature stops contradicting itself and starts compounding.

→ **[Full vision](docs/vision.md)**

## The four paths

1. **Problem-first** — strategy-driven. *"I don't know what to build yet."*
2. **Human-first** — cognition-driven. *"I know what I'm building; it's confusing to use."*
3. **Craft-first** — artifact-driven. *"I need to ship something real this week."*
4. **Interaction-first** — flow-driven. *"I know the goals; the hard part is the flows."*

Plus the **meta-path**: switching lanes deliberately when one constraint stops being dominant. → **[Full paths framework](docs/paths.md)**

## Try it now — `/design-path` skill (alpha)

A Claude Code skill that asks 1–2 questions about your current constraint, names the lane, and outputs the first concrete artifact for it (a value-prop template, a mental-model sketch, a design-token starter, or a persona-scenario walkthrough).

```bash
git clone https://github.com/mkw202/paths-to-design-.git
mkdir -p ~/.claude/skills
cp -r paths-to-design-/skill/design-path ~/.claude/skills/
# Restart Claude Code, then invoke:
/design-path
```

Full install + uninstall steps → [`skill/design-path/INSTALL.md`](skill/design-path/INSTALL.md).

## What's shipped today (alpha)

- The four-paths framework + lane-switching guide → [`docs/paths.md`](docs/paths.md)
- The product vision and three-horizon roadmap → [`docs/vision.md`](docs/vision.md)
- **`/design-path` skill** — diagnose your lane + first artifact → [`skill/design-path/`](skill/design-path/)
- Planned tools with concrete specs → [`docs/tools.md`](docs/tools.md)
- 11 distilled book summaries grounding the framework → [`book-notes/`](book-notes/)

## What's coming

- **Color / typography / spacing generators** from natural-language prompts. *"Cherry blossom in Japan"* → a real palette with named colors and rationale, output in Tailwind / CSS / SwiftUI / Figma tokens.
- **Vertical galleries** with critique callouts — restaurants, finance, legal, real estate, healthcare, e-commerce, SaaS, education. Both *what to study* and *what to avoid* in your domain.
- **Chrome investigation** — point the assistant at your live UI's URL; get a lane-informed audit grounded in what's actually on the page (Playwright MCP / chrome-devtools-mcp under the hood).
- **Later stages of each lane** — the v0 skill outputs the FIRST artifact; subsequent stages (research synthesis, IA, etc.) are planned.

Concrete specs for each → [`docs/tools.md`](docs/tools.md).

## What this is, and isn't

**Is:** an opinionated routing layer + AI-native tools that produce concrete artifacts. Every tool maps to one or more of the four paths.

**Isn't:** a design school. A portfolio platform. A hiring replacement. A certification body. Not opinionated about brutalism vs. glass vs. Swiss — that's your call; the generators output tokens for whatever style you point them at.

## License

MIT. Use, fork, remix, ship.

## Contributing

Open an issue or a PR. The bar is *"would this help someone find their path faster, correct one I've gotten wrong, or contribute a vertical sample with a real critique callout?"*

Especially welcome:
- Practicing designers who disagree with how a book has been routed.
- Vertical-gallery contributions (one entry per PR, with what's working / what's broken / screenshot / link).
- Generator improvements (better palette naming, more output formats, image-reference extraction).
- Lane-specific Chrome audit rules grounded in the framework.

# paths-to-design

> Synthesized paths to UI/UX and product design — distilled book notes plus a multi-path framework for getting from a problem to a shipped interface, no matter where you start.

## Why this exists

There is no single right way to learn or do UI design. A founder racing to launch starts very differently from a researcher reshaping an existing product, and they're both right — for *their* starting point. The classic books each take a strong stance, and read in the wrong order they contradict each other.

This repo synthesizes 11 of those books into **four named paths** to a final design, each with its own reading order, stage artifacts, and failure modes. Plus the meta-path: how mature practitioners cycle between them.

## The four paths

1. **Problem-first** — strategy-driven. "I don't know what to build yet." (Inspired → Continuous Discovery → Lean Product Playbook → … → craft last.)
2. **Human-first** — cognition-driven. "I know what I'm building; the job is to make it usable." (Design of Everyday Things → 100 Things → Don't Make Me Think → About Face → Refactoring UI.)
3. **Craft-first** — artifact-driven. "I need to ship something real this week." (Refactoring UI → Thinking with Type → Grid Systems → … → validate after.)
4. **Interaction-first** — flow-driven. "I know the goals; design the flows that achieve them." (About Face → Don't Make Me Think → Refactoring UI.)

Plus the meta-path: switching lanes deliberately when one constraint stops being the dominant one.

→ **[Full paths analysis](docs/paths.md)**

## What's in here

- [`docs/paths.md`](docs/paths.md) — the four paths in full: premise, reading order, stage artifacts, when to use, failure modes.
- [`book-notes/`](book-notes/) — distilled summaries of the 11 source books (author, thesis, core ideas, named frameworks, how to apply, honest caveats).
- `docs/glossary.md` *(coming)* — the working vocabulary across the books (affordance, signifier, gulfs, posture, appetite, Kano, hill chart, …).
- `skill/` *(coming)* — a Claude Code skill that asks a few questions about your current constraint and recommends the path that fits.

## Status

Alpha. Book notes are stable; the four-path framework is v0; the skill doesn't exist yet. PRs and corrections welcome — especially from practicing designers who disagree with how a book has been routed.

## License

MIT. Use, fork, remix, ship. Attribution appreciated but not required.

## Contributing

Open an issue or a PR. The bar is "would this help someone find their path faster, or correct one I've gotten wrong?"

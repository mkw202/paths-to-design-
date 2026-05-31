# Craft-first — First Artifact

You need a real, intentional-looking interface in front of people this week. The job is to build the **design tokens** (color, type, space, shadow) as **systems**, not ad-hoc values, so every screen is consistent and decisions are fast.

## Source

- *Refactoring UI* (Wathan & Schoger) — the whole book; this template is its spine.
- *Thinking with Type* (Lupton) — type system specifics.

---

## Step 1 — Brand prompt (one sentence)

Pick a deliberate direction. NOT "clean and modern" — every product says this.

```
"This product should feel like [SPECIFIC EVOCATIVE REFERENCE]."
```

**Examples:**
- "Linear's calm precision"
- "Stripe Dashboard's quiet competence"
- "Apartamento magazine's editorial warmth"
- "Bloomberg Terminal's dense seriousness"
- "January sunset on Pasadena beach" (atmospheric reference works too)
- "A clinical lab's careful neutrality"

Write yours: ___________________________________________

---

## Step 2 — Color system

Build a SYSTEM, not a palette.

```
Neutrals (8 grays from lightest to darkest — most of your UI is these):
  --gray-50:  [hex]    --gray-500: [hex]
  --gray-100: [hex]    --gray-600: [hex]
  --gray-200: [hex]    --gray-700: [hex]  ← body text on white
  --gray-300: [hex]    --gray-800: [hex]
  --gray-400: [hex]    --gray-900: [hex]  ← ink, not pure black

Primary accent (6 shades of ONE hue — for action, focus, brand):
  --primary-50:  [hex]    --primary-500: [hex]  ← canonical
  --primary-100: [hex]    --primary-600: [hex]
  --primary-200: [hex]    --primary-700: [hex]

Secondary accent (use sparingly — one hue, fewer shades):
  --secondary-500: [hex]

Semantic (function, not decoration):
  --success: [hex]    --warning: [hex]    --danger: [hex]
```

**Rules:**
- One primary accent. Multiple primaries = no primary.
- Saturation low on grays (they should have a slight tint of your brand hue, not pure neutrals).
- Pure black is for ink, not UI chrome.
- Test text contrast: gray-700 on white = pass; gray-400 on white = fail.

*(Coming in this repo: a generator that builds this whole system from your Step 1 phrase. For v0, fill in by hand or start from Tailwind's slate/zinc/neutral palettes.)*

---

## Step 3 — Type scale

Pick a modular scale. Stick to it. Decisions about size become "pick from the ramp," not "guess a number."

```
--text-xs:   12px     ← captions, fine print
--text-sm:   14px     ← secondary body
--text-base: 16px     ← primary body
--text-lg:   18px
--text-xl:   20px
--text-2xl:  24px
--text-3xl:  30px
--text-4xl:  36px     ← page headings
--text-5xl:  48px     ← hero / display
```

Weights: 2–3, not 5. Common: 400 (body) / 500 (UI) / 700 (emphasis).

Body measure: 45–75 characters per line. Enforce it with max-width on long-form text containers.

---

## Step 4 — Spacing scale

```
--space-1:   4px
--space-2:   8px      ← tight gaps (icon-to-label)
--space-3:  12px
--space-4:  16px      ← default padding
--space-6:  24px
--space-8:  32px      ← section spacing
--space-12: 48px
--space-16: 64px      ← generous separation
```

**Rule:** if a value isn't on this scale, don't use it. Random pixel padding is the single biggest tell of an untrained designer.

---

## Step 5 — Shadow elevations

Layered shadows (light close + diffuse far) — not single drop-shadows.

```
--shadow-sm:
  0 1px 2px rgba(0,0,0,0.05),
  0 1px 1px rgba(0,0,0,0.04);

--shadow-md:
  0 4px 6px rgba(0,0,0,0.05),
  0 2px 4px rgba(0,0,0,0.04);

--shadow-lg:
  0 10px 20px rgba(0,0,0,0.06),
  0 4px 8px rgba(0,0,0,0.04);
```

Three elevations is enough. Don't invent a fourth.

---

## Step 6 — Hierarchy by de-emphasis

The single most important Refactoring UI insight: **don't make the important thing bigger; make the secondary stuff quieter** (less weight, less contrast, less saturation).

Audit: pick one screen in your current product. List every full-contrast (gray-900 / black) element on it. Pick ONE to keep at full strength. Quiet everything else — drop to gray-600, reduce weight, or shrink size. Re-look. Better, right?

---

## What "done" looks like

- [ ] Brand prompt written (Step 1).
- [ ] Tokens defined in code (CSS custom properties, Tailwind config, or design-token JSON).
- [ ] Type, space, shadow scales locked.
- [ ] Hierarchy audit completed on at least one screen.

## Next

Now you have a system. Apply it consistently across all screens — that consistency IS the polish. Re-run `/design-path` for **Interaction-first** (if the flows still feel off despite the polish) or **Human-first** (if users get lost despite intentional visuals).

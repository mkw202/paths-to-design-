# Refactoring UI

- **Authors:** Adam Wathan & Steve Schoger
- **Edition:** 2018 (self-published, e-book + hardcover bundle)
- **Field:** Practical visual / interaction craft for product UIs

## Thesis
Most "bad-looking" interfaces fail on a handful of craft details that
engineers don't know exist. Those details are teachable as systems — type
scales, color systems, spacing scales, shadow stacks, hierarchy by
de-emphasis. With the systems in place, design decisions reduce to
following the system.

## Core ideas
- **Start with constraints, not a blank canvas.** Build the palette, type
  scale, spacing scale, and shadow stack before designing screens.
- **Hierarchy through de-emphasis.** Don't make the important thing
  bigger — make everything else *quieter*. Less weight, less contrast,
  less saturation on secondary content.
- **Weight, not just size, drives hierarchy.** Two sizes + three weights
  beats five sizes.
- **Color systems, not palettes.** For every hue, build 8–10 shades.
  Build 8–10 grays. Distinguish neutrals from accents. Restrict accents
  to action and meaning, never decoration.
- **Type scale is a system.** A modular ramp (e.g., 12 / 14 / 16 / 18 /
  20 / 24 / 30 / 36 / 48). Pick from the scale; never invent a size.
- **Spacing scale.** 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64. Random padding
  values are the single biggest tell of an untrained designer.
- **Depth without skeuomorphism.** Layered shadows (light shadow close +
  diffuse shadow far) plus subtle gradients give realistic depth.
- **White space is a feature.** Cramming kills design. Negative space
  carries hierarchy.
- **Forms are 30% of your UI; treat them seriously.** Top-aligned labels,
  consistent input height, inline validation, visible required fields.
- **Imagery quality is non-negotiable.** Bad stock photography sinks an
  otherwise strong design.
- **Supporting elements at consistent style.** Icons one weight; one
  illustration style; one corner radius family.

## Named frameworks & heuristics
- **Type / color / space / shadow scales** as the four foundational
  systems.
- **Layered shadows** for realistic depth.
- **De-emphasis hierarchy** (the most important reframing).

## How to apply
- Before designing the first screen, define: 8 grays, 6 accent shades
  per hue, 8–10 sizes in the type scale, the spacing scale, three
  shadow elevations.
- Code review for design quality: any pixel value outside the scales is
  a flag.
- When a screen feels noisy, audit for too many full-contrast elements.
  Quiet the secondary, not amplify the primary.

## When to reach for it
Every engineer building a product UI should read it once cover-to-cover
and keep it on the shelf. It is the single highest-leverage book for
turning "looks like Bootstrap" into "looks intentional."

## Caveats
- SaaS / product-UI aesthetic specific. Less help for editorial, brand,
  print, or marketing experiences.
- Tailwind-adjacent worldview (both authors built Tailwind). Some
  conventions assume utility-class thinking.
- Light on accessibility — pair with WCAG references.

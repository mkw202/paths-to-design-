# Interaction-first — First Artifact

You know the goals; the hard part is the flows. This artifact gives you a **persona-with-goal** (not a demographic profile), one **scenario walkthrough**, a **posture decision**, and an **excise audit** — the four About-Face artifacts that route every subsequent interaction decision.

## Source

- *About Face* (Cooper et al.) — the canonical reference; this template is its core artifacts compressed.
- *Don't Make Me Think* (Krug) — convention layer applied after.

---

## Step 1 — Persona (goals, not demographics)

```
Name:            [pick one — makes the persona stickier than "User A"]
Role / context:  [their job, their situation, the moment they use your product]
Primary goal:    [what they're trying to ACCOMPLISH, not what they want to USE]
Secondary goal:  [the next-most-important thing]
Constraints:     [time, environment, skill, tools they're stuck with]
Anti-goal:       [what they explicitly do NOT want to do]
```

**Example (field service tech, chiller diagnostic):**
```
Name:            Maria
Role / context:  4-year field service tech, commercial HVAC, called to a hot building.
Primary goal:    Reach a confident root-cause within 15 minutes on-site,
                 to not delay the customer's operations.
Secondary goal:  Look competent in front of senior techs and the customer.
Constraints:     Tablet only; spotty cell signal; sometimes-cold mechanical room;
                 customer watching over her shoulder.
Anti-goal:       Reading more than 2 paragraphs of manual prose.
```

**Do NOT include:** age, gender, hobbies, brand preferences. Those are marketing personas, not design personas.

---

## Step 2 — Scenario walkthrough (present tense, concrete)

Narrate one specific instance of this persona using your product. Present tense. No "the user can" — only "Maria does."

```
[Persona name] is [doing X] when [trigger event].
She [first action]. The system [response].
She [second action]. The system [response].
She [third action]. The system [response].
...
She arrives at [the goal from Step 1].
```

**Example:**
```
Maria is finishing a coffee at 9am when a dispatch ping says
"YLAA chiller offline at Mercy Hospital, fault code 31."
She taps "New incident" in the app. The customer auto-fills from dispatch.
She types "31" in the fault-code field. The app surfaces the relevant
IOM extract in 1.2 seconds.
She drives to site, no cell signal in the parking structure. The extract
is cached locally.
She re-opens at the unit. Reads the 3 most-likely causes.
Picks "flow switch stuck open" and starts diagnosing.
She confirms the cause in 12 minutes — under her 15-minute target.
```

Write yours below. Be specific.

```
[YOUR SCENARIO HERE]
```

---

## Step 3 — Posture decision

What kind of app is this for this user, in this scenario?

```
[ ] Sovereign  — full-attention primary tool (Photoshop, Excel, IDEs).
                 Design language: dense, high-information, expert-friendly,
                 keyboard-shortcut-heavy, modes acceptable, more chrome OK.

[ ] Transient  — used briefly, single task at a time (ATMs, checkout, ride-hail).
                 Design language: simple, high-contrast, one-thing-per-screen,
                 error-tolerant, conventions strict.

[ ] Daemonic   — runs in the background, low-attention (system tray, notifications).
                 Design language: ambient, glanceable, non-intrusive.
```

Your scenario's posture: ____________________

**Why posture matters:** mismatched posture is the #1 source of "this feels wrong" in professional tools. A field tech's chiller-diagnostic app needs **sovereign** (dense, fast, expert-friendly) — designing it like a transient app (one-thing-per-screen, big buttons, no shortcuts) makes experts feel patronized.

---

## Step 4 — Excise audit

**Excise** = work the user does for the system, not toward their goal. Eliminate it.

For each action in your Step 2 scenario, mark:
- **P** = Payload (the user actually wants this action; it moves toward the goal)
- **E** = Excise (the system needs this; the user wouldn't choose to do it)

```
Action 1: __________________________________   [ P / E ]
Action 2: __________________________________   [ P / E ]
Action 3: __________________________________   [ P / E ]
Action 4: __________________________________   [ P / E ]
Action 5: __________________________________   [ P / E ]
Action 6: __________________________________   [ P / E ]
```

**Goal:** maximize P, minimize E. Every E is a design target.

**Common excise:**
- Dismissing confirmation modals on reversible actions.
- Re-entering data the system already has.
- Switching between modes when the action should be inferrable.
- Clicking through a multi-step wizard when a single page would do.
- "Are you sure?" prompts before low-stakes actions.

---

## Step 5 — Convention check

For each screen in your scenario, ask:

- Am I using **idiomatic** patterns (well-known conventions the user already knows from other software)?
- Or am I **inventing** a new way?

Inventing only pays off when the gain is large. If your novel pattern saves 0.5 seconds but costs 5 minutes of figuring out, you've lost.

List any non-idiomatic patterns in your flow and justify each:

```
Pattern 1: __________________________________
  Why invent: __________________________________

Pattern 2: __________________________________
  Why invent: __________________________________
```

If you can't write a strong "why invent" — switch to the idiomatic pattern.

---

## What "done" looks like

- [ ] Persona with explicit primary goal (not demographics).
- [ ] One scenario walked in present tense, end-to-end.
- [ ] Posture decision made and justified.
- [ ] Excise audit on the scenario (every action tagged P or E).
- [ ] Convention violations noted with justification (or removed).

## Next

Now the flows are designed. Re-run `/design-path` for **Craft-first** (apply the visual system to the screens) or **Human-first** (run a 5-user test on the scenario to find the gulfs you missed).

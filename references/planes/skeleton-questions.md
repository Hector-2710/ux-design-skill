# Skeleton — Question Bank (Ch 6)

> **Load this when** entering the **skeleton plane** — at intake when the session starts on skeleton, or when a mid-stream session back-fills into it — **see SKILL.md §6 (The plane loop)**.

**Plane's new question (AC-008g):** **"What form?"** (p. 108). *How do we know that?* "The skeleton plane… defines the form the product will take" (p. 108): the "concrete components that will make the product easy to use," including interface elements, navigation, and information design, "defined down to the level of the wireframe" (p. 111).

**Required artifacts:** `ux/skeleton.md` per `templates/skeleton.md` — interface design (3A), navigation + information design (3B), standard screens/wireframes + conventions vs deviations (3C).

**Book grounding:** Jesse James Garrett, *The Elements of User Experience* 2nd ed., **Chapter 6** (p. 108-130). Page anchors: form question (p. 108); interface design — "the arrangement of interface elements" including defaults (p. 114-118); navigation systems — global/local/supplementary/contextual/courtesy, "wayfinding" (p. 118-123, 127); information design — grouping/presentation of content (p. 124-127); **standard screens** + wireframes (p. 128-130).

---

## ARTIFACT GOALS

What "done" looks like on this plane (quoted):

- **Interface arrangements defined** — "the arrangement of interface elements" so users can act naturally (p. 114); answers the form question *concretely*, including **defaults** — "the interface should be designed so the user's most likely action requires the least effort" (p. 117-118).
- **Navigation systems chosen** — global, local, supplementary, contextual, and courtesy navigation (p. 118-123) plus **wayfinding** cues so users always know "where they are and where they can go" (p. 127).
- **Information design set** — how content is "grouped, ordered, and presented" on each screen (p. 124-127).
- **Standard screens + wireframes** — a set of "standard screens" (p. 128-130) specified at wireframe level so arrangement is testable before styling (p. 130).

---

## CORE QUESTIONS

**Ordered most-important-first** (4-6 required; this bank has **5**). Each carries (a) plain phrasing, (b) book rationale, (c) new-mode and redesign-mode variants, (d) what template block it feeds.

### CORE-1 — Interface elements & arrangement
- **Phrasing:** "What interface elements do we need on each screen, and how are they arranged — with which defaults?"
- **Why this?** The skeleton "defines the concrete components that will let the user accomplish their tasks" — the button, slider, text field set that makes the flow *usable* (p. 114-118). Defaults tie effort to likelihood: "the user's most likely action should require the least effort" (p. 117-118).
- **New-mode:** "We're new — layer out the elements for our main screens."
- **Redesign-mode:** "What elements does the current product use today, and which arrangements work against the skeleton we want?"
- **Feeds:** template §3A (interface design).

### CORE-2 — Navigation & wayfinding
- **Phrasing:** "How do users move through the product — and do they always know where they are?"
- **Why this?** "Navigation… lets users move from one part of the product to another" (p. 118); systems include global, local, supplementary, contextual, and courtesy navigation (p. 120-123) — and **wayfinding** "lets users know where they are and how to get where they want to go" (p. 127).
- **New-mode:** "We're new — what are our navigation systems, and how will users always place themselves?"
- **Redesign-mode:** "What navigation exists today, and where do users currently get lost?"
- **Feeds:** template §3B (navigation + wayfinding).

### CORE-3 — Information design
- **Phrasing:** "How is content grouped and presented on each screen so users can read it efficiently?"
- **Why this?** Information design is "the presentation of information" — grouping, ordering, and emphasis — so "users can quickly and accurately understand what they're looking at" (p. 124-127). It's the information side of skeleton; it cannot be blank (AC-010h).
- **New-mode:** "We're new — how do we arrange content so the important things are obvious?"
- **Redesign-mode:** "How is information currently presented — and which groupings hide or mislead?"
- **Feeds:** template §3B (information design).

### CORE-4 — Standard screens & wireframes
- **Phrasing:** "What set of standard screens emerges — and what does each look like at wireframe level?"
- **Why this?** "A relatively small number of standard screens will emerge" that "cover the vast majority of what users will do" (p. 128); wireframes show "the overall structure" so we can test arrangement before any visual styling (p. 130). This produces a testable form.
- **New-mode:** "We're new — sketch the standard screens for our main tasks."
- **Redesign-mode:** "What screens does the current product actually have, and which are convoluted or duplicated?"
- **Feeds:** template §3C (standard screens / wireframes).

### CORE-5 — Conventions vs deviations
- **Phrasing:** "Where do we follow convention, and where do we deviate — deliberately?"
- **Why this?** Consistency with familiar patterns reduces effort (wayfinding + interface, p. 117-118, 128); deliberate deviation is fine only when it buys a clear advantage. Deviations left unexamined become arbitrary.
- **New-mode:** "We're new — which conventions will users already know, and where do we break them on purpose?"
- **Redesign-mode:** "Which conventions does the current product follow by accident, and which should it adopt or break?"
- **Feeds:** template §3C (conventions/deviations ledger).

---

## ELABORATION QUESTIONS

*Shallower variants of the cores, in substitution-ladder readiness — optional (AC-008e).*

1. **Default-effort check.** "For each main task, is the most likely action the least-effort one?" (feeds CORE-1).
2. **Wayfinding cues.** "What tells a user where they are right now on every screen?" (feeds CORE-2).
3. **Navigation taxonomy.** "Do we need global/local or contextual/supplementary nav — which systems, and why?" (feeds CORE-2).
4. **Grouping rationale.** "Why is this content grouped together rather than apart?" (feeds CORE-3).
5. **Emphasis queue.** "What is the one thing each screen must make obvious?" (feeds CORE-3).
6. **Screen count check.** "Have we kept to a small number of standard screens rather than one-off layouts?" (feeds CORE-4).
7. **Deviation justification.** "For each deliberate deviation, what does the user gain?" (feeds CORE-5).

---

## OPTIONAL STEPS

*Optional items on this plane — only if the user wants them (AC-008f); each has a substitution-ladder fallback (`references/substitution-ladder.md`).*

| Optional item | When to offer | Substitute/fallback |
|---|---|---|
| Wireframe sketches | If user is visuals-first and engaged | Text-based screen-by-element list; flagged as untested arrangement |
| Click-through prototype | If navigation choices are contested | Ordered screen narrative; flagged |
| Wayfinding audit | In redesign, if users report getting lost | Enumerate from support/feedback; flag incomplete |

_Anything skipped or substituted is recorded as an assumption in §5 of the template (AC-011) — never silently dropped._

---

## DUALITY BLOCKS

Feeds template **§3** (duality enforced structurally — AC-010e):

- **3A — FUNCTIONALITY side:** **Interface design** — elements, arrangement, defaults (p. 114-118).
- **3B — INFORMATION side:** **Navigation systems + wayfinding** (p. 118-123, 127) and **information design** — grouping/presentation (p. 124-127). Never blank (AC-010h).
- **3C — Cross-cutting:** **Standard screens + wireframes** (p. 128-130) and the **conventions/deviations ledger**.

---

## REDESIGN PROBES

*Used with `references/redesign-audit.md` at the skeleton plane's current-state step (FR-016e).*

1. "What interface elements exist on the current screens, and which mislead or misfire?"
2. "Where do users currently lose their place — on which screens is wayfinding weakest?"
3. "How is information presented today, and which groupings contradict the skeleton?"
4. "How many bespoke one-off screens exist today that should collapse into standards?"
5. "What conventions does the product violate by accident now — and what would deliberate choice change?"

---

## GATE

Per-plane minimums (FR-013b skeleton / AC-013b) — gate **Pass**/**Pass-with-backlogs**; **Blocked** only on a downward contradiction (AC-013e):

- **Interface design** specified incl. **defaults** and trade-offs (p. 114-118).
- **Navigation + wayfinding** defined (p. 118-123, 127) — the information side is non-blank (AC-010e/h).
- **Information design** grouping/presentation captured or flagged (p. 124-127).
- **Standard screens / wireframes** sketched (p. 128-130).
- **Conventions vs deliberate deviations** listed.
- Every §3 decision has a non-empty "Why"; §1 never blank.
- Sweep verdict = Pass or Pass-with-backlogs (never Blocked) — `references/verification-sweep.md`.

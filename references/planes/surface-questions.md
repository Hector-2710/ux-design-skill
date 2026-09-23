# Surface — Question Bank (Ch 7)

> **Load this when** entering the **surface plane** — at intake when the session starts on surface, or when a mid-stream session back-fills into it — **see SKILL.md §6 (The plane loop)**.

**Plane's new question (AC-008g):** **"How does it look?"** (p. 133). *How do we know that?* "On the surface plane we are finally concerned with… the actual appearance of the product" (p. 133): the sensory design of content, functionality, and brand that the user perceives.

**Required artifacts:** `ux/surface.md` per `templates/surface.md` — sensory design for functionality (3A), sensory design for information (3B), visual design comps/style guide (3C).

**Book grounding:** Jesse James Garrett, *The Elements of User Experience* 2nd ed., **Chapter 7** (p. 133-151). Page anchors: look question (p. 133); **eye path** — "where does the eye go first" and the flow across the screen (p. 137-139); **contrast + uniformity** (p. 139-143); internal/external consistency + brand (p. 143-144); **color palette + typography** (p. 145-148); style guide (p. 148-151).

---

## ARTIFACT GOALS

What "done" looks like on this plane (quoted):

- **A designed eye path** — the design knows "where the eye goes first" and guides an eye path over the screen (p. 137-139) — "the eye travels in a path" users follow to scan content.
- **Contrast & uniformity balanced** — important elements stand out via contrast while uniformity keeps the product coherent (p. 139-143): "contrast between elements draws the eye; uniformity makes the interface feel cohesive."
- **Consistency with the brand** — internal consistency (within the product) and external consistency (with the brand/other products) (p. 143-144) so the surface expresses the strategy's brand intentionally.
- **Deliberate palette & typography** — a color palette and typography chosen to serve clarity and brand (p. 145-148), not decoration.
- **A style guide** — "a compendium of all the visual decisions made" (p. 148) — palette, type, grid, logo, components — that lets the surface stay consistent at scale.

---

## CORE QUESTIONS

**Ordered most-important-first** (4-6 required; this bank has **6**). Each carries (a) plain phrasing, (b) book rationale, (c) new-mode and redesign-mode variants, (d) what template block it feeds.

### CORE-1 — Eye path
- **Phrasing:** "Where should the user's eye go first, and what path should it take across each screen?"
- **Why this?** "Where does the eye go first?" is the surface plane's central sensory question (p. 137); "the eye travels a path" defined by arrangement and emphasis (p. 137-139). Design the path deliberately or the eye wanders.
- **New-mode:** "We're new — what should users see first, and then in what order?"
- **Redesign-mode:** "Where does the current eye actually land first — and does that match intent?"
- **Feeds:** template §3A (sensory design for functionality).

### CORE-2 — Contrast & emphasis
- **Phrasing:** "How do we use contrast so the important things stand out — and uniformity so the rest stays calm?"
- **Why this?** "Contrast" draws the eye to what matters; "uniformity" keeps everything else from competing (p. 139-143). Both, not one. Signals which surface elements are primary vs secondary.
- **New-mode:** "We're new — what is the primary visual emphasis on each screen?"
- **Redesign-mode:** "Does anything currently shout that shouldn't — or hide that should stand out?"
- **Feeds:** template §3A (sensory design for functionality).

### CORE-3 — Consistency & brand
- **Phrasing:** "How consistent are we — internally and with our brand — and what impression does that leave?"
- **Why this?** Internal consistency binds the product together; external consistency ties it to the brand and other products users already know (p. 143-144). The surface expresses the strategy's brand identity (p. 38-39).
- **New-mode:** "We're new — what brand impression should every screen consistently reinforce?"
- **Redesign-mode:** "What brand impression does the current surface accidentally leave?"
- **Feeds:** template §3C (style guide + brand).

### CORE-4 — Palette & typography
- **Phrasing:** "What color palette and typography do we choose — and why these?"
- **Why this?** Color and type are the surface's most visible decisions (p. 145-148) — chosen deliberately to serve readability and brand, not as default decoration.
- **New-mode:** "We're new — pick a palette and type system, with a rationale."
- **Redesign-mode:** "What palette/type does the current product use, and what would better serve readability and brand?"
- **Feeds:** template §3C (style guide).

### CORE-5 — Style guide coverage
- **Phrasing:** "What belongs in our style guide — from palette and type to grid, logo, and components?"
- **Why this?** "A style guide is a compendium of all the visual decisions," from "color palettes and typography" to "logo treatment" (p. 148); it keeps the surface consistent without re-deciding every screen (p. 148-151).
- **New-mode:** "We're new — what are the first five things our style guide must pin down?"
- **Redesign-mode:** "What visual rules exist today, and what's missing from them?"
- **Feeds:** template §3C (style guide).

### CORE-6 — Clarify vs undermine lower planes
- **Phrasing:** "Does this surface design clarify the skeleton, structure, scope, and strategy — or undermine them?"
- **Why this?** Every choice "either supports the planes below or undermines them" (p. 136-137); the surface is where higher-plane intent becomes visible. If the surface contradicts a lower plane, it surfaces the contradiction for a back-loop, not acceptance (FR-013 / AC-013e).
- **New-mode:** "We're new — does what we've designed visually mirror the structure and strategy?"
- **Redesign-mode:** "Where does the current look actively mislead users about how the product works?"
- **Feeds:** template §4 (verification) + back-loop queue.

---

## ELABORATION QUESTIONS

*Shallower variants of the cores, in substitution-ladder readiness — optional (AC-008e).*

1. **Eye-path probe.** "Sketch or name the first three things a user sees on our main screen — in order." (feeds CORE-1).
2. **Contrast audit.** "Which element absolutely must not be missed — and does it currently get the most contrast?" (feeds CORE-2).
3. **Uniformity check.** "Do secondary elements visually recede, or do they compete?" (feeds CORE-2).
4. **Brand resonance.** "Read back three words users should feel from the surface — do they match strategy?" (feeds CORE-3).
5. **Readability floor.** "Is body text legible at target size and contrast — typographically?" (feeds CORE-4).
6. **Style-guide gaps.** "What recurring elements lack a rule — buttons, empty states, errors?" (feeds CORE-5).
7. **Low-plane mirror.** "Point at one screen element and name the skeleton/structure decision it expresses." (feeds CORE-6).

---

## OPTIONAL STEPS

*Optional items on this plane — only if the user wants them (AC-008f); each has a substitution-ladder fallback (`references/substitution-ladder.md`).*

| Optional item | When to offer | Substitute/fallback |
|---|---|---|
| Visual comps/mockups | If the user is visual and engaged | Element-by-element text comp; flagged as unrendered |
| Style-guide draft | If the product will scale | List of the five highest-value rules; flagged partial |
| Contrast testing | If accessibility is a stated concern | Best-effort contrast flag; flagged for verified testing |

_Anything skipped or substituted is recorded as an assumption in §5 of the template (AC-011) — never silently dropped._

---

## DUALITY BLOCKS

Feeds template **§3** (duality enforced structurally — AC-010e):

- **3A — FUNCTIONALITY side:** **Sensory design for functionality** — eye path, contrast/emphasis on controls and action elements (p. 137-143).
- **3B — INFORMATION side:** **Sensory design for information** — how content is visually presented for readability (p. 137-143, 145-148). Never blank (AC-010h).
- **3C — Cross-cutting:** **Consistency + brand + style guide** (p. 143-151).

---

## REDESIGN PROBES

*Used with `references/redesign-audit.md` at the surface plane's current-state step (FR-016e).*

1. "Where does the current design's eye actually land first — screenshot if you have one?"
2. "What currently shouts louder than it should, and what hides?"
3. "What brand impression does the current look leave — by accident or design?"
4. "Which visual rules are broken inconsistently across screens today?"
5. "Where does the current styling trick users about how the product actually works?"

---

## GATE

Per-plane minimums (FR-013b surface / AC-013b) — gate **Pass**/**Pass-with-backlogs**; **Blocked** only on a downward contradiction (AC-013e):

- **Eye path** defined or flagged (p. 137-139).
- **Contrast & uniformity** balanced — primary emphasis identified (p. 139-143).
- **Consistency + brand** explicit (p. 143-144).
- **Palette & typography** chosen deliberately (p. 145-148).
- **Style guide contents** defined or flagged (p. 148-151).
- **No downward contradiction** — every surface choice either clarifies or flags a lower-plane conflict (AC-013e); contradictions go to the back-loop, not the gate.
- Every §3 decision has a non-empty "Why"; §1 never blank.
- Sweep verdict = Pass or Pass-with-backlogs (never Blocked) — `references/verification-sweep.md`.

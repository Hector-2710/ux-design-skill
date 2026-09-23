# Redesign Audit — Current State, Issues, and Target

> **Load this when** mode = `redesign` (or `both`) at intake and at each plane's current-state step — **see SKILL.md §13 (New vs redesign)**.

This file is the redesign-only companion to the plane loop. In redesign mode every plane doc carries the three-section granularity **current state → issues → target**: §1 captures the existing product's facts, §2 lists the issues found (severity, evidence, trace-to-plane), and §3 records the target decisions that answer the plane's core question once the current state and issues are understood (FR-016c). The plane loop and templates themselves are identical to new-product mode; only the direction of data differs.

---

## 0. Reading-order statement

**Load this file:**
1. **at intake**, when the mode is confirmed as `redesign` (or `both` — which uses the redesign flow for a product whose target resembles a new product; there is no third flow, FR-016f);
2. **at every plane's current-state step** in the plane loop (the "import current state" step) — apply its current-state extraction probes before asking that plane's core questions;
3. **whenever a symptom found in the existing product is assigned to a plane** — run its ripple diagnostic (§4) first.

Keeping this file open for the whole session is normal in redesign mode.

---

## 1. Current-state extraction per plane

**How to ask.** For each plane, begin every core question with a *current-state probe* before the generative question, per the book's redesign pattern (FR-016e):

> "What is the current <objective / spec / architecture / navigation / visual system>, and why does it exist?"

Ask for facts first, then reasons. You want to know what exists today **and** the story of how it got that way — the story is where the failure modes (§2) and unexamined assumptions hide.

**What counts as evidence.** Two sources, both recorded in §1 with provenance:
- **Interviews** — the user's own description of the product, its history, its users, and its known trouble spots.
- **Artifacts** — screenshots, URLs, specs, the live app, and the code itself if the user grants access. Record each as `Source: <user-provided X, v./date>` in the doc's §1 (AC-005a). Imported artifacts are never modified and are treated as current state to deepen, not to re-derive.

**Per-plane extraction targets** (what "the current state" means on each plane):

| Plane | Extract: the existing product's… |
|---|---|
| strategy | current product objectives, conditions for success (if any were ever stated), brand impression, metrics tracked, users and segments believed to exist |
| scope | current feature set, current content and its owners/update cadence, anything currently out-of-scope, existing content inventory status |
| structure | current conceptual models in use, how errors are handled today, current IA (nodes, structure, organizing principles), vocabulary used to the user |
| skeleton | current interface elements and arrangement, the navigation systems present, the standard screens that exist, wayfinding cues |
| surface | current visual system: palette, typography, grid, style-guide existence, eye path, and how (or whether) it expresses brand |

If nothing exists on a plane, write `None known — starting from scratch` plus one flagged assumption in §5, exactly as in new mode (AC-005d, AC-010g).

---

## 2. The three failure-mode probes (p. 156)

The book names three ways decisions slip into a product without reference to user needs and product objectives. Probe each current-state finding for all three (definitions live in `book-cheatsheet.md` §7 — this file applies them):

- **design by default** — Does the structure follow the technology or the organization instead of the users? Probe: "Does this feature exist because the platform/team makes it easy, rather than because users need it?"
- **design by mimicry** — Is a convention adopted uncritically? Probe: "Why does this work the way it does — is there a stated reason, or is it just how everyone does it?"
- **design by fiat** — Has personal preference driven the decision? Probe: "Was this chosen for a user need or a product objective, or because someone prominent preferred it?"

Every existing decision is questioned against user needs and objectives; a hit becomes a candidate issue (§3 classification). Don't stop at naming the failure mode — record the evidence that shows it and which plane the decision actually belongs to.

---

## 3. Issue classification vocabulary (shared with the issues template)

Issue classification uses **exactly the severity and category vocabulary defined in `templates/issues.md`** (contract C-3) — never a parallel vocabulary. Copy the definitions from that template rather than re-inventing them:

- **Severity:** Critical, High, Medium, Low (see `templates/issues.md` for the one-line definition of each).
- **Category:** Missing, Misaligned, Scope creep, Contradiction, Assumption-flag (same source).

In the current plane's §2 issues table, record each issue with `# / description / severity / evidence / trace-to-plane`. The **trace-to-plane** column is the plane the issue *belongs* to, which may differ from the plane where the symptom appears — assign it only after the ripple diagnostic in §4. Severity/category reuse guarantees that the per-plane §2 findings and the final consolidated `ux/issues.md` speak the same language.

---

## 4. Ripple diagnostics — the "big purple button" lesson (p. 154)

The book's example: the client wants to change a big purple button on the homepage, but *how* you change it depends on which plane the problem actually lives on — it could be a surface problem (the button's look), a skeleton problem (its placement and prominence), a structure problem (the conceptual model it triggers), or a scope/strategy problem (whether the action behind it should exist at all).

**Rule:** before assigning a symptom to a plane, test it against **all five planes**:

1. strategy — does the symptom imply wrong objectives or unmet user needs?
2. scope — is the feature/content behind it wrong, missing, or extra?
3. structure — is the conceptual model, flow, or error handling wrong?
4. skeleton — is the arrangement, navigation, or information grouping wrong?
5. surface — is it purely a presentation issue?

Assign the issue to the **lowest plane that explains it** (that's where a fix belongs); record higher-plane symptoms as *manifestations*. A single symptom can produce issues on multiple planes — that is normal and expected. The same habit is used in the final code-comparison pass (SKILL.md §15).

---

## 5. Content inventory habit (p. 74)

Before redesigning an existing product, build (or extend) a **content inventory** — an enumeration of all existing content so everyone knows exactly what they have to work with (p. 74). In this skill:

- At the **scope plane's current-state step**, ask the user to enumerate the content the product has today: main sections, pages, documents, media, and who owns each.
- Record whatever they can enumerate **with a completeness marker** (`Inventory incomplete` → flagged assumption in §5 if partial — see `substitution-ladder.md` item 5).
- Use the inventory to drive the content-requirement and out-of-scope decisions: content present but no longer needed is a candidate for removal; content needed but absent is a requirement.

The habit applies at every plane where existing artifacts are inventoried, not just scope: screens (skeleton), visual components (surface), vocabulary (structure) can each be inventoried the same way.

---

## 6. Competitive analysis with web disabled (AC-019e)

The skill has **no web access** (SKILL.md §16). Competitive analysis — a legitimate source of scope inspiration (p. 67-68) — is therefore **sourced from the user, not the network**:

- Ask the user to **describe** competitors' and non-competitors' approaches from memory: what they do, how they navigate, what their content/features look like.
- Ask them to **share a link or a screenshot** of a competitor they can retrieve, then analyze the artifact they supplied as current-state evidence.
- Record competitive findings with provenance in §1, and treat them as inputs to decisions, not as reasons to mimic (see the mimicry probe in §2).

Never attempt network access: no `web search`, no `webfetch`, no `curl`. If the user offers no competitive information, record that as an assumption rather than inventing competitors.

---

## Summary — this file's role in the loop

| Step in the plane loop | What redesign mode does |
|---|---|
| Intake | load this file; current-state evidence begins accumulating |
| Import current state (each plane) | run §1 probes + §5 inventory habit; record §1 with provenance |
| Core questions | prefixed with current-state probes; generative question answered as the target |
| Issues (each plane) | §2 table filled using §3 vocabulary, after §4 ripple diagnosis |
| Decisions (each plane) | target recommendations (§3) that answer the core question post-audit |
| Gate | verification sweep as usual; issues feed the §2 table only |
| Closing review & code pass | ripple diagnostics reused when findings are assigned to planes |
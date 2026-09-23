# Scope — Question Bank (Ch 4)

> **Load this when** entering the **scope plane** — at intake when the session starts on scope, or when a mid-stream session back-fills into it — **see SKILL.md §6 (The plane loop)**.

**Plane's new question (AC-008g):** **"What are we going to make?"** (p. 61). *How do we know that?* "On the scope plane we transform the strategy into the requirements of the product" (p. 57); the answer "tells us what we plan to build and what we plan not to build" (p. 59-60). *"What are we going to make — and what are we not going to make?"* (p. 60-61).

**Required artifacts:** `ux/scope.md` per `templates/scope.md` — functional specifications (3A), content requirements incl. ownership and update cadence (3B), out-of-scope/backlog + prioritization + product-wide constraints (3C).

**Book grounding:** Jesse James Garrett, *The Elements of User Experience* 2nd ed., **Chapter 4** (p. 57-77). Page anchors: the scope question (p. 60-61); functional specifications + the four writing rules (p. 62-71); content requirements + content inventory (p. 71-74); prioritization against "strategy and the feasibility of implementing" (p. 74-77); "what's out of scope" (p. 59-60); brand + technical constraints (p. 65). *"We should know what we're building and, just as important, what we're not building."* (p. 59-60)

---

## ARTIFACT GOALS

What "done" looks like on this plane (quoted):

- **Functional specifications** written as "a detailed description of the 'feature set' of the product" — every requirement stated **positive, specific, non-subjective, and quantitative where possible**: "State the requirement in positive terms… be specific… avoid subjective criteria… add quantification to specifications, where possible" (p. 70-71). "Functional specifications… define what the product will do for the user" (p. 62-63).
- **Content requirements** — "a description of the various content elements that will be required" defined by "size, format, ownership, currency, and relevance" (p. 74); for the "various content elements… as size, format, [and] ownership" of each (p. 71-72). Includes a content inventory habit where feasible (p. 74).
- **Explicit out-of-scope list** — "knowing what we're not building" recorded alongside what we are: out-of-scope items go to the backlog, where "there's a better chance that we'll be able to reconsider them" (p. 59-60).
- **Prioritized requirements** — candidate requirements "evaluated against the strategy… and the feasibility of implementing" them, scored so the team knows "what level of effort is involved" (p. 74-77) — a scored ranking between "must have" and "backlog."
- **Conditions / constraints** — product-wide constraints flagged early: branding ("brand identity… consistent with the strategy plane") and technical/hardware limits (p. 65) — because scope is where "the important [constraint] decisions… get made."
- **Content ownership + cadence** — "who is responsible for creating and maintaining" each content element and "how often it will be updated" (p. 74), so nothing silently goes stale.

---

## CORE QUESTIONS

**Ordered most-important-first** (4-6 required; this bank has **6**). Each carries (a) plain phrasing, (b) book rationale ("why this?"), (c) new-mode and redesign-mode variants, (d) the template block it feeds (AC-008f: functional specs / content requirements / out-of-scope / prioritization / constraints → template §3A/§3B/§3C).

### CORE-1 — Functional specifications
- **Phrasing:** "What features will the product offer — what will it do?"
- **Why this?** "Functional specifications define what the product will do for the user" (p. 62-63) — they are the foundation of scope ("the feature sets that describe the product we are building," p. 62). Written via the **four rules**: positive, specific, non-subjective, quantitative-where-possible (p. 70-71).
- **New-mode:** "We're starting fresh — what should the product let users do, in your own words?"
- **Redesign-mode:** "What does the current product do today — and which functions survive the redesign as-is, which change, which disappear?"
- **Feeds:** template §3A (functional specifications); violations of the four rules get pushed back once, then flagged (AC-013c).

### CORE-2 — Content requirements
- **Phrasing:** "What content will the product include — and what defines each content element?"
- **Why this?** The information side of scope: "content requirements are the answers to questions about what content the product needs" (p. 71) — "content elements" defined by **size, format, ownership, currency, and relevance** (p. 74). Scope is only half-real if it lists features but not the content those features serve (duality AC-010e).
- **New-mode:** "We're new — what content do users need, and what will it take to support it?"
- **Redesign-mode:** "What content does the current product carry today, and which of it is required vs. baggage (content inventory, p. 74)?"
- **Feeds:** template §3B (content requirements + inventory); uncontrolled items → flagged.

### CORE-3 — Out of scope / backlog
- **Phrasing:** "What are we explicitly *not* building — now, and ever?"
- **Why this?** "As important as understanding what we're building is understanding what we're not building" (p. 59); out-of-scope items get pushed to the backlog "with a better chance… we'll be able to reconsider them" later (p. 60). A product that tries to be everything serves no strategy (strategy discipline, p. 44-45).
- **New-mode:** "We're starting from scratch — what are we deliberately leaving out of the first version?"
- **Redesign-mode:** "What does the current product do that we're intentionally stopping or cutting?"
- **Feeds:** template §3C (out-of-scope + backlog row); never an empty list (AC-010h).

### CORE-4 — Prioritization
- **Phrasing:** "Of everything we could build — which do we build first, and why those?"
- **Why this?** "Prioritizing requirements… means evaluating them against the strategy and against the feasibility of implementing them" (p. 74-77). A requirement that serves neither the strategy's objectives nor the user's needs "isn't going to help anybody" (p. 74-75).
- **New-mode:** "We're new — what's the must-have core that proves the strategy, before anything optional?"
- **Redesign-mode:** "Which existing feature does user feedback most demand we fix — and which do power users use most (proxy for priority)?"
- **Feeds:** template §3A/§3B (priority column) + §3C (canonical scoring: strategy-tie + feasibility, p. 74-77).

### CORE-5 — Product-wide constraints
- **Phrasing:** "What constraints apply to *everything* we build — brand, technology, hardware?"
- **Why this?** Scope is where "the [important] constraint decisions" get made: "brand identity" must stay "consistent with the strategy plane," and "technical" / "hardware" constraints bind every higher plane (p. 65). Constraints stated here prevent re-litigating them at skeleton/surface (AC-008f).
- **New-mode:** "We're new — what technical/hardware platform or brand rules are fixed ahead of time?"
- **Redesign-mode:** "What platform and brand constraints shaped the current product — and which are still binding?"
- **Feeds:** template §3C (constraints list) → imported into structure/skeleton/surface gates.

### CORE-6 — Content ownership & update cadence
- **Phrasing:** "Who owns each content element, and how often does it get updated?"
- **Why this?** Content requirements must define "ownership, currency, and relevance" — "who is responsible for creating and maintaining" each element and "how often it will be updated" (p. 71, 74). Unowned content is the quiet failure of the information side (AC-010h).
- **New-mode:** "We're new — who will own each piece of content going forward?"
- **Redesign-mode:** "Who owns the current content, and is that cadence still working / still in one place?"
- **Feeds:** template §3B (ownership + update-frequency columns); unknown owner → flagged assumption row.

---

## ELABORATION QUESTIONS

*Optional depth — marked **optional**; skippable without blocking the gate (AC-008e). Only ask when the user seems engaged/interested.*

1. **Requirement quality.** "Could each requirement be understood the same way by everyone building from it — is it specific and measurable?" (the four writing rules, p. 70-71).
2. **Requirement conflict.** "Where do two requirements conflict (e.g., one feature that serves two user groups differently) — and how does strategy resolve it?" (p. 63-64 → trace to strategy).
3. **Content inventory depth.** "Do you have (or can we sketch) a content inventory — the list of content required, with owners?" (p. 74).
4. **Format vs. purpose.** "Are we listing content by format (FAQ, photo) or by what it does for users — which is truer to the need?" (p. 72-73).
5. **Backlog hygiene.** "What's already in the backlog, and does anything there actually belong *in* this version now?" (p. 59-60, 74-77).
6. **Feasibility probe.** "Which requirements would you guess are hardest to build — and have we validated feasibility or flagged it as unverified?" (p. 74-77, substitution ladder).
7. **Constraint trace.** "Do any brand/technical constraints here contradict the strategy's brand identity — and do we need a back-loop?" (link lower plane, see §9).

---

## OPTIONAL STEPS

Applies to this plane: **content inventory, feasibility research, requirement prioritization scoring** (design §4.8). If any has **no data**, follow the substitution ladder — see `references/substitution-ladder.md`: ① ALWAYS ASK → ② lightweight substitute built with the user → ③ flagged assumption row in template §5 (AC-011). Nothing optional blocks the gate.

| Optional item | Substitute offered (built WITH the user) | Assumption fallback |
|---|---|---|
| Content inventory (p. 74) | List of content the user can enumerate at the keyboard, owners assigned by user | `Content inventory incomplete; ownership unassigned` |
| Feasibility data (p. 74-77) | User's best guess on build-cost for each candidate requirement | `Feasibility unverified — flagged for engineering validation` |
| Prioritization scores | Two-column reverse-sort: strategy-fit + user-need-fit first pass | `Priorities provisional — not yet validated against feasibility` |

---

## DUALITY BLOCKS

Feeds template **§3** (duality enforced by structure — AC-010e):

- **3A — FUNCTIONALITY side:** **Functional specifications** — the feature set "defined as a positive, specific, non-subjective, and quantitative-where-possible list" (p. 62-71).
- **3B — INFORMATION side:** **Content requirements** — content elements with size/format/ownership/currency/relevance (p. 71-74) + update cadence; never blank; degrades to a flagged assumption (AC-010h).
- **3C — Cross-cutting:** **Out-of-scope/backlog** (p. 59-60) + **prioritization** (strategy-fit × feasibility, p. 74-77) + **product-wide constraints** (brand + technical, p. 65).

---

## REDESIGN PROBES

*Used with `references/redesign-audit.md` at the scope plane's current-state step (FR-016e).* "In a redesign we first extract what the current product actually offers before proposing a target scope."

1. "What features does the current product offer today — from screenshots, the live app, or a spec?"
2. "What content does it currently carry, and who owns/updates it (content inventory, p. 74)?"
3. "What does it do that nothing in the strategy requires — features that exist by default, not intent?"
4. "What's already recorded as out-of-scope or backlogged — and is that still honored?"
5. "Which current feature gets the most complaints / is the least used — proxy for what the redesign should cut or fix?" (back-loop to strategy first: does cutting serve the objectives?)

---

## GATE

Per-plane minimums (FR-013b scope / AC-013b) — gate **Pass**/**Pass-with-backlogs** only; **Blocked** on a downward contradiction (AC-013e):

- **Functional specifications** follow the **four writing rules** — positive, specific, non-subjective, quantitative where possible (p. 70-71) — stated in this file (AC-013c).
- **Content requirements** non-empty, with ownership + update cadence defined **or flagged** (p. 71, 74).
- **Out-of-scope/backlog list** present (p. 59-60) — never empty.
- **Prioritization** scored against **strategy + feasibility** (p. 74-77) — a must-have core is identifiable.
- **Product-wide constraints** (brand + technical/hardware) captured or flagged (p. 65).
- Template §1, §3A, §3B, §3C, §5 all non-empty; every §3 decision has a non-empty "Why."
- Sweep verdict = Pass or Pass-with-backlogs (never Blocked) — `references/verification-sweep.md`.

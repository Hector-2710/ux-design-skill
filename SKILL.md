---
name: ux-design-skill
description: Interactive, plane-by-plane UX **design or redesign** coach grounded in Jesse James Garrett's *The Elements of User Experience*. Use when the user wants to design a new product, app, site, or feature; **redesign, audit, or improve** an existing experience; define UX strategy, scope, structure, skeleton, or surface; plan features, content, information architecture, navigation, UI/wireframes, or visual design; or compare implemented code against UX plans to produce a consolidated issues list (`ux/issues.md`). The agent asks 3–6 prioritized questions per plane, records decisions, writes one document per plane (strategy.md, scope.md, structure.md, skeleton.md, surface.md) into a `ux/` folder, and flags missing data as assumptions instead of blocking. Covers **both the functionality side** (tasks, features, tools) **and the information side** (content, meaning, architecture) of every plane, for new products and redesigns/audits alike.
license: MIT
metadata:
  version: 1.0.0
  author: Hector Rosales
  tags:
    - ux
    - design
    - redesign
    - audit
    - product-strategy
    - information-architecture
allowed-tools:
  - read
  - edit
  - write
  - list
  - glob
  - grep
  - bash
---

# UX Design Skill — Method

An interactive, plane-by-plane UX design/redesign coach grounded in Jesse James Garrett's *The Elements of User Experience* (the 5-planes model). This file is the method; every plane-specific detail lives in `references/` and `templates/` and is loaded on demand. 

## 1. When to use

**Use this skill when the user wants to:**
- design a new product, app, site, or feature;
- redesign, audit, or improve an existing experience;
- define UX strategy, scope, structure, skeleton, or surface;
- plan features, content, information architecture, navigation, UI/wireframes, or visual design;
- compare implemented code against UX plans to produce a consolidated issues list (`ux/issues.md`).

**Do NOT use this skill when…**
- the user wants single-step or one-off design advice (a color choice, a button label, "make this page nicer") rather than a plane-by-plane session;
- the work is visual/UI design only, without lower-plane (strategy/scope/structure) context — this method builds bottom-up, and every later plane traces to the planes below it.

## 2. What you will produce

By default the skill writes into a `ux/` folder in the user's working directory (configurable — the agent prompts once at intake for an override):

- `ux/session.md` — the running state machine (mode, per-plane status, back-loop queue, next question): written at intake, updated at every transition;
- `ux/strategy.md`, `ux/scope.md`, `ux/structure.md`, `ux/skeleton.md`, `ux/surface.md` — one document per plane, each written and saved **at its plane's gate, before the next plane begins**;
- `ux/issues.md` — one consolidated issues list, generated last (section 15).

Every doc mirrors its template in `templates/` — never invent a document shape. Writing is **incremental, plane by plane**: a doc is durable before any next-plane work starts, and it is never batch-written. The saved `ux/<plane>.md` files plus `session.md` are the **plan of record** — on resume these, not chat history, are the memory. Imported inputs are treated as **current state** to deepen, never re-derived, and the user's source files are never modified (imported per-plane into template §1 with provenance `Source: <X, v./date>`). Generated docs are **English**; if the user answers in another language, paraphrase their decisions into English in the docs and confirm once at the first gate (§2/§5).

## 3. The method in one screen

Five planes, built bottom-up:

1. **Strategy** — what we want to get out of the product, and what users want (product objectives + user needs).
2. **Scope** — what we are going to make (functional specifications + content requirements).
3. **Structure** — how it is going to work (interaction design + information architecture).
4. **Skeleton** — what form (interface, navigation, and information design).
5. **Surface** — how it looks and feels (sensory design that clarifies, not undermines, the planes below).

- **Bottom-up dependency + bidirectional ripple** (p. 22–24). Each plane builds on the one below, yet decisions ripple both ways: a surface decision can force a rethink all the way down to strategy. Back-loops are normal and are handled in a controlled way (sections 10–12).
- **The duality split** (p. 25–31). Every plane has a **functionality side** (tasks, features, tools) and an **information side** (content, meaning, architecture); both are covered in every plane (section 9).
- **Master check:** "**Why did you do it that way?**" (p. 157). Every decision must trace to a lower plane, a deliberately chosen convention, or a flagged assumption. Applied at every gate (section 10).
- **Marathon, not sprint** (p. 159–161); don't build the roof before you know the shape of its foundation (p. 24). The invisible planes are the first things projects cut — and the highest leverage.

## 4. Mode detection (intake)

Run `references/intake.md` **always — first, on every activation, before any design question**. Intake: detects mode — new product / redesign of existing / both (confirmed with the user, stored in `ux/session.md`, re-surfaced at every gate); detects a **starting plane** for mid-stream entry (section 12); imports existing inputs (PRD, spec, design system, mockups, analytics) for per-plane import; collects project fixtures; and writes the initial `ux/session.md`. **Do this BEFORE any questions.**

## 5. Session contract

- **One plane per session by default**, resumed via `ux/session.md` (section 12).
- At every gate, state: "**this is a natural stopping point; we can continue to <next plane> or stop here — the docs are saved for next time**".
- **Sprint warning.** If the user tries to rush or skip strategy/scope, warn **once**, recall the marathon-not-sprint reasoning (p. 159–161), and offer to proceed deliberately or defer. It is a warning, not a block.
- Update `ux/session.md` at **every** transition (mode, status change, back-loop entry, next question).
- Translation rule: paraphrase non-English user answers into English in the docs; confirm once at the first gate (also §2).

## 6. The plane loop

For every plane — in this order when starting at plane 1: **strategy → scope → structure → skeleton → surface** (back-loop arcs may revisit a lower plane; section 12):

1. **Load** the plane's question bank (`references/planes/<plane>-questions.md`) and its template (`templates/<plane>.md`). Consult `references/00-INDEX.md` on activation to know what to load and what not to.
2. **Import current state** into template §1 (existing inputs with provenance, or current-state extraction probes in redesign mode).
3. **Ask 3–6 prioritized core questions** from the bank — batched, most-important-first.
4. **Record answers** into the template copy (decisions in §3A/§3B/§3C).
5. **Apply the optional-step substitution ladder** where an optional item has no data (section 8).
6. **Write the doc at the gate** — save `ux/<plane>.md` before any next-plane work begins.
7. **Run the verification sweep** at the gate (section 10).
8. **Apply the gate criteria** (section 11).
9. **Advance** to the next plane or **back-loop** to a lower plane.

## 7. Asking rules

- **Batch questions** — group them; don't drip one at a time.
- **Core first** — ask the bank's core questions before anything else; elaboration questions only when the user is engaged.
- **Plain language** — no jargon; ask in everyday words.
- **The user answers in their own words** — the user supplies content; you shape it into the doc.
- **Never invent low-plane answers** — if the user doesn't know a lower-plane fact, record a flagged assumption (section 8), never a plausible guess.
- **Pause/scope discipline** — one plane per session by default (section 5); go deep only as far as the user wants.

## 8. Optional steps → assumptions

Optional items — personas, segmentation, success metrics, user research, content inventory, feasibility data — **never block the gate**. No-data rule, in order:

1. **Always ask first** — the user may know more than the prompt suggests.
2. **Offer the lightweight substitute** from `references/substitution-ladder.md` (e.g., provisional persona from stated audience, candidate metrics from objectives, server logs as cheap research) — built **with** the user, never alone.
3. **If still no data: record a flagged assumption** — a row in the plane template's §5 table (`item | source | why flagged | plane | how to validate | validated?`), back-referenced by the §3 decisions that lean on it.

Optional ≠ skippable: the 3A/3B section always exists; only its content may degrade to an assumption row. Keep required vs. optional material crisply distinct.

## 9. Duality rule

Every plane covers **BOTH the functionality side and the information side**, enforced structurally by the template (paired §3A/§3B sections, plus a §3C cross-cutting) and behaviorally by the gate's duality check. Never leave a side blank — a side with no data degrades to an assumption row, it does not disappear. Per-plane mapping:

- **Strategy:** 3A product objectives (goals, conditions for success); 3B user needs (segments, personas, research); 3C brand identity + success metrics.
- **Scope:** 3A functional specifications; 3B content requirements (types, sizes, ownership, update frequency, audience); 3C prioritization + out-of-scope/backlog + product-wide constraints.
- **Structure:** 3A interaction design (conceptual model, error-handling ladder); 3B information architecture (nodes, structure type, organizing principles, controlled vocabulary/metadata); 3C architecture/flow (text form).
- **Skeleton:** 3A interface design (elements, arrangement, defaults, trade-offs); 3B navigation design (systems, wayfinding) + information design (grouping, error messages); 3C standard screens + wireframe-level arrangement.
- **Surface:** 3A sensory design for functionality; 3B sensory design for information; 3C consistency, brand expression, eye-path/contrast/uniformity, color/type, style-guide + comp decisions.

## 10. Verification sweep at the gate

At every gate, run `references/verification-sweep.md` **once** — at the gate, not after every answer; don't interrogate the user on each decision. The sweep:

- asks **"Why did you do it that way?"** per decision — acceptable answers: traces to a lower plane/strategy; deliberately chosen convention with a stated reason; recorded flagged assumption. Anything else → the agent prompts the user once;
- checks for failure modes (design by default / mimicry / fiat);
- checks **upward ripples** → record in the back-loop queue, resolved at the closing review (§14);
- checks **downward contradictions** → **Blocked: do not advance** until reconciled (back-loop);
- checks duality — both §3A and §3B non-empty and consistent;
- writes the verdict — **Pass / Pass-with-backlogs / Blocked**, with reasons — into template §4.

**No cheap passes**: a sweep that rubber-stamps decisions fails the gate.

## 11. Gate criteria

**Generic gate (every plane):** required template sections non-empty (§1, §3A, §3B, §3C, §5; §2 in redesign mode); every §3 decision row has a non-empty "Why"; the sweep verdict is **Pass or Pass-with-backlogs, never Blocked**; and there is no unresolved lower-plane contradiction (any forced lower-plane change is scheduled, executed, and re-gated).

**Per-plane minimums:** see the `GATE` block of each plane's question bank for the book-grounded artifact minimums (e.g., strategy: conditions for success stated without pre-defining the path, user needs for at least the primary audience, metrics defined or flagged; scope: the four writing rules and an explicit out-of-scope list; and so on per plane).

**Required question with no answer:** the agent pushes back **once** — explains why the plane matters ("strategy feeds every later plane; without it, later gates have nothing to trace to") — and only on a second "no" records a **critical flagged assumption** and proceeds. The flow never stalls.

## 12. Resume & mid-stream

- If intake finds a starting plane N, run **back-fill**: for planes 1..N-1, ask each plane's single most important question; anything unanswered becomes a flagged assumption in that plane's template §5 and an entry in the back-loop queue.
- **Direction of travel is always upward** — from the starting plane, planes are entered only in strategy→scope→structure→skeleton→surface order (back-loops to lower planes are the only exception, and they re-gate the lower plane).
- On **resume**: read `ux/session.md` plus all existing `ux/*.md` as current state, state where the session is, and pick up at the recorded next question — **without re-interviewing**.
- The docs are the **durable memory**; `session.md` is the lightweight pointer.
- On repeat runs, existing `ux/*.md` files are **read as current state and updated in place** with a changelog entry (date / what changed / why); any destructive edit is preceded by a written statement that the content will be overwritten.

## 13. New vs redesign

New-product mode builds up from foundations; redesign/audit mode reads an existing product and then builds a target. The plane loop and templates are identical across modes — only the data direction differs. In **redesign**, load `references/redesign-audit.md` at intake and at each plane's current-state step, and every doc carries a 3-section granularity: **§1 current state → §2 issues → §3 target**. Mode "both" uses the redesign flow for a product whose target resembles a new product — there is no third flow.

## 14. Closing cross-plane review

After the surface gate, run an **interactive** two-part review before anything else:

1. **Consistency checklist** — "does any decision in a higher plane force rethinking a plane below (and vice versa)?" Walk **every** flagged back-loop item, plane pair by plane pair; resolve or schedule each.
2. **Agent summary** — one paragraph per plane plus a cross-plane consistency statement.

The user **approves** the summary before the code-comparison pass runs (§15). Disapproval → fix the cited items and re-review.

## 15. Final code-comparison pass → issues.md

Only after the closing review is approved. Read the project code (scope confirmed at intake) and compare each plane's §3 decisions against it:

- **strategy** — product shape consistent with objectives/conditions-for-success;
- **scope** — planned features/content present (Missing) or absent (Scope creep); the out-of-scope list respected;
- **structure** — implemented flows/state transitions/IA match the architecture, error handling, vocabulary;
- **skeleton** — implemented screens match the wireframe-level arrangements, navigation systems, wayfinding;
- **surface** — implemented styling matches the style-guide/palette/typography decisions.

Ripple-diagnose each finding (the issue may belong to a different plane than the code it appears in). Promote unvalidated assumptions the code could have resolved → **Assumption-flag** issues. If code is inaccessible, say so explicitly and label findings **artifact-based**. Then fill `templates/issues.md` → `ux/issues.md` and **STOP** — the implementer handoff is out of scope for this skill.

## 16. Permissions & safety

Writing is allowed (edit/write into `ux/`); **web/network access is disabled** — `allowed-tools` permits no web tool and bash is used without the network. If a write capability is unavailable in-session, **print the full doc content in chat and retry writing at the next gate** — never silently drop output. Docs are **user-owned local files** in the user's working directory; no exfiltration; sensitive strategy content stays on the user's disk.

## 17. References index

Consult `references/00-INDEX.md` on activation — it maps every file to its load trigger (the table below mirrors it exactly).

| Reference file | When to load |
|---|---|
| `references/intake.md` | Always, first, on every activation (see §4) |
| `references/planes/strategy-questions.md` | Only when entering the **strategy** plane (see §6) |
| `references/planes/scope-questions.md` | Only when entering the **scope** plane (see §6) |
| `references/planes/structure-questions.md` | Only when entering the **structure** plane (see §6) |
| `references/planes/skeleton-questions.md` | Only when entering the **skeleton** plane (see §6) |
| `references/planes/surface-questions.md` | Only when entering the **surface** plane (see §6) |
| `references/redesign-audit.md` | Only in **redesign (or both) mode** — at intake and every current-state step (see §13) |
| `references/substitution-ladder.md` | Only when an **optional step has no data** (see §8) |
| `references/verification-sweep.md` | Only **at a plane's gate** (see §10) |
| `references/book-cheatsheet.md` | Only for **book grounding / definition needs** (see §3) |
| `references/examples/new-product-session.md` | Only for **first-time users or confusion** about a plane (see §6) |
| `references/examples/redesign-session.md` | Only for **first-time redesign users or confusion** (see §13) |
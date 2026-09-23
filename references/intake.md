# Intake — Always First

> **Load this when** — always, on every activation or new session, before any design question — **see SKILL.md §4 (Mode detection (intake))**.
>
> **No design questions before intake completes** (AC-003a, AC-003d). You may greet the user, but the first substantive work is this script.

Intake is the one-time step that sets up the whole session: it greets the user, detects the **mode** (new / redesign / both), detects **mid-stream entry** (a starting plane with lower planes to back-fill), finds **existing inputs** to import, records **project fixtures**, and writes the initial `ux/session.md`. Everything after it — every plane, every gate, the closing review, the code-comparison pass — keys off the records made here. If the session is being **resumed** (a `ux/session.md` already exists from a previous session), intake still runs, takes the confirmation, then hands off to SKILL.md §12 (Resume & mid-stream) instead of re-interviewing.

---

## 0. The intake checklist (run in this order)

1. **Greet and set expectations** — 5 planes, one plane per session by default.
2. **Probe the mode** — new product / redesign existing / both, with distinct trigger-language; **confirm the mode with the user**.
3. **Probe for mid-stream entry** — "have any planes already been decided?" If yes, detect the starting plane `N` and **back-fill** planes `1..N-1`.
4. **Probe for existing inputs** — PRD / spec / design system / mockups / analytics; import per plane with provenance.
5. **Record project fixtures** — product name, working directory, desired output folder (default `ux/`), which optional artifacts exist vs. are wanted.
6. **Write the initial `ux/session.md`** — per contract C-1 (FR-014).

There is no step zero shortcut: even a user who says "just ask me a question" gets the greeting and the mode probe first. If the user refuses every probe, record the mode as a flagged assumption and proceed — the flow never stalls, but you never skip intake silently.

---

## 1. Greeting and expectations

Open with a short, plain-language framing so the user knows what they signed up for:

> "We'll design (or redesign) this product across **five planes**, working upward: **strategy** (what we want and what users want) → **scope** (what we build) → **structure** (how it works) → **skeleton** (what form it takes) → **surface** (how it looks and feels). Each plane builds on the one below it, and every plane covers **both the functionality side and the information side**. By default we do **one plane per session**, writing each plane's document to a `ux/` folder as we finish it — so we can always stop at a natural stopping point and resume later, with nothing lost. I'll ask a small set of prioritized questions per plane, record your answers, and flag anything we don't know as an assumption rather than stalling."

Then state what the session will produce, per the output contract (FR-006a / SKILL.md §2):

- `ux/session.md` — the lightweight state pointer (mode, start plane, per-plane status, back-loop queue, next question).
- `ux/strategy.md`, `ux/scope.md`, `ux/structure.md`, `ux/skeleton.md`, `ux/surface.md` — one document per plane, written at its gate.
- `ux/issues.md` — at the very end, after review and a code-comparison pass.

State the one-plane-per-session default explicitly (AC-015a) and that each gate is a natural stopping point where we decide together whether to continue.

> **Note (AC-020c):** if the user answers in a non-English language, you paraphrase their answers into English in the docs and confirm the paraphrase once, at the first gate.

---

## 2. Mode probe

Ask the mode question in plain language, with **distinct trigger phrases** for each mode so the user self-identifies cleanly. The three modes map to exactly two flows — there is **no third flow** (AC-016f):

**Ask (one combined question, or three framed alternatives):**

> "To start us off — which of these describes the situation?
> - **New product** — *the product doesn't exist yet; we're designing it, or a new feature of it, from scratch.*
> - **Redesign existing** — *the product already exists and we're reshaping, auditing, or improving the experience users have today.*
> - **Both** — *an existing product is being re-platformed or rebuilt so substantially that the target resembles a new product* (for example, a desktop system being rebuilt as a mobile-first service)."

**Trigger-language to recognize and confirm (AC-003b):**

| Trigger the user might say | Mode to record |
|---|---|
| "We're building something new", "there's an idea, nothing exists yet", "greenfield", "we don't have a product", "just a concept" | `new` |
| "We have this product and users hate X", "we need to fix/improve/refresh the site", "audit", "modernize what we have", "it exists, here's a link" | `redesign` |
| "We're moving the existing app to a new platform", "rebuild the whole thing", "re-platform", "two things actually — new back end, same users" | `both` |

**Confirm, never auto-answer.** After you propose a reading, say it back and get agreement:

> "Just to confirm: this is a **redesign** of the existing product — the target experience is the new one, and every plane doc will carry the current state → issues → target structure. Correct?"

Record the confirmed mode in `ux/session.md` (AC-003c). The mode is **re-surfaced at every subsequent gate** — each gate confirmation opens with, e.g., "mode: redesign — continuing with the current-state → issues → target structure."

**Mode semantics (AC-016d, AC-016f):**

- `new` — §1 of each doc is *Foundations* (the brief and constraints we import); §2 (Issues found) is `N/A`.
- `redesign` — load `references/redesign-audit.md` at intake and keep it open; §1 captures the existing product's current state, §2 lists issues, §3 records the target decisions.
- `both` — use the **redesign flow** for a product whose target resembles a new product. There is no third flow: every `both` plane runs current state → issues → target, and the docs say so in their metadata.

---

## 3. Mid-stream probe

Ask whether any planes are already decided, **listing all five** (AC-003b):

> "Have any of these planes already been decided — **strategy, scope, structure, skeleton, surface**? For example, maybe the requirements are already fixed (scope is done), or the wireframes already exist (skeleton is partially done). Please name the *first* plane that is genuinely already decided."

**If the user names a starting plane `N`** (e.g., "scope is settled and so is strategy" → the first decided plane is scope → `N = scope`... note: read it as *the highest plane the user considers decided*, i.e., their starting point), then:

1. **Set `state.start = N`** and record it in `ux/session.md`.
2. **Run the back-fill script** for planes `1..N-1` (every plane *below* the start): for each, ask **that plane's single most important (first-priority core) question** — just one, not the full battery. The first-priority core question per plane (from the question banks, CORE-1 of each):

   | Lower plane | Its single most important question (CORE-1) |
   |---|---|
   | strategy | "What do we want to get out of this product — what are the product objectives?" |
   | scope | "What features will the product offer — what will it do?" |
   | structure | "How does the product respond to the user — what options, patterns, and sequences of actions does it offer?" |
   | skeleton | "What interface elements do we need on each screen, and how are they arranged — with which defaults?" |
   | surface | "Where should the user's eye go first, and what path should it take across each screen?" |

   (Ask, in order, the questions for every plane *below* `N` — a user starting at skeleton gets one strategy, one scope, and one structure question; a user starting at structure gets one strategy and one scope question; and so on.)

3. **Anything unanswered** after that single question — including the whole rest of the plane — is recorded in two places (AC-004a):
   - a **flagged assumption row** in that plane's template §5 (item / source / why flagged / plane / how to validate), and
   - an entry in the **back-loop queue** (`ux/session.md` + the plane doc's §6): `{plane, item, reason: "not covered at back-fill intake; open for a later visit", status: open}`.

4. **State the direction rule once**, plainly (AC-004b):

   > "From here on, we travel **strictly upward**: after the back-fill, we only work planes in the order strategy → scope → structure → skeleton → surface, starting at the done plane. We won't enter a lower plane again unless a gate back-loop or the closing review forces one."

For example, if the user says "the wireframes are basically done" (`N = skeleton`): you set `state.start = skeleton`, ask the strategy CORE-1 question, the scope CORE-1 question, and the structure CORE-1 question; whatever stays unknown becomes flagged assumptions + back-loop entries; then the session runs the **skeleton** plane first, and afterward proceeds to surface only (AC-007c).

**If nothing is decided** (`N` not named): `state.start = strategy` and the session runs the full bottom-up order from plane 1.

> **On resume** (a `ux/session.md` already exists): do not re-run the mid-stream probe. Read `session.md` + all existing `ux/*.md` as current state, state where the session is, and pick up at the recorded next question (SKILL.md §12 / AC-014c). Intake's greeting, mode confirmation, and fixture confirmation still apply; the probes for mid-stream and imports do not re-interview by default.

---

## 4. Import probe

Ask what exists already (AC-003b, FR-005):

> "Do you have any existing materials to import — a **PRD**, a **spec**, a design **system** or style guide, any **mockups** or screen designs, or **analytics**/usage data? Anything you provide becomes the starting truth I deepen with questions — I never re-derive it from scratch."

**If materials are provided, import them per plane** into that plane doc's **template section 1** (Current state / Foundations), each with a **provenance record** of the form (AC-005a / FR-005b):

```
Source: <user-provided X, v./date>
```

Examples:
- `Source: user-provided PRD v2 (2026-09-10)`
- `Source: user-provided design-system tokens export, 2026-09-12`
- `Source: user-provided analytics export (last 90 days), 2026-09-14`

Then note, in the same section-1 entry, *what was taken from it and where it now lives* (e.g., "→ §3A objective 1; §3B content requirement 3").

**Routing of common imports:**

| Import | Landing plane(s) |
|---|---|
| PRD / requirements doc | scope (functionality + content), strategy (objectives) |
| Spec / technical feasibility notes | scope (constraints, prioritization) |
| Design system / style guide / branded assets | surface (consistency, palette), skeleton (components) |
| Mockups / screen designs | skeleton (standard screens / wireframes), surface |
| Analytics / usage data | strategy (metrics), scope (what to cut) |
| Architecture / flow diagrams | structure (IA, flow) |

**Rules that hold for every import (AC-005b, FR-005):**

- **Never modify the user's source files.** They are read-only inputs; the skill only writes into `ux/`.
- **Imported inputs are current state to deepen, not to re-derive.** You may re-ask about gaps, but you do not silently rebuild what was given.
- Anything imported is treated as *evidence with provenance*, exactly like a redesign's current-state artifacts. A claim that comes only from an import is not an assumption — but an *absence* in the import is (record it as a flag in §5 if it matters).
- **Competitive analysis with web disabled (AC-019e):** the skill has no network access. If the user references competitors or conventions, ask them to **describe** the competitors' approach from memory or **share a link/screenshot**, then analyze the artifact they supplied as current-state evidence. Never attempt a network fetch; record "no competitive information available" as an assumption rather than inventing competitors.

---

## 5. Project fixtures

Collect the four fixtures and confirm them back (AC-003b / FR-006b):

1. **Product name** — "What should we call the product in the documents?" (a working name is fine).
2. **Working directory** — confirm the folder the session runs in, where `ux/` will be created (usually the current working directory; record it so on resume the docs are found).
3. **Desired output folder** — prompt once; **default `ux/`**:

   > "I'll write the docs into a `ux/` folder in this directory by default. Is `ux/` fine, or would you like a different folder (e.g., `docs/ux/` or `design/`)?"

   Record the choice (absolute or relative path). This is the only override prompt — it is asked once, at intake (AC-006b). On later runs the folder is read from `ux/session.md`.

4. **Optional artifacts — which exist vs. which are wanted.** Present the six optional items and record each as *exists / wanted / not wanted*:

   | Optional artifact | Belongs to |
   |---|---|
   | Personas | strategy (§3B) |
   | Segmentation | strategy (§3B) |
   | Success metrics | strategy (§3C) |
   | User research | strategy (§3B) |
   | Content inventory | scope (§3B) |
   | Feasibility data | scope (§3C) |

   For each that is *wanted but missing data*, the plane loop will run the substitution ladder (`references/substitution-ladder.md`): ① always ask → ② lightweight substitute built with the user → ③ flagged assumption row in template §5. None of them blocks a gate.

Also record, as free-text, any **hard constraints the user states up front** (brand, technology, hardware, deadline) — these feed the scope plane's §3C constraints row later.

---

## 6. Write the initial `ux/session.md`

After the probes, **write the initial `ux/session.md`** in the confirmed output folder, filled from intake, using the contract C-1 schema (FR-014). It must contain every field below — the schema may be table or list based, but the field names must be present:

- **Product name** — from fixtures.
- **Mode** — `new` \| `redesign` \| `both`, exactly as confirmed in the mode probe.
- **Start plane** — `strategy` for full runs; the named plane `N` for mid-stream entry.
- **Output folder** — the confirmed path (default `ux/`).
- **Per-plane status** — all five planes, each exactly one of `not-started`, `in-progress`, `gate-passed`, `back-loop`.
- **Back-loop queue** — list of `{plane, item, reason, status}` (may be empty; back-fill entries land here at intake).
- **Current plane in-progress** — plane name + next question (added once a plane starts; `—` at intake; on resume it holds the exact next question).
- **Assumptions register** — list of assumption rows in the contract C-2 §5 shape (item / source / why flagged / plane / how to validate / validated? (open/yes/no)); back-fill assumptions land here too.
- **Changelog pointer** — a `{date, what changed, why}` row echoing the latest doc change (at intake: the session file itself).

**Template for the initial file** (fill the bracketed values from intake):

```markdown
# Session — <Product name>

- Product name: <name>
- Mode: <new | redesign | both>          <!-- confirmed with the user at intake -->
- Start plane: <strategy | scope | structure | skeleton | surface>
- Output folder: <ux/ | override>

## Per-plane status
| plane | status |
|---|---|
| strategy | <not-started | in-progress | gate-passed | back-loop> |
| scope | <…> |
| structure | <…> |
| skeleton | <…> |
| surface | <…> |

## Back-loop queue
| plane | item | reason | status |
|---|---|---|---|
| <back-filled plane> | <item left unanswered at back-fill> | not covered at intake | open |

## Current plane in-progress
- Plane: —                        <!-- set when the first plane starts -->
- Next question: —                <!-- the exact next question, for resume -->

## Assumptions register
| item | source | why flagged | plane | how to validate | validated? (open/yes/no) |
|---|---|---|---|---|---|
| <back-filled assumption> | <where it came from> | not covered at intake | <plane> | <how to check later> | open |

## Changelog pointer
| date | what changed | why |
|---|---|---|
| <YYYY-MM-DD> | session started | intake completed; mode confirmed |
```

**After writing:** say out loud what was recorded, confirm the mode once more, and point at the corrected `ux/session.md` as the memory of record:

> "Recorded: mode = `redesign`, start plane = `scope`, output folder = `ux/`, planes below the start back-filled as flagged assumptions. This is all saved in `ux/session.md`; on resume we'll pick up from the recorded next question. The mode will be re-surfaced at each gate."

---

## 7. After intake: hand off to the plane loop

Once intake is complete and `ux/session.md` is written:

1. If `state.start = strategy`, begin the plane loop at strategy per SKILL.md §6 (load `references/planes/strategy-questions.md` + `templates/strategy.md`).
2. If `state.start = N` (mid-stream), run the back-fill assumptions already recorded, then begin at plane `N` and continue **strictly upward**.
3. If this was a resume, apply SKILL.md §12: read the docs, state where the session is, ask the recorded next question.

Intake is finished when the **mode is confirmed, fixtures are recorded, and `ux/session.md` exists**. No plane's core questions may be asked before this point (AC-003d).
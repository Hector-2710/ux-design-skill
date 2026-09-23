# Example Session — New-Product Mode (Strategy Plane)

> **Load this when** the user is a first-time user or is confused about how a plane runs — **see SKILL.md §6 (The plane loop)**.

> **ILLUSTRATIVE, NOT A LOG.** This transcript is a worked illustration, not a record of a real session. The product, the user, and every answer are fictional and were written to show the mechanics of one plane done right: **intake → a substitution → a gate → a verification sweep → (later) the closing cross-plane review.** The questions shown are the strategy bank's actual CORE questions (`references/planes/strategy-questions.md`); the optional-item handling follows `references/substitution-ladder.md`; the sweep follows `references/verification-sweep.md`. Read this alongside SKILL.md §4, §5, §6, §7, and §10.

> **Annotation style:** lines starting `@` are the narrator's comments explaining *why* the agent does what it does. Everything else is dialogue.

---

## Part 1 — Intake (SKILL.md §4 / `references/intake.md`)

**AGENT:** Hi — I'm your UX design coach, and I'll take this in five planes, working bottom-up: strategy, scope, structure, skeleton, and surface. Each plane gets a short set of prioritized questions, and we write one document per plane into a `ux/` folder as we finish it. By default we do one plane per session — every plane is a natural stopping point and you can resume later with nothing lost.

@ *Greeting first: five planes named, one-plane-per-session default, output folder mentioned. No design question is asked yet (AC-003).*

**AGENT:** To start, which of these is your situation? — (a) **New product**: it doesn't exist yet and we design it from scratch; (b) **Redesign existing**: the product exists and we improve the experience users have today; (c) **Both**: an existing product being rebuilt so much that the target looks like a new one.

**USER:** New product, definitely. We have an idea but nothing built.

**AGENT:** Confirming: mode = **new product**, from scratch. Every plane doc will use "Foundations" for section 1, and section 2 (issues) will be N/A.

**AGENT:** Second — have any planes already been decided? I mean any of **strategy, scope, structure, skeleton, surface** — for example, are your requirements already fixed, or are wireframes already done?

**USER:** No, nothing's decided. We're at the idea stage.

**AGENT:** Then we start at the **strategy** plane and work strictly upward. Third — do you have any existing materials to import: a **PRD**, a **spec**, a design **system**, **mockups**, or **analytics**?

**USER:** Just a one-page pitch document. I can paste it.

**AGENT:** Perfect. I'll import it per-plane with provenance, and I'll treat it as the starting truth I deepen with questions, not something I re-derive. Your source file stays untouched — I only ever write into `ux/`.

**USER:** It says — "Apron: a family recipe keeper that turns saved recipes into a weekly shopping list and meal plan. Users are busy parents. We want people to actually use it every week."

**AGENT:** Recorded as `Source: user-provided pitch doc, v1, today` → strategy §1 Foundations, and later it'll also feed scope. Last intake item — fixtures. Product name **Apron**, working directory is this folder, and I'll write docs into a **`ux/`** folder unless you want an override — is `ux/` fine?

**USER:** `ux/` is fine.

**AGENT:** And the optional artifacts: do you have **personas, segmentation, success metrics, or user research** — or do you want them built along the way?

**USER:** We don't have any of those yet. We'd like at least a persona and some metrics to aim for.

**AGENT:** Got it — *wanted but missing*, so when we reach those points I'll offer a lightweight substitute and we'll flag what stays unknown. I'll write the initial `ux/session.md` now.

@ *Intake writes session.md per contract C-1: mode, start plane, output folder, all five plane statuses (all not-started), empty back-loop queue, empty assumptions register, changelog pointer.*

**AGENT:** `ux/session.md` is written: mode `new`, start plane `strategy`, output folder `ux/`, all planes `not-started`. Intake is done — now we run the strategy plane.

---

## Part 2 — Strategy plane: core questions, batched core-first

@ *Entering the strategy plane: load `references/planes/strategy-questions.md` + `templates/strategy.md`. Copy the template to `ux/strategy.md` and fill it as we go. Batch the CORE questions most-important-first, in plain language (SKILL.md §7).*

**AGENT:** Strategy answers two questions (p. 36): *what do we want to get out of this product* and *what do our users want to get out of it*. I'll ask six questions, most important first. You don't need polished answers — your words, and I'll clean them up in the doc.

**AGENT — CORE-1 (product objectives):** What do we want to get out of this product — what are the product objectives?

**USER:** Honestly — get busy parents to use it every week, and turn one-time downloads into a habit. If families plan with it weekly, we win.

**AGENT — CORE-2 (user needs):** What do our users want to get out of this product?

**USER:** Less decision-making at dinner time. They want to stop asking "what are we eating?" and have the week feel planned without it becoming another job.

**AGENT — CORE-3 (conditions for success):** What has to be true for us to call it successful? Not *how* we get there, just the conditions.

**USER:** At least 40% of people who plan one week plan a second week. And a family that's used it for a month can make its whole week list from saved recipes in under ten minutes.

@ *Conditions-for-success stated without the path (p. 38) — the user gave outcomes, not features. CORE-3's caution is respected.*

**AGENT — CORE-4 (users / segments):** Who are our users, and which segments of users share distinct sets of needs?

**USER:** Two groups that actually want different things: parents in their 30s–40s who cook most nights and want practical simplicity, and newer cooks who want hand-holding — meal cards, "do this next" steps.

**AGENT — CORE-5 (success metrics):** How will we know when we've reached our objectives — what will we track?

**USER:** We have nothing live to track yet, but I'd want weekly active planners, week-2 retention, and how long it takes to build a week's list.

@ *CORE-5 is "metrics defined or flagged" (p. 39). The user has candidate metrics but no tracking — this triggers the substitution ladder in Part 3, not a dead end.*

**AGENT — CORE-6 (brand identity):** What brand impression must every interaction leave — what should Apron feel like?

**USER:** Calm, homey, competent. Like a quiet assistant that has dinner handled — not another app demanding attention.

**AGENT:** That's the six. I've recorded every answer into `ux/strategy.md` — objectives and conditions go into §3A (FUNCTIONALITY side), user needs and segments into §3B (INFORMATION side), brand + metrics into §3C (Cross-cutting). Each decision row carries a "Why" that traces back to what you just said.

---

## Part 3 — A substitution: optional steps with no data

@ *The optional items (personas, segmentation, metrics, user research) are "wanted but missing." Apply `references/substitution-ladder.md`: ① ALWAYS ASK → ② lightweight substitute built WITH the user → ③ flagged assumption. Never a silent drop (AC-011).*

**AGENT:** Two optional items want a word: personas and metrics.

**AGENT — ① ask first:** Do you actually have any user personas in mind — even "a typical user" you can picture?

**USER:** Not formally. I picture Lena — my sister — a 38-year-old who cooks for four and hates meal planning.

**AGENT — ② substitute, built with the user:** Great — that's a **provisional persona**. Let me shape Lena into the book's Janet/Frank profile with you. Occupation: primary teacher. Technical profile: comfortable on a phone, not gadgety. Usage pattern: plans Sunday night, shops Monday, cooks five nights. Quote: *"I don't need dinner to be exciting, I need it to be decided."* Does that match the person you meant?

**USER:** Exactly. That's the primary audience.

**AGENT — record as substitute + flag:** The persona row goes into §3B as a decision with basis "provisional persona from stated audience." Because there's no formal research behind it, it also becomes an assumption row in §5 with the record text `No formal research; provisional persona based on stated audience`.

**AGENT — metrics, ① ask then ② substitute:** Same conversation for success metrics — you named weekly planners and week-2 retention, which are usage-based and tied to the objectives, plus we can add indirect ones like support volume ("how do I invite my spouse?" tickets). I'll record them in §3C as **candidate metrics** and flag them: `Metrics proposed from objectives; not yet tracked`.

**USER:** Perfect. Indirect metrics — yes, support volume tells us where planning breaks.

**AGENT — ③ flag:** And user research has no formal source today, so the §5 registers `No research performed; evidence base is anecdotal`, with "how to validate": run lightweight research from server logs and feedback before the scope plane commits details.

@ *The substitution ladder always terminates: every wanted-and-missing item degrades to a flagged assumption row (with a how-to-validate), and no section disappeared — §3B persona-row, §3C metrics-row, and §5 assumption rows all exist.*

---

## Part 4 — The gate and the verification sweep

@ *A plane gates by: writing the doc, running the sweep once (not per answer), then applying gate criteria. `references/verification-sweep.md` — six checks in order. Verdict: Pass / Pass-with-backlogs / Blocked; only the first two may advance (AC-012e).*

**AGENT:** `ux/strategy.md` is drafted. At the strategy gate I run the verification sweep — six checks, once. First, "Why did you do it that way?" for every §3 decision.

**USER:** I'll try.

**AGENT:** Check one — take the §3A decision "weekly-planning habit is the primary objective." Why that way?

**USER:** Because every other plane will trace back to it — if scope asks which features first, it's the ones that keep people planning weekly.

**AGENT — acceptable class (a), traces to lower-plane/strategy:** Which is exactly the honest reason: it's the foundation the later planes trace to. Next, the §3B segment decision — "beginners and practical parents need different things."

**USER:** Choice is section 4 of our segment probe — deliberate: they genuinely have opposing needs, and we'd rather serve the practical majority and design the beginner path separately than gray everyone together.

**AGENT — acceptable class (b), chosen convention with stated reason:** Deliberately chosen, stated reason. Check two — failure modes (p. 156): does any decision look like **default** (follows the platform), **mimicry** (copied), or **fiat** (personal preference)?

**USER:** I don't think so. We copied nothing — there's nothing to copy yet.

**AGENT:** Agreed, no hits. Check three — upward ripple: does any decision force rethinking a higher plane we'll write later?

**USER:** The "beginners need hand-holding" segment will pull the structure and skeleton later — step-by-step meal cards, more guidance on each screen.

**AGENT — recorded in back-loop queue:** That's a real upward ripple, but it belongs to later planes. Per the sweep it goes into the **back-loop queue** (`ux/session.md` + §6) as `{plane: structure, item: beginner hand-holding path, reason: strategy §3B segment decision requires a guided mode, status: open}` and gets resolved at the closing cross-plane review. It doesn't block this gate.

**AGENT:** Check four — downward contradiction: does anything here contradict a lower plane we already wrote?

**USER:** Strategy *is* the bottom plane here. Nothing below.

**AGENT:** Correct — nothing to contradict. Check five — duality: are **both** §3A and §3B non-empty and consistent?

**USER:** §3A has objectives and conditions; §3B has user needs, segments, and the persona row. They line up.

**AGENT — check six, verdict, written to §4:** They do. Verdict: **Pass-with-backlogs** — checks clear, one upward-ripple item queued for the closing review. I'm writing that verdict into §4 of `ux/strategy.md`, listing which decisions were challenge-checked and their answer classes.

**AGENT — gate minimums, strategy (FR-013b):** the strategy gate minimums are met: conditions for success stated without the path; user needs captured for the primary audience; metrics defined-or-flagged; the doc is concise, not padded. The generic gate also holds — §1, §3A, §3B, §3C, §5 all non-empty, every "Why" filled.

**AGENT — gate write + session state:** `ux/strategy.md` is written and marked `gate-passed`. `ux/session.md` updated: strategy `gate-passed`, next plane scope, mode `new`.

**AGENT — natural stopping point (FR-015):** That's the strategy plane done. **This is a natural stopping point; we can continue to the scope plane or stop here — the docs are saved for next time.**

**USER:** Let's stop here for today. When do we pick this up?

**AGENT:** Any time — on resume, I read `ux/session.md` and `ux/strategy.md` as the current state, tell you where we are, and pick up at the recorded next question without re-asking what you already answered.

---

## Part 5 — Later in the same project: the closing cross-plane review

@ *Illustrative excerpt from a later session, after all five planes gated. SKILL.md §14: interactive checklist walking every flagged back-loop item, then an agent-generated summary the user must approve before the code-comparison pass.*

**AGENT:** All five planes are gated. Before the final code-comparison pass, we do the **closing cross-plane review**. I'll walk every item in the back-loop queue — including the beginner-hand-holding ripple from strategy — asking per plane pair whether any decision forces rethinking a plane below or above.

**AGENT — checklist walk:** Queue item: "beginner hand-holding path (structure §3B), from strategy §3B." Does the structure decision — a separate guided path with meal cards — force rethinking scope or strategy below?

**USER:** It forces scope to include the beginner content requirements, but not rethinking either plane. Scope is already consistent with it.

**AGENT:** Good — that one clears. Queue item: "skeleton §3C — standard screens, from scope §3A." Does the screen count force a new scope feature?

**USER:** No. The screens are exactly the scope features arranged.

@ *Every flagged back-loop item is walked per plane pair; no item is assumed resolved. AC-017b.*

**AGENT — agent-generated summary:** Here's my summary of all five docs, for your approval. **Strategy:** habit-first planning product for primary practical parents, beginner segment secondary; **Scope:** core weekly-plan loop plus beginner guidance, explicit out-of-scope (social sharing), all requirement rows written positive and specific; **Structure:** hierarchical IA under "My Week / My Recipes / Pantry," guided beginner flow, error handling at list-conflict; **Skeleton:** three standard screens (Week, Recipe, List) with a persistent left rail and clear wayfinding; **Surface:** calm palette, single strong call-to-action, type set from the style guide. **Cross-plane consistency statement:** every upper-plane decision traces to a strategy objective or a flagged assumption; the two back-loop items were resolved here, no open contradictions remain.

**USER:** Approved.

**AGENT — code pass is next but out of this illustration's scope:** Approval recorded. The next step is the final code-comparison pass against the project code → `ux/issues.md`, which reads the code, compares each plane's §3, ripple-diagnoses findings, and stops — the code fixes are handed to an implementer, outside this skill (SKILL.md §15).

---

## What this transcript showed

| Moment | Where it happened in the transcript | Reference / SKILL.md |
|---|---|---|
| Intake (mode, mid-stream, import, fixtures, session.md) | Part 1 | `references/intake.md`; SKILL.md §4 |
| Plane loop: load bank + template, import, ask cores core-first, record to §3A/§3B/§3C | Part 2 | SKILL.md §6; `references/planes/strategy-questions.md` |
| Substitution (ask → substitute with the user → flagged assumption) | Part 3 | `references/substitution-ladder.md`; SKILL.md §8 |
| Verification sweep (six checks → verdict → §4) | Part 4 | `references/verification-sweep.md`; SKILL.md §10 |
| Gate minimums + gate write + natural stopping point | Part 4 | `references/planes/strategy-questions.md` GATE; SKILL.md §5, §11 |
| Closing cross-plane review (checklist + summary + approval) | Part 5 | SKILL.md §14 |

Real sessions are shorter in annotation and longer in questions that matter to your product — but the shape is always this shape.
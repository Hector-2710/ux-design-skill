# Example Session — Redesign Mode (Skeleton Plane)

> **Load this when** a redesign user is confused — **see SKILL.md §13 (New vs redesign)**.

> **ILLUSTRATIVE, NOT A LOG.** A worked illustration, not a record of a real session; the product, the user, and every answer are fictional. It shows a **redesign** session on the **skeleton** plane done right, with the redesign-specific shape every doc takes: **current state → issues → target** (`references/redesign-audit.md`), plus the same five moments as the new-product example — **intake, a substitution, a gate, a verification sweep, the closing cross-plane review.** The core questions are the skeleton bank's actual CORE questions (`references/planes/skeleton-questions.md`); the audit probes, failure modes, and ripple lesson follow `references/redesign-audit.md`. Read this alongside SKILL.md §4, §6, §10, §13, and §14.

> **Annotation style:** lines starting `@` are the narrator's comments. Everything else is dialogue.

---

## Part 1 — Intake: mode = redesign

**AGENT:** Hi — I'm your UX coach. We'll work five planes bottom-up — strategy, scope, structure, skeleton, surface — one per session by default, writing one doc per plane into a `ux/` folder as we finish. Which is your situation: **new product**, **redesign existing**, or **both** — an existing product being rebuilt so much it looks new?

**USER:** Redesign, definitely. BentoRow is our campus meal-ordering app — it works, but students say it's confusing and the bold Order button doesn't stand out.

**AGENT:** Confirming: mode = **redesign**. That means every plane doc carries the three-section structure **current state → issues → target**, and I load the redesign-audit reference now and at every plane's current-state step.

@ *Mode stored in ux/session.md and re-surfaced at every gate (AC-003c). Loading references/redesign-audit.md at intake because mode = redesign (AC-016a).*

**AGENT:** Mid-stream check — have any of the five planes already been decided: **strategy, scope, structure, skeleton, surface**?

**USER:** Strategy's fresh. Scope is roughly known — order from a menu, pay, pick up. Structure and skeleton are what we're really after, but nothing's decided formally.

**AGENT:** Then nothing below skeleton is decided either, so we start at **strategy** and work strictly upward, one plane at a time. Import probe — do you have anything to bring in: a **PRD**, **spec**, design **system**, **mockups**, or **analytics**?

**USER:** We've got analytics exports — drop-off numbers — and a few screenshots of the current app. I'll share them per plane.

**AGENT:** Recorded with provenance — I'll import them into each doc's section 1 as current-state evidence and deepen with questions; I never modify your files, and screenshots are the standing evidence for the skeleton plane.

@ *With web disabled (AC-019e), competitive context is also asked from the user, not fetched.*

**AGENT:** One more — if competitors matter, describe competing food apps from memory or share a screenshot and I'll analyze that as current-state evidence; I have no web access.

**USER:** Okay, I'll describe GrubHub-style flows later.

**AGENT:** Fixtures — product name **BentoRow**, working directory here, output folder **`ux/`** unless you want an override? And which optional artifacts exist vs. are wanted — personas, segmentation, metrics, research, content inventory, feasibility?

**USER:** `ux/` is fine. No personas. Metrics: we have the analytics. The rest, we'll see.

**AGENT:** Perfect. Writing the initial `ux/session.md` — mode `redesign`, start plane `strategy`, all planes `not-started`. Intake done.

---

## Part 2 — Strategy and scope: heavy lifting, briefly (current state → issues → target)

@ *The example's focus is the skeleton plane, but a redesign starts at strategy, so the transcript skims those gates honestly — each ran its own intake-style loop, sweep, and gate before this session.*

**AGENT (strategy gate, later session):** Strategy is gated `Pass-with-backlogs`. Current state: BentoRow's stated objective was "fast ordering," but analytics show users think it's about browsing menus casually. Issues: objective misalignment (High) — the app is built as a convenience tool students treat as a decision tool; target: re-state objectives as "help students decide quickly with confidence," segments re-derived from ordering data. Next: scope, then structure, then we reach the skeleton — where your complaint lives.

**USER:** So the purple Order button thing is *skeleton* work, not the whole app?

**AGENT — ripple preview, p. 154:** Not yet — that's exactly the mistake redesigns make. When we audit, I'll test the button symptom against all five planes before assigning it. Symptom *appears* at surface (it's a contrast thing), but it may *belong* to skeleton or structure. Wait for it.

---

## Part 3 — Skeleton plane: current state → issues → target

@ *Entering skeleton: load references/planes/skeleton-questions.md + templates/skeleton.md + the audit probes. Section 1 fills from current-state extraction; §2 fills issues; §3 records the target decisions that answer the CORE questions after the audit. Prefix every core question with a current-state probe (FR-016e).*

**AGENT:** Skeleton answers "what form?" — the concrete components, arrangements, navigation, and standard screens, down to wireframe level (p. 108, 111). Run the current-state probes first.

**AGENT — current-state probe (then CORE-1, p. 114-118):** What interface elements does the current app use today, and which arrangements work against the skeleton we want? Let's read the home screen from the screenshot you shared: a search bar, a category rail, a list of vendor cards, and the Order button.

**USER:** Right — and the Order button is a tiny purple button tucked under the vendor card text. Students tap everything *except* it.

**AGENT:** Recorded in §1. Now the redesign variant behind it — with which defaults, and what does "most likely action" mean here?

**USER:** The most likely action is "find what to eat fast." The button should make *that path* effortless, not hide behind a typed search.

**AGENT — CORE-2 (navigation & wayfinding, p. 118-123, 127):** How do users move through the product today — and do they always know where they are?

**USER:** A top bar with tabs — Menu, Orders, Account. It mimics every food app we looked at. Students say they lose their place after tapping a vendor: "where am I? how do I get back to the list?"

**AGENT:** §1: current nav = one bar of tabs, vendor depth pages, no breadcrumbs, no "you are here." That "mimicry" pattern is a candidate issue.

**AGENT — CORE-3 (information design, p. 124-127):** How is content grouped and presented today, and which groupings hide or mislead?

**USER:** Vendor cards group photo, name, rating, *and* the Order button — five things in a tiny tile. The rating and photo shout; the actual action whispers.

**AGENT — CORE-4 (standard screens, p. 128-130):** What screens does the app actually have, and which are convoluted or duplicated?

**USER:** Honestly, every vendor acts like a one-off page. Maybe 20 different layouts that should be 3 standard screens.

**AGENT — CORE-5 (conventions vs deviations, p. 117-118):** Which conventions does it follow by accident, and which should it adopt or break deliberately?

**USER:** Tab-bar convention: fine, keep. But the orange header — that's the founder's favorite color, not a decision. Students read orange as "on sale."

@ *The audit's failure-mode probes (p. 156) are being applied as each finding surfaces: search-by-default reeks of mimicry, the header is fiat, and — see below — the checkout is default.*

### §2 — Issues found (current-state findings, classified)

**AGENT:** Let me consolidate what we found on the skeleton plane into the §2 issues table, with severity, evidence, and trace-to-plane.

| # | description | severity | evidence | trace-to-plane |
|---|---|---|---|---|
| 1 | Order action is buried in vendor tiles; the most likely action isn't the least-effort one | High | screenshot home.png; analytics: 68% of sessions never reach checkout | **skeleton** |
| 2 | Users lose their place after tapping a vendor: no wayfinding cues, no back-path | High | session logs: "back" binge; user test note | skeleton |
| 3 | ~20 bespoke vendor layouts instead of standard screens | Medium | screenshot inventory: vendor/ clone pages | skeleton |
| 4 | Orange header with no stated purpose — design by fiat | Low | brand audit; founder interview | skeleton (§3C) + surface |
| 5 | Checkout flow exists because the POS requires it — design by default | High | structure doc §2 issue 2; maps to 4-step flow | **structure** (belongs lower than where it appears) |

**AGENT — the big purple button: the ripple diagnostic (p. 154):** Now your complaint. The purple Order button *appears* at surface (contrast), so let me test it against all five planes before assigning it: **strategy** — does it imply wrong objectives? No, objectives cover decision-making, not button color. **scope** — is ordering in scope? Yes, it's the core feature. **structure** — is the order flow itself wrong? Partly — the 4-step flow behind the button is the real friction, that's issue 5. **skeleton** — is the button's arrangement and prominence wrong? Yes — the action placement, not the paint. **surface** — is this purely presentation? No — recoloring alone wouldn't fix it.

**AGENT:** So the button is really two issues: **skeleton #1** (arrangement/prominence — where the action lives on the tile) and **structure #5** (the flow it triggers — too many steps). We fix the lower plane first: the structure flow gets re-gated with its own fix, and the skeleton target below reflects it. The purple color itself shrinks to a surface note, and we won't pretend paint is the solution.

### §3 — Target decisions (the redesign answers the CORE questions)

**AGENT:** Now the target — §3 decisions that answer each CORE question *after* the audit. Feed these back to me as decisions, not opinions:

- **3A (interface, CORE-1):** Vendor tiles keep photo + name + rating; the Order action becomes a **primary, always-visible** "Order" button with largest contrast; default action on a vendor card = "view menu," per "most likely action = least effort" (p. 117-118). Trade-off stated: less tile space for description, deliberately traded for action prominence.
- **3B (navigation, CORE-2):** Keep the tab bar (deliberate convention); add **vendor-level wayfinding**: breadcrumb "Home > Granny's Bowl", back affordance, "you are here" on the active tab (p. 127).
- **3B (information design, CORE-3):** Group per tile: identity → reason-to-pick → action. One emphasis rule: the action gets the strongest cue, not the rating.
- **3C (standard screens, CORE-4):** Collapse to **three standard screens** — Home/Browse, Vendor detail, Order/Checkout — described at wireframe level in the doc (§3C), each ≤ the same skeleton.
- **3C (conventions/deviations, CORE-5):** Follow: tab bar, card list. Deviate: order-button prominence (deliberate, stated reason: strategy says "decide quickly"; deviation buys the objective).

**USER:** Yes to all — and the orange header goes to the surface plane to be re-decided as the brand's accent color, not left as founder preference.

**AGENT:** Recorded. §3's §3A and §3B are both non-empty and consistent — the FUNCTIONALITY (actions/arrangement) and INFORMATION (grouping/wayfinding) sides both have decisions with "Why" rows.

---

## Part 4 — A substitution: optional step with no data

@ *The step: wireframe sketches. The user hasn't drawn any — `references/substitution-ladder.md` chain: ① always ask → ② lightweight substitute WITH the user → ③ flagged assumption.*

**AGENT:** One optional item: **wireframe sketches** for the three standard screens. Do you have any drawings?

**USER:** No, none yet.

**AGENT — substitute, built with the user:** Let's build the lightweight substitute together — instead of pixels, I'll record each standard screen as a **text-based element list** at wireframe level: per screen, the elements and their order/top/bottom placement. You sanity-check placement; I type the list into §3C. So Home/Browse: search top → category rail → vendor cards... does the Order button go bottom-right of each card?

**USER:** Bottom-right, yes — thumb reach.

**AGENT:** Doing it. Since it's a substitute, I'm flagging it in §5 so we record it as an example, not rendered layout: `Wireframes are provisional; arrangement captured as text element lists, not yet rendered/tested`. It doesn't block the gate.

---

## Part 5 — The gate and the verification sweep

@ *Gate = write the doc, run the sweep once, apply skeleton per-plane minimums. `references/verification-sweep.md` — six checks in order.*

**AGENT:** `ux/skeleton.md` is drafted with the full current-state → issues → target shape and the wireframe-level text. Gate sweep, six checks.

**AGENT — check 1, "Why did you do it that way?" (p. 157):** Take the §3A decision "Order button is the strongest cue on the tile." Why that way?

**USER:** Because strategy said "decide quickly with confidence," and the current state proved the action was invisible. It traces to strategy, and to the issue evidence.

**AGENT — class (a), traces to lower plane + strategy:** Acceptable answer. Check 2 — failure modes (p. 156): any decision here look like **default, mimicry, or fiat**?

**USER:** No — each one now has a stated reason or tracks to the audit.

**AGENT:** Agreed. Check 3 — upward ripple: does anything here force rethinking a higher plane?

**USER:** The orange header decision ripples up to **surface** — the palette has to re-state it as accent color. And the three standard screens will dictate surface layouts.

**AGENT — queued, not blocking:** Both are genuine upward ripples → back-loop queue entries, resolved at the closing review. Check 4 — downward: does anything contradict a lower plane already written?

**USER:** Structure's issue 5 fix — we're re-gating structure per its own flow fix, and skeleton #1 matches it. No contradiction remains.

**AGENT:** Confirmed clear. Check 5 — duality: §3A and §3B both non-empty and consistent?

**USER:** Yes — actions on one side, wayfinding/grouping on the other, both feed the same standard screens.

**AGENT — check 6, verdict:** Verdict: **Pass-with-backlogs** — checks clear, two upward ripples queued. Writing that into §4 with the challenge-checked decisions. Gate minimums hold: interface decisions with defaults and trade-offs, navigation + wayfinding defined, information design captured, standard screens sketched at wireframe level, conventions vs. deliberate deviations listed — and the generic gate's "no unresolved downward contradiction" is satisfied.

**AGENT:** `ux/skeleton.md` marked `gate-passed`; `ux/session.md` updated; mode `redesign` re-surfaced at this gate, as it will be at every gate. **This is a natural stopping point; we can continue to the surface plane or stop here — the docs are saved for next time.**

**USER:** Continue to surface — I want the orange fixed properly.

---

## Part 6 — Later: the closing cross-plane review

@ *After the surface gate. SKILL.md §14: interactive checklist walking every flagged back-loop item, then an agent-generated summary the user approves; only then the code-comparison pass.*

**AGENT:** All five planes gated. Closing review — I walk the back-loop queue. Item: "orange → surface accent (from skeleton §3C)." Does re-deciding it as an accent force rethinking a plane below?

**USER:** No — it was never a lower-plane decision; it was a fiat that structure and skeleton had to design around. Surface re-decides it; skeleton stays as written.

**AGENT:** Clears. Item: "three standard screens → surface layouts (from skeleton §3C)." Does the surface layout force adding a fourth screen?

**USER:** No — surface worked within the three.

**AGENT — summary for approval:** Cross-plane summary — **Strategy:** decision-first ordering, segments from data; **Scope:** order flow + menu browsing, out-of-scope: loyalty gamification; **Structure:** re-gated 3-step checkout (was 4), error prevention at payment; **Skeleton:** 3 standard screens, action-prominence rule, wayfinding added; **Surface:** orange re-decided as brand accent, contrast on one primary action, style-guide items listed. **Consistency statement:** every plane traces to strategy objectives or a flagged assumption; the two back-loop items resolved here; structure's issue-5 flow fix and skeleton's issue-1 prominence fix are mutually consistent.

**USER:** Approved.

**AGENT — next, the code pass:** Approval recorded. Next is the final **code-comparison pass** → `ux/issues.md`: read the code, compare each plane's §3, ripple-diagnose, promote unresolved assumptions to issue rows, then stop — the fixes themselves belong to an implementer agent, outside this skill (SKILL.md §15). If the code isn't accessible to me, I'll label every finding "artifact-based" and say so.

---

## What this transcript showed

| Moment | Where | Reference / SKILL.md |
|---|---|---|
| Intake, mode = redesign, audit loaded | Part 1 | `references/intake.md`; `references/redesign-audit.md`; SKILL.md §4, §13 |
| Current state → issues → target (the redesign triad) | Part 3 | `references/redesign-audit.md` §1-3; SKILL.md §13 |
| Failure-mode probes (default / mimicry / fiat) | Part 3 (CORE-2, CORE-5, issues 4-5) | `references/redesign-audit.md` §2 |
| Ripple ("big purple button") diagnostics | Part 3 (§2, issues 1 & 5) | `references/redesign-audit.md` §4; p. 154 |
| Substitution (text wireframes → flagged assumption) | Part 4 | `references/substitution-ladder.md` |
| Verification sweep → verdict → §4 | Part 5 | `references/verification-sweep.md`; SKILL.md §10 |
| Gate minimums + gate write + natural stopping point | Part 5 | `references/planes/skeleton-questions.md` GATE; SKILL.md §5, §11 |
| Closing cross-plane review + approval | Part 6 | SKILL.md §14 |

Real redesigns vary — some planes are mostly intact, some are fully reworked — but every doc always reads current state → issues → target, and every symptom is ripple-checked before it's assigned a plane.
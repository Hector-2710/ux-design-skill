# References Index — What to Load, When

> **Consult this file on activation** to know what to load and what not to (AC-007d). This index is the load-on-demand source of truth; SKILL.md §17 mirrors it.

> **Loading rule: the only file that is always loaded is `intake.md`** — first, before any design question (NFR-003c, FR-003). Everything else is loaded only when its trigger fires. Sizes are actual `wc -l` values.

| Reference file (name) | When to load | Size |
|---|---|---|
| `intake.md` | **Always, first, on every activation** — mode detection, mid-stream entry/back-fill, imports, fixtures, initial `ux/session.md` (see SKILL.md §4) | 246 lines |
| `planes/strategy-questions.md` | Only when entering the **strategy** plane (see SKILL.md §6) | 132 lines |
| `planes/scope-questions.md` | Only when entering the **scope** plane (see SKILL.md §6) | 132 lines |
| `planes/structure-questions.md` | Only when entering the **structure** plane (see SKILL.md §6) | 133 lines |
| `planes/skeleton-questions.md` | Only when entering the **skeleton** plane (see SKILL.md §6) | 125 lines |
| `planes/surface-questions.md` | Only when entering the **surface** plane (see SKILL.md §6) | 134 lines |
| `redesign-audit.md` | Only in **redesign (or `both`) mode** — at intake and at every plane's current-state step (see SKILL.md §13) | 118 lines |
| `substitution-ladder.md` | Only when an **optional step has no data** (see SKILL.md §8) | 107 lines |
| `verification-sweep.md` | Only **at a plane's gate** (see SKILL.md §10) | 59 lines |
| `book-cheatsheet.md` | Only for **book grounding / definition needs** — when the user asks what Garrett says about a concept (see SKILL.md §3) | 118 lines |
| `examples/new-product-session.md` | Only for **first-time users or confusion** about how a plane runs (see SKILL.md §6) | 197 lines |
| `examples/redesign-session.md` | Only for **first-time redesign users or confusion** in redesign mode (see SKILL.md §13) | 205 lines |

**What is NOT in this index:** the plane templates (`templates/*.md`) live in their own directory and are loaded with their plane; and this file does not list itself.

**Load-on-demand discipline (design §4.1):**
- Do not pre-load question banks for planes you aren't about to enter — context stays lean and the user isn't overwhelmed.
- In redesign mode, `redesign-audit.md` stays open across the session; everything else is loaded and closed as its trigger fires.
- If a trigger fires mid-session (a gate reached, an optional step with no data), load the file at that moment, not before.
- `intake.md` is the single mandated load on activation; `00-INDEX.md` is a lookup, not a context load.
# Verification Sweep — The Gate-Time Script

> **Load this when** a plane reaches its gate (and only then) — **see SKILL.md §10 (Verification sweep at the gate)**.

The verification sweep is the "Why did you do it that way?" check (p. 157) run **once per gate, not after every answer** (FR-012, AC-012c). It is the behavioral backstop to the template structure and produces the verdict that decides whether the plane can advance.

---

## How to run the sweep

- Run at a plane's gate, after the plane's doc has been written to `ux/<plane>.md`.
- Work through the **six checks in order** below; do not skip or reorder them.
- Apply each check to the *recorded decisions* in the doc's §3 — no cheap passes, no reading only surface rows.
- Write the verdict and the challenge-checked decisions into the plane template's **§4 (Rationale & verification)** (AC-012d).
- One sweep per gate: never run it per answer, which would tire the user without adding diligence.

The generic gate (SKILL.md §11) requires the sweep verdict to be **Pass** or **Pass-with-backlogs** — never **Blocked** — to advance (AC-012e).

---

## The six checks

1. **"Why did you do it that way?" for every decision (p. 157)** — for each decision row in §3, the "Why" must belong to one of three acceptable classes:
   - (a) it **traces to a lower-plane decision or the strategy** (e.g., "the IA uses a hierarchy because scope required matching the user's mental model"),
   - (b) it is a **deliberately chosen convention with a stated reason** (e.g., "we keep the left rail global-nav because that is the platform's established pattern and we stay consistent with it"),
   - (c) it is a **recorded flagged assumption** — back-referenced to a §5 row (e.g., "assumption A-1").
   Anything else → the agent prompts the user **once** for a real reason. If the user has none, the decision records the highest honest reason or becomes a flagged assumption — it is never left blank.

2. **Failure-mode check (p. 156)** — probe each decision for the three failure modes: is it **design by default** (it follows the technology or the organization rather than the user), **by mimicry** (an uncritical adoption of convention), or **by fiat** (a personal preference)? Any hit is challenged against user needs and product objectives, exactly as in the redesign probes.

3. **Upward-ripple check** — "does this decision force rethinking any higher plane not yet written?" If yes, **record it in the back-loop queue** (template §6 + `ux/session.md` with `plane / item / reason / status`); it is resolved at the closing cross-plane review, not here.

4. **Downward-override check** — "does this decision contradict a lower plane we already wrote?" If yes: **stop. Do not advance** until the contradiction is reconciled — either adjust the current plane's decision or schedule a lower-plane revisit and return to it (that lower doc gets a changelog row, its gate is re-run). A sweep with an unresolved downward contradiction is **Blocked** (FR-012c/e).

5. **Duality check** — are **both** template sections **§3A (FUNCTIONALITY)** and **§3B (INFORMATION)** non-empty **and** consistent with each other? If either side is missing or the sides contradict, return to the missing/inconsistent side and complete it before gating.

6. **Verdict output** — emit exactly one of:

   - **Pass** — all checks 1–5 clear; no open downward contradiction.
   - **Pass-with-backlogs** — checks 1–5 clear, but the back-loop queue carries upward-ripple / open items that will be resolved at the closing review.
   - **Blocked** — an unresolved downward contradiction exists; reconcile before advancing (never skip, never mark a Blocked plane as gated).

---

## Verdicts at a glance

| Verdict | Meaning | May the plane advance? |
|---|---|---|
| Pass | All checks clear; queue empty or no impact on this gate | Yes |
| Pass-with-backlogs | Checks clear; upward-ripple / open items queued for the closing review | Yes |
| Blocked | Unresolved downward contradiction (check 4) | No — reconcile, re-run the sweep |

---

## After the verdict

- Write the verdict into template **§4**, listing which decisions were challenge-checked and each "Why did you do it that way?" answer class (AC-012d).
- Update `ux/session.md`: plane status becomes `gate-passed` (Pass / Pass-with-backlogs) or `back-loop` (Blocked); append back-loop queue items.
- A **Blocked** verdict returns the session to the current plane (or the lower plane to revisit); the plane is not gated until a re-run sweeps clean.
- Only then state the natural stopping point and offer to continue to the next plane or stop (SKILL.md §5).
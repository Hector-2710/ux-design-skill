# Strategy — <Product>

<!-- Copy this template to ux/strategy.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2). -->

## 0. Metadata

<!-- Fill every field. Keep history: add changelog rows, never delete old ones. -->

- Product: <name>
- Mode: `new` | `redesign` | `both`
- Plane status: `drafted` | `gate-passed` | `revised`
- Date: <YYYY-MM-DD>

| date | what changed | why |
|---|---|---|
| <YYYY-MM-DD> | <initial write> | <first pass of this plane> |

Sources imported (PRD / spec / design system / brief / analytics / …):
- `Source: <user-provided X, v./date>` — <what was taken from it, where it now lives>
- <repeat per source; record provenance per intake>

## 1. Current state / Foundations

<!-- NEVER blank (AC-010g, AC-005d).
     Redesign mode: capture the existing product's facts for this plane,
     extracted per the current-state probes.
     New mode: record the imported brief / constraints / org context.
     If nothing exists, keep exactly the sentence below AND add one flagged
     assumption in §5 flagging the missing data. -->

None known — starting from scratch

## 2. Issues found (redesign mode only; N/A in new mode)

<!-- Redesign mode only (AC-010f): table of issues found in the current state.
     New mode: write N/A exactly. -->

| # | description | severity | evidence | trace-to-plane |
|---|---|---|---|---|
| 1 | <issue> | <Critical/High/Medium/Low> | <file:line / screenshot / URL> | <plane it belongs to> |

## 3. Decisions — FUNCTIONALITY side (3A)

<!-- Strategy 3A = Product objectives (AC-010e): the goals for the product and
     the conditions we will use to judge success. Fill rows as decided; if an
     optional item has no data it degrades to an assumption row in §5 — the
     3A section itself always exists (AC-010h). -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <product objective / condition for success> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — INFORMATION side (3B)

<!-- Strategy 3B = User needs (AC-010e): segments, personas, and research basis.
     Optional items (segmentation, personas, user research) follow the
     substitution ladder: ask → substitute with the user → flagged assumption.
     The section itself always exists. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <user-need fact or assumption-derived basis> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — Cross-cutting (3C)

<!-- Strategy 3C = Brand identity + success metrics (both sides) (AC-010e).
     Metrics with no tracked data still get candidate metrics tied to stated
     objectives, or a flagged assumption row. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <brand identity statement / success metric> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 4. Rationale & verification

<!-- Result of the verification sweep at this plane's gate (AC-012d).
     Verdict must be Pass or Pass-with-backlogs to advance; Blocked blocks. -->

**Sweep verdict:** `Pass` | `Pass-with-backlogs` | `Blocked`

Challenge-checked decisions and the "Why did you do it that way?" answer for each:
- <decision> — <traces to a lower plane / deliberately chosen convention with stated reason / recorded flagged assumption>

## 5. Assumptions (flagged)

<!-- Table columns per contract C-2 §5 (AC-010c). Every §3 decision that rests
     on an assumption back-references its row (e.g., "assumption A-1"). -->

| item | source | why flagged | plane | how to validate | validated? (open/yes/no) |
|---|---|---|---|---|---|
| <assumption> | <where it came from> | <why it is not yet known> | <plane that depends on it> | <how to check later> | open |

## 6. Back-loop queue & open items

<!-- Lower-plane revisits and higher-plane open items (contract C-2 §6). -->

| # | item | plane | reason | status |
|---|---|---|---|---|
| 1 | <thing to revisit> | <lower/higher plane> | <why> | open |
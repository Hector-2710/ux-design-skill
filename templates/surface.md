# Surface — <Product>

<!-- Copy this template to ux/surface.md and fill every section in place.
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

<!-- Surface 3A = Sensory design for functionality (AC-010e): the look and feel
     applied to the functional elements (controls, feedback, states) so that
     functionality reads clearly. The 3A section always exists. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <sensory decision for a functional element> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — INFORMATION side (3B)

<!-- Surface 3B = Sensory design for information (AC-010e): the look and feel
     applied to content and meaning — how information is made visually
     legible and ordered. The 3B section always exists. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <sensory decision for information/content> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — Cross-cutting (3C)

<!-- Surface 3C = Consistency, brand expression, eye-path / contrast /
     uniformity, color / type, and the style guide + design comp decisions
     (AC-010e). Record the internal and external consistency rules, the
     palette and typography, and the style-guide / comp contents. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <consistency rule / brand / eye-path / color / type / style-guide / comp> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

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
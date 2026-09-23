# Skeleton — <Product>

<!-- Copy this template to ux/skeleton.md and fill every section in place.
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

<!-- Skeleton 3A = Interface design (AC-010e): interface elements, their
     arrangement and defaults, and the trade-offs accepted for the user's
     most likely actions. The 3A section always exists. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <interface-design decision / element arrangement / default / trade-off> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — INFORMATION side (3B)

<!-- Skeleton 3B = Navigation design (AC-010e): navigation systems and
     wayfinding; plus information design: how content is grouped and
     presented, including error messages. The 3B section always exists. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <navigation / wayfinding / information-design decision> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3. Decisions — Cross-cutting (3C)

<!-- Skeleton 3C = Standard screens + wireframe-level arrangement (AC-010e):
     the list of standard screens and, per screen, the wireframe-level
     arrangement of the elements that make it up. -->

| Decision | Why (trace to lower plane / convention / assumption) | Back-loop flag? |
|---|---|---|
| <standard screen / wireframe-level arrangement> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

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
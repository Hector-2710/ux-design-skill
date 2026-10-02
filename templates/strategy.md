# Strategy — <Product>

<!-- Copy this template to ux/strategy.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2).
     The book's deliverable for this plane is the strategy document —
     product objectives + user needs, kept concise: "bigger is not
     necessarily better" (p. 36, 53). -->

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

## 3A. Product Objectives — FUNCTIONALITY side

<!-- Strategy 3A = Product objectives (AC-010e): what the organization wants
     to get out of the product (p. 36-38). State each objective WITH its
     condition for success — the observable state that lets us judge success
     later, "without defining the path to get there" (p. 38). If an optional
     item has no data it degrades to an assumption row in §5 — the 3A section
     itself always exists (AC-010h). -->

| Objective | Condition for success (no path pre-defined) | Why (trace to brief / convention / assumption) | Back-loop flag? |
|---|---|---|---|
| <product objective> | <what must observably be true to call it a success> | <traces to … / chosen convention because … / assumption A-N> | <yes/no> |

## 3B. User Needs — INFORMATION side

<!-- Strategy 3B = User needs (AC-010e): what users want to get out of the
     product (p. 36). Segments share "key characteristics and, critically,
     distinct sets of user needs" (p. 42-45); personas may be provisional
     (built with the user per the substitution ladder) and are then flagged
     in §5; research with no formal source degrades to a substitute or a
     flagged assumption. The section itself always exists (AC-010h). -->

**Segments**

| Segment | Key characteristics | Distinct needs | Why (trace) | Back-loop flag? |
|---|---|---|---|---|
| <segment name> | <who they are> | <needs only this segment has — note opposing needs> | <traces to … / assumption A-N> | <yes/no> |

**Personas** (one block per persona; provisional allowed → flagged in §5)

- **<Persona name>** — <role, one line>
  - Context: <situation of use>
  - Goals: <what success looks like for them>
  - Needs: <what the product must do for them>
  - Quote: *"<a representative sentence>"*
  - Basis: `research` | `provisional` (assumption A-N)
- <repeat per persona>

**User research basis:** <research performed (surveys, interviews, focus groups, contextual inquiry, task analysis, user testing — p. 46-49) | substitute used (server logs, feedback messages, informal testing — p. 157) | assumption A-N if none>

## 3C. Brand Identity & Success Metrics — Cross-cutting

<!-- Strategy 3C = the remaining strategy artifacts (AC-010e). Brand
     identity: the impression every interaction must leave — "the only
     choice is whether the impression happens by accident or as a result
     of conscious choices" (p. 38-39). Success metrics: the finish line for
     each objective, tracked after launch (p. 39-41). -->

**Brand identity:** <the conceptual associations and emotional reactions the product must create — a conscious choice, not an accident> — Why (trace): <…> | Back-loop flag?: <yes/no>

| Success metric | Tied to objective | Type | Tracked? | Why (trace) | Back-loop flag? |
|---|---|---|---|---|---|
| <metric> | <objective it measures> | <usage-based / indirect> | <yes / candidate — assumption A-N> | <traces to …> | <yes/no> |

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

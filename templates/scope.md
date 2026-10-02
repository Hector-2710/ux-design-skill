# Scope — <Product>

<!-- Copy this template to ux/scope.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2).
     The book's deliverables for this plane: functional specifications +
     content requirements (p. 62-74). -->

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

## 3A. Functional Specifications — FUNCTIONALITY side

<!-- Scope 3A = Functional specifications (AC-010e): the detailed
     description of the "feature set" of the product (p. 62). Write every
     requirement per the book's four rules (p. 70-71): POSITIVE (what the
     system will do), SPECIFIC (little left to interpretation),
     NON-SUBJECTIVE (falsifiable), QUANTITATIVE where possible (e.g.,
     "support at least 1,000 simultaneous users"). Optional feasibility
     data with no source degrades to a flagged assumption row in §5 — the
     3A section itself always exists. -->

| ID | Requirement (positive, specific, non-subjective, quantitative where possible) | Priority | Why (trace to strategy) | Back-loop flag? |
|---|---|---|---|---|
| F-1 | <what the product will do for the user> | <must / should / backlog> | <traces to strategy §3A/§3B … / assumption A-N> | <yes/no> |

## 3B. Content Requirements — INFORMATION side

<!-- Scope 3B = Content requirements (AC-010e): each content element defined
     by its attributes (p. 71-74) — don't confuse format with purpose (an
     FAQ is a format for "ready access to commonly needed information").
     Content inventory (p. 74): for redesigns, enumerate what exists; a
     partial inventory is allowed and flagged. Unknown owner → flagged
     assumption row in §5. The section itself always exists (AC-010h). -->

| Content element | Format | Size estimate | Owner | Update frequency | Audience | Why (trace) | Back-loop flag? |
|---|---|---|---|---|---|---|---|
| <element, by purpose not just format> | <text / image / audio / video / …> | <word count / pixel dimensions / …> | <who creates and maintains it> | <how often it is updated> | <which segment> | <traces to strategy … / assumption A-N> | <yes/no> |

**Content inventory** (redesign mode; new mode: N/A): `complete` | `partial — assumption A-N` — <what was enumerated, with the completeness marker>

## 3C. Prioritization, Out-of-Scope & Constraints — Cross-cutting

<!-- Scope 3C = the scope boundary (AC-010e). Prioritization weighs each
     requirement against strategy × feasibility (p. 74-77). Out-of-scope is
     explicit — knowing what we are NOT building (p. 59-60); the list is
     never empty. Constraints bind every higher plane (p. 65). -->

**Must-have core** (the requirements that prove the strategy): <F-…, and why these first> — Why (trace): <…>

**Out-of-scope / backlog** (never empty):

| Item | In the backlog because | Revisit when |
|---|---|---|
| <what we are deliberately NOT building, now or ever> | <reason / the strategy served by excluding it> | <trigger to reconsider> |

**Product-wide constraints:**

| Constraint | Type | Why / source | Back-loop flag? |
|---|---|---|---|
| <constraint> | <brand / technical / hardware> | <traces to strategy §3C / stated limit> | <yes/no> |

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

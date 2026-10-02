# Structure — <Product>

<!-- Copy this template to ux/structure.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2).
     The book's deliverable for this plane: the architecture diagram —
     "the major documentation tool" of this plane, expressed here in text
     form (p. 101). -->

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

## 3A. Interaction Design — FUNCTIONALITY side

<!-- Structure 3A = Interaction design (AC-010e): "the way the system
     responds to the user, and the way the user responds to the system"
     (p. 81-82). Two named artifacts: the conceptual model (p. 83-84) and
     the error-handling ladder (p. 86-88) — prevention first ("the best
     error message is the one that never appears"), then correction, then
     recovery. The 3A section always exists. -->

**Conceptual model:** <what users should believe about how the product works — "a thing the user consumes, a place the user visits, or an object the user acquires" (p. 83)>
- Basis: <familiar convention the model is built on / deliberate deviation + why> — Why (trace): <…> | Back-loop flag?: <yes/no>

**System response** (options, patterns, sequences of actions — p. 81-82):

| Interaction | Options / patterns offered | Sequence | Why (trace to scope) | Back-loop flag? |
|---|---|---|---|---|
| <user action or task> | <how the system accommodates it> | <order of steps> | <traces to scope … / assumption A-N> | <yes/no> |

**Error-handling ladder** (prevention → correction → recovery — p. 86-88):

| Error risk | Prevention | Correction | Recovery | Why (trace) | Back-loop flag? |
|---|---|---|---|---|---|
| <what can go wrong> | <design so it is impossible, then merely difficult> | <guide the user to figure out and fix it> | <undo / restore> | <traces to … / assumption A-N> | <yes/no> |

## 3B. Information Architecture — INFORMATION side

<!-- Structure 3B = Information architecture (AC-010e): how content is
     organized (p. 90-101). Nodes are "any piece or group of information"
     (p. 92); structure types: hierarchy / matrix / organic / sequential
     (p. 92-95); organizing principles "govern the arrangement of nodes"
     (p. 96-98); a controlled vocabulary keeps internal jargon off the
     surface, and metadata is "information about information" (p. 98-101).
     The 3B section always exists (AC-010h). -->

**Nodes:** <the major nodes — content units and their granularity>

**Structure type:** `hierarchy` | `matrix` | `organic` | `sequential` — Why (trace): <…> | Back-loop flag?: <yes/no>

**Organizing principles:**

| Principle | Groups together | Why (trace to strategy) | Back-loop flag? |
|---|---|---|---|
| <criterion> | <which nodes> | <traces to objectives/needs … / assumption A-N> | <yes/no> |

**Controlled vocabulary & metadata:**

| Canonical term | Avoid / alias | Why (trace) | Metadata fields (if any) | Back-loop flag? |
|---|---|---|---|---|
| <term users understand> | <jargon / synonyms it replaces> | <…> | <"information about information" the node carries> | <yes/no> |

## 3C. Architecture Diagram (text form) & Key Flows — Cross-cutting

<!-- Structure 3C = the plane's major documentation tool, the diagram
     (p. 101), expressed as a text/indented outline plus the key user
     flows, stepwise. This is the artifact the higher planes will read. -->

```
<text architecture diagram — indented outline of the structure, e.g.:>
Home
├── My Week
│   ├── Plan
│   └── Shopping list
└── My Recipes
    ├── Add
    └── Browse
```

**Key flows** (stepwise):

1. <flow name>: <step 1> → <step 2> → <step 3> — Why (trace): <…> | Back-loop flag?: <yes/no>
2. <repeat per key flow>

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

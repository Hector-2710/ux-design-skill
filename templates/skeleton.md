# Skeleton — <Product>

<!-- Copy this template to ux/skeleton.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2).
     The book's deliverable for this plane: wireframes over a small set of
     standard screens (p. 128-130). -->

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

## 3A. Interface Design — FUNCTIONALITY side

<!-- Skeleton 3A = Interface design (AC-010e): selecting the right interface
     elements and arranging them so they are readily understood and easily
     used (p. 114-118). Include DEFAULTS: "the interface should be designed
     so the user's most likely action requires the least effort"
     (p. 117-118). The 3A section always exists. -->

| Screen | Interface elements & arrangement | Default / most-likely action | Trade-off accepted | Why (trace to structure) | Back-loop flag? |
|---|---|---|---|---|---|
| <screen> | <the elements and how they are laid out> | <the least-effort action> | <what was traded, deliberately> | <traces to structure … / assumption A-N> | <yes/no> |

## 3B. Navigation Design & Information Design — INFORMATION side

<!-- Skeleton 3B = Navigation design + information design (AC-010e).
     Navigation: the five systems — global, local, supplementary,
     contextual, courtesy (p. 120-123) — plus wayfinding: users always know
     "where they are and where they can go" (p. 127), on every screen,
     because any page can be an entry point (p. 119-120). Information
     design: grouping and presentation for effective communication,
     including error messages and instructional text (p. 124-127). The 3B
     section always exists (AC-010h). -->

**Navigation systems:**

| System (global / local / supplementary / contextual / courtesy) | Covers | Why (trace) | Back-loop flag? |
|---|---|---|---|
| <system> | <what it lets users reach> | <traces to structure … / assumption A-N> | <yes/no> |

**Wayfinding cues** (on every screen): <color-coding (almost never alone), icons, labels, typography — what tells users where they are and where they can go> — Why (trace): <…>

**Information design** (grouping, presentation — p. 124-127):

| Content group | Presentation / emphasis | Why (trace) | Back-loop flag? |
|---|---|---|---|
| <what is grouped together> | <how it is arranged and emphasized> | <…> | <yes/no> |

**Error / instructional message composition:** <how messages are composed — plain language, the next step offered>

## 3C. Standard Screens & Wireframes — Cross-cutting

<!-- Skeleton 3C = the plane's deliverable (AC-010e): a small number of
     standard screens emerges (p. 128-130), each specified as a wireframe —
     "a bare-bones depiction of all the components of a page and how they
     fit together," as light as "pencil sketches with sticky notes
     attached" (p. 128-130). One text wireframe block per standard screen,
     with behavior notes attached. Deviate from convention only with
     explicitly defined reasons (p. 111) — the ledger records both. -->

**Standard screens:** <the list — keep it small>

**Wireframe — <screen name>** (repeat this block per standard screen)

```
<text wireframe: indented/ASCII layout of the elements on this screen>
```

- Behavior notes: <what each region does, the intended behavior>
- Why (trace to structure / §3A / §3B): <…> | Back-loop flag?: <yes/no>

**Conventions vs deliberate deviations:**

| Decision | Convention followed / deviation | Reason | Back-loop flag? |
|---|---|---|---|
| <element or pattern> | <convention / deviation> | <the explicitly defined reason — deviations need one (p. 111)> | <yes/no> |

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

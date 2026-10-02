# Surface — <Product>

<!-- Copy this template to ux/surface.md and fill every section in place.
     Never invent a doc shape: this template IS the structure (contract C-2).
     The book's deliverables for this plane: the design comp and the style
     guide (p. 148-151). -->

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

## 3A. Visual Design — Functionality side

<!-- Surface 3A = Sensory design for the functionality side (AC-010e): how
     interactive elements look so actions read clearly. Eye path: "where
     does the eye go first?" and the flow across the screen (p. 137-139).
     Contrast draws the eye to what matters; uniformity keeps the rest
     calm (p. 139-143). The 3A section always exists. -->

**Eye path** (per key screen — first → then → then):

| Key screen | Eye path (order of visual attention) | Why (trace to lower planes) | Back-loop flag? |
|---|---|---|---|
| <screen> | <first …, then …, then …> | <traces to skeleton/structure … / assumption A-N> | <yes/no> |

**Contrast & emphasis on functional elements** (controls, feedback, states — p. 139-143):

| Element | Contrast / emphasis decision | Why (trace) | Back-loop flag? |
|---|---|---|---|
| <control / state> | <how it stands out — or recedes> | <…> | <yes/no> |

## 3B. Visual Design — Information side

<!-- Surface 3B = Sensory design for the information side (AC-010e): how
     content is made visually legible and ordered — type sizes, hierarchy,
     information emphasis (p. 145-148). Distinct styles only to indicate
     actual differences in the information. Never blank (AC-010h). -->

| Content / information | Visual presentation decision | Why (trace) | Back-loop flag? |
|---|---|---|---|
| <content type> | <readability/legibility choice — sizes, hierarchy, emphasis> | <traces to … / assumption A-N> | <yes/no> |

## 3C. Design Comps & Style Guide — Cross-cutting

<!-- Surface 3C = the plane's two deliverables (AC-010e): the design comp
     (p. 148) — the visual analog of the wireframe, with a one-to-one
     mapping to wireframe components — and the style guide (p. 148-151),
     the compendium of every visual decision: grid, palette, typography,
     logo treatment, down to individual interface and navigation elements.
     Internal consistency (within the product) and external consistency
     (with the brand / other products) — p. 143-144. -->

**Consistency rules:**
- Internal: <different parts of the product reflect the same approach — the rules that make it one cohesive whole> — Why (trace to skeleton): <…>
- External: <how the product matches the brand / the organization's other products> — Why (trace to strategy §3C brand identity): <…>

**Design comps** (one per key standard screen — the visual analog of its wireframe, p. 148):

**Comp — <screen name>** (repeat this block per key screen)
- Described comp: <the finished look of this screen, in words>
- Wireframe mapping (1:1): <each wireframe component → the visual treatment it receives>
- Why (trace): <…> | Back-loop flag?: <yes/no>

**Style guide** (the compendium — p. 148-151):

| Area | Decision | Why (trace) | Back-loop flag? |
|---|---|---|---|
| Color palette | <role, color, usage — colors complement without competing (p. 145-147)> | <traces to brand …> | <yes/no> |
| Typography | <faces, sizes/weights, usage — simpler ones for body text (p. 147-148)> | <…> | <yes/no> |
| Grid / spacing | <uniformity standards — consistent element sizes, the grid (p. 139-143)> | <…> | <yes/no> |
| Logo treatment | <how and where the logo appears> | <…> | <yes/no> |
| Interface element standards | <buttons, forms, empty states, errors — down to individual elements> | <…> | <yes/no> |
| Navigation element standards | <nav bars, tabs, breadcrumbs — their visual rules> | <…> | <yes/no> |

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

# Structure — Question Bank (Ch 5)

> **Load this when** entering the **structure plane** — at intake when the session starts on structure, or when a mid-stream session back-fills into it — **see SKILL.md §6 (The plane loop)**.

**Plane's new question (AC-008g):** **"How is it going to work?"** (p. 81). *How do we know that?* "On the structure plane, we must identify how the product will work — the way the parts of the product fit together and behave" (p. 81). We "define how the pieces of the product fit together and behave… and how the product will respond to the user" (p. 81-82, "architecture").

**Required artifacts:** `ux/structure.md` per `templates/structure.md` — interaction design incl. conceptual models + error-handling strategy (3A), information architecture incl. vocabulary/metadata (3B), high-level flow + structure type (3C).

**Book grounding:** Jesse James Garrett, *The Elements of User Experience* 2nd ed., **Chapter 5** (p. 79-101). Page anchors: structure question (p. 81); interaction design — "the way the system responds to the user, and the way the user responds to the system" (p. 82-83); conceptual models (p. 83-84); error handling ladder *prevention → correction → recovery* (p. 86-88); IA nodes + structure types (hierarchy/matrix/organic/sequential) (p. 92-95); organizing principles (p. 96-98); controlled vocabulary + metadata (p. 98-101); the "architecture" of the high-level flow (p. 101).

---

## ARTIFACT GOALS

What "done" looks like on this plane (quoted):

- **Interaction design de ned** — "the way the system responds to the user, and the way the user responds to the system," including the "options provided to the user," "patterns" of behavior, and "sequences of actions" (p. 81-82). No interaction "black box": how the product behaves at each step is specified.
- **Consistent conceptual models** — "a conceptual model [is] how we believe our product will work in the minds of the user" (p. 83); models come from "metaphors, a spoken or unspoken understanding of how patterns of behavior work" (p. 84) and must "make sense to the users" (p. 83). Real-world convention is the default (p. 84); exotic models only when they "afford users a better way" (p. 83-84).
- **Error-handling ladder explicit** — the product pre-empts errors where it can ("the best error message is the one that never appears," p. 86); wherever errors can't be prevented it states how the user is "guided to correct" them and "how to recover" from them (p. 86-88). Actually an error-handling strategy, not a blank "the user will just figure it out."
- **A clear information architecture** — a "structure that doesn't force people to understand concepts they don't need to" (p. 96); nodes defined, a structure type chosen (p. 92-95), organizing principles stated (p. 96-98). IA is the information side of structure — never blank (AC-010e).
- **Shared vocabulary + metadata** — "a controlled vocabulary" where possible (p. 98), terms used consistently (p. 98), and metadata defined for the content that needs it (p. 100-101). This is the metadata half of the structure duality.

---

## CORE QUESTIONS

**Ordered most-important-first** (4-6 required; this bank has **6**). Each carries (a) plain phrasing, (b) book rationale ("why this?"), (c) new-mode and redesign-mode variants, (d) what template block it feeds.

### CORE-1 — How the system responds
- **Phrasing:** "How does the product respond to the user — what options, patterns, and sequences of actions does it offer?"
- **Why this?** Interaction design is "the way the system responds to the user, and the way the user responds to the system" (p. 81-82); the response includes the *options* offered, repeatable *patterns*, and the order/sequence of steps (p. 82). The most important interaction decisions shape everything above.
- **New-mode:** "We're new — when a user does X, what should the product do?"
- **Redesign-mode:** "How does the current product respond today — and where do those responses not match the strategy?"
- **Feeds:** template §3A (interaction design).

### CORE-2 — Conceptual model
- **Phrasing:** "What conceptual model are we using — what do we want users to *believe* about how this works?"
- **Why this?** "We can base our conceptual model on conventions the user is already familiar with" (p. 84); keep consistency "within the design" (p. 83). "People don't need to understand how the product works internally — only that it behaves the way they expect" (p. 83). An inconsistent or exotic model makes users guess.
- **New-mode:** "We're new — what real-world or familiar model should users rely on to predict us?"
- **Redesign-mode:** "What model does the current product implicitly use — and is that model carrying the right meaning?"
- **Feeds:** template §3A (conceptual model row).

### CORE-3 — Error-handling strategy
- **Phrasing:** "When something goes wrong, how do we prevent, correct, and recover — in that order?"
- **Why this?** The book's ladder: "the best error message is the one that never appears"; prevent where possible, then "guide the user" to correct, then "how the user can recover" (p. 86-88). Error handling is a structure-plane decision with a clear ladder — prevention, not blame.
- **New-mode:** "We're new — which user errors can we prevent outright, and where must we design correction/recovery?"
- **Redesign-mode:** "Where does the current product fail to prevent, correct, or recover — and which failure causes the most damage?"
- **Feeds:** template §3A (error-handling strategy) + verification gate.

### CORE-4 — Information architecture / nodes
- **Phrasing:** "How is content organized — what nodes exist, what structure type, and by what organizing principles?"
- **Why this?** IA "focuses on how the content… is organized" (p. 90); we define "the nodes," the structure type — hierarchy, matrix, organic, or sequential (p. 92-95) — and the "organizing principles" that "govern the arrangement of nodes" (p. 96-98). Users rely on this to find content; a bad IA hides everything.
- **New-mode:** "We're new — what are the top-level categories, and what principle orders them?"
- **Redesign-mode:** "What organizing principles does the current product actually use — even by accident — and which contradict each other?"
- **Feeds:** template §3B (IA).

### CORE-5 — Vocabulary & metadata
- **Phrasing:** "What vocabulary will the product use, consistently — and what metadata does the content need?"
- **Why this?** "A controlled vocabulary… ensures users and the system agree on terms" (p. 98); metadata "describes the content" to support retrieval and consistency (p. 100-101). Terminology consistency is a structure-plane decision that later planes must honor.
- **New-mode:** "We're new — what are the canonical names for our concepts, and what fields describe each content item?"
- **Redesign-mode:** "What overlapping terms does the current product use for the same thing — and which name wins?"
- **Feeds:** template §3B (vocabulary + metadata).

### CORE-6 — High-level flow / architecture
- **Phrasing:** "What is the overall pattern of how the product fits together — its architecture at a glance?"
- **Why this?** Structure is where we see "how the product will work as a whole" — the high-level flow and architecture tie the pieces together (p. 101). Capture the architecture as a flow, not a pile of screens.
- **New-mode:** "We're new — sketch the main path a user takes end to end."
- **Redesign-mode:** "What is the current end-to-end flow, and where does it no longer serve the structure we want?"
- **Feeds:** template §3C (flow/architecture).

---

## ELABORATION QUESTIONS

*Shallower variants of the cores, in `references/substitution-ladder.md` readiness — optional; use only when the user seems engaged/interested (AC-008e).*

1. **Error ladder depth.** "For each task, where do users most often slip — and can we prevent or correct that first?" (feeds CORE-3).
2. **Metaphor probe.** "Is there a familiar metaphor we could anchor our model to (e.g., shopping cart, inbox)?"
3. **Node granularity.** "How fine or coarse should our units of content be — what does one 'node' mean here?"
4. **Structure-type fit.** "Would our content be better served by a hierarchy, matrix, organic, or sequential structure?" (p. 94-95).
5. **Organizing-principle clarity.** "Have we named the organizing principles explicitly so nothing ships by accident?" (p. 96-98).
6. **Vocabulary conflicts.** "Which two terms are most likely to be used interchangeably by users — and which is canonical?" (p. 98).
7. **Metadata sufficiency.** "What metadata, if any, is needed to make content findable — without gold-plating?" (p. 100-101).

---

## OPTIONAL STEPS

*These optional items on this plane — only if the user wants them (AC-008f); each has a substitution-ladder fallback (`references/substitution-ladder.md`).*

| Optional item | When to offer | Substitute/fallback |
|---|---|---|
| IA diagram | If the flow is getting complex and the user is visuals-first | Map it inline as text/flow list; flag upstream |
| Error-state inventory | In redesign, if errors keep surfacing | Enumerate from what the user can name today; flag incomplete |
| Vocabulary/thesaurus list | If terms keep colliding | Small controlled-vocab table, flagged as partial |

_Anything skipped or substituted is recorded as an assumption in §5 of the template (AC-011) — never silently dropped._

---

## DUALITY BLOCKS

Feeds template **§3** (duality enforced structurally — AC-010e):

- **3A — FUNCTIONALITY side:** **Interaction design** — system response, options, patterns, sequences, conceptual model, error-handling ladder (p. 81-88).
- **3B — INFORMATION side:** **Information architecture** — nodes, structure type, organizing principles (p. 92-98); **vocabulary + metadata** (p. 98-101). Never blank (AC-010h).
- **3C — Cross-cutting:** **High-level flow / architecture** tying both sides into one whole (p. 101).

---

## REDESIGN PROBES

*Used with `references/redesign-audit.md` at the structure plane's current-state step (FR-016e).* "The difference is one of direction: structure must first extract what the existing product actually does."

1. "What conceptual model does the current product implicitly use — and is it consistent?"
2. "Where do users currently get stuck — which errors does the product fail to prevent?"
3. "What does the current IA actually look like, by accident — and which organizing principle, if any, governs it?"
4. "What terms does the current product use inconsistently for the same idea?"
5. "What is the current end-to-end flow — and which step is where users abandon?"

---

## GATE

Per-plane minimums (FR-013b structure / AC-013b) — gate **Pass**/**Pass-with-backlogs**; **Blocked** only on a downward contradiction (AC-013e):

- **Interaction design** specified: options, patterns, sequences, and a **conceptual model** stated positively (p. 81-84).
- **Error-handling ladder** present: prevention documented (or flagged), correction, recovery (p. 86-88).
- **Information architecture** non-blank: nodes + structure type + **organizing principles** (p. 92-98) — the information side is never empty (AC-010e/h).
- **Vocabulary/metadata** captured or flagged (p. 98-101).
- **High-level flow/architecture** sketched (p. 101).
- Every §3 decision has a non-empty "Why"; §1 never blank.
- Sweep verdict = Pass or Pass-with-backlogs (never Blocked) — `references/verification-sweep.md`.

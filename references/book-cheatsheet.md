# Book Cheatsheet — Concept Definitions and Page Anchors

> **Load this when** the user asks for book grounding or you need to explain a term from *The Elements of User Experience* — **see SKILL.md §3 (The method in one screen)**.

This file is the **single source of book-concept definitions** (NFR-008). Question banks and templates cite chapter and page anchors for rationale, but they do not re-define these concepts: a definition lives here, once, and the banks point to it. Page numbers are the printed book pagination (running page headers) and are navigation aids, not legal citations.

## How to use this file

- Look up a concept by its section heading or by scanning the tables below; each concept has a one-line definition and its page anchor.
- When a user asks "what does Garrett say about X?", answer from here, then continue the plane session normally.
- When you need the *why* behind a rule in a bank or template, quote the definition here rather than re-deriving it.

---

## 1. The model and the five plane dualities (p. 19-31, 161)

### The five planes (p. 19-21)

Five planes — Strategy, Scope, Structure, Skeleton, Surface — are a conceptual framework for talking about UX problems and the tools used to solve them. The whole user experience is the result of a stack of decisions that build on each other, and the goal is that no aspect happens without conscious, explicit intent (p. 19).

### Bottom-up dependency and the ripple effect (p. 22-24)

Each plane is dependent on the planes below it; decisions ripple both ways — choices on the strategy plane ripple all the way up, and an upper-plane decision that goes "out of bounds" forces rethinking lower planes. You cannot skip planes: the least visible ones (strategy and scope) play the most important role in success (p. 162). Planning rule: do not require work on a plane to finish before lower planes have finished — "do not build the roof of the house before you know the shape of its foundation" (p. 24).

### The five dualities (p. 25-31, 161)

Every plane splits down the middle: on the **functionality side** the product is a set of tools for accomplishing tasks; on the **information side** it is a set of content that must be findable, absorbable, and meaningful. Few products fall exclusively on one side (p. 31). Each row is the grounding for the template's paired FUNCTIONALITY / INFORMATION sections:

| Plane | FUNCTIONALITY side | INFORMATION side |
|---|---|---|
| Strategy | Product objectives | User needs |
| Scope | Functional specifications | Content requirements |
| Structure | Interaction design | Information architecture |
| Skeleton | Interface design | Navigation design (+ information design crossing both) |
| Surface | Sensory design | Sensory design |

---

## 2. Strategy concepts (Chapter 3)

| Concept | One-line definition | Page |
|---|---|---|
| **Conditions for success** | The objectives stated clearly enough to judge success later, "without defining the path to get there" — this keeps a project from leaping ahead to solutions (p. 38). | p. 38 |
| **Brand identity** | The set of conceptual associations or emotional reactions formed by any interaction with the product; branding is inescapable, so the only choice is by accident or by conscious choice (p. 38-39). | p. 38-39 |
| **Success metrics** | Indicators tracked after launch to see whether the product is meeting its own objectives and the users' needs — "races have finish lines"; usage-based (visits, conversion, returns) or indirect (support volume) (p. 39-41). | p. 39-41 |
| **User segmentation** | Dividing the audience into segments that share key characteristics and, critically, distinct sets of user needs; you need as many segments as you have different sets of needs, and segments can have directly opposing needs (p. 42-45). | p. 42-45 |
| **User research** | The methods for getting a sense of who users are — surveys/interviews/focus groups, contextual inquiry, task analysis, user testing, card sorting — because "users need usable products," the most universal need of all (p. 46-49). | p. 46-49 |
| **Personas** | A fictional character constructed to represent the needs of a whole range of real users; details are fictional inventions consistent with research, used at decision time — "Would that work for Janet? How would Frank react?" (p. 49-51). | p. 49-51 |

**Grounded note for this plane.** The two questions every product must answer (p. 36): *What do we want to get out of this product?* (product objectives, from the organization) and *What do our users want to get out of it?* (user needs, imposed from outside). Keep the strategy document **concise** — "bigger is not necessarily better" (p. 53) — and use it actively, not filed away.

---

## 3. Scope concepts (Chapter 4)

| Concept | One-line definition | Page |
|---|---|---|
| **Scope** | What the product will offer: strategy becomes scope when user needs and product objectives are translated into specific requirements for functionality and content (p. 57-58). | p. 57-58 |
| **Out-of-scope** | Knowing what you are NOT building, now or ever — an explicit list that keeps the project honest and gives the backlog somewhere to grow (p. 59-60). | p. 59-60 |
| **Four rules for requirements** | Write requirements (1) positively — what the system will do, not what it won't; (2) specifically — little left to interpretation; (3) without subjective language — falsifiable; (4) quantitatively where possible — e.g., "support at least 1,000 simultaneous users" (p. 70-71). | p. 70-71 |
| **Content requirements** | The information side of scope: required content elements (text, images, audio, video) specified with size estimates, ownership, update frequency/currency, and audience targeting; don't confuse format with purpose (e.g., an FAQ is a format for "ready access to commonly needed information") (p. 71-74). | p. 71-74 |
| **Content inventory** | An enumeration of all existing content so the whole team knows exactly what they have to work with — the starting habit for any redesign or content rework (p. 74). | p. 74 |
| **Prioritization and feasibility** | Requirements are weighed against strategic goals (product objectives and user needs) plus technical feasibility; features conflict and trade off, and conflicts are resolved by appealing to strategy — "focus on strategic goals, not proposed means of accomplishing them" (p. 74-77). | p. 74-77 |

---

## 4. Structure concepts (Chapter 5)

| Concept | One-line definition | Page |
|---|---|---|
| **Conceptual models** | Users' impressions of how the interactive components will behave — "a thing the user consumes, a place the user visits, or an object the user acquires"; the choice matters less than consistency across the product (p. 83). | p. 83 |
| **Error-handling ladder** | The layered defense: design so errors are impossible first, then merely difficult; help the user figure out and fix the error; then provide recovery (the famous undo function); warnings are the last resort — over-asking "Are you sure?" annoys more users than it helps (prevention → correction → recovery) (p. 86-88). | p. 86-88 |
| **Nodes and architecture types** | The node — "any piece or group of information" — is the basic unit of information structures, and its size sets the level of detail; nodes are arranged in structures: hierarchical (most common), matrix, organic, and sequential (p. 92-95). | p. 92-95 |
| **Organizing principles** | The criterion by which nodes are grouped together or kept separate; high-level principles tie closely to objectives and needs; the challenge is not creating a structure but creating the right one (p. 96-98). | p. 96-98 |
| **Controlled vocabulary and metadata** | A controlled vocabulary is a set of standard terms users will understand, enforced so internal jargon stays off the surface; metadata — "information about information" — enables flexible architectures and smarter search (p. 98-101). | p. 98-101 |

**Grounded note.** The structure plane's question is *How is it going to work?* — interaction design covers the options in performing tasks; information architecture covers conveying information, and neither is about technology but about understanding how people behave and think (p. 81). The major documentation tool is the architecture diagram, which communicates conceptual relationships (p. 101).

---

## 5. Skeleton concepts (Chapter 6)

| Concept | One-line definition | Page |
|---|---|---|
| **Interface design** | Selecting the right interface elements for the task and arranging them so they are readily understood and easily used; the test is whether the user "immediately notices the important stuff" (p. 114-118). | p. 114-118 |
| **Navigation systems** | The means by which users move through the product and see its structure: global, local, supplementary, contextual/inline, and courtesy navigation, plus the remote tools of a site map (hierarchical outline) and an index (alphabetical topic list) (p. 120-123). | p. 120-123 |
| **Wayfinding** | The cues — color-coding (almost never alone), icons, labels, typography — that help users understand "where they are and where they can go," jointly produced by information design and navigation design (p. 127). | p. 127 |
| **Information design** | The presentation of information for effective communication — grouping and arranging to reflect how users think, composing error messages and instructional text; good navigation cannot correct bad information design (p. 108, 124-127). | p. 108, 124-127 |
| **Standard screens and wireframes** | A small number of recurring standard screens usually emerges; wireframes are bare-bones depictions of all the components of a page and how they fit together, and can be as light as "pencil sketches with sticky notes attached" (p. 128-130). | p. 128-130 |

**Grounded note.** The telling test (p. 109): if it lets users *do* things, it's interface design; if it lets them *go* places, it's navigation design; if it *communicates ideas*, it's information design. Every screen must communicate "where am I, where can I go," because any page can be an entry point (p. 119-120). Convention matters: deviate from convention only with explicitly defined reasons (p. 111).

---

## 6. Surface concepts (Chapter 7)

| Concept | One-line definition | Page |
|---|---|---|
| **Eye path** | "Where does the eye go first?" — a successful design's eye path follows a smooth flow and gives users a guided tour of possibilities without overwhelming them with detail (p. 137-139). | p. 137-139 |
| **Contrast and uniformity** | Contrast is the primary tool for drawing the user's attention — make the important stuff stand out; uniformity (consistent element sizes, a grid) enables recombination and a shared visual order, but standards inadequate to your needs can be worse than none (p. 139-143). | p. 139-143 |
| **Internal and external consistency** | Internal consistency: different parts of the product reflect the same approach, designed once and reworked into "a system that operates as a cohesive, consistent whole"; external consistency: the product reflects the same design approach as other products from the same organization, a uniform impression of brand identity (p. 143-144). | p. 143-144 |
| **Color palettes and typography** | A standard palette selected so colors complement without competing; a handful of typefaces, simpler ones for body text; use distinct styles only to indicate actual differences in the information (p. 145-148). | p. 145-148 |
| **Design comp** | A visualization of the finished product built up from the components that have been chosen — the visual analog of the wireframe, with a one-to-one mapping to wireframe components even when the layout differs (p. 148). | p. 148 |
| **Style guide** | The definitive documentation of the design decisions — grids, palettes, typography, logo treatment, down to individual interface and navigation elements — because the reasons for decisions fade from memory; the single most effective way to keep a product looking like a cohesive whole (p. 148-151). | p. 148-151 |

**Grounded note.** Visual design is judged not by aesthetics alone but by "how effectively the design supports the objectives defined by each of the lower planes" (p. 136-137) — a surface decision can undermine or clarify every plane below it.

---

## 7. Method-level concepts (Chapter 8)

| Concept | One-line definition | Page |
|---|---|---|
| **The three failure modes** | Design by default (structure follows technology or the organization instead of users), design by mimicry (adopting conventions uncritically), and design by fiat (personal preference — "orange dominates because the senior VP is fond of it") — each a way decisions slip in without reference to user needs and objectives (p. 156). | p. 156 |
| **"Why did you do it that way?"** | The first question to ask yourself — and the first question you should be able to answer — about any aspect of the user experience; it grounds every decision in the underlying issues (p. 157). | p. 157 |
| **The marathon and the sprint** | Product development is a marathon, not a sprint: know which kind of race you're in and run accordingly; phases of pushing forward alternate with phases of pulling back, and thoughtful decisions cost time in the short term but save far more later (p. 159-161). | p. 159-161 |
| **Conscious intent** | The closing principle: by making everything the user experiences the result of a conscious, explicit decision, you ensure the product works to fulfill both strategic goals and user needs (p. 163). | p. 163 |

**Grounded note.** The two basic ideas behind successful UX design (p. 154): understand what problem you are solving — surface, skeleton, or structure — and understand the consequences of your solution, because every decision ripples up and down the planes. "Testing is never a substitute for a thoughtful, informed user experience design process" (p. 158), and the challenge is to understand users' needs better than they articulate them themselves (p. 159).
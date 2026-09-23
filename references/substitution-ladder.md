# Substitution Ladder — Optional Steps → Flagged Assumptions

> **Load this when** an optional step has no data — **see SKILL.md §8 (Optional steps → assumptions)**.

The substitution ladder rules how the six optional artifacts (personas, segmentation, success metrics, user research, content inventory, feasibility data) degrade when the user has no data for them. It guarantees the chain always terminates: an optional step never blocks a plane's gate, and a missing artifact is never dropped silently — it either gets a lightweight substitute built together with the user, or it becomes a flagged assumption.

---

## The three-part chain (apply in this order, always)

1. **① ALWAYS ASK** — ask the user directly for the data first. Users often know more than the prompt suggests; never assume "no data" without asking (FR-011, AC-011e).
2. **② Offer the lightweight substitute** — if there is no data, offer the per-item substitute below, and build it **with the user, never alone**: the user supplies what they *do* know (audience, job roles, objectives, existing artifacts), and you shape it into the substitute. The stream must never stall.
3. **③ Record a flagged assumption** — if the user declines the substitute or still has nothing, record a flagged assumption row in that plane's template §5 with the fields `item | source | why flagged | plane | how to validate`, and back-reference it from every §3 decision that rests on it.

**Rules that hold for every item:**
- Assumptions are never silent: they appear in template §5, and each §3 decision leaning on one carries a back-reference (e.g., "assumption A-1").
- Optional ≠ skippable: the optional artifact degrades to an *assumption row*, but its side section (§3A or §3B) always exists per the plane template (FR-010h, AC-011f).
- Optional items never block the gate: a plane can gate "Pass" or "Pass-with-backlogs" with assumption rows in place (AC-011a).

---

## 1. Personas

- **① Always ask:** "Do you have any user personas for this product — or anyone you could describe as the typical user?" (Even a self-described "sales rep who logs in twice a day" is a start.)
- **② Substitute offered:** a provisional persona built from what the user *does* know (role, behaviors, needs) following the book's Janet/Frank profile shape — a quote, age, occupation, technical profile, usage pattern (p. 49-51). Built with the user, never alone.
- **③ Assumption record:** `No formal research; provisional persona based on stated audience`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| Personas | user's stated audience / role descriptions | no formal persona research available | strategy (3B) | validate the provisional persona against real users at the first usability check or launch |

## 2. Segmentation

- **① Always ask:** "Who are the different audiences for this product, and do any of them have conflicting needs?"
- **② Substitute offered:** candidate segments derived from the stated audience(s), explicitly noting where their needs oppose each other (p. 42-45). Built with the user — confirm the segments against their own description of the audience.
- **③ Assumption record:** `Segments are hypotheses`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| Segmentation | stated audiences and their opposing needs | no data-backed segmentation study exists | strategy (3B) | confirm or refute with user research once budget allows |

## 3. Success metrics

- **① Always ask:** "How will you know the product has succeeded — what would you like to be able to track?"
- **② Substitute offered:** candidate metrics tied to the stated objectives, usage-based (visits, conversion, return visits) and indirect (support volume, sales-cycle time) (p. 39-41). Built with the user — each metric is checked against an objective it could measure.
- **③ Assumption record:** `Metrics proposed from objectives; not yet tracked`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| Success metrics | stated product objectives | no tracking plan or data exists yet | strategy (3C) | confirm the metrics are tracked and reviewable after launch |

## 4. User research

- **① Always ask:** "Do you have any research on users — surveys, interviews, any testing, session data?"
- **② Substitute offered:** the book's own lightweight substitutes for formal research — server logs, feedback messages, informal testing (p. 157). Built with the user: ask what data they already have sitting in logs, support tickets, or message threads and mine that together.
- **③ Assumption record:** `No research performed; evidence base is anecdotal`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| User research | informal / anecdotal evidence from the user | no formal research was performed | strategy (3B) | run lightweight research (logs, feedback, informal testing) before committing lower planes |

## 5. Content inventory

- **① Always ask:** "What content does the product have or need today — can you list the pages/assets you know about?"
- **② Substitute offered:** a partial inventory from what the user can enumerate at the keyboard (p. 74), recorded with a clear completeness marker. Built with the user — they type the list; you structure it.
- **③ Assumption record:** `Inventory incomplete`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| Content inventory | only the content the user can enumerate | full content audit not performed | scope (3B) | extend the inventory from the live product before content work starts |

## 6. Feasibility data

- **① Always ask:** "Have any of these requirements been checked against technical or resource feasibility?"
- **② Substitute offered:** a best-guess feasibility assessment per requirement — marked clearly as *unverified* — flagged for technical validation (p. 74-77). Built with the user — they supply the guess; you record the flag.
- **③ Assumption record:** `Feasibility unverified`

| item | source | why flagged | plane | how to validate |
|---|---|---|---|---|
| Feasibility data | best-guess from the user | no technical validation performed | scope (3C) | sign off feasibility with the implementing team before those items are committed |

---

## Summary table (design §4.8)

| Optional item | Substitute offered | Assumption record text |
|---|---|---|
| Personas (p. 49-51) | Provisional persona from stated audience in the Janet/Frank profile shape | `No formal research; provisional persona based on stated audience` |
| Segmentation (p. 42-45) | Candidate segments from stated audiences, noting opposing needs | `Segments are hypotheses` |
| Success metrics (p. 39-41) | Candidate metrics tied to stated objectives — usage-based and indirect | `Metrics proposed from objectives; not yet tracked` |
| User research (p. 46-49) | Server logs / feedback messages / informal testing (p. 157) | `No research performed; evidence base is anecdotal` |
| Content inventory (p. 74) | Partial inventory from what the user can enumerate | `Inventory incomplete` |
| Feasibility data (p. 74-77) | Best-guess feasibility flagged for technical validation | `Feasibility unverified` |

---

## Where each item lands in the plane docs

| Optional item | Plane doc | Side section |
|---|---|---|
| Personas | strategy.md | §3B INFORMATION (user needs) |
| Segmentation | strategy.md | §3B INFORMATION (user needs) |
| Success metrics | strategy.md | §3C Cross-cutting |
| User research | strategy.md | §3B INFORMATION (user needs) |
| Content inventory | scope.md | §3B INFORMATION (content requirements) |
| Feasibility data | scope.md | §3C Cross-cutting (prioritization) |

The assumption row is written into that doc's §5; the section named above still exists regardless of data availability (FR-010h).
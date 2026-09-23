# UX Issues — <Product>

<!-- Copy this template to ux/issues.md at the very end, after the closing
     cross-plane review is approved (contract C-3). Fill every section. -->

- Generated: <YYYY-MM-DD>
- Mode: `new` | `redesign` | `both`
- Plans reviewed: ux/strategy.md, ux/scope.md, ux/structure.md, ux/skeleton.md, ux/surface.md (and their revisions/changelog rows)
- Codebase reviewed: <paths / scope actually read, or "none accessible — artifact-based">
- Method note: every issue below traces to a plan decision or a code finding; none is invented.

## 0. Summary

<!-- Counts by plane and by severity, then the top 3 systemic themes. -->

**Counts by plane:** strategy <n> | scope <n> | structure <n> | skeleton <n> | surface <n>
**Counts by severity:** Critical <n> | High <n> | Medium <n> | Low <n>

**Top 3 systemic themes:**
1. <theme> — <one-line recommendation>
2. <theme> — <one-line recommendation>
3. <theme> — <one-line recommendation>

## 1. Issues

<!-- One row per issue. Fields per contract C-3. Section 1 is the offense list;
     section 2 lists what was verified as aligned. -->

| ID | Plane | Severity | Category | Finding | Evidence | Plan ref | Suggested direction | Status |
|---|---|---|---|---|---|---|---|---|
| UX-001 | <strategy/scope/structure/skeleton/surface> | <Critical/High/Medium/Low> | <Missing/Misaligned/Scope creep/Contradiction/Assumption-flag> | <1–2 concrete sentences> | <file path + line number, or the artifact pointed to> | <doc + section compared against> | <required change on the plan or code side> | open |

**Plane field note:** the plane the issue *belongs* to, which may differ from the plane where the code lives — a problem is ripple-diagnosed against all five planes before being assigned.

**Severity definitions:**
- **Critical** — blocks launch, loses data/trust, or actively harms the user (e.g., a core planned flow is missing entirely).
- **High** — materially contradicts a plan decision or a usability/IA baseline in the book's terms.
- **Medium** — deviation from plan with limited impact; scope creep that should be a decision, not an accident.
- **Low** — cosmetic, informational, or an assumption still unvalidated.

**Category definitions:**
- **Missing** — planned feature/content absent from code.
- **Misaligned** — implemented differently from the plan.
- **Scope creep** — present in code, absent from the plan (a decision made by default).
- **Contradiction** — implementation contradicts an explicit plan decision (incl. cross-plane conflicts).
- **Assumption-flag** — built on a plan assumption that code doesn't validate.

**Status note:** every issue starts `open`; this skill never closes them — the implementer agent updates Status later, outside this skill.

## 2. Verified-aligned (optional)

<!-- Plan areas checked and found consistent, so the implementer can skip them
     confidently. Delete this section or mark it N/A if nothing was checked. -->

- <plane / section> — <what was compared against code and found consistent>
- <repeat per checked area>

## 3. Handoff note

<!-- The closing statement of this skill's work. Keep, fill, and do not move. -->

- **This skill's work ends here; hand off to the implementer agent.** No fixing of code is performed by this skill.
- **Task brief (for the implementer):** <one paragraph the implementer could read: fix the Critical/High issues first, treat the Suggested direction column as the required change, and revisit Assumption-flag issues to validate or re-plan.>
- **Standing open assumptions:** <the unvalidated assumptions still open after the code pass — copied from each plane doc's §5 / the closing review, with their how-to-validate hints.>
  - <assumption A-1 — plane — how to validate — status: open>
  - <repeat per standing assumption>
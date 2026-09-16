---
name: ux-filters
description: "Apply filter and refinement pattern guidelines when building or reviewing list and table page UIs. Use this skill whenever anyone is implementing or reviewing the filtering experience for a list or table — including free-form text filters, structured filter side panels, active filter chips, and multi-value filter logic. Trigger for requests like: 'add filters to this table', 'implement a search/filter bar', 'how do I show active filters?', 'should this filter be all or any?', 'review my filter UX', or any task involving narrowing down rows in a list or table view. Apply pattern guidelines for filter behavior, layout, and logic only; defer to the project's existing design system for component and visual decisions."
---

# UX Filters Skill

This skill ensures filter and refinement experiences on list and table pages follow
the team's established guidelines for unstructured text filtering, structured filter
side panels, active filter chips, and multi-value filter logic. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/lists-and-tables/filters.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the filter guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page contains relative-path markdown links to other `.md` files (e.g. `tooltips.md`, `../entering-information/anatomy-of-form-field.md`), those are cross-references to other guidelines in the same repository. To follow them:

1. Resolve each relative path against the base URL of the guideline you just fetched. Sibling links stay in the same directory; `../` links climb to the parent and descend into the specified category folder.
2. Apply the URL confirmation policy to each resolved URL before fetching.
3. If a link points to a fragment/anchor within the same page (e.g. `guideline-name.md#section`), do not re-fetch — it's a self-reference.
4. If a link points to a file that returns a 404, note the gap in your response and proceed without that reference rather than stopping.

Do not wait for the user to provide these URLs — follow the links automatically as needed, subject to confirmation.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement filters on a list/table** | Apply the fetched rules for unstructured text filtering, structured filter side panels, active filter chips, and multi-value logic. |
| **Distinguish filtering from search** | Clarify the distinction per the fetched guidelines — filtering narrows visible items, search queries a broader dataset. |
| **Implement multi-value filter logic** | Apply the fetched "All / Any" button group pattern for ambiguous multi-select filters. |
| **Review existing filter behavior** | Evaluate hierarchy, layout, chip display, and multi-value logic against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the filter rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct unstructured text filter placement, hint text format, structured filter side panel pattern, active filter chip display, and multi-value All/Any logic per the fetched guidelines.
- Ensure unstructured and structured filters combine as an "and" relationship per the guidelines.
- Never default-apply filters on page load — list pages arrive with no filters applied per the guidelines.
- If the project's design system has filter, side panel, chip, or button group components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For distinguishing filtering from search
- Apply the fetched distinction directly. If the use case looks like site search rather than filtering, say so and redirect.

### For multi-value logic
- When a multi-select filter is in use, apply the fetched All/Any rule for resolving ambiguous "and" versus "or" behavior.

### For reviews
- Identify the filter hierarchy, chip display, and multi-value handling present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations such as ambiguous multi-value logic, missing active filter chips, or default-applied filters.

---

## Guidelines

- Always cite the source: _"Per the [Filter Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/filters)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

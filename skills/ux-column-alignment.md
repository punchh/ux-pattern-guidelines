---
name: ux-column-alignment
description: "Apply column alignment guidelines when building or reviewing tables or data grids. Use this skill whenever anyone is implementing or reviewing the horizontal or vertical alignment of data in table columns — including column headers, data types, and multi-line cell content. Trigger for requests like: 'how should I align this column?', 'prototype a data table', 'review my table alignment', 'should dates be left or right aligned?', 'how do I handle multi-line cells?', or any task involving tabular data display and alignment decisions. Apply pattern guidelines for alignment rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Column Alignment Skill

This skill ensures table and data grid column alignment follows the team's established
guidelines for data type, header alignment, and vertical alignment rules. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/lists-and-tables/column-alignment.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the column alignment guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
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
| **Determine alignment for a column** | Identify the data type and apply the correct horizontal alignment per the fetched guidelines. |
| **Generate a table prototype** | Build the table with correct horizontal and vertical alignment for all columns per the fetched guidelines. |
| **Review an existing table** | Evaluate column alignment against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the alignment rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For alignment decisions
- Identify the data type for each column in question.
- Apply the correct horizontal alignment per the fetched guidelines.
- Apply the correct vertical alignment rule based on the number of lines of text in the cell, per the fetched guidelines.

### For prototype generation
- Implement all column alignment per the fetched guidelines, including header alignment matching.
- If the project's design system has a table component with its own alignment conventions, defer to that component — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which alignment rules were applied per column.

### For reviews
- Identify the data type and current alignment of each column.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate data-type-driven alignment decisions.

---

## Guidelines

- Always cite the source: _"Per the [Column Alignment Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/column-alignment)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

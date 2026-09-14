---
name: ux-tables
description: "Apply table pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a data table experience — including landing pages showing a list of items, page-level and table-level actions, tabs, filters, sort selectors, item counts, table body structure, row interaction, and column resizing. Trigger for requests like 'build a data table page', 'add sorting to this table', 'review my table layout', or any question about filters on a table, or any task involving displaying records for browsing, managing, or drilling into. Also trigger when a design is presented for review or prototyping and any of the following are present — even without the user mentioning tables: a landing page showing a collection of records, a grid of rows and columns, or a management screen where users organize items and perform tasks on one or many. Apply pattern guidelines for structure, hierarchy, interaction, and behavior only; defer to the project's design system for visual decisions."
---

# UX Tables Skill

This skill ensures table landing pages follow the team's established guidelines for
element hierarchy, page and table-level actions, tabs, filters, sort selectors, item
counts, table body composition, row interaction, and column behavior. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from the
latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/tables
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the tables guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 2.5 — Proactively check for table pattern violations (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned tables,
check whether the design contains any context where the fetched guidelines would
apply. If so, flag violations or missing elements before proceeding.

- If the design shows a table with editable fields directly on rows, flag this as a violation per the fetched guidelines and recommend moving edits to a side panel, modal, or detail page.
- If the design shows row-click behavior that expands the row (accordion) rather than opening a detail view, flag this as a violation per the fetched guidelines.
- If the design shows specific action buttons on every row rather than a single overflow menu, flag this as a violation.
- If the design shows manually resizable columns, flag this against the fetched guideline against user-resizable columns.
- If the design lacks expected elements per the fetched guidelines (item count, sort selector, filters, page/table-level actions where warranted), flag the omissions.
- If the user explicitly wants to keep their current pattern despite the recommendation, note the concern, respect their decision, and proceed.
- If no violations or omissions are present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Design or prototype a table page** | Apply the fetched hierarchy, element placement, and interaction rules. |
| **Review an existing table page** | Evaluate structure, hierarchy, and interaction against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on element placement** | Answer questions about where page actions, tabs, filters, sort selectors, item counts, and table-level actions belong. |
| **Advise on row interaction** | Apply the fetched rules for drill-down behavior, bulk actions, and prohibited patterns. |
| **Explain the guidelines** | Summarise the table pattern in plain language. |

---

## Step 4 — Respond using the guidelines

### For design and prototyping
- Apply the correct element hierarchy: page-level actions clustered with the H1, tabs (if present), filters left-aligned above the table body, table-level actions right-aligned in the same span, item count and sort selector in the row just above the table body.
- Apply the fetched table body structure: checkboxes column (leftmost, if bulk actions are needed), identifier column, other data columns in priority order, action menu column (rightmost).
- Apply the fetched interaction rules for row clicks (drill down to detail view), bulk actions, and column resizing.
- Never put editable fields directly on table rows — editing happens in a side panel, modal, or dedicated detail page per the fetched guidelines.
- Never expand a row as an accordion on click — use a slide-out panel or navigate to a detail page.
- Never place specific action buttons on every row — use a single overflow context menu.
- Prefer a separate sort dropdown over sortable column headers per the fetched guidelines.
- If the project's design system has table, tab, filter, dropdown, checkbox, or context menu components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For reviews
- Identify each element of the table pattern present in the design.
- Evaluate placement, hierarchy, and behavior against the fetched guidelines.
- Flag violations — particularly inline row editing, accordion row expansion, per-row action buttons, sortable column headers on mixed-content tables, or user-resizable columns.

### For advising
- Answer directly from the fetched guidelines.
- If the question touches a related pattern (tabs, filters, bulk actions, empty states, cards, column alignment, truncation), the cross-reference step will surface those guidelines automatically.

---

## Guidelines

- Always cite the source: _"Per the [Tables Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/tables)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

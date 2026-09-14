---
name: ux-bulk-actions
description: "Apply bulk actions pattern guidelines when building or reviewing list and table UIs. Use this skill whenever anyone is implementing or reviewing a bulk selection experience, a floating action bar, multi-item operations, or checkboxes in a list or table context. Trigger for requests like: 'add bulk actions to this table', 'prototype a bulk delete flow', 'how should the action bar behave?', 'review my multi-select pattern', or any task involving selecting and acting on multiple items at once. Apply pattern guidelines for behavior, anatomy, and layout only; defer to the project's existing design system for component and visual decisions."
---

# UX Bulk Actions Skill

This skill ensures bulk action patterns follow the team's established guidelines
for anatomy, behavior, selection logic, and mixed-eligibility handling. Guidelines
are maintained externally and **must be fetched at runtime** so you always work
from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/bulk-actions
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the bulk actions guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Generate a prototype** | Build the bulk actions experience following the fetched guidelines for anatomy, visibility, selection logic, and mixed-eligibility behavior. |
| **Review an existing design** | Evaluate against the fetched guidelines. Flag violations with specific rule references and suggest corrections. |
| **Advise on behavior** | Apply the fetched rules to answer questions about when the bar appears/disappears, how mixed eligibility is handled, pagination scope, and filter scope. |
| **Explain the guidelines** | Summarise the relevant principles in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For prototype generation
- Implement the bulk actions bar anatomy and behavior per the fetched guidelines, including counter, button cluster, and clear selection link.
- Apply the correct visibility, positioning, and selection trigger rules from the fetched guidelines.
- Apply the fetched guidelines for mixed-eligibility scenarios and confirmation messaging.
- If the project's design system has components that cover any part of the bulk actions pattern (e.g. checkboxes, action bars, floating toolbars), defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component's behavior or layout and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For design reviews
- Identify which aspects of the bulk actions pattern are present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For behavior questions
- Answer directly from the fetched guidelines.
- If the scenario isn't explicitly covered, flag it to the user rather than assuming.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the pattern.

---

## Guidelines

- Always cite the source: _"Per the [Bulk Actions Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/bulk-actions)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

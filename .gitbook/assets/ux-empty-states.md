---
name: ux-empty-states
description: "Apply empty state pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a state where a list, table, feed, or container has no items to show — including first-use blank states, cleared empty states, no-results states, and coming-soon states. Trigger for requests like: 'what should this screen say when there's no data?', 'write copy for an empty list', 'prototype a blank state', 'review my no results message', or any task involving zero-item UI states. Apply pattern guidelines for copy tone, structure, and state classification only; defer to the project's existing design system for component and visual decisions."
---

# UX Empty States Skill

This skill ensures empty, blank, no-results, and coming-soon states follow the team's
established guidelines for classification, copy, and structure. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/empty-states
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the empty state guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Classify the state (required before generating anything)

The fetched guidelines define distinct state types, each with a different copy strategy.
Use the fetched guidelines to identify which type applies before writing copy or building
a prototype.

If the situation is ambiguous, ask the user one clarifying question before proceeding.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Generate copy** | Write main text and supporting text following the fetched guidelines for the identified state type. |
| **Generate a prototype** | Build the empty state UI with correct copy structure. Use the project's existing design system components for visual elements. |
| **Review existing copy or design** | Evaluate against the fetched guidelines. Flag misclassified states or copy that doesn't match the intended tone. |
| **Explain the guidelines** | Summarise the state types and copy principles in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For copy generation
- Provide main text and supporting text.
- Label which state type guided the copy.
- Note where placeholder content (content type, actor, benefit) should be substituted for the real context.
- Offer 1–2 alternatives if tone could reasonably vary.

### For prototype generation
- Implement the correct copy structure for the state type per the fetched guidelines.
- If the project's design system has an empty state component with its own structure or layout, defer to the design system component — do not override it to match the guidelines.
- If a conflict exists between the design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which state type and rules were applied.
- Use the project's existing design system components for all visual elements.

### For design reviews
- Identify the intended state type.
- Evaluate whether the copy and structure match the fetched guidelines for that type.
- Flag mismatches and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the guideline examples or invent minimal ones to illustrate the distinction between state types.

---

## Guidelines

- Always cite the source: _"Per the [Empty State Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/empty-states)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

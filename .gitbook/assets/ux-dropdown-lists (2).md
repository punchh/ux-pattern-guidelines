---
name: ux-dropdown-lists
description: "Apply dropdown list field guidelines when building or reviewing forms. Use this skill whenever anyone is choosing between dropdown lists, radio buttons, button groups, or combo boxes for a single-select field — or implementing a dropdown list. Trigger for requests like: 'should this be a dropdown or radio buttons?', 'implement a dropdown list', 'how many items should the menu show?', 'review my dropdown field', or any task involving a single-select field with a fixed set of options. Apply pattern guidelines for field type selection, behavior, and width rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Dropdown Lists Skill

This skill ensures dropdown list fields are used in the right context and follow the
team's established guidelines for option count thresholds, menu behavior, width, and
keyboard interaction. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/dropdown-lists
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the dropdown list guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Evaluate the option count, value length variability, and whether a default exists
against the fetched decision criteria to determine whether a dropdown list is the
correct field type. If another field type is more appropriate, recommend it before
proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Choose the right field type** | Evaluate the use case against the fetched decision criteria. |
| **Implement a dropdown list** | Apply the fetched toggle, max height, truncation, width, and keyboard behavior rules. |
| **Review a dropdown list** | Evaluate usage appropriateness and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the dropdown list rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct toggle behavior, max visible items, text truncation rule, width sizing, and keyboard interaction per the fetched guidelines.
- If the project's design system has a dropdown or select component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Evaluate whether the dropdown list is the correct field type.
- Evaluate behavior against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Dropdown List Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/dropdown-lists)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

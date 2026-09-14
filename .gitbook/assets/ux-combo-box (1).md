---
name: ux-combo-box
description: "Apply combo box field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a single-select or multi-select combo box — including option count thresholds, menu behavior, match highlighting, truncation, loading states, and no-match states. Trigger for requests like: 'implement a combo box', 'add a searchable dropdown', 'how should the multi-select combo box behave when populated?', 'review my combo box', or any task involving a searchable single or multi-select field with 10 or more options. Apply pattern guidelines for field type selection, behavior, and interaction only; defer to the project's existing design system for component and visual decisions."
---

# UX Combo Box Fields Skill

This skill ensures combo box fields are used in the right context and follow the team's
established guidelines for single and multi-select behavior, menu interaction, match
highlighting, populated state, truncation, and exception states. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/combo-box-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the combo box guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Determine whether single-select or multi-select is needed, and verify the option count
meets the fetched threshold for a combo box. If option count is below the threshold,
recommend the correct alternative field type before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Choose the right field type** | Evaluate option count and selection type against the fetched thresholds. |
| **Implement a combo box** | Apply the fetched behavior rules for the identified variant (single or multi-select). |
| **Review a combo box** | Evaluate usage appropriateness and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the combo box rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct menu trigger, keyboard behavior, max height, match highlighting, populated state, truncation, loading state, and no-match state rules per the fetched guidelines for the identified variant.
- If the project's design system has a combo box component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which variant and rules were applied.

### For reviews
- Evaluate whether the combo box is the correct field type.
- Evaluate all relevant behavior aspects against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Combo Box Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/combo-box-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

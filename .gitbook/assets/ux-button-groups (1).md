---
name: ux-button-groups
description: "Apply button group (segmented control) field guidelines when building or reviewing forms. Use this skill whenever anyone is choosing between button groups, radio buttons, dropdowns, or combo boxes for a single-select field — or implementing a button group field. Trigger for requests like: 'should this be a button group or radio buttons?', 'implement a segmented control', 'add a button group for this filter', 'review my button group field', or any task involving a horizontally grouped single-select input with a small number of short options. Apply pattern guidelines for field type selection and layout only; defer to the project's existing design system for component and visual decisions."
---

# UX Button Groups Skill

This skill ensures button group (segmented control) fields are used in the right
context and follow the team's established guidelines for usage, layout, and behavior.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/button-groups
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the button groups guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Evaluate the option count, option label length, and selection type against the fetched
guidelines to determine whether a button group is the correct field type. If another
field type is more appropriate, recommend it before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Choose the right field type** | Evaluate the use case against the fetched decision criteria and recommend button group or an alternative. |
| **Implement a button group** | Apply the fetched layout and behavior rules. |
| **Review a button group field** | Evaluate usage appropriateness and layout against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the button group rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct layout and behavior rules per the fetched guidelines.
- If the project's design system has a segmented control or button group component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Evaluate whether the button group is the correct field type for the use case.
- Evaluate layout and behavior against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Button Groups Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/button-groups)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

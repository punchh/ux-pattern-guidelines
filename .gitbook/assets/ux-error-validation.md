---
name: ux-error-validation
description: "Apply error validation pattern guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing form validation behavior — including when errors appear, how they are displayed on the submit button, in a toast, and on individual fields. Trigger for requests like: 'implement form validation', 'when should errors show?', 'add field-level error states', 'should I use inline validation?', 'review my error handling', or any task involving how a form communicates validation errors to the user. Apply pattern guidelines for validation timing, error display, and animation only; defer to the project's existing design system for component and visual decisions."
---

# UX Error Validation Skill

This skill ensures form error validation follows the team's established guidelines
for validation type, error display on the submit button, toast usage, field-level
error styling, and button animation. Guidelines are maintained externally and
**must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/error-validation
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the error validation guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
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
| **Implement form validation** | Apply the fetched rules for validation timing, submit button behavior, toast usage, and field-level error display. |
| **Review existing validation** | Evaluate validation type, error display, and button behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on validation approach** | Answer questions about inline vs summary validation, toast thresholds, and button animation from the fetched guidelines. |
| **Explain the guidelines** | Summarise the validation rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct validation type, submit button error behavior, toast threshold rule, field-level error styling, and button animation spec per the fetched guidelines.
- If the project's design system has form field error states, toast components, or button components, defer to those for visual treatment — do not override them to match the guidelines.
- If a conflict exists between a design system component's error styling and the guidelines (e.g. field error color), flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the validation type and all error display touchpoints present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations (including use of inline validation where the guidelines prohibit it) and suggest corrections.

### For advising
- Answer directly from the fetched guidelines.
- If the scenario isn't explicitly covered, flag it to the user rather than assuming.

---

## Guidelines

- Always cite the source: _"Per the [Error Validation Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/error-validation)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

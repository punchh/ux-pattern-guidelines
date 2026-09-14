---
name: ux-required-optional-fields
description: "Apply required versus optional field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing how required fields are marked — including asterisk usage, color, instructions, and accessibility. Trigger for requests like: 'mark required fields on this form', 'do I need to explain what the asterisk means?', 'how should required fields look?', 'review my required field indicators', or any task involving the visual and accessible treatment of required form fields. Apply pattern guidelines for required field marking only; defer to the project's existing design system for component and visual decisions."
---

# UX Required vs Optional Fields Skill

This skill ensures required field indicators follow the team's established guidelines
for asterisk usage, color treatment, instruction copy, and accessibility. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/required-versus-optional-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the required fields guidelines right now. Could you paste the
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
| **Implement required field indicators** | Apply the fetched asterisk, color, instruction, and accessibility rules. |
| **Review existing required field treatment** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the required field rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct asterisk usage, color treatment, instruction omission, and accessibility markup rules per the fetched guidelines.
- If the project's design system has a required field indicator component or form field anatomy, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify how required fields are currently marked.
- Evaluate each aspect (symbol, color, copy, accessibility) against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Required vs Optional Fields Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/required-versus-optional-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

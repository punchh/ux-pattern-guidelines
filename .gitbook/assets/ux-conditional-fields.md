---
name: ux-conditional-fields
description: "Apply conditional field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a field that appears or disappears based on another field's value — including placement, indentation, value preservation, and hide vs disable behavior. Trigger for requests like: 'add a conditional field to this form', 'show this field only when X is selected', 'should I hide or disable the conditional field?', 'review my conditional field logic', or any task involving progressive disclosure of form fields. Apply pattern guidelines for conditional field behavior and layout only; defer to the project's existing design system for component and visual decisions."
---

# UX Conditional Fields Skill

This skill ensures conditional fields follow the team's established guidelines for
placement, indentation, value preservation, and show/hide behavior. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/conditional-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the conditional fields guidelines right now. Could you paste the
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
| **Implement conditional fields** | Apply the fetched placement, indentation, value preservation, and show/hide rules. |
| **Review existing conditional fields** | Evaluate placement, indentation, and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on hide vs disable** | Answer directly from the fetched guidelines — this is a clear, unambiguous rule. |
| **Explain the guidelines** | Summarise the conditional field rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct placement (immediately following the trigger field), indentation treatment, value preservation logic, and show/hide behavior per the fetched guidelines.
- Never disable a conditional field — hide it, per the fetched guidelines.
- If the project's design system has indentation or dependency indicator components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the conditional field's trigger, placement, and show/hide behavior.
- Evaluate each against the fetched guidelines.
- Flag disabled-instead-of-hidden violations and misplaced conditional fields.

---

## Guidelines

- Always cite the source: _"Per the [Conditional Fields Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/conditional-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

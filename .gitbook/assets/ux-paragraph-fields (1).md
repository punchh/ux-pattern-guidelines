---
name: ux-paragraph-fields
description: "Apply paragraph field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a multi-line text input — including hint text, character counters, resize behavior, variant sizing, and auto-grow behavior. Trigger for requests like: 'add a text area to this form', 'implement a paragraph field', 'how should the character counter work?', 'how tall should this text area be?', 'review my paragraph field', or any task involving a multi-line freeform text input. Apply pattern guidelines for anatomy, sizing, and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Paragraph Fields Skill

This skill ensures paragraph fields follow the team's established guidelines for hint
text, character counters, resize behavior, variant sizing, and auto-grow interaction.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/paragraph-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the paragraph field guidelines right now. Could you paste the relevant
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
| **Implement a paragraph field** | Apply the fetched hint text, character counter, resize, variant sizing, and auto-grow rules. |
| **Review a paragraph field** | Evaluate anatomy and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on sizing** | Apply the fetched guidance on matching variant size to anticipated input length. |
| **Explain the guidelines** | Summarise the paragraph field rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct hint text pattern, character counter behavior (including threshold color change and over-limit messaging), resize grabber constraints, variant size selection, and auto-grow behavior per the fetched guidelines.
- If the project's design system has a textarea or paragraph field component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the hint text, character counter, resize, and sizing behavior present.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Paragraph Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/paragraph-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

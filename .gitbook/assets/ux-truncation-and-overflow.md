---
name: ux-truncation-and-overflow
description: "Apply truncation and overflow pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing how overflowing text or multiple values are handled in constrained spaces — including ellipsis usage, overflow counts, chip truncation in tables and fields, and hover reveal behavior. Trigger for requests like: 'how should I truncate this value?', 'implement overflow for this table cell', 'how do I show multiple chip values in a cell?', 'review my truncation behavior', or any task involving text or value overflow in lists, tables, dropdowns, or horizontal layouts. Apply pattern guidelines for truncation and overflow rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Truncation and Overflow Skill

This skill ensures truncation and overflow patterns follow the team's established
guidelines for ellipsis usage, truncation position, overflow labeling, chip behavior,
and hover reveal. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/truncation-and-overflow
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the truncation and overflow guidelines right now. Could you paste
> the relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the truncation context (required before generating anything)

The fetched guidelines distinguish between single-value truncation and multiple-value
truncation, and further between chips in a table cell, chips in a field or horizontal
layout, and vertical lists. Identify which context applies before implementing or
reviewing anything. If ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Implement truncation or overflow** | Apply the fetched rules for the identified context, including ellipsis style, position, overflow labeling, hover reveal, and accessibility. |
| **Review existing truncation behavior** | Evaluate against the fetched guidelines for the identified context. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the truncation rules in plain language with examples for each context. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct truncation style, position, overflow label format, hover reveal, and accessibility behavior per the fetched guidelines for the identified context.
- If the project's design system has chip, tag, or truncation components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which context and rules were applied.

### For reviews
- Identify the truncation context.
- Evaluate ellipsis usage, truncation position, overflow labeling, and hover reveal against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate each context's rules.

---

## Guidelines

- Always cite the source: _"Per the [Truncation and Overflow Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/truncation-and-overflow)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

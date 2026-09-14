---
name: ux-field-alignment
description: "Apply field alignment and column layout guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing the column layout of a form — including single vs multi-column decisions, field alignment, and reference pane usage. Trigger for requests like: 'lay out this form', 'should this form be two columns?', 'review my form layout', 'can I put fields side by side?', or any task involving the structural layout of form fields on a page. Apply pattern guidelines for layout and alignment rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Field Alignment and Column Layout Skill

This skill ensures form layouts follow the team's established guidelines for single-column
structure, left alignment, and reference pane usage. Guidelines are maintained externally
and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/field-alignment-and-column-layout
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the field alignment guidelines right now. Could you paste the
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
| **Lay out a form** | Apply the fetched single-column and left-alignment rules. Push back on multi-column requests per the guidelines. |
| **Review an existing form layout** | Evaluate column structure and field alignment against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on layout decisions** | Answer questions about column count, white space, and reference panes from the fetched guidelines. |
| **Explain the guidelines** | Summarise the layout rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For layout implementation
- Apply the correct column structure and field alignment per the fetched guidelines.
- If a multi-column layout is requested, push back and explain why per the fetched guidelines, then offer the correct single-column alternative.
- If the project's design system has form layout components or grid conventions, defer to those for structural scaffolding — do not override them to match the guidelines.
- If a conflict exists between a design system layout convention and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the column structure and field alignment in the design.
- Evaluate against the fetched guidelines.
- Flag multi-column layouts or misaligned fields and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Field Alignment Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/field-alignment-and-column-layout)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

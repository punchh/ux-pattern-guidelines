---
name: ux-descriptions-vs-tooltips
description: "Apply field description versus tooltip guidelines when building or reviewing forms. Use this skill whenever anyone is deciding whether supporting copy for a form field should be a visible description or a tooltip, writing field descriptions or tooltip content, or reviewing whether the right pattern is being used. Trigger for requests like: 'should this be a description or a tooltip?', 'write field help text', 'is this too long to be a description?', 'review my form copy', or any task involving supporting text or help content attached to a form field. Apply pattern guidelines for copy classification and usage only; defer to the project's existing design system for component and visual decisions."
---

# UX Descriptions vs Tooltips Skill

This skill ensures field descriptions and tooltips are used correctly and written
appropriately per the team's established guidelines for content type, length, and
usage intent. Guidelines are maintained externally and **must be fetched at runtime**
so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/descriptions-versus-tooltips
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the descriptions vs tooltips guidelines right now. Could you paste
> the relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the content (required before generating anything)

Use the decision guide in the fetched guidelines to determine whether the content
belongs in a description or a tooltip before writing or reviewing anything.

If the situation is ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Decide description vs tooltip** | Apply the fetched decision guide to determine the correct pattern. |
| **Write description or tooltip copy** | Write copy appropriate to the classified pattern, following the fetched guidelines for length and tone. |
| **Review existing field copy** | Evaluate whether the pattern and copy length match the fetched guidelines. Flag misclassifications and suggest corrections. |
| **Explain the guidelines** | Summarise the distinction in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For classification decisions
- State clearly which pattern is appropriate and why, using the fetched decision guide.
- If the content could reasonably go either way, explain the tradeoff and make a recommendation.

### For writing copy
- Write copy appropriate to the classified pattern per the fetched length and tone guidelines.
- Offer 1–2 alternatives if the content could be scoped differently.

### For reviews
- Identify the pattern currently in use (description or tooltip).
- Evaluate whether it's the right choice and whether the copy fits the fetched length and tone guidelines.
- Flag misclassifications and suggest corrected copy.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the distinction.

---

## Guidelines

- Always cite the source: _"Per the [Descriptions vs Tooltips Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/descriptions-versus-tooltips)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-information-banners
description: "Apply information banner guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an informational, warning, or tip banner — or deciding whether a banner is appropriate at all. Trigger for requests like: 'add a warning banner to this page', 'should this be a banner or a tooltip?', 'prototype an info banner', 'review my banner placement', 'what variant should this banner be?', or any task involving page-level or field-level alert or informational banner components. Apply pattern guidelines for usage, placement, and variant selection only; defer to the project's existing design system for component and visual decisions."
---

# UX Information Banners Skill

This skill ensures information banners follow the team's established guidelines for
usage frequency, placement, variant selection, and scope. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/information-banners
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the information banner guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the banner (required before generating anything)

Use the fetched guidelines to determine the correct variant (informational, warning,
or tip) and scope (page level or field level) before building or reviewing anything.
If the situation is ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use a banner** | Evaluate the use case against the fetched usage guidelines. |
| **Generate a banner prototype** | Build the banner using the correct variant, placement, and scope per the fetched guidelines. |
| **Review an existing banner** | Evaluate variant choice, placement, and scope against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the variants, placement rules, and usage principles in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For usage decisions
- State clearly whether a banner is appropriate and which variant fits, per the fetched guidelines.
- If it's not appropriate, name the correct alternative (e.g. field description, tooltip).

### For prototype generation
- Implement the correct variant, placement, and scope per the fetched guidelines.
- If the project's design system has banner or alert components, defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which variant and placement rules were applied.

### For reviews
- Identify the variant and placement of the banner in scope.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate variant and placement decisions.

---

## Guidelines

- Always cite the source: _"Per the [Information Banners Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/information-banners)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-autocomplete
description: "Apply autocomplete pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an autocomplete or type-ahead experience — including on-focus behavior, match highlighting, sort order, keyboard and mouse selection, and post-selection display. Trigger for requests like: 'add autocomplete to this field', 'implement type-ahead search', 'how should matches be highlighted?', 'review my autocomplete behavior', or any task involving predicting and surfacing matches as a user types. Apply pattern guidelines for autocomplete behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Autocomplete Skill

This skill ensures autocomplete and type-ahead patterns follow the team's established
guidelines for focus behavior, character threshold, match highlighting, sort options,
keyboard and mouse interaction, and post-selection display. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/autocomplete
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the autocomplete guidelines right now. Could you paste the relevant
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
| **Implement autocomplete** | Apply the fetched rules for focus behavior, character threshold, highlighting, sort order, keyboard and mouse selection, and post-selection display. |
| **Review existing autocomplete** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the autocomplete rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct on-focus behavior, character threshold, non-matching portion emphasis, sort strategy, keyboard and mouse/touch selection rules, and post-selection display per the fetched guidelines.
- If the project's design system has an autocomplete or combobox component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the autocomplete behavior present in the implementation or design.
- Evaluate each aspect against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Autocomplete Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/autocomplete)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

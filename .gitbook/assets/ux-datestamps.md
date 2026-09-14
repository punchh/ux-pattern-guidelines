---
name: ux-datestamps
description: "Apply datestamp and timestamp pattern guidelines when building or reviewing UI. Use this skill whenever anyone is displaying, formatting, or writing copy for dates, times, or time ranges — including absolute timestamps, relative timestamps, schedules, and time range displays. Trigger for requests like: 'how should I show when this was posted?', 'format this date correctly', 'prototype a notification timestamp', 'should this be relative or absolute time?', or any task involving date or time display in a UI. Apply pattern guidelines for format and display rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Datestamps and Timestamps Skill

This skill ensures date and time displays follow the team's established guidelines
for format, relative vs. absolute usage, and time range syntax. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/datestamps-and-timestamps
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the datestamp guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Identify the display context (required before generating anything)

The fetched guidelines distinguish several display situations with different formatting
rules. Use the fetched guidelines to identify which context applies before generating
anything.

If the context is ambiguous, ask one clarifying question before proceeding.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Format a specific date/time** | Apply the correct format from the fetched guidelines for the identified context. |
| **Decide relative vs. absolute** | Evaluate the use case against the fetched guidance on when each is appropriate. |
| **Generate a prototype** | Implement timestamp display using the correct format. Use the project's existing design system components for visual elements. |
| **Review existing timestamps** | Evaluate against the fetched guidelines. Flag format violations and suggest corrections. |
| **Explain the guidelines** | Summarise the relevant formatting rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For formatting
- Provide the correctly formatted output for the given date/time and context.
- Note which rule (absolute, relative, space-constrained, or range) governed the format.
- If both full and space-constrained formats are relevant, provide both.

### For relative vs. absolute decisions
- State clearly which is appropriate for the use case and why, per the fetched guidelines.

### For prototype generation
- Implement timestamp formatting per the fetched guidelines for the identified context.
- If the project's design system has a timestamp or date display component with its own formatting behavior, defer to the design system component — do not override it to match the guidelines.
- If a conflict exists between the design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which formatting rules were applied.
- Use the project's existing design system components for all visual elements.

### For design reviews
- Identify the timestamp format in use.
- Evaluate whether it matches the fetched guidelines for the context.
- Flag violations (e.g. wrong relative format, hyphen used in a range, trailing zeroes) and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the guideline tables or invent minimal examples to illustrate format decisions.

---

## Guidelines

- Always cite the source: _"Per the [Datestamp Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/datestamps-and-timestamps)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

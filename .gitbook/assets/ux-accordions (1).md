---
name: ux-accordions
description: "Apply accordion pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an accordion component — including deciding whether an accordion is appropriate, anatomy, icon and click region behavior, and supported content types. Trigger for requests like: 'add an accordion to this page', 'should this be an accordion?', 'review my expand/collapse component', 'can I put images inside this accordion?', or any task involving collapsible text content sections. Apply pattern guidelines for usage, anatomy, and content rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Accordions Skill

This skill ensures accordion components follow the team's established guidelines for
usage, anatomy, icon and click region behavior, content type, and expand/collapse
controls. Guidelines are maintained externally and **must be fetched at runtime** so
you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/accordions
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the accordion guidelines right now. Could you paste the relevant
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
| **Decide whether to use an accordion** | Evaluate the content type and context against the fetched usage criteria. |
| **Implement an accordion** | Apply the fetched anatomy, icon, click region, and expand/collapse rules. |
| **Review an existing accordion** | Evaluate anatomy and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the accordion rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether an accordion is appropriate for the use case per the fetched guidelines.
- If the content isn't suitable for an accordion, suggest the correct alternative per the fetched guidelines.

### For implementation
- Apply the correct icon style and direction, prepended icon position, full-row click region, and expand/collapse behavior per the fetched guidelines.
- Apply the fetched rules for what content is supported and what isn't.
- If the project's design system has an accordion or disclosure component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the accordion anatomy, icon treatment, click region scope, and content type present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Accordion Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/accordions)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

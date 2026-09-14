---
name: ux-tabs
description: "Apply tab pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a tab navigation component, deciding whether to use tabs, or asking about tab layout, usage rules, or nesting behavior. Trigger for requests like: 'should I use tabs here?', 'add tabs to this page', 'review my tab layout', 'how many tabs is too many?', 'can I nest tabs?', or any task involving tab-based navigation or content organization. Apply pattern guidelines for usage, layout, and interaction only; defer to the project's existing design system for component and visual decisions."
---

# UX Tabs Skill

This skill ensures tab patterns follow the team's established guidelines for usage,
layout, interaction, and nesting rules. Guidelines are maintained externally and
**must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/tabs
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the tab guidelines right now. Could you paste the relevant section
> here so I can apply them?"_
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
| **Decide whether to use tabs** | Evaluate the use case against the fetched "use tabs when" and "don't use tabs when" criteria. |
| **Generate a tab prototype** | Build the tab layout following the fetched guidelines for alignment, viewport behavior, nesting, and content placement. |
| **Review an existing tab layout** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the relevant principles in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether tabs are appropriate for the use case and why, per the fetched guidelines.
- If tabs are not appropriate, suggest the correct alternative per the fetched guidelines.

### For prototype generation
- Implement tab layout and interaction per the fetched guidelines.
- If the project's design system has a tab component with its own layout or interaction behavior, defer to that component — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For reviews
- Identify which tab pattern decisions are present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate usage and nesting decisions.

---

## Guidelines

- Always cite the source: _"Per the [Tabs Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/tabs)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-hover-interactions
description: "Apply hover interaction pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing hover behavior — including tooltips, revealed content, affordances, hover timing, or hover zone definitions. Trigger for requests like: 'how should this tooltip appear on hover?', 'implement a hover reveal', 'review my hover behavior', 'when should hover content show or hide?', or any task involving mouse-over interactions and the timing or zone logic behind them. Apply pattern guidelines for behavior and timing only; defer to the project's existing design system for component and visual decisions."
---

# UX Hover Interactions Skill

This skill ensures hover interaction patterns follow the team's established guidelines
for timing, affordances, hover zones, and content persistence. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/hover-interactions
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the hover interaction guidelines right now. Could you paste the
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
| **Implement hover behavior** | Apply the fetched timing, affordance, hover zone, and persistence rules to the implementation. |
| **Review existing hover behavior** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on hover behavior** | Answer questions about timing, zone scope, or affordance rules directly from the fetched guidelines. |
| **Explain the guidelines** | Summarise the relevant principles in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct timing delays, affordance behavior, hover zone scope, and content persistence rules per the fetched guidelines.
- If the project's design system has components with their own hover behavior (e.g. a tooltip component with baked-in timing), defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component's hover behavior and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify which hover behaviors are present.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For behavior questions
- Answer directly from the fetched guidelines.
- If the scenario isn't explicitly covered, flag it to the user rather than assuming.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate timing and zone decisions.

---

## Guidelines

- Always cite the source: _"Per the [Hover Interaction Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/hover-interactions)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

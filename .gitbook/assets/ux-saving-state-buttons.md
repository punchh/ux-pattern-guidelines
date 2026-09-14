---
name: ux-saving-state-buttons
description: "Apply saving state button guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing the loading/saving state of a submit, save, next, or back button — including spinner usage, text changes, disabled state during save, and minimum persistence duration. Trigger for requests like: 'add a saving state to this button', 'what should the button say while saving?', 'how long should the spinner show?', 'review my save button behavior', or any task involving a button that triggers a save, submit, or navigation action in a form. Apply pattern guidelines for saving state behavior and timing only; defer to the project's existing design system for component and visual decisions."
---

# UX Saving State on Buttons Skill

This skill ensures save/submit buttons exhibit the correct saving state behavior per
the team's established guidelines for spinner usage, label text, disabled state timing,
and minimum persistence. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/saving-state-on-buttons
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the saving state guidelines right now. Could you paste the relevant
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
| **Implement saving state** | Apply the fetched rules for state change, spinner, label text, disabled behavior, and minimum persistence. |
| **Review existing button saving state** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on saving state** | Answer questions about which buttons need saving state and how long to persist it. |
| **Explain the guidelines** | Summarise the saving state rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct on-click state change, spinner insertion, label text pattern, temporary disabled state, and minimum persistence duration per the fetched guidelines.
- Apply the fetched guidelines for which button types require saving state.
- If the project's design system has a loading button or spinner component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify which buttons have saving state implemented and how.
- Evaluate each against the fetched guidelines.
- Flag missing saving states or timing violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Saving State on Buttons Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/saving-state-on-buttons)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-success-notification
description: "Apply success notification guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a success toast notification — including fade timing, persistence duration, stacking behavior, and accessibility. Trigger for requests like: 'add a success toast to this action', 'how long should the toast show?', 'implement stacked notifications', 'review my success message behavior', or any task involving post-action success feedback to the user. Apply pattern guidelines for toast behavior, timing, and animation only; defer to the project's existing design system for component and visual decisions."
---

# UX Success Notification Skill

This skill ensures success toast notifications follow the team's established guidelines
for fade timing, persistence duration, stacking behavior, positioning, and accessibility.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/success-notification
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the success notification guidelines right now. Could you paste the
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
| **Implement a success toast** | Apply the fetched fade, persistence, stacking, positioning, and accessibility rules. |
| **Review an existing success toast** | Evaluate timing, stacking, and accessibility against the fetched guidelines. Flag violations and suggest corrections. |
| **Write success toast copy** | Apply the fetched copy guidelines, or refer to the `ux-grammar-voice-tone` skill for tone guidance. |
| **Explain the guidelines** | Summarise the success notification rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct fade in/out timing, persistence duration, stacking animation behavior, positioning, and ARIA accessibility markup per the fetched guidelines.
- If the project's design system has a toast or notification component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component's animation or positioning and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the toast timing, stacking, positioning, and accessibility implementation.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For copy
- Apply the fetched copy guidelines, and cross-reference the grammar, voice, and tone guidelines if linked from the fetched page.

---

## Guidelines

- Always cite the source: _"Per the [Success Notification Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/success-notification)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

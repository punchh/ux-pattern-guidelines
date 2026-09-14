---
name: ux-saving-drafts
description: "Apply draft saving pattern guidelines when building or reviewing multi-step forms. Use this skill whenever anyone is implementing or reviewing the ability to save an incomplete form as a draft — including when to surface the save and close button, navigation button draft-saving behavior, and success feedback. Trigger for requests like: 'add save as draft to this form', 'when should save and close appear?', 'do the back and next buttons save a draft?', 'review my draft saving behavior', or any task involving preserving incomplete form state for later completion. Apply pattern guidelines for draft saving rules and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Saving Drafts Skill

This skill ensures draft saving patterns follow the team's established guidelines for
when to surface the save and close button, navigation button draft-saving behavior, and
success feedback. Guidelines are maintained externally and **must be fetched at runtime**
so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/saving-drafts
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the saving drafts guidelines right now. Could you paste the relevant
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
| **Implement draft saving** | Apply the fetched rules for save and close surfacing, navigation button behavior, and success feedback. |
| **Review existing draft saving behavior** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on draft saving decisions** | Answer questions about when save and close should appear and how navigation buttons relate to draft saving. |
| **Explain the guidelines** | Summarise the draft saving rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct save and close surfacing trigger, navigation button draft-save behavior, destination on save, and success toast feedback per the fetched guidelines.
- If the project's design system has button or toast components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the draft saving touchpoints in the design (save and close button, navigation buttons, feedback).
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Saving Drafts Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/saving-drafts)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

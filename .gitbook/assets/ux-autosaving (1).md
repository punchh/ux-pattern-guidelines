---
name: ux-autosaving
description: "Apply autosaving pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an autosave experience — including deciding whether autosave is appropriate, which controls support it, and how to communicate save feedback. Trigger for requests like: 'implement autosave for this form', 'should this toggle switch autosave?', 'can I mix autosave and manual save?', 'review my autosave pattern', or any task involving passively saving form state without an explicit user save action. Apply pattern guidelines for autosave usage and control rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Autosaving Skill

This skill ensures autosave patterns follow the team's established guidelines for
when autosave is appropriate, which control types support it, mixing rules, and
feedback requirements. Guidelines are maintained externally and **must be fetched
at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/autosaving
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the autosaving guidelines right now. Could you paste the relevant
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
| **Decide whether to use autosave** | Evaluate the form's control types and context against the fetched guidelines. |
| **Implement autosave** | Apply the fetched rules for control types, mixing restrictions, and feedback requirements. |
| **Review an existing autosave pattern** | Evaluate control types, mixing, and feedback against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the autosave rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- Evaluate the form's control types against the fetched guidelines to determine whether autosave is appropriate.
- If it's not appropriate, explain why per the fetched rules and suggest the correct alternative.

### For implementation
- Apply the correct control type requirements, mixing restrictions, and save feedback rules per the fetched guidelines.
- If the project's design system has toggle switch or save feedback components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the control types in use and whether autosave feedback is present.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the control type and mixing rules.

---

## Guidelines

- Always cite the source: _"Per the [Autosaving Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/autosaving)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

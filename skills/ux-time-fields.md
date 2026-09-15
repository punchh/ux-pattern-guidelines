---
name: ux-time-fields
description: "Apply time field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a time input — including typed-only vs interval-dropdown behavior, segment-to-segment focus advancement, and type-ahead behavior. Trigger for requests like: 'add a time field to this form', 'implement a time picker', 'how should the hours and minutes segments work?', 'review my time input', or any task involving time entry in a form. Apply pattern guidelines for time field behavior and interaction only; defer to the project's existing design system for component and visual decisions."
---

# UX Time Fields Skill

This skill ensures time fields follow the team's established guidelines for typed-only
vs interval-dropdown behavior, segment navigation, and type-ahead interaction. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/time-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the time field guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Determine whether the time field is typed-only (free-form) or interval-based
(typed + dropdown selectable), as the interaction rules differ.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Implement a time field** | Apply the fetched segment navigation, valid character acceptance, and type-ahead rules for the identified variant. |
| **Review a time field** | Evaluate behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the time field rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct segment-to-segment focus advancement, valid character acceptance, Tab key behavior, menu interaction, option alignment, and type-ahead behavior per the fetched guidelines for the identified variant.
- If the project's design system has a time picker component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which variant and rules were applied.

### For reviews
- Identify the time field variant and evaluate behavior against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Time Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/time-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

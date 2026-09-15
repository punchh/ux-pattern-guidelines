---
name: ux-checkbox-fields
description: "Apply checkbox field guidelines when building or reviewing forms. Use this skill whenever anyone is choosing between checkboxes, toggle switches, combo boxes, or other field types for a multi-select or single-confirmation scenario — or implementing a checkbox field. Trigger for requests like: 'should this be a checkbox or a toggle?', 'implement a multi-select checkbox list', 'add a single confirmation checkbox', 'how do I handle an indeterminate checkbox state?', 'review my checkbox field', or any task involving a checkbox input. Apply pattern guidelines for field type selection, layout, and interaction only; defer to the project's existing design system for component and visual decisions."
---

# UX Checkbox Fields Skill

This skill ensures checkbox fields are used in the right context and follow the team's
established guidelines for usage, layout, indeterminate state, and interaction. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/checkbox-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the checkbox field guidelines right now. Could you paste the relevant
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

Evaluate the option count, selection type, and form save behavior against the fetched
guidelines to determine whether a checkbox is the correct field type. If another field
type is more appropriate (e.g. toggle switch, multi-select combo box), recommend it
before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Choose the right field type** | Evaluate the use case against the fetched decision criteria. |
| **Implement a checkbox field** | Apply the fetched layout, interaction, and indeterminate state rules. |
| **Review a checkbox field** | Evaluate usage appropriateness, layout, and interaction against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the checkbox rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct layout, interaction rules, and indeterminate state behavior per the fetched guidelines.
- If the project's design system has a checkbox component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Evaluate whether the checkbox is the correct field type for the use case.
- Evaluate layout and interaction against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Checkbox Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/checkbox-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

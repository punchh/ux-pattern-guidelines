---
name: ux-date-fields
description: "Apply date field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a date input — including hint text format, date picker behavior, date range handling, criss-crossed date logic, and error validation messages. Trigger for requests like: 'add a date picker to this form', 'implement a date range field', 'what error message should show for an invalid date?', 'review my date field', or any task involving date input in a form. Apply pattern guidelines for date field behavior and validation only; defer to the project's existing design system for component and visual decisions."
---

# UX Date Fields Skill

This skill ensures date fields follow the team's established guidelines for hint text,
picker behavior, date range highlighting, criss-crossed date logic, and error messages.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/date-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the date field guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page contains relative-path markdown links to other `.md` files (e.g. `tooltips.md`, `../entering-information/anatomy-of-form-field.md`), those are cross-references to other guidelines in the same repository. To follow them:

1. Resolve each relative path against the base URL of the guideline you just fetched. Sibling links stay in the same directory; `../` links climb to the parent and descend into the specified category folder.
2. Apply the URL confirmation policy to each resolved URL before fetching.
3. If a link points to a fragment/anchor within the same page (e.g. `guideline-name.md#section`), do not re-fetch — it's a self-reference.
4. If a link points to a file that returns a 404, note the gap in your response and proceed without that reference rather than stopping.

Do not wait for the user to provide these URLs — follow the links automatically as needed, subject to confirmation.

---

## Step 3 — Classify the use case (required before generating anything)

Determine whether this is a single date field or a date range (start + end pair),
as the behavior rules differ. If a date range, the criss-crossed date logic also applies.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Implement a date field** | Apply the fetched hint text, picker behavior, and state rules for the identified variant. |
| **Implement a date range** | Apply the fetched range highlighting and criss-crossed date resolution rules. |
| **Write error validation messages** | Apply the fetched error message copy for too-early, too-late, and invalid date scenarios. |
| **Review a date field** | Evaluate behavior and validation against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the date field rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct hint text format, picker invocation behavior, disabled date styling, selected date highlighting, and criss-crossed date resolution per the fetched guidelines.
- If the project's design system has a date picker component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For error messages
- Apply the fetched error copy for each scenario (too early, too late, invalid date).
- Do not invent error copy that isn't in the fetched guidelines.

### For reviews
- Identify the date field variant and evaluate all behavior aspects against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Date Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/date-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

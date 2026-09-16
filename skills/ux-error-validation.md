---
name: ux-error-validation
description: "Apply error validation pattern guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing form validation behavior — including when errors appear, how they are displayed on the submit button, in a toast, and on individual fields. Trigger for requests like: 'implement form validation', 'when should errors show?', 'add field-level error states', 'should I use inline validation?', 'review my error handling', or any task involving how a form communicates validation errors to the user. Apply pattern guidelines for validation timing, error display, and animation only; defer to the project's existing design system for component and visual decisions."
---

# UX Error Validation Skill

This skill ensures form error validation follows the team's established guidelines
for validation type, error display on the submit button, toast usage, field-level
error styling, and button animation. Guidelines are maintained externally and
**must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/error-validation.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the error validation guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
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

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement form validation** | Apply the fetched rules for validation timing, submit button behavior, toast usage, and field-level error display. |
| **Review existing validation** | Evaluate validation type, error display, and button behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on validation approach** | Answer questions about inline vs summary validation, toast thresholds, and button animation from the fetched guidelines. |
| **Explain the guidelines** | Summarise the validation rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct validation type, submit button error behavior, toast threshold rule, field-level error styling, and button animation spec per the fetched guidelines.
- If the project's design system has form field error states, toast components, or button components, defer to those for visual treatment — do not override them to match the guidelines.
- If a conflict exists between a design system component's error styling and the guidelines (e.g. field error color), flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the validation type and all error display touchpoints present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations (including use of inline validation where the guidelines prohibit it) and suggest corrections.

### For advising
- Answer directly from the fetched guidelines.
- If the scenario isn't explicitly covered, flag it to the user rather than assuming.

---

## Guidelines

- Always cite the source: _"Per the [Error Validation Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/error-validation)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

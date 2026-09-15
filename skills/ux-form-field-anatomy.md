---
name: ux-form-field-anatomy
description: "Apply form field anatomy guidelines when building or reviewing any form field. Use this skill whenever anyone is implementing or reviewing the supporting elements of a form field — including description text, tooltips, required indicators, input region sizing, syntax icons, hint text, clear buttons, right-most icons, and error messages. Trigger for requests like: 'add a description to this field', 'where does the error message go?', 'how wide should this input be?', 'review my field layout', or any task involving the structural elements that surround or support a form field's input region. Apply pattern guidelines for field anatomy and element hierarchy only; defer to the project's existing design system for component and visual decisions."
---

# UX Form Field Anatomy Skill

This skill ensures form field anatomy follows the team's established guidelines for
element hierarchy, placement, and usage of all supporting field elements. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/anatomy-of-form-field.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the form field anatomy guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement a form field** | Apply the fetched anatomy elements in the correct hierarchy and placement. Include only the elements warranted by the field's context. |
| **Review a form field layout** | Evaluate which anatomy elements are present, their placement, and their usage against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on a specific element** | Answer questions about description text, tooltip, input region width, hint text, syntax icons, or error placement from the fetched guidelines. |
| **Explain the guidelines** | Summarise the anatomy elements and their hierarchy in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply only the anatomy elements warranted by the field's context — not all elements are required on every field.
- Apply the correct input region width relative to anticipated value length per the fetched guidelines.
- If the project's design system has form field components with their own anatomy conventions, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component's anatomy and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which elements were applied and why.

### For reviews
- Identify which anatomy elements are present in the field.
- Evaluate placement and usage of each against the fetched guidelines.
- Flag violations (e.g. input region spanning full width unnecessarily, error message placement) and suggest corrections.

### For advising
- Answer directly from the fetched guidelines.
- If the element in question has its own dedicated skill (e.g. tooltips, descriptions vs tooltips, required fields, error validation), flag that skill to the user.

---

## Guidelines

- Always cite the source: _"Per the [Form Field Anatomy Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/anatomy-of-form-field)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

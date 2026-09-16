---
name: ux-environmental-errors
description: "Apply environmental error pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing error states caused by server-side or system-level problems — including generic load/save failures, deadlock conditions, and missing or deleted content. Trigger for requests like: 'what should this page say when the server fails?', 'write a toast message for a load error', 'implement a deadlock error state', 'review my server error copy', or any task involving system-originated errors that are not caused by user input. Apply pattern guidelines for error classification, copy, and layout only; defer to the project's existing design system for component and visual decisions."
---

# UX Environmental Errors Skill

This skill ensures environmental error states follow the team's established guidelines
for error classification, copy tone, layout pattern, and escalation paths. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/environmental-errors.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the environmental errors guidelines right now. Could you paste the
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

## Step 3 — Classify the error (required before generating anything)

Use the fetched guidelines to identify which error scenario applies before writing
copy or building a prototype. If the scenario is ambiguous, ask one clarifying
question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Write error copy** | Write main and descriptive text following the fetched guidelines for the classified error type. |
| **Generate an error state prototype** | Build the error state UI using the correct layout pattern per the fetched guidelines for the classified error type. |
| **Review existing error states** | Evaluate copy and layout against the fetched guidelines. Flag misclassifications and violations. |
| **Explain the guidelines** | Summarise the error types and patterns in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For writing copy
- Write main text and descriptive text per the fetched guidelines for the classified error type.
- Do not invent copy structures that aren't in the fetched guidelines.

### For prototype generation
- Implement the correct layout pattern (toast vs empty state region) per the fetched guidelines for the classified error type.
- If the project's design system has toast or empty state components, defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which error type and rules were applied.

### For reviews
- Identify the error type being handled.
- Evaluate copy and layout against the fetched guidelines for that type.
- Flag misclassifications and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples to illustrate the distinction between error types and layout choices.

---

## Guidelines

- Always cite the source: _"Per the [Environmental Errors Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/environmental-errors)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

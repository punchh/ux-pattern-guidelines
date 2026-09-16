---
name: ux-empty-states
description: "Apply empty state pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a state where a list, table, feed, or container has no items to show — including first-use blank states, cleared empty states, no-results states, and coming-soon states. Trigger for requests like: 'what should this screen say when there's no data?', 'write copy for an empty list', 'prototype a blank state', 'review my no results message', or any task involving zero-item UI states. Apply pattern guidelines for copy tone, structure, and state classification only; defer to the project's existing design system for component and visual decisions."
---

# UX Empty States Skill

This skill ensures empty, blank, no-results, and coming-soon states follow the team's
established guidelines for classification, copy, and structure. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/lists-and-tables/empty-states.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the empty state guidelines right now. Could you paste the relevant
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

## Step 3 — Classify the state (required before generating anything)

The fetched guidelines define distinct state types, each with a different copy strategy.
Use the fetched guidelines to identify which type applies before writing copy or building
a prototype.

If the situation is ambiguous, ask the user one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Generate copy** | Write main text and supporting text following the fetched guidelines for the identified state type. |
| **Generate a prototype** | Build the empty state UI with correct copy structure. Use the project's existing design system components for visual elements. |
| **Review existing copy or design** | Evaluate against the fetched guidelines. Flag misclassified states or copy that doesn't match the intended tone. |
| **Explain the guidelines** | Summarise the state types and copy principles in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For copy generation
- Provide main text and supporting text.
- Label which state type guided the copy.
- Note where placeholder content (content type, actor, benefit) should be substituted for the real context.
- Offer 1–2 alternatives if tone could reasonably vary.

### For prototype generation
- Implement the correct copy structure for the state type per the fetched guidelines.
- If the project's design system has an empty state component with its own structure or layout, defer to the design system component — do not override it to match the guidelines.
- If a conflict exists between the design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which state type and rules were applied.
- Use the project's existing design system components for all visual elements.

### For design reviews
- Identify the intended state type.
- Evaluate whether the copy and structure match the fetched guidelines for that type.
- Flag mismatches and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the guideline examples or invent minimal ones to illustrate the distinction between state types.

---

## Guidelines

- Always cite the source: _"Per the [Empty State Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/empty-states)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

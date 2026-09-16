---
name: ux-placeholder-variables
description: "Apply placeholder variable guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a feature that lets users insert dynamic lookup variables into text fields — including the Add Placeholder link button, search menu behavior, and how selected values are displayed. Trigger for requests like: 'add placeholder variable support to this field', 'implement a merge tag feature', 'how should the placeholder menu work?', 'review my placeholder variable UI', or any task involving inserting named variables into a text or paragraph field. Do not use the word 'tag' for this feature per the guidelines. Apply pattern guidelines for placeholder behavior and labeling only; defer to the project's existing design system for component and visual decisions."
---

# UX Placeholder Variables Skill

This skill ensures placeholder variable features follow the team's established guidelines
for invocation, search menu behavior, naming conventions, and post-selection display.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/placeholder-variables.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the placeholder variable guidelines right now. Could you paste the
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
| **Implement placeholder variables** | Apply the fetched link button, search menu, syntax display, and post-selection rules. |
| **Review a placeholder variable feature** | Evaluate against the fetched guidelines. Flag naming violations (e.g. use of "tag") and behavioral issues. |
| **Explain the guidelines** | Summarise the placeholder variable rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct invocation pattern (link button labeled "Add placeholder"), search menu behavior, syntax display in menu, and post-selection plain text rendering per the fetched guidelines.
- Never use the word "tag" to label or describe this feature per the guidelines.
- If the project's design system has a search menu or link button component, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the invocation pattern, menu behavior, and post-selection display.
- Check for prohibited use of "tag" as a label.
- Evaluate each against the fetched guidelines and flag violations.

---

## Guidelines

- Always cite the source: _"Per the [Placeholder Variables Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/placeholder-variables)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

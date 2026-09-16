---
name: ux-line-lengths
description: "Apply line length and text wrapping guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing body text, long-form content, or any readable passage in a UI — including cards, tooltips, onboarding dialogs, information banners, and footnotes. Trigger for requests like: 'how wide should this text block be?', 'when should text wrap?', 'review my content layout for readability', 'is this line too long?', or any task involving the column width or wrapping behavior of readable text. Apply pattern guidelines for line length and wrapping rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Line Lengths and Text Wrapping Skill

This skill ensures text line lengths and wrapping behavior follow the team's established
guidelines for readability across body content and UI components. Guidelines are maintained
externally and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/line-lengths-and-text-wrapping.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the line length guidelines right now. Could you paste the relevant
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

## Step 3 — Identify the container context (required before generating anything)

The fetched guidelines distinguish between standard body content and exceptions for
specific container types. Identify which applies before making any line length
recommendations or implementations. If the context is ambiguous, ask one clarifying
question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Determine line length for a context** | Apply the fetched guidelines for the identified container type. |
| **Implement text layout** | Apply the correct wrapping behavior per the fetched guidelines for the container context. |
| **Review existing text layout** | Evaluate line lengths against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the wrapping rules and exceptions in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For line length decisions
- Identify the container context and apply the correct guideline per the fetched rules.
- Note any applicable exceptions for the identified container type.

### For implementation
- Apply the correct wrapping behavior for the container context per the fetched guidelines.
- If the project's design system defines content column widths or text container constraints, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system constraint and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the container type and current line length behavior.
- Evaluate against the fetched guidelines for that context.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate standard wrapping versus exceptions.

---

## Guidelines

- Always cite the source: _"Per the [Line Lengths and Text Wrapping Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/line-lengths-and-text-wrapping)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

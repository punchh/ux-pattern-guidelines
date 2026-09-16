---
name: ux-hyperlinks-vs-link-buttons
description: "Apply hyperlink versus link button pattern guidelines when building or reviewing UI. Use this skill whenever anyone is deciding whether to use a hyperlink or a link button, implementing navigation or action controls styled as text, or reviewing whether inline text controls are using the right pattern. Trigger for requests like: 'should this be a link or a button?', 'implement a text link for this action', 'review my navigation links', 'where should the icon go on this link?', or any task involving text-based interactive controls that navigate or trigger actions. Apply pattern guidelines for usage and icon placement only; defer to the project's existing design system for component and visual decisions."
---

# UX Hyperlinks vs Link Buttons Skill

This skill ensures hyperlinks and link buttons are used correctly and consistently
per the team's established guidelines for usage intent and icon placement. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/layout-and-navigation/hyperlinks-versus-link-buttons.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the hyperlink vs link button guidelines right now. Could you paste
> the relevant section here so I can apply them?"_
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
| **Decide which to use** | Evaluate the use case against the fetched guidelines to determine whether a hyperlink or link button is appropriate. |
| **Implement a hyperlink or link button** | Apply the fetched usage and icon placement rules. |
| **Review existing controls** | Evaluate against the fetched guidelines. Flag misuse and suggest corrections. |
| **Explain the guidelines** | Summarise the distinction and rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly which pattern is appropriate and why, per the fetched guidelines.
- If the use case is ambiguous, explain the distinction and ask one clarifying question.

### For implementation
- Apply the correct usage pattern and icon placement per the fetched guidelines.
- If the project's design system has hyperlink or link button components with their own icon placement or styling conventions, defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify which controls are present and what pattern they're using.
- Evaluate each against the fetched guidelines.
- Flag misuse and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the distinction.

---

## Guidelines

- Always cite the source: _"Per the [Hyperlinks vs Link Buttons Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/layout-and-navigation/hyperlinks-versus-link-buttons)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

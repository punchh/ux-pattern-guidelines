---
name: ux-tabs
description: "Apply tab pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a tab navigation component, deciding whether to use tabs, or asking about tab layout, usage rules, or nesting behavior. Trigger for requests like: 'should I use tabs here?', 'add tabs to this page', 'review my tab layout', 'how many tabs is too many?', 'can I nest tabs?', or any task involving tab-based navigation or content organization. Apply pattern guidelines for usage, layout, and interaction only; defer to the project's existing design system for component and visual decisions."
---

# UX Tabs Skill

This skill ensures tab patterns follow the team's established guidelines for usage,
layout, interaction, and nesting rules. Guidelines are maintained externally and
**must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/layout-and-navigation/tabs.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the tab guidelines right now. Could you paste the relevant section
> here so I can apply them?"_
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
| **Decide whether to use tabs** | Evaluate the use case against the fetched "use tabs when" and "don't use tabs when" criteria. |
| **Generate a tab prototype** | Build the tab layout following the fetched guidelines for alignment, viewport behavior, nesting, and content placement. |
| **Review an existing tab layout** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the relevant principles in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether tabs are appropriate for the use case and why, per the fetched guidelines.
- If tabs are not appropriate, suggest the correct alternative per the fetched guidelines.

### For prototype generation
- Implement tab layout and interaction per the fetched guidelines.
- If the project's design system has a tab component with its own layout or interaction behavior, defer to that component — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For reviews
- Identify which tab pattern decisions are present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate usage and nesting decisions.

---

## Guidelines

- Always cite the source: _"Per the [Tabs Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/layout-and-navigation/tabs)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

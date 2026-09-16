---
name: ux-time-zone-fields
description: "Apply time zone field guidelines when building or reviewing forms and reporting UI. Use this skill whenever anyone is implementing or reviewing a time zone selector — including organization, search behavior, display format, sort order, and default values. Trigger for requests like: 'add a time zone selector', 'how should time zones be organized?', 'what should show in the populated time zone field?', 'review my time zone picker', or any task involving selecting or displaying a time zone. Apply pattern guidelines for time zone field behavior and organization only; defer to the project's existing design system for component and visual decisions."
---

# UX Time Zone Fields Skill

This skill ensures time zone fields follow the team's established guidelines for
organization, search behavior, sort order, naming conventions, and populated display.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/time-zone-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the time zone field guidelines right now. Could you paste the relevant
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

## Step 3 — Classify the context (required before generating anything)

Determine whether this is a scheduling context (typically unpopulated by default) or
a reporting context (typically pre-populated), as the default state differs.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Implement a time zone field** | Apply the fetched organization, search, sort, naming, and populated display rules. |
| **Review a time zone field** | Evaluate organization, search behavior, naming, and display against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the time zone field rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct continental organization, time zone list format (name, abbreviation, UTC offset), official-names-only rule, sort order, search match support (name, abbreviation, offset), and populated display rules per the fetched guidelines.
- Never organize by city or country unless it's in the official time zone name, per the guidelines.
- If the project's design system has a dropdown or combo box component, defer to that for structural scaffolding — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Evaluate organization, naming, sort order, and populated display against the fetched guidelines.
- Flag city/country-based organization and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Time Zone Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/time-zone-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-breadcrumbs
description: "Apply breadcrumb pattern guidelines when building or reviewing UI navigation. Use this skill whenever anyone is implementing or reviewing breadcrumbs — including deciding whether a page warrants breadcrumbs, anatomy, parent/current node styling, dividers, placement, and truncation. Trigger for requests like 'add breadcrumbs to this page', 'should this page have breadcrumbs?', 'review my breadcrumb design', 'how do breadcrumbs work on the Edit version of this page?', or any task involving secondary hierarchical navigation. Also trigger when a design is presented for review or prototyping and any of the following are present — even without the user mentioning breadcrumbs: a detail page under a content-type landing page, a page deep in a multi-level hierarchy, or a hierarchy where users may need to navigate back to a parent. Apply pattern guidelines for usage, anatomy, and placement only; defer to the project's design system for component and visual decisions."
---

# UX Breadcrumbs Skill

This skill ensures breadcrumb navigation follows the team's established guidelines for
when to use breadcrumbs, anatomy, hierarchy-vs-history construction, placement, and
truncation. Guidelines are maintained externally and **must be fetched at runtime** so
you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/layout-and-navigation/breadcrumbs.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the breadcrumb guidelines right now. Could you paste the relevant
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

## Step 2.5 — Proactively check for breadcrumb opportunities (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned breadcrumbs,
check whether the design contains any context where the fetched guidelines would
recommend breadcrumbs. If so, surface the opportunity or flag the violation before
proceeding.

- If a page that would qualify for breadcrumbs per the fetched guidelines is missing them, flag the opportunity to the user.
- If a page that should not have breadcrumbs per the fetched guidelines is showing them (e.g. a create form, a wizard, a top-level dashboard), flag the violation.
- If the user explicitly wants to keep their current pattern despite the recommendation, note the concern, respect their decision, and proceed.
- If no breadcrumb opportunity or violation is present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether a page should have breadcrumbs** | Evaluate the page's depth and type against the fetched usage criteria. |
| **Implement a breadcrumb** | Apply the fetched anatomy, divider, placement, and styling rules. |
| **Review an existing breadcrumb** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on edge cases** | Apply the fetched rules for Edit-mode pages, create flows, and truncation scenarios. |
| **Explain the guidelines** | Summarise the breadcrumb rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether the page should have breadcrumbs and why, per the fetched depth and page-type criteria.
- For Edit-mode pages on a record, apply the fetched rule that the breadcrumb stays the same as the read-only version of that record — do not add a new node for "Edit."
- For create-new pages, do not add breadcrumbs per the fetched guidelines.

### For implementation
- Apply the correct parent node styling, divider choice, current page node styling, placement (above the page title), and truncation behavior per the fetched guidelines.
- Apply the fetched rule that breadcrumbs must be hierarchy-based, not history-based.
- If the project's design system has a breadcrumb component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the breadcrumb's anatomy, placement, and depth.
- Evaluate each against the fetched guidelines.
- Flag violations such as history-based construction, clickable current page node, wrapping to multiple lines, placement outside the standard location, or extra nodes for Edit mode.

---

## Guidelines

- Always cite the source: _"Per the [Breadcrumbs Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/layout-and-navigation/breadcrumbs)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

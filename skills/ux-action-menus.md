---
name: ux-action-menus
description: "Apply action menu pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an action menu (overflow, kebab, ellipsis, or 'More actions' menu), including deciding which actions belong in a menu versus as regular buttons, how the menu is accessed, and how menu items are labeled. Trigger for requests like 'should these buttons go in a menu?', 'add a kebab menu to each row', 'review my action menu labels', or any task involving grouping repeated or secondary actions. Also trigger unprompted when a design is presented for review or prototyping and it shows the same buttons repeated on every row of a table or list, several seldom-used utility buttons competing with primary actions, or an existing action menu whose items may break labeling conventions. Apply pattern guidelines for usage, access, and labeling only; defer to the project's design system for visual decisions."
---

# UX Action Menus Skill

This skill ensures action menus follow the team's established guidelines for when to
house actions in a menu, how the menu is accessed, and how menu items are labeled.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/layout-and-navigation/action-menus.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the action menu guidelines right now. Could you paste the relevant
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

## Step 2.5 — Proactively check for action menu opportunities and violations (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned action menus, check whether the design contains any context where the fetched guidelines apply. If so, surface it before proceeding.

- If the design repeats the same action buttons on every row of a table or list, flag this per the fetched guidelines and recommend moving those actions into an action menu.
- If the design shows several seldom-used utility actions as persistent buttons competing with more commonly used actions, raise it as a candidate for an action menu. The fetched guidelines acknowledge this case is subjective and varies by business context, so frame it as a suggestion, not a violation.
- If the design already includes an action menu, check its items against the fetched labeling rules and flag any that break them.
- If the user explicitly wants to keep their current pattern despite the recommendation, note the concern, respect their decision, and proceed.
- If no opportunity or violation is present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether actions belong in a menu** | Evaluate the actions against the fetched usage criteria (repeated across rows, or distant secondary and tertiary actions). |
| **Implement an action menu** | Apply the fetched access and labeling rules. |
| **Label menu items** | Apply the fetched labeling rules to each item and provide corrected labels where needed. |
| **Review an existing action menu** | Evaluate usage, access, and labeling against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarize the action menu rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether each action belongs in a menu or as a regular button, per the fetched usage criteria.
- For the secondary and tertiary actions case, acknowledge the subjectivity the fetched guidelines describe. If you don't know how often an action gets used, ask rather than assume.

### For implementation
- Apply the fetched rules for how the menu is accessed and how its items are labeled.
- If the project's design system has an overflow button, menu, or icon component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For labeling and reviews
- List each menu item, whether it passes the fetched labeling rules, and a corrected label for any that don't.
- Flag usage problems separately from labeling problems so the user can address them independently.

---

## Guidelines

- Always cite the source: _"Per the [Action Menu Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/layout-and-navigation/action-menus)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labeled as such.

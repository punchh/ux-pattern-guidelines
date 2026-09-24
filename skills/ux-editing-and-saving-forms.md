---
name: ux-editing-and-saving-forms
description: "Apply the editing and saving forms pattern guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a single-page edit form — including how the user arrived, when the Save Bar appears, what happens on successful save, on save failure, and on cancel. Trigger for requests like 'add an edit form for this record', 'when should the save bar show?', 'what happens after the user saves?', 'review my edit page', or any task involving a single-page form the user modifies and saves. Also trigger when a design is presented for review or prototyping and any of the following are present — even without the user mentioning editing: a single-page form the user modifies, a sticky footer with save/cancel actions, an edit page entered from a read-only view or list page, or a settings-style form entered from primary nav. Apply pattern guidelines for entry paths, Save Bar visibility, and save/cancel behavior only; defer to the project's design system for visual decisions."
---

# UX Editing and Saving Forms Skill

This skill ensures single-page edit forms follow the team's established guidelines for
entry paths, Save Bar visibility, successful save behavior, save failure behavior, Save
Bar anatomy, and cancel behavior. Guidelines are maintained externally and **must be
fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/editing-and-saving-forms.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the editing and saving forms guidelines right now. Could you paste the
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

## Step 2.5 — Proactively check for editing-and-saving pattern violations (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned editing or saving, check whether the design contains any context where the fetched guidelines would apply. If so, flag violations or missing elements before proceeding.

- If the design shows an edit form with no Save Bar at all (or with save/cancel buttons at the end of a scrolling form rather than in a sticky footer), flag this as a violation per the fetched guidelines.
- If the design shows an edit form entered directly from primary navigation (path 3) with the Save Bar always visible from arrival, flag this against the fetched hidden-until-dirty rule.
- If the design shows an edit form entered from a read-only view or list page (paths 1 and 2) with the Save Bar hidden on arrival, flag this against the fetched visible-from-arrival rule.
- If the design specifies that a successful save on path 1 or 2 keeps the user on the page (rather than auto-navigating to the origin), flag this against the fetched auto-navigate rule.
- If the design specifies that a successful save on path 3 auto-navigates the user away, flag this against the fetched stay-on-page rule.
- If the design shows the user being navigated away on save failure, flag this against the fetched "do not navigate away on failure" rule.
- If the user explicitly wants to keep their current pattern despite the recommendation, note the concern, respect their decision, and proceed.
- If no violations or omissions are present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Design or prototype an edit form** | Apply the fetched rules for entry-path-appropriate Save Bar visibility, successful save behavior, save failure behavior, and Save Bar anatomy. |
| **Advise on entry-path routing** | Help the user determine which of the three entry paths applies to their case, and apply the appropriate rules from the fetched guideline. |
| **Review an existing edit form** | Evaluate entry path, Save Bar visibility, save behavior, and failure behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on Save Bar behavior on mobile** | Apply the fetched rules for how the Save Bar should behave when the virtual keyboard is present. |
| **Explain the guidelines** | Summarise the editing and saving pattern in plain language. |

---

## Step 4 — Respond using the guidelines

### For design and prototyping
- First, identify which of the three entry paths applies to this edit form (from a read-only view, from a parent list, or directly from primary navigation).
- Apply the fetched Save Bar visibility rules for that entry path.
- Apply the fetched successful save behavior (auto-navigate to origin vs. stay on page) for that entry path.
- Apply the fetched save failure behavior — do not navigate away, follow error validation, keep Save Bar persistent.
- Apply the fetched Save Bar anatomy (Save primary right-aligned, Cancel positioned per button alignment rules, secondary/destructive actions per combining buttons rules).
- If the project's design system has a Save Bar, sticky footer, or button group component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For entry-path routing
- Ask the user (or determine from context) which entry path applies. If ambiguous, list the three paths from the fetched guidelines and ask.
- Apply the appropriate rules for that path.

### For reviews
- Identify the entry path, current Save Bar visibility, save behavior, and failure behavior.
- Evaluate each against the fetched guidelines.
- Flag violations — particularly missing Save Bar, incorrect visibility for the entry path, non-navigating success on paths 1/2, navigating success on path 3, or navigation-away on failure.

### For advising
- Answer directly from the fetched guidelines.
- If the question touches a related pattern (multi-step forms, button alignment, canceling, error validation, success notifications, destructive actions, combining buttons), the cross-reference step will surface those guidelines automatically.

---

## Guidelines

- Always cite the source: _"Per the [Editing and Saving Forms Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/editing-and-saving-forms)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

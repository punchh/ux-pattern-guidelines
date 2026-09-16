---
name: ux-listbox-fields
description: "Apply listbox field guidelines when building or reviewing forms. Use this skill whenever anyone is considering implementing a listbox (shuttle) field. Trigger for requests like: 'implement a listbox', 'add a shuttle component', 'build a dual-list selector', or any task involving moving items between two visible lists. The guideline position is clear: don't use a listbox. Apply pattern guidelines by redirecting to the correct alternative."
---

# UX Listbox Fields Skill

This skill applies the team's established guideline on listbox fields, which takes a
clear position against using them. Guidelines are maintained externally and **must be
fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/listbox-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the listbox guidelines right now. Could you paste the relevant
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

## Step 3 — Apply the guideline

The fetched guidelines take a clear position: **do not use a listbox**. When a listbox
is requested, apply the guideline as follows:

- Explain why the guideline recommends against listboxes, per the fetched reasoning.
- Redirect to the multi-select combo box as the correct alternative.
- Offer to implement the multi-select combo box instead, referencing the `ux-combo-box` skill or the combo box guidelines.
- If the user explicitly wants a listbox despite the recommendation, note the concern clearly, respect their decision, and proceed — but do not omit the pushback.

---

## Guidelines

- Always cite the source: _"Per the [Listbox Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/listbox-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.

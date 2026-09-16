---
name: ux-disabled-buttons
description: "Apply disabled button guidelines when building or reviewing UI. Use this skill whenever anyone is considering disabling a button, implementing a form submit button, or reviewing whether button states are correct. Trigger for requests like: 'should I disable the submit button until the form is valid?', 'disable this button when no items are selected', 'review my button states', or any task involving button enabled/disabled logic. Apply pattern guidelines for button state rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Disabled Buttons Skill

This skill ensures disabled button patterns follow the team's established guidelines —
which take a strong stance against disabling buttons in most cases. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from the
latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/disabled-buttons.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the disabled buttons guidelines right now. Could you paste the
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
| **Decide whether to disable a button** | Evaluate the use case against the fetched guidelines. In most cases the answer will be: don't. |
| **Implement the correct alternative** | Apply the fetched guidance on what to do instead of disabling. |
| **Review existing button states** | Evaluate against the fetched guidelines. Flag inappropriate disabled states and suggest corrections. |
| **Explain the guidelines** | Summarise the rules and rationale in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- Apply the fetched guidelines directly. If the use case calls for disabling a button, push back per the guidelines and explain the correct alternative.
- Note the one permitted exception per the fetched guidelines and apply it only when that specific case matches.

### For implementation
- Implement the correct alternative to disabling per the fetched guidelines.
- If the use case matches the one permitted exception in the fetched guidelines, use the design system's disabled button state for that case only. For all other cases, use the enabled state — do not use the disabled state even if the design system offers it.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify any disabled button states present in the design.
- Evaluate each against the fetched guidelines.
- Flag inappropriate disabled states and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Disabled Buttons Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/disabled-buttons)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

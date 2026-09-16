---
name: ux-steppers
description: "Apply stepper pattern guidelines when building or reviewing multi-step form UI. Use this skill whenever anyone is implementing or reviewing a stepper component — including anatomy, progress status states, error handling, and page placement. Trigger for requests like: 'add a stepper to this form', 'what should the stepper show on an error step?', 'review my stepper layout', 'how wide should the stepper be?', or any task involving a progress indicator for a multi-step form. Apply pattern guidelines for stepper anatomy, states, and placement only; defer to the project's existing design system for component and visual decisions."
---

# UX Steppers Skill

This skill ensures stepper components follow the team's established guidelines for
anatomy, progress status states, error handling, and page orientation. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from the
latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/steppers.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the stepper guidelines right now. Could you paste the relevant
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

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement a stepper** | Apply the fetched anatomy, status states, error handling, and placement rules. |
| **Review an existing stepper** | Evaluate anatomy, states, and placement against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the stepper rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct stepper anatomy elements, progress status states, error state treatment, and page placement rules per the fetched guidelines.
- If the project's design system has a stepper or progress indicator component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component's anatomy or states and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the stepper anatomy and status states present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Steppers Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/steppers)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

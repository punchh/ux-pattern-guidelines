---
name: ux-canceling
description: "Apply cancel pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a cancel action in a create or edit experience — including when to offer cancel, when to show a confirmation dialog, and how to write the confirmation copy. Trigger for requests like: 'add a cancel button to this form', 'should this cancel show a confirmation?', 'write cancel dialog copy', 'review my cancel behavior', or any task involving a user exiting a form with unsaved changes. Apply pattern guidelines for usage, confirmation logic, and copy only; defer to the project's existing design system for component and visual decisions."
---

# UX Canceling Skill

This skill ensures cancel patterns follow the team's established guidelines for
when to offer cancel, when to show a confirmation prompt, dialog anatomy, and
copy defaults. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/canceling.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the canceling guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the context (required before generating anything)

Use the fetched guidelines to determine whether cancel should be offered at all,
and whether a confirmation dialog is required, based on the form type and state.
If the context is ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to offer cancel** | Evaluate the form type and context against the fetched usage rules. |
| **Decide whether to show a confirmation** | Evaluate the form state against the fetched confirmation trigger rules. |
| **Implement cancel behavior** | Apply the fetched dialog anatomy and copy defaults. |
| **Write cancel dialog copy** | Write copy per the fetched anatomy and copy guidelines. |
| **Review existing cancel behavior** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the cancel rules in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For usage and confirmation decisions
- State clearly whether cancel should be offered and whether a confirmation is required, per the fetched guidelines.

### For implementation and copy
- Apply the correct dialog anatomy and copy structure per the fetched guidelines.
- If the project's design system has a modal or dialog component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the cancel behavior and confirmation logic present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Canceling Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/canceling)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

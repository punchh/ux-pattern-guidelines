---
name: ux-autosaving
description: "Apply autosaving pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an autosave experience — including deciding whether autosave is appropriate, which controls support it, and how to communicate save feedback. Trigger for requests like: 'implement autosave for this form', 'should this toggle switch autosave?', 'can I mix autosave and manual save?', 'review my autosave pattern', or any task involving passively saving form state without an explicit user save action. Apply pattern guidelines for autosave usage and control rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Autosaving Skill

This skill ensures autosave patterns follow the team's established guidelines for
when autosave is appropriate, which control types support it, mixing rules, and
feedback requirements. Guidelines are maintained externally and **must be fetched
at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/autosaving.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the autosaving guidelines right now. Could you paste the relevant
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
| **Decide whether to use autosave** | Evaluate the form's control types and context against the fetched guidelines. |
| **Implement autosave** | Apply the fetched rules for control types, mixing restrictions, and feedback requirements. |
| **Review an existing autosave pattern** | Evaluate control types, mixing, and feedback against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the autosave rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- Evaluate the form's control types against the fetched guidelines to determine whether autosave is appropriate.
- If it's not appropriate, explain why per the fetched rules and suggest the correct alternative.

### For implementation
- Apply the correct control type requirements, mixing restrictions, and save feedback rules per the fetched guidelines.
- If the project's design system has toggle switch or save feedback components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the control types in use and whether autosave feedback is present.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the control type and mixing rules.

---

## Guidelines

- Always cite the source: _"Per the [Autosaving Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/autosaving)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

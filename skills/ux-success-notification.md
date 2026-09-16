---
name: ux-success-notification
description: "Apply success notification guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a success toast notification — including fade timing, persistence duration, stacking behavior, and accessibility. Trigger for requests like: 'add a success toast to this action', 'how long should the toast show?', 'implement stacked notifications', 'review my success message behavior', or any task involving post-action success feedback to the user. Apply pattern guidelines for toast behavior, timing, and animation only; defer to the project's existing design system for component and visual decisions."
---

# UX Success Notification Skill

This skill ensures success toast notifications follow the team's established guidelines
for fade timing, persistence duration, stacking behavior, positioning, and accessibility.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/success-notification.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the success notification guidelines right now. Could you paste the
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
| **Implement a success toast** | Apply the fetched fade, persistence, stacking, positioning, and accessibility rules. |
| **Review an existing success toast** | Evaluate timing, stacking, and accessibility against the fetched guidelines. Flag violations and suggest corrections. |
| **Write success toast copy** | Apply the fetched copy guidelines, or refer to the `ux-grammar-voice-tone` skill for tone guidance. |
| **Explain the guidelines** | Summarise the success notification rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct fade in/out timing, persistence duration, stacking animation behavior, positioning, and ARIA accessibility markup per the fetched guidelines.
- If the project's design system has a toast or notification component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component's animation or positioning and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the toast timing, stacking, positioning, and accessibility implementation.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For copy
- Apply the fetched copy guidelines, and cross-reference the grammar, voice, and tone guidelines if linked from the fetched page.

---

## Guidelines

- Always cite the source: _"Per the [Success Notification Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/success-notification)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-tooltips
description: "Apply tooltip pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a tooltip — including trigger behavior, content rules, positioning, and visual treatment. Trigger for requests like: 'add a tooltip to this field', 'review my tooltip content', 'how should this tooltip be triggered?', 'is this tooltip positioned correctly?', or any task involving tooltip components in a form or informational context. Apply pattern guidelines for usage, content, and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Tooltips Skill

This skill ensures tooltips follow the team's established guidelines for trigger
behavior, content purpose, positioning, and visual treatment. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/tooltips.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the tooltip guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement a tooltip** | Apply the fetched trigger, content, positioning, and visual rules. |
| **Write tooltip content** | Write content that follows the fetched guidelines for what tooltips are and aren't for. If content belongs in a description instead, say so. |
| **Review an existing tooltip** | Evaluate trigger behavior, content, positioning, and visual treatment against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the tooltip rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct trigger behavior, content purpose, positioning, line-breaking, and opacity rules per the fetched guidelines.
- If the project's design system has a tooltip component, defer to that component — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines (e.g. background transparency), flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For writing content
- Evaluate whether the intended content fits the tooltip's purpose per the fetched guidelines.
- If it belongs in a description instead, redirect to the `ux-descriptions-vs-tooltips` skill or the descriptions vs tooltips guidelines.
- Write content that follows the fetched rules for what tooltips are for.

### For reviews
- Identify the trigger behavior, content, positioning, and visual treatment of the tooltip.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate correct tooltip usage.

---

## Guidelines

- Always cite the source: _"Per the [Tooltips Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/tooltips)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

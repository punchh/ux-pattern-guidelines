---
name: ux-loading-dialogs
description: "Apply loading dialog pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing an interstitial loading state for a high-latency action — including deciding whether a loading dialog is warranted, implementing timing rules, or reviewing an existing loading dialog. Trigger for requests like: 'add a loading state to this action', 'how long should the loading dialog show?', 'implement a spinner for this API call', 'should this action have a loading dialog?', or any task involving feedback for actions that take time to process. Apply pattern guidelines for usage, timing, and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Loading Dialogs Skill

This skill ensures loading dialogs follow the team's established guidelines for
when to use them, timing thresholds, persistence rules, and background dimming.
Guidelines are maintained externally and **must be fetched at runtime** so you
always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/loading-dialogs.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the loading dialog guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
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
| **Decide whether to use a loading dialog** | Evaluate the action's expected latency against the fetched usage criteria. |
| **Implement a loading dialog** | Apply the fetched timing, persistence, dismissal, and background rules. |
| **Review an existing loading dialog** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the usage and timing rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether a loading dialog is appropriate based on the expected latency of the action, per the fetched guidelines.
- If it's not appropriate, suggest the correct alternative feedback pattern.

### For implementation
- Apply the correct timing thresholds, minimum persistence duration, dismissal behavior, and background dimming per the fetched guidelines.
- If the project's design system has a loading dialog, spinner, or modal component, defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the loading dialog behavior present in the design.
- Evaluate timing, persistence, and dismissal behavior against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate timing and usage decisions.

---

## Guidelines

- Always cite the source: _"Per the [Loading Dialogs Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/loading-dialogs)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

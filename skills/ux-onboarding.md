---
name: ux-onboarding
description: "Apply onboarding pattern guidelines when building or reviewing UI. Use this skill whenever anyone is deciding whether to use onboarding, implementing an onboarding element, or reviewing an existing onboarding experience — including modal-style and tooltip-style onboarding. Trigger for requests like: 'should we add onboarding here?', 'prototype an onboarding modal', 'implement a first-use tooltip', 'review this onboarding flow', 'is this a good use case for onboarding?', or any task involving one-time instructional UI elements. Apply pattern guidelines for usage, type selection, and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Onboarding Skill

This skill ensures onboarding elements follow the team's established guidelines for
when to use onboarding, which type to use, and how to implement it correctly. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/onboarding.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the onboarding guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Use the fetched "when to use onboarding" criteria to evaluate whether onboarding
is warranted at all before proceeding. If onboarding is appropriate, identify
which type (modal-style or tooltip-style) fits the use case.

If the situation is ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use onboarding** | Evaluate the use case against the fetched usage criteria. Push back if the criteria aren't met. |
| **Implement an onboarding element** | Build the onboarding experience using the correct type and behavior per the fetched guidelines. |
| **Review an existing onboarding element** | Evaluate type choice, dismissal behavior, and re-fire logic against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the usage rules and types in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For usage decisions
- Evaluate honestly against the fetched criteria. If the use case doesn't meet the threshold, say so clearly and suggest alternatives (e.g. usability testing and iteration first).
- If onboarding is appropriate, recommend the correct type per the fetched guidelines.

### For implementation
- Implement the correct onboarding type, dismissal behavior, and one-time-only firing logic per the fetched guidelines.
- If the project's design system has modal or tooltip components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which type and rules were applied.

### For reviews
- Identify the onboarding type and evaluate whether it matches the use case per the fetched guidelines.
- Check dismissal behavior and re-fire logic against the fetched rules.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Emphasize the high bar for using onboarding at all, per the fetched guidelines.

---

## Guidelines

- Always cite the source: _"Per the [Onboarding Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/onboarding)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

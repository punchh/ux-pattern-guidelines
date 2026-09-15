---
name: ux-toggle-switches
description: "Apply toggle switch guidelines when building or reviewing forms. Use this skill whenever anyone is choosing between a toggle switch, checkbox, or other field type for a binary on/off state — or implementing a toggle switch. Trigger for requests like: 'should this be a toggle or a checkbox?', 'implement a toggle switch', 'what labels should the toggle states use?', 'review my toggle switch usage', or any task involving a binary two-state control. Apply pattern guidelines for toggle switch usage and labeling only; defer to the project's existing design system for component and visual decisions."
---

# UX Toggle Switches Skill

This skill ensures toggle switches are used in the right context and follow the team's
established guidelines for usage, state labeling, and instant-apply behavior. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/toggle-switches.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the toggle switch guidelines right now. Could you paste the relevant
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

Evaluate the state labels, selection type, and whether a Save/Apply button is present
against the fetched guidelines. If the toggle's intended state labels are anything other
than "On" and "Off," that is a signal per the guidelines that a toggle switch is likely
the wrong component — flag this before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Choose between toggle and checkbox** | Evaluate the use case against the fetched decision criteria — particularly the presence or absence of a Save/Apply button. |
| **Implement a toggle switch** | Apply the fetched state labeling and instant-apply rules. |
| **Review a toggle switch** | Evaluate usage appropriateness and labeling against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the toggle switch rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- Apply the correct "On"/"Off" state labels and instant-apply (autosave) behavior per the fetched guidelines.
- If the context includes a Save/Apply button, flag that a toggle switch is not appropriate — use a checkbox instead.
- If the project's design system has a toggle switch component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Evaluate whether the toggle switch is the correct field type.
- Evaluate state labeling and instant-apply behavior against the fetched guidelines.
- Flag violations — particularly non-On/Off labels and use alongside Save/Apply buttons.

---

## Guidelines

- Always cite the source: _"Per the [Toggle Switch Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/toggle-switches)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

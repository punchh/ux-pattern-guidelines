---
name: ux-multi-step-forms
description: "Apply multi-step form pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a multi-step or multi-page form — including field count per step, navigation bar behavior, stepper usage, draft saving, and review step inclusion. Trigger for requests like: 'build a multi-step form', 'how many fields per step?', 'add a back and next button', 'review my wizard flow', or any task involving a form spread across multiple pages or steps. Also trigger when a single-page form is presented for review or prototyping and the field count is high enough that a multi-step approach may be warranted — even if the user has not mentioned multi-step forms at all. Apply pattern guidelines for structure, navigation, and behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Multi-Step Forms Skill

This skill ensures multi-step forms follow the team's established guidelines for
field count, navigation bar anatomy, stepper usage, draft saving, and review step
inclusion. It also catches single-page forms that should be broken into multiple
steps. Guidelines are maintained externally and **must be fetched at runtime**
so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/multi-step-forms.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the multi-step forms guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 2.5 — Pre-assess field count (required when a form is presented)

Before identifying the task, count the fields in the form being reviewed or built.
Evaluate whether the total field count warrants a multi-step approach per the fetched
guidelines.

- If the form exceeds the fetched field count threshold for a single page, **stop and
  recommend restructuring as a multi-step form before proceeding**. Explain why per
  the fetched guidelines, and offer to help design the step structure.
- If the user explicitly wants to keep it as a single page despite the recommendation,
  note the concern, respect their decision, and proceed.
- If the field count is within the acceptable range for a single page, continue to
  Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Design or prototype a multi-step form** | Apply the fetched guidelines for field count, navigation bar, stepper, draft saving, and review step. |
| **Review an existing multi-step form** | Evaluate structure and behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on multi-step form decisions** | Answer questions about step structure, navigation behavior, and supporting patterns from the fetched guidelines. |
| **Explain the guidelines** | Summarise the multi-step form rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For design and prototyping
- Apply the correct field count guidance, navigation bar anatomy, stepper, draft saving triggers, and review step inclusion per the fetched guidelines.
- If the project's design system has navigation bar, stepper, or button components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For reviews
- Identify the step structure, navigation bar anatomy, and supporting patterns present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Multi-Step Forms Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/multi-step-forms)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

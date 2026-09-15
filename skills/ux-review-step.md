---
name: ux-review-step
description: "Apply review step pattern guidelines when building or reviewing multi-step forms. Use this skill whenever anyone is building, prototyping, or reviewing a multi-step form — even if they haven't mentioned a review step at all. The review step is a standard part of most multi-step forms and should be proactively checked for. Also trigger for explicit requests like: 'add a review step to this form', 'implement a summary page', 'how should the revisit flow work?', 'review my review step design', or any task involving a confirmation or summary step at the end of a multi-step form. Apply pattern guidelines for structure, display, and navigation behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Review Step Skill

This skill ensures review steps in multi-step forms follow the team's established
guidelines for organization, read-only display, revisit navigation, and conditional
field handling. It also proactively checks whether a review step is present whenever
a multi-step form is being built or reviewed. Guidelines are maintained externally
and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/reviewing-review-step.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the review step guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 2.5 — Proactively check for a review step (required when a multi-step form is present)

When a multi-step form is being built or reviewed and no review step has been
mentioned or accounted for, check whether one should be included per the fetched
guidelines.

- If the fetched guidelines indicate a review step is expected and none is present,
  flag it to the user and recommend adding one before proceeding.
- If the user explicitly wants to omit it, note the concern, respect their decision,
  and proceed.
- If a review step is already present or accounted for, continue to Step 3 without
  comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Implement a review step** | Apply the fetched guidelines for organization, read-only display, long value handling, and revisit navigation. |
| **Implement revisit behavior** | Apply the fetched rules for the revisit navigation bar and conditional field handling. |
| **Review an existing review step** | Evaluate structure, display, and revisit behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the review step rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct organization structure, read-only display format, long value handling, and revisit navigation bar behavior per the fetched guidelines.
- Include conditional field prompt behavior per the fetched guidelines when relevant.
- If the project's design system has read-only display or navigation components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which key rules were applied.

### For reviews
- Identify the review step structure, display treatment, and revisit behavior in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Review Step Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/reviewing-review-step)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

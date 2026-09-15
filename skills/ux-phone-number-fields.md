---
name: ux-phone-number-fields
description: "Apply phone number field guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a phone number input — including single-country input masking, multi-country composite field behavior, country code dropdown, flag display, and hint text. Trigger for requests like: 'add a phone number field', 'implement a country code selector', 'should this phone field support international numbers?', 'review my phone number input', or any task involving phone number entry. Apply pattern guidelines for phone field behavior and formatting only; defer to the project's existing design system for component and visual decisions."
---

# UX Phone Number Fields Skill

This skill ensures phone number fields follow the team's established guidelines for
single-country input masking and multi-country composite field behavior. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from the
latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/entering-information/phone-number-fields.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the phone number field guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the use case (required before generating anything)

Determine whether this is a single-country or multi-country/international phone field,
as the implementation rules differ significantly.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Implement a phone number field** | Apply the fetched rules for the identified variant (single-country or multi-country). |
| **Review a phone number field** | Evaluate behavior and anatomy against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the phone field rules in plain language. |

---

## Step 5 — Respond using the guidelines

### For implementation
- For single-country: apply the correct input mask, hint text format, and numeric-only acceptance rule per the fetched guidelines.
- For multi-country: apply the correct composite field anatomy (flag, code, chevron), dropdown search behavior, country sorting, default value, and per-country input mask rules per the fetched guidelines.
- If the project's design system has a phone input component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which variant and rules were applied.

### For reviews
- Identify the phone field variant and evaluate all behavior aspects against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Phone Number Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/phone-number-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

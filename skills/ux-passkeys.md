---
name: ux-passkeys
description: "Apply passkey and third-party sign-in pattern guidelines when building or reviewing sign-in forms. Use this skill whenever anyone is adding, designing, or reviewing passkey or third-party sign-in options (often called social sign-in, or 'Sign in with Google' buttons), including which methods the form leads with, element order, button labels, icons, and styles, separators between methods, passkey explanatory text, terminology, and the account creation link. Trigger for requests like 'add passkey sign-in to this form', 'where do the Google and Apple buttons go?', 'should passkeys go first?', or 'review the sign-in options on my page'. Also trigger unprompted when a design is presented for review or prototyping and its sign-in form includes a passkey option or third-party sign-in buttons. The browser or OS passkey sheet and each third party's own sign-in flow are out of scope. Apply pattern guidelines for hierarchy, layout, and copy only; defer to the project's design system for visual decisions."
---

# UX Passkeys and Third-Party Sign-in Skill

This skill ensures passkey and third-party sign-in options on sign-in forms follow the
team's established guidelines for hierarchy, element order, button labeling and styling,
separators, explanatory text, terminology, and the account creation link. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/passkeys.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the passkey and third-party sign-in guidelines right now. Could you paste the relevant
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

## Step 2.5 — Proactively check sign-in method layouts (required when a design is presented)

When a design is being reviewed or prototyped, the user has not asked about sign-in methods, and the design's sign-in form includes a passkey option or third-party sign-in buttons:

1. Determine which hierarchy approach from the fetched guidelines the design follows. Infer it from the layout if it's clear; otherwise ask the user which their product prioritizes.
2. Check the element order, button styling, separators, explanatory text, labels, and account creation link against the fetched rules for that approach.
3. Flag only the specific issues found, each tied to the fetched rule it breaks, and keep the feedback secondary to what the user actually asked for.
4. If the user explicitly wants to keep their current layout despite the recommendation, note the concern, respect their decision, and proceed.
5. If the sign-in options are clean, continue to Step 3 without comment.

If the sign-in form has no passkey option or third-party buttons, do not suggest adding them. Which sign-in methods to offer is a product decision, not a pattern violation.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Choose a hierarchy approach** | Explain the approaches described in the fetched guidelines and what each optimizes for. Leave the decision to the user, since the fetched guidelines tie it to product priorities. |
| **Design or prototype a sign-in form with passkey or third-party options** | Establish the hierarchy approach first, then apply the fetched rules for element order, styling, separators, labels, explanatory text, and the account creation link. |
| **Write sign-in method copy** | Apply the fetched guidance for passkey and third-party button labels, passkey explanatory text, and the account creation link. |
| **Review an existing sign-in form** | Evaluate against the fetched guidelines for the approach in use. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarize the passkey and third-party sign-in rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For design and prototyping
- If the hierarchy approach isn't known, ask before building. Do not default to one.
- Apply the fetched rules for that approach in full, including the related password field and sign-in wording guidelines surfaced by the cross-reference step.
- Do not design the browser or OS passkey sheet, or any third party's own sign-in flow. The fetched guidelines treat both as out of scope.
- Use the terminology the fetched guidelines specify for these sign-in methods, even when the user uses a different term.
- If the project's design system has button, separator, or icon components, defer to those — do not override them to match the guidelines.
- For third-party button and icon styling, apply the fetched guidance, which depends on whether the product is web-based or an installed app. If the product context isn't clear, ask.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which approach and key rules were applied.

### For reviews
- State which hierarchy approach the design follows.
- List each issue with the fetched rule it breaks and a correction.

---

## Guidelines

- Always cite the source: _"Per the [Passkeys and Third-Party Sign-in Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/passkeys)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labeled as such.

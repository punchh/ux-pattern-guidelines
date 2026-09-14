---
name: ux-modals
description: "Apply modal, lightbox, and dialog pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing a modal, dialog, confirmation overlay, or lightbox — or asking whether one should be used at all. Trigger for requests like: 'add a confirmation dialog', 'prototype a modal form', 'should this be a modal?', 'review my overlay layout', or any task involving overlays, stacked modals, or dialog button placement. Apply pattern guidelines for behavior, layout, and usage rules only; defer to the project's existing design system for component and visual decisions."
---

# UX Modals, Lightboxes, and Dialogs Skill

This skill ensures modal and dialog patterns follow the team's established guidelines
for usage, anatomy, layout, and alignment. Guidelines are maintained externally and
**must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/modals-lightboxes-and-dialogs
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the modal guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use a modal** | Evaluate the use case against the fetched usage rules (when to use / when not to use). |
| **Generate a modal prototype** | Build the modal following the fetched guidelines for anatomy, centering, size, and layout variation. Use the project's existing design system components; apply these guidelines for behavior and structure. |
| **Review an existing modal design** | Evaluate against the fetched guidelines. Flag violations with specific rule references and suggest corrections. |
| **Advise on stacked modals** | Apply the fetched rules for modal-on-modal usage. |
| **Explain the guidelines** | Summarise the relevant principles in plain language with examples. |

---

## Step 3 — Respond using the guidelines

### For prototype generation
- Implement modal anatomy, centering, size, and layout per the fetched guidelines.
- If the project's design system has a modal component with its own layout or alignment behavior, defer to the design system component — do not override it to match the guidelines.
- If a conflict exists between the design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which layout rules were applied.
- Use the project's existing design system components for all visual elements.

### For usage decisions
- State clearly whether the use case fits the fetched usage criteria.
- If it doesn't fit, name the correct alternative per the fetched guidelines.

### For design reviews
- Quote or describe the specific pattern being reviewed.
- List what conforms and what doesn't, each tied to a specific guideline.
- Suggest corrected versions for anything that doesn't pass.

### For explaining principles
- Keep it concise and practical.
- Use real examples from the guidelines or invent minimal ones to illustrate.

---

## Guidelines

- Always cite the source: _"Per the [Modal Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/modals-lightboxes-and-dialogs)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- Button alignment inside modals is governed by a separate skill. If button placement questions arise, refer to the `ux-button-alignment` skill or the button alignment guidelines at `https://partech.gitbook.io/ux-pattern-guidelines/button-alignment`.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

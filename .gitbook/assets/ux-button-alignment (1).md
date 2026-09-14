---
name: ux-button-alignment
description: "Apply button alignment guidelines when working on UI prototypes or design reviews. Use this skill whenever anyone is generating a prototype, evaluating a design, checking button placement, or asking whether their layout follows alignment best practices. Trigger for requests like: 'does this follow the button guidelines?', 'generate a form following our standards', 'check my button layout', 'prototype a modal with a CTA', or any task where buttons appear in a UI and alignment or scannability could be relevant — even if the user doesn't say 'button alignment' explicitly. Apply pattern guidelines for alignment and placement only; defer to the project's existing design system for component and visual decisions."
---

# Button Alignment Guidelines Skill

This skill ensures AI-generated prototypes and design reviews follow the team's
established button alignment standards for scannability and form submission accuracy.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/button-alignment
```

> **If the page is unreachable:** Stop and tell the designer:
> _"I can't reach the button alignment guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

Determine which of the following is needed:

| Task | What to do |
|---|---|
| **Generate a prototype** | Build the UI following the fetched guidelines. Call out which alignment rules shaped the layout. |
| **Review / audit a design** | Evaluate the provided design or description against the fetched guidelines. Flag specific violations and explain why. |
| **Check button placement** | Run a focused pass on button position, grouping, and alignment relative to the guidelines. |
| **Explain the guidelines** | Summarise the relevant principles in plain language, with examples where helpful. |

---

## Step 4 — Respond using the guidelines

### For prototype generation
- Build the UI (component, screen, or flow) with button placement that matches the guidelines.
- If the project's design system has a button component with its own alignment behavior, defer to the design system component — do not override it to match the guidelines.
- If a conflict exists between the design system component's alignment and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation (2–3 lines) naming which alignment rules were applied.
- Offer a variant if the context could reasonably call for a different alignment pattern.

### For design reviews
- Quote or describe the specific button placement being reviewed.
- List what conforms and what doesn't, each tied to a specific guideline.
- Suggest corrected versions for anything that doesn't pass.

### For placement checks
- Call out each issue with the rule it violates.
- Provide a corrected description or redline.

### For explaining principles
- Keep it concise and practical.
- Use real UI examples (from the guidelines or invented) to illustrate alignment decisions.

---

## Guidelines

- Always cite the source: _"Per the [Button Alignment Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/button-alignment)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your
  best general UX judgment as a fallback — clearly labelled as such.

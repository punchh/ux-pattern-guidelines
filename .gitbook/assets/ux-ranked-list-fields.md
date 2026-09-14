---
name: ux-ranked-list-fields
description: "Apply ranked list field pattern guidelines when building or reviewing forms. Use this skill whenever anyone is implementing or reviewing a ranking interface — including drag-and-drop reordering, priority ordering, sequence definition, or any field where the position of items carries meaning as the field's saved value. Trigger for requests like: 'add a drag and drop ranking to this form', 'let users prioritize these items', 'implement a sortable list field', 'review my ranking field', or any task involving capturing a user-defined order as form data. Also trigger when a design is presented for review or prototyping and any of the following are present — even if the user has not mentioned ranking: a list of items where order matters and is intended to be saved, a drag-and-drop reorder pattern, or a listbox/shuttle pattern being used to express priority. Apply pattern guidelines for anatomy, interactivity, accessibility, and saving behavior only; defer to the project's existing design system for component and visual decisions."
---

# UX Ranked List Fields Skill

This skill ensures ranked list fields follow the team's established guidelines for
anatomy, interactivity, accessibility compliance (WCAG 2.5.7), and saving behavior.
Guidelines are maintained externally and **must be fetched at runtime** so you always
work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/ranked-list-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the ranked list field guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 2.5 — Proactively check for ranking opportunities (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned ranking,
check whether the design contains any context where the fetched guidelines would
recommend a ranked list field. If so, surface the opportunity or flag the violation
before proceeding.

- If the design uses a listbox/shuttle pattern to express ordering, flag it as a
  violation per the fetched guidelines and recommend a ranked list field instead.
- If the design captures item priority or sequence through other means (numeric inputs,
  drag-and-drop without the documented accessibility affordances, etc.), flag it and
  recommend the ranked list field pattern.
- If the user explicitly wants to keep their current pattern despite the recommendation,
  note the concern, respect their decision, and proceed.
- If no ranking opportunity or violation is present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use a ranked list field** | Evaluate the use case against the fetched usage criteria (priority, preference, sequence with saved order). Distinguish ranking from sorting. |
| **Implement a ranked list field** | Apply the fetched anatomy, drag-and-drop, context menu, and keyboard interaction rules. |
| **Review an existing ranking field** | Evaluate anatomy, interactivity, and accessibility against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on accessibility compliance** | Apply the fetched WCAG 2.5.7 single-pointer alternative rule. |
| **Explain the guidelines** | Summarise the ranked list field rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- Distinguish ranking (saved order is the data) from sorting (transient view reorder) per the fetched guidelines.
- Apply the fetched rules for when not to use this field type.

### For implementation
- Apply the correct grabber dots placement, context menu placement, drag-and-drop interaction, and accessibility reorder actions per the fetched guidelines.
- Apply the fetched rules for whether the broader card body is clickable. This is context-sensitive in the live guidelines — do not assume a single rule applies to every scenario.
- Always include Move up / Move down actions in the context menu, even when the host application provides no other per-item utility actions. The context menu must be present on every card per the fetched guidelines.
- Never rely on drag and drop alone — WCAG 2.5.7 compliance is a hard requirement per the fetched guidelines.
- Announce position changes through an ARIA live region per the fetched guidelines.
- If the project's design system has card, icon button, or context menu components, defer to those — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the anatomy, interaction patterns, and accessibility provisions in the design.
- Evaluate each against the fetched guidelines.
- Flag violations such as listbox-based ranking, drag-only interaction with no non-drag alternative, missing context menu, or auto-save on each reorder.
- For card body interactivity, evaluate against the fetched context-sensitive rule rather than assuming a single answer.

### For accessibility advising
- Apply the fetched WCAG 2.5.7 rule directly. The context menu's Move up / Move down actions are mandatory, not optional.

---

## Guidelines

- Always cite the source: _"Per the [Ranked List Field Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/ranked-list-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

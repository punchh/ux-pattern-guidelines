---
name: ux-cards
description: "Apply card pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a card component — including deciding whether a card is appropriate, anatomy, context menus, calls to action, and interactivity rules. Trigger for requests like: 'use cards for this layout', 'should this be a card or a list row?', 'add a context menu to these cards', 'review my card design', 'can I put a button on this card?', or any task involving grouping related information into a container, dashboard tile, form-array item, list item, or navigation portal tile. Also trigger when a design is presented for review or prototyping and any of the following are present — even if the user has not mentioned cards: a repeated array of items with the same structure, a list or table item that includes images or highly variable text, a dashboard with grouped metrics or visualizations, or a landing/navigation page with major navigational tiles. Apply pattern guidelines for usage, anatomy, and interactivity only; defer to the project's existing design system for component and visual decisions."
---

# UX Cards Skill

This skill ensures cards follow the team's established guidelines for usage, anatomy,
context menus, calls to action, and interactivity. Guidelines are maintained externally
and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/reading-information/cards
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the card guidelines right now. Could you paste the relevant section
> here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 2.5 — Proactively check for card opportunities (required when a design is presented)

When a design is being reviewed or prototyped and the user has not mentioned cards,
check whether the design contains any context where the fetched guidelines would
recommend cards. If so, surface the opportunity to the user before proceeding.

- If a card-friendly context is present and the design uses a different pattern,
  flag the opportunity and explain the tradeoff per the fetched guidelines.
- If the user explicitly wants to keep their current pattern despite the recommendation,
  note the concern, respect their decision, and proceed.
- If no card-friendly context is present, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use a card** | Evaluate the context (form array, list/table item, navigation portal, dashboard) against the fetched usage criteria. |
| **Implement a card** | Apply the fetched anatomy, context menu, CTA, and interactivity rules. |
| **Decide card vs list row** | Apply the fetched guidance on when cards beat traditional table rows. |
| **Review an existing card** | Evaluate anatomy, interactivity, and content against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the card rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether a card is appropriate for the context and which usage pattern (form array, list item, navigation portal, dashboard) fits per the fetched guidelines.

### For implementation
- Apply the correct anatomy elements, context menu placement, CTA usage, and interactivity rules per the fetched guidelines.
- Apply the fetched rule for whole-card click behavior versus card-with-buttons behavior.
- Apply the fetched prohibition on hyperlinked text inside cards.
- If the project's design system has a card component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the card's anatomy, interactivity pattern, and content elements.
- Evaluate each against the fetched guidelines.
- Flag violations such as hyperlinked text inside cards, conflicting click targets, or missing hover feedback.

---

## Guidelines

- Always cite the source: _"Per the [Card Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/cards)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

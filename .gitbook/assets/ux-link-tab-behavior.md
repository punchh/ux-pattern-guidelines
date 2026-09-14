---
name: ux-link-tab-behavior
description: "Apply same-tab versus new-tab link behavior guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing how links and buttons open their destinations — whether in the same tab or a new one. Trigger for requests like: 'should this open in a new tab?', 'implement an external link', 'review my link behavior', 'add a new tab icon to this link', or any task involving the target behavior of links or buttons. Apply pattern guidelines for tab behavior and iconography only; defer to the project's existing design system for component and visual decisions."
---

# UX Link Tab Behavior Skill

This skill ensures links and buttons follow the team's established guidelines for
opening destinations in the same tab versus a new tab, including iconography rules
for signaling new-tab behavior. Guidelines are maintained externally and **must be
fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/opening-links-in-same-vs-new-tab
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the link tab behavior guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide same vs new tab** | Evaluate the destination context against the fetched guidelines to determine the correct behavior. |
| **Implement a link or button** | Apply the fetched tab behavior and iconography rules. |
| **Review existing link behavior** | Evaluate against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the rules in plain language with examples. |

---

## Step 4 — Respond using the guidelines

### For tab behavior decisions
- State clearly whether the link should open in the same tab or a new tab, and why, per the fetched guidelines.
- If the destination context is ambiguous, ask one clarifying question before proceeding.

### For implementation
- Apply the correct tab behavior and iconography per the fetched guidelines.
- If the project's design system has link components with their own new-tab iconography conventions, defer to those components — do not override them to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the tab behavior of each link or button in scope.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline examples or invent minimal ones to illustrate the same-tab vs new-tab decision.

---

## Guidelines

- Always cite the source: _"Per the [Link Tab Behavior Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/opening-links-in-same-vs-new-tab)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

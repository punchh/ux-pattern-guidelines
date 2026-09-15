---
name: ux-destructive-actions
description: "Apply destructive action and deletion pattern guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a delete action or any other permanently destructive operation — including labeling, confirmation dialogs, and the distinction between delete and remove. Trigger for requests like: 'add a delete option to this list', 'implement a delete confirmation', 'write delete dialog copy', 'should this say delete or remove?', 'review my destructive action pattern', or any task involving permanently destroying a record or item. Apply pattern guidelines for labeling, confirmation, and copy only; defer to the project's existing design system for component and visual decisions."
---

# UX Destructive Actions and Deleting Skill

This skill ensures destructive action patterns follow the team's established guidelines
for when to offer deletion, how to label it, and how to confirm it. Guidelines are
maintained externally and **must be fetched at runtime** so you always work from the
latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/form-experience/destructive-actions-and-deleting.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the destructive actions guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Classify the action (required before generating anything)

Use the fetched guidelines to determine whether the action is a permanent deletion
or a disassociation (remove), as the labeling and confirmation rules differ. If
the context is ambiguous, ask one clarifying question before proceeding.

---

## Step 4 — Identify the task

| Task | What to do |
|---|---|
| **Decide the correct label** | Evaluate whether the action is delete or remove per the fetched guidelines. |
| **Implement a destructive action** | Apply the fetched labeling, placement, and confirmation rules. |
| **Write confirmation dialog copy** | Write copy per the fetched dialog anatomy guidelines. |
| **Review an existing destructive action pattern** | Evaluate labeling, confirmation presence, and copy against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the rules in plain language with examples. |

---

## Step 5 — Respond using the guidelines

### For labeling decisions
- State clearly whether "delete" or "remove" is correct for the action, per the fetched guidelines.

### For implementation and copy
- Apply the correct labeling, confirmation dialog anatomy, and copy structure per the fetched guidelines.
- If the project's design system has a modal or confirmation dialog component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the label and confirmation behavior in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [Destructive Actions Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/form-experience/destructive-actions-and-deleting)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

---
name: ux-listbox-fields
description: "Apply listbox field guidelines when building or reviewing forms. Use this skill whenever anyone is considering implementing a listbox (shuttle) field. Trigger for requests like: 'implement a listbox', 'add a shuttle component', 'build a dual-list selector', or any task involving moving items between two visible lists. The guideline position is clear: don't use a listbox. Apply pattern guidelines by redirecting to the correct alternative."
---

# UX Listbox Fields Skill

This skill applies the team's established guideline on listbox fields, which takes a
clear position against using them. Guidelines are maintained externally and **must be
fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/listbox-fields
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the listbox guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
> Do not proceed by guessing at the rules.

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Apply the guideline

The fetched guidelines take a clear position: **do not use a listbox**. When a listbox
is requested, apply the guideline as follows:

- Explain why the guideline recommends against listboxes, per the fetched reasoning.
- Redirect to the multi-select combo box as the correct alternative.
- Offer to implement the multi-select combo box instead, referencing the `ux-combo-box` skill or the combo box guidelines.
- If the user explicitly wants a listbox despite the recommendation, note the concern clearly, respect their decision, and proceed — but do not omit the pushback.

---

## Guidelines

- Always cite the source: _"Per the [Listbox Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/listbox-fields)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.

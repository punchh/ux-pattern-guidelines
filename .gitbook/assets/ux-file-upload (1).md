---
name: ux-file-upload
description: "Apply file upload field guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a file upload experience — including drag-and-drop anatomy, files region feedback, upload progress, error handling, and file violation messaging. Trigger for requests like: 'add a file upload to this form', 'implement drag and drop', 'what should show during upload?', 'how should file errors be handled?', 'review my file upload component', or any task involving uploading one or more files in a form context. Apply pattern guidelines for anatomy, feedback, and error handling only; defer to the project's existing design system for component and visual decisions."
---

# UX File Upload Skill

This skill ensures file upload fields follow the team's established guidelines for
drag-and-drop anatomy, upload feedback, progress display, and error handling. Guidelines
are maintained externally and **must be fetched at runtime** so you always work from
the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://partech.gitbook.io/ux-pattern-guidelines/entering-information/file-upload
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the file upload guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
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
| **Implement a file upload** | Apply the fetched anatomy, files region feedback, progress, and error handling rules. |
| **Review a file upload** | Evaluate anatomy, feedback, and error handling against the fetched guidelines. Flag violations and suggest corrections. |
| **Advise on error handling** | Apply the fetched rules for connection errors vs file violations. |
| **Explain the guidelines** | Summarise the file upload rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For implementation
- Apply the correct drag-and-drop region anatomy, files region feedback elements (icon, filename, progress, status, rate, completed size, remove button), and error handling rules per the fetched guidelines.
- Note that file upload errors are an exception to the standard error validation pattern — immediate feedback is required per the fetched guidelines.
- If the project's design system has a file upload component, defer to that — do not override it to match the guidelines.
- If a conflict exists between a design system component and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the anatomy elements and feedback states present in the design.
- Evaluate each against the fetched guidelines.
- Flag violations and suggest corrections.

---

## Guidelines

- Always cite the source: _"Per the [File Upload Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/entering-information/file-upload)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

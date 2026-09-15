---
name: ux-grammar-voice-tone
description: "Apply grammar, voice, and tone guidelines when writing or reviewing UI copy. Use this skill whenever anyone is writing, generating, or reviewing microcopy, labels, button text, tooltips, field descriptions, toast messages, banners, confirmation prompts, error messages, empty states, or any other words that appear in a UI. Trigger for requests like: 'does this copy sound right?', 'write a button label for this action', 'review my tooltip copy', 'is this the right tone?', 'check my capitalization', or any task involving the words, phrasing, punctuation, or tone of UI text. Apply pattern guidelines for copy only; defer to the project's existing design system for component and visual decisions."
---

# UX Grammar, Voice, and Tone Skill

This skill ensures UI copy follows the team's established guidelines for grammar,
voice, tone, capitalization, and punctuation. Guidelines are maintained externally
and **must be fetched at runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/grammar-voice-and-tone.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the grammar, voice, and tone guidelines right now. Could you paste
> the relevant section here so I can apply them?"_
> Do not proceed by guessing at the rules.

**URL confirmation policy:** Before fetching the URL above, announce it to the user and ask for confirmation. Example phrasing: "I need to fetch the [topic] guideline from [URL] to apply your team's standards. Proceed?" If multiple URLs are being fetched from the same prompt, consolidate them into one confirmation. Track approved URLs per session — once the user approves a URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. If the user declines, ask them to paste the guideline content directly instead of proceeding on assumptions. (If a parent instruction file such as `CLAUDE.md` or `copilot-instructions.md` is present, defer to its fuller version of this policy.)

---

## Step 2 — Fetch linked guidelines (if relevant)

If the fetched guideline page links to other guidelines that are relevant to the
current task, fetch those pages too and apply them. Do not wait for the user to
provide those URLs — follow the links automatically and silently as needed.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Write new copy** | Generate copy that follows the fetched guidelines. Note which key rules shaped the output. |
| **Review / critique copy** | Evaluate the provided copy against the fetched guidelines. Call out specific violations and explain why. |
| **Check grammar and formatting** | Run a focused pass on punctuation, capitalisation, tense, abbreviations, and any other grammar rules in the fetched guidelines. |
| **Explain voice and tone** | Summarise the relevant principles from the fetched guidelines in plain language, with examples where helpful. |

---

## Step 4 — Respond using the guidelines

### For writing new copy
- Provide the copy.
- Add a short note (2–3 lines max) on which voice, tone, or grammar rules guided it.
- Offer 1–2 alternatives if tone could reasonably vary.

### For reviews
- Quote the specific copy being reviewed.
- List what works and what doesn't, each tied to a fetched guideline.
- Suggest revised versions for anything that doesn't pass.

### For grammar and formatting checks
- Call out each issue with the rule it violates.
- Provide a corrected version.

### For explaining principles
- Keep it concise and practical.
- Use real UI examples from the fetched guidelines or invent minimal ones to illustrate.

---

## Guidelines

- Always cite the source: _"Per the [Grammar, Voice, and Tone Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/grammar-voice-and-tone)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX writing judgment as a fallback — clearly labelled as such.

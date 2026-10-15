---
name: ux-grammar-voice-tone
description: "Apply grammar, voice, and tone guidelines when writing or reviewing UI copy. Use whenever anyone writes, generates, or reviews microcopy: buttons, links, titles, headings, nav and feature names, field descriptions, tooltips, toasts, banners, prompts, errors, empty states, or how numbers, currency, and units are displayed. Trigger for requests like 'does this copy sound right?', 'Save or Done?', 'check my capitalization', 'should this have a period?', or any task involving the wording, word choice, capitalization, punctuation, abbreviations, or tone of UI text. Also trigger unprompted when a design is presented for review or prototyping and its copy likely breaks capitalization, punctuation, word choice, or number formatting conventions, such as Title Case buttons, 'Please', exclamation points, or generic labels like OK or Submit. Apply pattern guidelines for copy only; defer to the project's design system for visual decisions."
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

If the fetched guideline page contains relative-path markdown links to other `.md` files (e.g. `tooltips.md`, `../entering-information/anatomy-of-form-field.md`), those are cross-references to other guidelines in the same repository. To follow them:

1. Resolve each relative path against the base URL of the guideline you just fetched. Sibling links stay in the same directory; `../` links climb to the parent and descend into the specified category folder.
2. Apply the URL confirmation policy to each resolved URL before fetching.
3. If a link points to a fragment/anchor within the same page (e.g. `guideline-name.md#section`), do not re-fetch — it's a self-reference.
4. If a link points to a file that returns a 404, note the gap in your response and proceed without that reference rather than stopping.

Do not wait for the user to provide these URLs — follow the links automatically as needed, subject to confirmation.

---

## Step 2.5 — Proactively check copy (required when a design is presented)

When a design is being reviewed or prototyped and the user has not asked about copy, check the design's visible text against the fetched guidelines. If any copy violates them:

- Flag only the specific violations found, each with a suggested revision tied to the fetched guideline it breaks.
- Keep copy feedback brief and secondary to what the user actually asked for. Do not rewrite all of the design's copy unprompted.
- If the user explicitly wants to keep their current wording despite the recommendation, note the concern, respect their decision, and proceed.
- If the copy is clean, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Write new copy** | Generate copy that follows the fetched guidelines. Note which key rules shaped the output. |
| **Review / critique copy** | Evaluate the provided copy against the fetched guidelines. Call out specific violations and explain why. |
| **Check grammar and formatting** | Run a focused pass on punctuation, capitalization, tense, abbreviations, and any other grammar rules in the fetched guidelines. |
| **Choose between similar terms** | Apply the fetched word choice rules (for example Save versus Done, Delete versus Remove) and recommend one term with the reason. |
| **Explain voice and tone** | Summarize the relevant principles from the fetched guidelines in plain language, with examples where helpful. |

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

### For word choice questions
- Recommend one term, not a list of options.
- State the distinction from the fetched guidelines in one sentence (for example: Delete erases from the database; Remove only takes it out of the current view).

### For explaining principles
- Keep it concise and practical.
- Use real UI examples from the fetched guidelines or invent minimal ones to illustrate.

---

## Guidelines

- Always cite the source: _"Per the [Grammar, Voice, and Tone Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/grammar-voice-and-tone)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX writing judgment as a fallback — clearly labeled as such.

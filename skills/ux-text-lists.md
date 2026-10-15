---
name: ux-text-lists
description: "Apply text list pattern guidelines when writing or reviewing UI copy. Use this skill whenever anyone is writing or reviewing bulleted or numbered lists of text in an interface, including choosing between bulleted and numbered lists, introducing a list, capitalizing and punctuating list items, and using emoji or icons as bullets. This covers lists within copy, not list pages, tables, or list-based form fields. Trigger for requests like 'should this be a numbered list?', 'how should I format these bullets?', 'write the steps for this flow', or 'review my list copy'. Also trigger unprompted when a design is presented for review or prototyping and it contains text lists with lowercase starts, trailing commas, mixed bullet icons, a numbered list for items whose order doesn't matter, or bullets for sequential steps. Apply pattern guidelines for list structure and copy only; defer to the project's design system for visual decisions."
---

# UX Text Lists Skill

This skill ensures bulleted and numbered lists in UI copy follow the team's established
guidelines for choosing a list type, introducing a list, capitalization, punctuation,
and bullet substitution. Guidelines are maintained externally and **must be fetched at
runtime** so you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/lists-and-tables/text-lists.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the text list guidelines right now. Could you paste the relevant
> section here so I can apply them?"_
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

## Step 2.5 — Proactively check text lists (required when a design is presented)

When a design is being reviewed or prototyped and the user has not asked about lists, check any bulleted or numbered lists in the design's copy against the fetched guidelines. If any break them:

- Flag only the specific list issues found, each with a corrected version tied to the fetched guideline it breaks.
- Keep list feedback brief and secondary to what the user actually asked for.
- If the user explicitly wants to keep their current formatting despite the recommendation, note the concern, respect their decision, and proceed.
- If the lists are clean, or the design has no text lists, continue to Step 3 without comment.

---

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Choose a list type** | Apply the fetched criteria for bulleted versus numbered lists and recommend one. |
| **Write a list** | Write the list following the fetched rules for introducing, capitalizing, and punctuating it. |
| **Review list formatting** | Evaluate the provided list against the fetched guidelines. Call out each issue and provide a corrected version. |
| **Explain the guidelines** | Summarize the text list rules in plain language. |

---

## Step 4 — Respond using the guidelines

### For choosing a list type
- Recommend one list type and state the reason in one sentence, per the fetched criteria.

### For writing lists
- Provide the list.
- Add a short note (1–2 lines) on which rules shaped it.

### For reviews
- Quote the list being reviewed.
- Call out each issue with the rule it breaks.
- Provide a corrected version of the full list.

### For copy inside list items
- List items are UI copy. The fetched page links to the grammar, voice, and tone guidelines, so apply those to the wording of each item as well (via the cross-reference step).

---

## Guidelines

- Always cite the source: _"Per the [Text List Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/lists-and-tables/text-lists)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labeled as such.

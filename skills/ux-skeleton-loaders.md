---
name: ux-skeleton-loaders
description: "Apply skeleton loader guidelines when building or reviewing UI. Use this skill whenever anyone is implementing or reviewing a loading state for page content — including deciding whether a skeleton loader is appropriate, implementing animation and color rules, or reviewing an existing skeleton loader. Trigger for requests like: 'add a skeleton loader to this page', 'should this use a spinner or skeleton?', 'implement a loading state for this list', 'review my skeleton animation', or any task involving perceived performance and content loading feedback. Apply pattern guidelines for usage, animation, and timing only; defer to the project's existing design system for component and visual decisions."
---

# UX Skeleton Loaders Skill

This skill ensures skeleton loaders follow the team's established guidelines for
when to use them, animation behavior, color rules, and individual element loading
logic. Guidelines are maintained externally and **must be fetched at runtime** so
you always work from the latest version.

---

## Step 1 — Fetch the guidelines (required)

Before doing anything else, retrieve the live guidelines from:

```
https://raw.githubusercontent.com/punchh/ux-pattern-guidelines/main/reading-information/skeleton-loaders.md
```

> **If the page is unreachable:** Stop and tell the user:
> _"I can't reach the skeleton loader guidelines right now. Could you paste the
> relevant section here so I can apply them?"_
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

## Step 3 — Identify the task

| Task | What to do |
|---|---|
| **Decide whether to use a skeleton loader** | Evaluate the expected load time against the fetched usage threshold. |
| **Implement a skeleton loader** | Apply the fetched animation, color, timing, and individual element removal rules. |
| **Review an existing skeleton loader** | Evaluate animation style, color, and persistence behavior against the fetched guidelines. Flag violations and suggest corrections. |
| **Explain the guidelines** | Summarise the usage rules and animation specifications in plain language. |

---

## Step 4 — Respond using the guidelines

### For usage decisions
- State clearly whether a skeleton loader is appropriate based on the expected load time, per the fetched guidelines.
- If not appropriate, suggest the correct alternative loading pattern.

### For implementation
- Apply the correct animation style, color rules, and individual element removal logic per the fetched guidelines and animation specifications.
- If the project's design system has a skeleton loader component, defer to that component — do not override it to match the guidelines.
- If a conflict exists between a design system component's animation or color behavior and the guidelines, flag it explicitly to the user so they can make an informed decision.
- Add a short annotation naming which rules were applied.

### For reviews
- Identify the skeleton loader behavior present in the design or implementation.
- Evaluate animation style, colors, timing, and element removal logic against the fetched guidelines.
- Flag violations and suggest corrections.

### For explaining principles
- Keep it concise and practical.
- Use the fetched guideline rationale (perceived performance, layout shift prevention) to explain why the rules exist.

---

## Guidelines

- Always cite the source: _"Per the [Skeleton Loaders Guidelines](https://partech.gitbook.io/ux-pattern-guidelines/reading-information/skeleton-loaders)…"_
- Never invent rules that aren't in the fetched guidelines.
- If a guideline is ambiguous, flag it to the user rather than assuming.
- If the request falls outside the scope of the guidelines, say so and offer your best general UX judgment as a fallback — clearly labelled as such.

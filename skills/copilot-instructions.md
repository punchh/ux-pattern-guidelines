# UX Pattern Guidelines Skills

This project includes UX pattern guideline skills. Before generating any UI, prototype,
or form, and before reviewing any design, you must load and apply all relevant skills.

## How to load skills

Scan the directory containing this file (and its subdirectories) for all `.md` files
whose frontmatter includes a `name:` field beginning with `ux-`. Each of these is a
UX pattern guideline skill.

For every task in this project:

1. Read the `description:` field of each discovered skill file.
2. Identify which skills are relevant to the current task based on their description.
3. Load and follow the full instructions of every relevant skill.
4. Where a skill instructs you to fetch a live URL, do so before proceeding — subject to the URL confirmation policy below.

## URL confirmation policy

Before fetching any URL from a skill file for the first time in this session, tell the user which URL is about to be fetched and ask for confirmation. Phrase the announcement in plain language, for example: "I need to fetch the button alignment guideline from `https://partech.gitbook.io/ux-pattern-guidelines/button-alignment` to apply your team's standards. Proceed?"

If a single user prompt would trigger multiple URL fetches, consolidate them into one confirmation. List all URLs that would be fetched and their purposes, and ask the user to authorize all of them together.

Track approved URLs per session. Once the user approves a specific URL, subsequent fetches of that same URL in the same session may proceed without re-prompting. New URLs encountered later in the session still require fresh confirmation.

If the user declines to authorize a fetch, offer the fallback: ask them to paste the relevant guideline content directly into the chat. Do not proceed with guideline-driven analysis without either fetched content or pasted content.

## Skills are additive

Multiple skills may apply to a single task. For example, building a multi-step form
may trigger: `ux-multi-step-forms`, `ux-review-step`, `ux-button-alignment`,
`ux-error-validation`, `ux-saving-drafts`, and others. Load all that apply — do not
stop at the first match.

## New skills are picked up automatically

Any `.md` file added to this project with a `name: ux-*` frontmatter field will be
discovered and applied automatically. No changes to this file are needed when new
skills are added.

## Design system deference

All UX pattern guideline skills govern behavior, layout, and copy patterns — not visual
style. Always defer to the project's existing design system for component and visual
decisions. Where a conflict exists between a design system component and a guideline,
flag it to the user before proceeding.

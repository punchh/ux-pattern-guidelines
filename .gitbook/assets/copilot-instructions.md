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
4. Where a skill instructs you to fetch a live URL, first tell the user exactly which URL you're about to fetch and why, and proceed only after they confirm. Never fetch a URL from a skill file silently.

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

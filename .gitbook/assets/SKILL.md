---
name: ux-pattern-guidelines
description: >-
  Partech UX pattern guidelines from local markdown. Use when designing or
  reviewing UI/UX, forms, fields, validation, passwords, sign-in, sign-up,
  error messages, accessibility, or any topic covered by the linked guideline
  files in this skill folder.
---

# UX pattern guidelines (local)

This skill is a **folder of markdown files** next to this `SKILL.md`. Every `*.md` file in **this same directory** except `SKILL.md` is a guideline document.

`SKILL.md` does **not** watch the filesystem (Cursor skills are static). Instead, **discover files fresh whenever this skill applies**: you do not need to edit `SKILL.md` when new guideline `.md` files are added.

## Discovery (required — do not skip)

1. Resolve the skill directory: **`~/.cursor/skills/ux-pattern-guidelines/`** (same folder as this `SKILL.md`).
2. **Enumerate** all markdown files there — e.g. glob `**/*.md` under that path, or list the directory.
3. **Ignore** `SKILL.md` only. Every other `*.md` is a guideline.
4. **Route using frontmatter first (required).** For each discovered guideline `*.md` (not `SKILL.md`), read only the **YAML frontmatter** between the first pair of `---` lines. Each file’s frontmatter is the authoritative **“when to use this guideline”** signal — especially `description`, and any other fields the author added for triggers (e.g. `triggers`, `tags`, `topics`). **Match the user’s request to that frontmatter text**, not to the filename. Filenames are a **fallback** hint when frontmatter is ambiguous or two files overlap.
5. **Select** one or more guideline files whose frontmatter clearly applies. If several apply, read and apply **all** that are relevant; if none apply, say so and briefly list each file’s `name` / first line of `description` so the user can steer you.
6. **Read the full body** of the chosen file(s) (not only frontmatter), then **apply** what those bodies say. Do not contradict the guidelines. If the docs are silent on a point, say that explicitly.

## How to use after discovery

1. **Identify the topic** from the user request.
2. **Score or match** discovered files using **frontmatter triggers** (primary), filename (secondary).
3. **Open** the matching guideline file(s) in full and follow their instructions (including any “fetch at runtime” or linked-doc steps **inside** that file).
4. If the body says to fetch external URLs, do that; the local `.md` is still the routing source via its frontmatter.

## File locations

- Skill folder: `~/.cursor/skills/ux-pattern-guidelines/`
- Guidelines: any `*.md` in that folder **except** `SKILL.md`

## Adding new guidelines

Drop new `.md` files into that folder. **No change to `SKILL.md` is required.** The next time this skill is used, discovery step above will pick them up.

## Copying files from elsewhere (optional)

```bash
# Example: copy without overwriting SKILL.md
for f in SOURCE_DIR/*.md; do
  base=$(basename "$f")
  [[ "$base" == SKILL.md ]] && continue
  cp "$f" ~/.cursor/skills/ux-pattern-guidelines/
done
```

# UX Pattern Guideline Skills

This folder holds a set of AI agent skill files, one per guideline in the PAR UX Pattern Guidelines library. Drop any of these files into your Claude Code, Cursor, or GitHub Copilot project and the corresponding UX guideline gets enforced automatically as you work.

## What this repo is

The PAR UX Pattern Guidelines library lives in two places at once:

- **Human readers** read the guidelines at [partech.gitbook.io/ux-pattern-guidelines](https://partech.gitbook.io/ux-pattern-guidelines), where they render as a proper documentation site with images, callouts, and cross-links.
- **AI agents** fetch the same content as raw markdown from this GitHub repository, which mirrors the GitBook site.

Both destinations show the same content. The GitBook site is where the guidelines are authored and where humans go to read them. This repository is where automated tools go to fetch them.

## Why a GitHub mirror exists

GitBook renders content beautifully for humans but isn't reliably reachable by AI agents at runtime. Some AI fetch tools reject URLs that haven't appeared in a prior search result, and GitBook's Basic plan blocks search engine indexing, so those URLs stay out of every search index. A public GitHub repository sidesteps both issues: raw GitHub URLs are reliably fetchable and freely indexable.

The tradeoff worth naming: exported markdown loses some formatting subtleties (styled callouts, image captions, embedded components) that GitBook renders. AI agents don't need the pretty rendering — they need the words — so this loss is acceptable for the mirror's purpose.

## How content flows

Content is authored in GitBook. GitBook's Git Sync feature exports each guideline page as a markdown file into this repository, preserving the category folder structure (`layout-and-navigation/`, `form-experience/`, `lists-and-tables/`, `reading-information/`, `entering-information/`). Updates to guidelines in GitBook appear in this repo within seconds via the automated sync.

The sync is technically bidirectional — GitBook and GitHub can both drive changes to the mirrored guideline files. The convention, though, is that **guideline content is only edited in GitBook**. Editing a guideline `.md` file directly in this repo would push that change back into GitBook and overwrite the authored version, which is almost never what anyone wants. If you spot a typo or want to suggest a change to a guideline, do it in GitBook.

## What this `/skills/` folder contains

Unlike the guideline `.md` files at the repository root (which are exports from GitBook), the files in this `/skills/` folder are authored and maintained directly in this repository. They aren't touched by GitBook's Git Sync.

Each skill file corresponds to one guideline. When an AI agent loads a skill, the skill instructs it to fetch the matching guideline's raw markdown from this repo at runtime, follow any cross-references it finds, and apply the guideline's rules to whatever the user is working on.

Also in this folder:

- `CLAUDE.md` — a parent instruction file for Claude Code that governs how the skill files interact, including a URL confirmation policy
- `copilot-instructions.md` — the GitHub Copilot equivalent

## How to install a skill

Each skill file has a permanent download URL on this repo of the form:

```
https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-[guideline-name].md
```

Every published guideline page on GitBook links to its matching skill file. Download the skill file, drop it into your Claude Code, Cursor, or GitHub Copilot project, and the guideline will be applied automatically when relevant to your task.

## When skills need updating

Skill files are authored to be reusable and fetch their guideline content live, so they rarely need to change even when guideline content changes. When a skill *does* need updating — for example, if a new cross-reference resolution rule is needed, or if the URL confirmation policy changes — that update happens directly in this repo, not in GitBook. Skill files are the one exception to the "author in GitBook" rule.

## Contact

Dan Owens

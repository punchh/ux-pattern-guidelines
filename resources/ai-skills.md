---
description: >-
  Skills and markdown files for AI design reviews, AI prototyping, and vibe
  coding
---

# AI skills

### Using with AI tools

Before using the [individual skill files](ai-skills.md#individual-skills-for-each-ux-pattern-guideline) below, get your AI tool ready to use them.

{% hint style="warning" %}
**Don't let your AI agent hard code the&#x20;**_**contents**_**&#x20;of any UX pattern guideline page to your own skill files.**

These pages get updated often, so it would quickly become out of date. Each skill file is crafted to do runtime lookups to the live UX pattern guidelines on this website each time it's invoked so that it gets the latest and greatest.
{% endhint %}

<details>

<summary>Without any specific tool</summary>

Just copy the URL from the desired guideline page(s) and paste to your agent.

Ask your agent to use it to shape your design. That's it.&#x20;

You don't even _need_ the skill files.

Otherwise, some tools also let you drag and drop .md files into the agent prompt.

</details>

<details>

<summary>With <strong>Claude Code</strong></summary>

Download `CLAUDE.md` and place it in the same folder as your skill files. Claude Code will automatically discover any `ux-*.md` skill files in that folder and apply the relevant ones to your work — no additional setup needed.

{% hint style="info" %}
**If you already have a CLAUDE.md file** in your project, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.
{% endhint %}

When you download new skills, just drop them in the same folder. `CLAUDE.md` picks them up automatically.

{% file src="../.gitbook/assets/CLAUDE.md" %}

</details>

<details>

<summary>With <strong>Cursor</strong></summary>

Each UX pattern guideline below is a markdown file with a short description at the top so the AI knows when it applies.

1. (Create the `skills` folder if it doesn’t exist.)
2. Add our starter `SKILL.md` to that folder _once_ (we provide it—it tells Cursor how to find and use every other `.md` in the same folder).
3. Drop in whichever guideline `.md` files you downloaded. You can add more anytime—no need to edit `SKILL.md` each time.

In Cursor, mention the skill (e.g. type `@` and choose ux pattern guidelines) or ask the agent to follow your UX pattern guidelines before you review or build UI.

That’s it.

{% file src="../.gitbook/assets/SKILL.md" %}

</details>

<details>

<summary>With <strong>GitHub Copilot in VS Code</strong></summary>

Download the skill files plus `copilot-instructions.md`. Place `copilot-instructions.md` in a `.github/` folder at your project root (so the path is `.github/copilot-instructions.md`) and put the skill files in a dedicated folder in your project, such as `docs/ux-skills/` or wherever fits your project's structure. The instructions file tells Copilot to scan recursively, so any folder location works.

If you already have a `.github/copilot-instructions.md` file, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.

When you download new skills, drop them into the same folder. Copilot picks them up automatically.

{% hint style="info" %}
Setup varies across Copilot configurations and team settings. If this path doesn't work in your environment, check with your team for how custom instructions are configured.
{% endhint %}

{% file src="../.gitbook/assets/copilot-instructions.md" %}

</details>

***

### Individual skills for each UX pattern guideline

Pick and choose which skills are relevant for your scope. Download as many or as few as are relevant.

#### Layout and navigation

{% file src="../.gitbook/assets/ux-button-alignment (1).md" %}

{% file src="../.gitbook/assets/ux-breadcrumbs (1).md" %}

{% file src="../.gitbook/assets/ux-cards (2).md" %}

{% file src="../.gitbook/assets/ux-hover-interactions.md" %}

{% file src="../.gitbook/assets/ux-hyperlinks-vs-link-buttons.md" %}

{% file src="../.gitbook/assets/ux-modals (1).md" %}

{% file src="../.gitbook/assets/ux-link-tab-behavior.md" %}

{% file src="../.gitbook/assets/ux-tabs.md" %}

#### Lists and tables

{% file src="../.gitbook/assets/ux-bulk-actions.md" %}

{% file src="../.gitbook/assets/ux-column-alignment.md" %}

{% file src="../.gitbook/assets/ux-empty-states (1).md" %}

{% file src="../.gitbook/assets/ux-filters (1).md" %}

{% file src="../.gitbook/assets/ux-tables (1).md" %}

#### Reading information

{% file src="../.gitbook/assets/ux-accordions (1).md" %}

{% file src="../.gitbook/assets/ux-datestamps (1).md" %}

{% file src="../.gitbook/assets/ux-descriptions-vs-tooltips.md" %}

{% file src="../.gitbook/assets/ux-environmental-errors.md" %}

{% file src="../.gitbook/assets/ux-grammar-voice-tone (1).md" %}

{% file src="../.gitbook/assets/ux-information-banners.md" %}

{% file src="../.gitbook/assets/ux-line-lengths.md" %}

{% file src="../.gitbook/assets/ux-loading-dialogs.md" %}

{% file src="../.gitbook/assets/ux-onboarding.md" %}

{% file src="../.gitbook/assets/ux-skeleton-loaders.md" %}

{% file src="../.gitbook/assets/ux-tooltips.md" %}

{% file src="../.gitbook/assets/ux-truncation-and-overflow.md" %}

#### Form experience

{% file src="../.gitbook/assets/ux-autosaving.md" %}

{% file src="../.gitbook/assets/ux-canceling.md" %}

{% file src="../.gitbook/assets/ux-destructive-actions.md" %}

{% file src="../.gitbook/assets/ux-disabled-buttons.md" %}

{% file src="../.gitbook/assets/ux-combining-buttons.md" %}

{% file src="../.gitbook/assets/ux-error-validation.md" %}

{% file src="../.gitbook/assets/ux-field-alignment.md" %}

{% file src="../.gitbook/assets/ux-multi-step-forms.md" %}

{% file src="../.gitbook/assets/ux-required-optional-fields.md" %}

{% file src="../.gitbook/assets/ux-review-step.md" %}

{% file src="../.gitbook/assets/ux-saving-drafts.md" %}

{% file src="../.gitbook/assets/ux-saving-state-buttons.md" %}

{% file src="../.gitbook/assets/ux-steppers.md" %}

{% file src="../.gitbook/assets/ux-success-notification.md" %}

#### Entering information

{% file src="../.gitbook/assets/ux-form-field-anatomy (2).md" %}

{% file src="../.gitbook/assets/ux-autocomplete (2).md" %}

{% file src="../.gitbook/assets/ux-button-groups (2).md" %}

{% file src="../.gitbook/assets/ux-checkbox-fields (2).md" %}

{% file src="../.gitbook/assets/ux-combo-box (2).md" %}

{% file src="../.gitbook/assets/ux-conditional-fields (2).md" %}

{% file src="../.gitbook/assets/ux-date-fields (2).md" %}

{% file src="../.gitbook/assets/ux-dropdown-lists (2).md" %}

{% file src="../.gitbook/assets/ux-file-upload (2).md" %}

{% file src="../.gitbook/assets/ux-listbox-fields (2).md" %}

{% file src="../.gitbook/assets/ux-paragraph-fields (2).md" %}

{% file src="../.gitbook/assets/ux-password-fields (2).md" %}

{% file src="../.gitbook/assets/ux-phone-number-fields (2).md" %}

{% file src="../.gitbook/assets/ux-placeholder-variables (2).md" %}

{% file src="../.gitbook/assets/ux-radio-button-fields (2).md" %}

{% file src="../.gitbook/assets/ux-ranked-list-fields (1).md" %}

{% file src="../.gitbook/assets/ux-time-fields (2).md" %}

{% file src="../.gitbook/assets/ux-time-zone-fields (2).md" %}

{% file src="../.gitbook/assets/ux-toggle-switches (2).md" %}

***

### Contact

**Dan Owens**\
Principal UX Designer

PAR Engagement
